Solution to check for SSL expiration with warnings beginning at 30 days and critical warnings beginning at 15 days from expiration.

Services Used To Monitor SSL Certificate:
AWS Lambda — Execute code without provisioning servers
AWS Cloud watch — Schedules lambda job
AWS SNS — Provides alerting for warnings and critical warnings on given days

Setup:

1. Create SNS Topic to receive alerts from SNS Dashboard from AWS Console
2. Create Lambda function
     'Edit the function Code Section'
     Code entry type: Edit Code inline
     Runtime: Python 2.7
     Handler: index.lambda_handler
     Download the Lambda function code below: 
     https://github.com/wed002/python-ssl-check/blob/main/ssl-check.py

3. Create a Schedule event using CloudWatch to call Lambda function daily   

