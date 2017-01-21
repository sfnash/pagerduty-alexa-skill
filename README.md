# PagerDuty skill for Amazon Echo (Alexa)

An Amazon Alexa skill that provides information about PagerDuty.
This is a fork of Steve Rice's [project](https://github.com/steverice/pagerduty-alexa-skill) which allows PagerDuty integration via an API key, rather than OAuth.

To use this skill you'll need a PagerDuty API key, which can be created using the following [instructions](https://support.pagerduty.com/hc/en-us/articles/202829310-Generating-an-API-Key).

## Getting started

Before you begin, make the following changes to the project:

### index.js

Set the following constants at the top of the file:

APP_ID       - This is your personal skill id from developer.amazon.com

ACCESS_TOKEN - Your personal PagerDuty API key

DEFAULT_NAME - Your name (this should match exactly what you've defined in your USER_KEYWORD customer slot type)

### Gruntfile.js

Update the ARN and region values in the lambda_deploy section, with the specifics from your own Amazon lambda instance.

## Development

Run `npm install` to install needed dependencies.

The PagerDuty skill runs on Node 4.3 in AWS Lambda. [Node Version Manager](https://github.com/creationix/nvm) (`nvm`) is used to run the same version of Node locally.

[`grunt-aws-lambda`](https://github.com/Tim-B/grunt-aws-lambda) is used to manage the Lambda code.

To run the skill locally, provide a `test/event.json` file with a mock Lambda request. Execute `grunt invoke` to run the code.

## Deployment

To deploy, run `grunt deploy`. The code will be packaged and uploaded to AWS Lambda.

You must have [valid AWS credentials](https://github.com/Tim-B/grunt-aws-lambda#aws-credentials).
