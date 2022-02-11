# AWS CloudFormation Inline Python Lambda Example

## What it does

This CloudFormation template deploys an AWS Lambda function, Amazon DynamoDB table, Amazon CloudWatch Logs log group, and all IAM roles with the minimum necessary permissions.

The Lambda function itself inserts a random 10-character alphabetic string into the DynamoDB table whenever it's invoked. The function also makes use of the [logging library](https://docs.aws.amazon.com/lambda/latest/dg/python-logging.html#python-logging-lib) to display relevant output.

This project is intended to act as a boilerplate to reduce the development effort of deploying a Python Lambda function with CloudFormation. It also exposes Lambda environment variables through CloudFormation parameters. Please fork this repo and customize the Lambda function and other services to meet your needs.

## Prerequisites

1. An [AWS account](https://aws.amazon.com/account/)
2. Access to the console or [AWS CLI](https://aws.amazon.com/cli/). I recommend using [AWS CloudShell](https://aws.amazon.com/cloudshell/) for easy CLI access.

## Deployment Steps

You can deploy this template [using the console](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-using-console.html), or [use the AWS CLI, as detailed here](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/deploy/).

### Invoking the deployed Lambda function

- Check the 'Outputs' section of the CloudFormation console to get the CLI command that will invoke the Lambda function.

### Validating functionality

- After the Lambda was invoked, check the DynamoDB table to verify that the new random value added.

- Under the 'Resources' section of the CloudFormation console, navigate to the newly-created CloudWatch Logs log group to see the output from the Lambda function.

### Clean up

- When you're done experimenting with this, delete the CloudFormation stack by using the console. Navigate to **CloudFormation** > **Stacks** > Choose the stack you deployed > Select **Delete**

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.
