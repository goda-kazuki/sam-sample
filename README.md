# sam-sample

## 移行要件

### 必須要件

- API Gateway + LambdaをベースとしたWeb APIの実装が容易であること
- EventBridgeをトリガーとしたLambdaの実行が容易に実現できること
  - API Gateway
  - スケジューラ
  - Glue
    - SAMだとCloudFormationを自前で書く必要がある
  - StepFunctions
  - Kinesis Data Streams
  - s3
  - DynamoDB
- CloudFormation等を利用したIaCが実現できること
- 商用利用できること
- CI/CDパイプラインへの組み込みが容易であること

### 尚良し

- 環境変数の取り扱いが容易であること（.env）
- $ serverless invoke でCLIから実行、$ serveless invoke local みたいにローカルで実行といったことができるか？
- Lambda@Edgeへのデプロイができる
  - このプラグイン使ってました
  - <https://www.serverless.com/plugins/serverless-lambda-edge-pre-existing-cloudfront>
- IaCのドライランができること
- スナップショットテストが実施できること
