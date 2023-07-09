# Amazon Web Services - Voting Application

Here's a simplified breakdown of the proposed scheme for deploying the voting application on AWS using various services:

1. Front-end Components:
   - The application has two front-end components written in JavaScript as a Single-Page Application (SPA).
   - Each front-end component's static files will be published in separate S3 buckets.

2. Back-end Components:
   - The application has three back-end components written in Python.
   - The back-end components will be hosted as Lambda functions, which are serverless compute services provided by AWS.
   - The Lambda functions will be made accessible to the front-end components using API Gateway, which acts as a proxy and handles HTTP requests.

3. Vote Processor:
   - The vote processor, which is a part of the back-end, can be run on EC2 instances. EC2 is a virtual server provided by AWS.
   - Alternatively, you can choose to implement the vote processor using serverless architecture as well.

Overall, the proposed deployment scheme suggests using S3 buckets to store static front-end files, Lambda functions with API Gateway to host and access the back-end components, and optionally using EC2 or serverless architecture for the vote processor.

![Screenshot_31](https://user-images.githubusercontent.com/4441068/212905590-feb78ec6-16ba-428e-99bd-c08d3da777ac.png)


Note that while all the code has already been written, you still have a lot of work to do in creating resources (queues, DynamoDB tables) and assigning access to them. If necessary, use the hints located in the appropriate folders.

## Used tech

* ✅ EC2
* ✅ S3
* ✅ CloudFront
* ✅ database (DynamoDB)
* ✅ VPC
* ✅ SQS queue
* ✅ SNS notifications
* ✅ Serverless (API Gateway, Lambda)
* ✅ IAM

Challenge:
* ⚠️ IaaC (Terraform, CloudFormation, Cloud Development Kit)
* ⚠️ Billing и Costs

## Components

* [API Gateway](./gateway)
* [voting frontend, Javascript](./voting-frontend)
* [voting backend, Python](./voting-backend)
* [vote processor, Python](./vote-processor)
* [database, DynamoDB](./dynamodb)
* [result backend, Python](./result-backend)
* [result frontend, Javascript](./result-frontend)

## Architecture


![Screenshot_31](https://user-images.githubusercontent.com/4441068/212555680-28762471-036b-4beb-af78-6c4e38e2276e.png)




For terraform, i used serverless lambda instead of ec2

![Screenshot_43](https://user-images.githubusercontent.com/4441068/215296208-a9f390c4-9d32-461e-8b46-0450a737b71f.png)

