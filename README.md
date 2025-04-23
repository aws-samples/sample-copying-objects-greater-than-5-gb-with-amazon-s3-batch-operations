# s3-batch-invoke-lambda

External Blog: https://aws.amazon.com/blogs/storage/copying-objects-greater-than-5-gb-with-amazon-s3-batch-operations/

**Copying objects greater than 5 GB with Amazon S3 Batch Operations**


A large number of customers store their data in Amazon S3, and some of these customers scale to millions or billions of individual objects. Amazon S3 customers need an easy, reliable, and scalable way to perform bulk operations on these large datasets – with objects ranging in size from a few kilobytes up to 5 GB. Amazon S3 Batch Operations lets you manage billions of objects at scale with just a few clicks in the Amazon S3 console or a single API request. A few of the supported operations include copying, replacing tags, replacing access control, and invoking AWS Lambda functions.

As of the writing of this blog, the copy operation supports objects up 5-GB individual size. As customers have objects of all sizes stored in Amazon S3, you may at times need to copy objects larger than 5 GB.

This cloudformation deploys a Lambda function that that provides you with the ability to copy objects larger than 5 GB using the S3 Batch Invoke Lambda operation.

Not all objects larger than 5 GB can be copied within the current Lambda function 15-minute timeout limit, especially across AWS Regions. The solution has been tested successfully, under ideal conditions, with up to 2-TB single objects size in the same region and with a 1-TB single object size between two regions EU-WEST-2 and US-EAST-1.
