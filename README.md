# [Copying objects greater than 5 GB with Amazon S3 Batch Operations](https://aws.amazon.com/blogs/storage/copying-objects-greater-than-5-gb-with-amazon-s3-batch-operations/)


## Description
[AWS Cloudformation](https://aws.amazon.com/cloudformation/) template to deploy [AWS Lambda](https://aws.amazon.com/lambda/) function and [AWS IAM roles](https://aws.amazon.com/iam/) required for [Amazon S3 Batch Operations](https://aws.amazon.com/s3/features/batch-operations/) [Invoke Lambda Job](https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops-invoke-lambda.html)

## Features
1. Copying Amazon S3 individual objects larger than 5GB
2. Rename objects during copy, by changing the destination prefix, for example copy objects in 's3://mybucket/oldprefix/object1' 's3://mybucket/newprefix/myobject1'. To use this, enter a value for the stack parameter destination prefix and set "UpdateKeyLeadingPrefix" to Enable.
3. Copy object metadata and tags
4. Cross region, cross Account copy [Not all objects larger than 5 GB can be copied within the current Lambda function 15-minute timeout limit, especially across AWS Regions. The solution has been tested successfully, under ideal conditions, with up to 2-TB single objects size in the same region and with a 1-TB single object size between two regions EU-WEST-2 and US-EAST-1.]

## Prerequisites
1. [An AWS Account](https://aws.amazon.com/account/)
2. [An AWS IAM Identity](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction_identity-management.html) with appropriate permissions to deploy the Cloudformation stack and resources
3. Your source and destination [Amazon S3 bucket](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html)
4. An Amazon S3 bucket to store the [Amazon S3 Batch Operation job report](https://docs.aws.amazon.com/AmazonS3/latest/userguide/batch-ops-job-status.html)


## Installation and Usage

1. Download the cloudformation template
2. Deploy the template and modify the parameters to match your specific resources and use case
3. Create or generate a manifest or use Amazon S3 Inventory report
4. Create an Amazon S3 Batch Operations Invoke Lambda job
5. Monitor the progress and confirm successful completion


Refer to the [blog](https://aws.amazon.com/blogs/storage/copying-objects-greater-than-5-gb-with-amazon-s3-batch-operations/)  for more details.

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.