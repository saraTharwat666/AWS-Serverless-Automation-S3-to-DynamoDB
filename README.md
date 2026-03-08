🚀 AWS Serverless Automation: S3 to DynamoDB
Building a seamless file management pipeline using AWS Lambda, S3, and DynamoDB.

The Workflow:
Storage Setup: Created a Public S3 Bucket (Uploads) and a Private S3 Bucket (Secure Storage).

Database Logging: Provisioned a DynamoDB Table (xfusion-S3CopyLogs) to track every transfer with a unique LogID.

The Engine (Lambda): Developed a Python-based Lambda function triggered by S3 ObjectCreated events.

Security First: Configured a custom IAM Role (Least Privilege) to allow S3 Copying and DynamoDB Writing.

Execution: Once a file hits the public bucket, Lambda instantly:

Copies the file to the private bucket.

Logs the metadata (Source, Dest, Key) into DynamoDB.

Tech Stack:
☁️ AWS Lambda | 📦 Amazon S3 | 🗄️ Amazon DynamoDB | 🐍 Python (Boto3) | 🔐 IAM
