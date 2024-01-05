# sam-sample

## 移行要件

### 必須要件

- API Gateway + LambdaをベースとしたWeb APIの実装が容易であること
  - OK
- EventBridgeをトリガーとしたLambdaの実行が容易に実現できること
  - API Gateway
    - OK
  - スケジューラ
    - OK
  - Kinesis Data Streams
    - たぶんOK
    - <https://github.com/aws/serverless-application-model/blob/master/versions/2016-10-31.md#kinesis>
  - s3
    - たぶんOK
    - <https://github.com/aws/serverless-application-model/blob/master/versions/2016-10-31.md#s3>
  - DynamoDB
    - たぶんOK
    - <https://github.com/aws/serverless-application-model/blob/master/versions/2016-10-31.md#dynamodb>
  - Glue
    - SAMだとCloudFormationを自前で書く必要がある
      - EventBridgeRuleを指定すればできた
  - StepFunctions
    - たぶんOK
- CloudFormation等を利用したIaCが実現できること
  - OK
- 商用利用できること
  - OK
  - <https://github.com/aws/serverless-application-model?tab=Apache-2.0-1-ov-file>
- CI/CDパイプラインへの組み込みが容易であること
  - たぶんOK
  - <https://aws.amazon.com/jp/builders-flash/202110/new-lambda-container-development-6>

### 尚良し

- 環境変数の取り扱いが容易であること（.env）
- $ serverless invoke でCLIから実行、$ serverless invoke local みたいにローカルで実行といったことができるか？
  - OK
  - `sam local invoke HelloWorldFunction`
- Lambda@Edgeへのデプロイができる
  - たぶんOK
  - <https://dev.classmethod.jp/articles/net307-customizing-lambda-edge-sam/>
- IaCのドライランができること
  - deployコマンド実行時に変更セットを確認することが可能
- スナップショットテストが実施できること
  - 全リソース定義するため、そもそも不要
