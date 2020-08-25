# Automatic deletion of S3 bucket on Cloudformation stack deletion

A common problem when deploying S3 buckets with Cloudformation is when deleting the stack, the S3 bucket might not be empy.

This is some boilerplate code to automatically empty an S3 bucket, so it can be deleted together with the stack. Uses Cloudformation AWS::Serverless library (AWS SAM) and requires the `requests` package.

Based on Amazon's own code for `cfnrequest` for [Cloudformation Custom Resource backed by Lambda](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-lambda-function-code-cfnresponsemodule.html).