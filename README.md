# PagerDuty skill for Amazon Echo (Alexa)

An Amazon Alexa skill that provides information about PagerDuty.

To use this skill you'll need a PagerDuty API key, which can be created as follows: 
https://support.pagerduty.com/hc/en-us/articles/202829310-Generating-an-API-Key

## Development

Run `npm install` to install needed dependencies.

The PagerDuty skill runs on Node 4.3 in AWS Lambda. [Node Version Manager](https://github.com/creationix/nvm) (`nvm`) is used to run the same version of Node locally.

[`grunt-aws-lambda`](https://github.com/Tim-B/grunt-aws-lambda) is used to manage the Lambda code.

To run the skill locally, provide a `test/event.json` file with a mock Lambda request. Execute `grunt invoke` to run the code.

## Deployment

To deploy, run `grunt deploy`. The code will be packaged and uploaded to AWS Lambda.

You must have [valid AWS credentials](https://github.com/Tim-B/grunt-aws-lambda#aws-credentials).
