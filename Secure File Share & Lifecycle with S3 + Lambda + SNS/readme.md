# AWS File Processing Pipeline with Notifications

## Overview

This project automates the movement of files uploaded to an S3 bucket to an archive bucket using AWS Lambda. It also sends email notifications about the success or failure of the file processing using AWS SNS.

## Architecture

- S3 Upload Bucket: Receives new files  
- AWS Lambda: Triggered by new S3 uploads, moves files to Archive Bucket  
- S3 Archive Bucket: Stores processed files  
- SNS Topic: Sends email notifications about processing status

## Prerequisites

- AWS Account with appropriate IAM permissions  
- AWS CLI configured (optional for advanced usage)  
- Basic knowledge of AWS services (S3, Lambda, SNS)

## Setup Instructions

1. Create two S3 buckets: one for upload, one for archive  
2. Create an IAM role with permissions for Lambda to access S3, CloudWatch, and SNS  
3. Create a Lambda function with the IAM role attached  
4. Add an S3 trigger for the upload bucket on the Lambda function  
5. Create an SNS topic and subscribe your email  
6. Add environment variables to Lambda for the archive bucket name and SNS topic ARN  
7. Deploy Lambda code (see `lambda_function.py`)

## Lambda Function Code

python
<your-lambda-code-here>

## Testing
Upload a test file to the upload bucket
Verify the file moves to the archive bucket
Check your email for notification

## Future Improvements
Add Slack or SMS notifications
Implement retries and error handling improvements
Add CloudFormation or Terraform for infra as code

## Author
Kanika Arya

