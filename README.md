# Lambda Auto Deploy Base

## Setup

There are two aws users needed:

### S3 User

Needed Policies:

- AmazonS3FullAccess

### Lambda User

Needed Policies:

- AmazonS3ReadOnlyAccess
- AWSCloudFormationFullAccess
- AWSLambda_FullAccess
- AWSLambdaRole
- CloudWatchLogsFullAccess
- IAMFullAccess

### Lambda Function With API Gateway Attached

- Use arm64
- Set Lambda function handler to `app/index.handler`

### Github Repository Secrets

`Repository Settings` -> `Secrets and Variables` -> `Actions` -> `New repository secret`

The following secrets are needed:

- AWS_LAMBDA_FUNCTION_NAME: Lambda Function name
- AWS_LAMBDA_REGION: Lambda Function region
- AWS_LAMBDA_USER_ACCESS_KEY_ID: Access key id for Lambda Function user credential
- AWS_LAMBDA_USER_SECRET_ACCESS_KEY: Secret access key for Lambda Function user credential
- AWS_S3_BUCKET_NAME: S3 bucket name
- AWS_S3_BUCKET_REGION: S3 bucket región
- AWS_S3_BUCKET_USER_AWS_ACCESS_KEY_ID: Access key id for S3 user credential
- AWS_S3_BUCKET_USER_AWS_SECRET_ACCESS_KEY: Secret access key for S3 user credential
