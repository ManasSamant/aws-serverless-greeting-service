# AWS Serverless Greeting Service

A simple serverless application developed using **AWS Lambda** and **Amazon API Gateway**. The project demonstrates how a Lambda function can be deployed and exposed through an HTTP API, with invocation activity monitored using **Amazon CloudWatch**.

## Overview

This project was developed as part of a Cloud Computing assignment to gain practical experience with AWS serverless technologies.

The application implements a simple greeting service using:

* AWS Lambda
* Amazon API Gateway
* Amazon CloudWatch
* AWS IAM execution roles
* HTTP API
* `/hello` route

The Lambda function was deployed and connected to an HTTP API through Amazon API Gateway. The resulting endpoint was tested through a web browser, and CloudWatch logs were reviewed to verify successful Lambda invocations.

## Architecture

The basic request flow is:

```text
Client / Browser
       |
       v
Amazon API Gateway
       |
       |  HTTP GET /hello
       v
AWS Lambda Function
       |
       v
Greeting Response
       |
       v
Amazon CloudWatch Logs
```

## AWS Services Used

### AWS Lambda

AWS Lambda was used to create and deploy the serverless function responsible for processing the incoming request and returning a greeting response.

The Lambda function was configured with an appropriate execution role and tested after deployment.

### Amazon API Gateway

Amazon API Gateway was used to expose the Lambda function through an HTTP API.

A `/hello` route was configured to invoke the Lambda function.

### Amazon CloudWatch

Amazon CloudWatch was used to inspect Lambda invocation logs and verify that requests were successfully processed.

### AWS IAM

An execution role was configured for the Lambda function to provide the required permissions for its operation.

## Implementation

The project involved the following steps:

1. Created an AWS Lambda function.
2. Configured the Lambda function and its execution role.
3. Deployed and tested the Lambda function.
4. Created an HTTP API using Amazon API Gateway.
5. Configured the `/hello` route.
6. Connected the API route to the Lambda function.
7. Deployed the API.
8. Obtained the API invocation URL.
9. Tested the endpoint through a web browser.
10. Verified successful Lambda invocations using Amazon CloudWatch logs.

## API Endpoint

The application exposes the following route:

```text
GET /hello
```

The endpoint can be accessed through the API Gateway invocation URL generated during deployment.

## Testing

The deployed API was tested through the browser using the generated API Gateway invocation URL.

The testing process verified that:

* The API Gateway endpoint was accessible.
* The `/hello` route successfully invoked the Lambda function.
* The Lambda function generated the expected greeting response.
* Lambda invocation activity was recorded in Amazon CloudWatch.
* The integration between API Gateway and Lambda was functioning correctly.

## Evidence

The repository contains documentation and screenshots demonstrating the implementation and testing process.

### Lambda

* Lambda function configuration
* Lambda deployment and completion
* Lambda Function ARN

### API Gateway

* API Gateway configuration
* HTTP API and `/hello` route
* API invocation URL
* Endpoint output

### CloudWatch

* CloudWatch log groups
* Lambda invocation logs

### AWS Region

* AWS region used during the implementation

### Assignment Documentation

The repository also contains the assignment documentation and reflection describing the learning outcomes and implementation experience.

## Learning Outcomes

Through this assignment, I gained practical experience with serverless application development using AWS.

The main concepts learned include:

* Understanding the working principles of AWS Lambda.
* Creating, configuring, deploying, and testing Lambda functions.
* Understanding serverless application architecture.
* Creating HTTP APIs using Amazon API Gateway.
* Configuring API routes and Lambda integrations.
* Understanding API access and data mapping concepts.
* Configuring Lambda execution permissions.
* Monitoring Lambda executions using CloudWatch.
* Understanding how AWS services interact to provide a serverless application.

## Reflection

The recommended AWS learning courses provided the foundation required to complete this practical implementation.

The **AWS Lambda Foundations** course helped me understand how AWS Lambda works and how Lambda functions can be configured, deployed, and tested.

The **Amazon API Gateway for Serverless Applications** course provided an understanding of API Gateway, including HTTP/REST APIs, API access management, and data mapping.

The practical implementation helped connect these concepts by building a complete serverless greeting service using Lambda and API Gateway and verifying its operation through CloudWatch logs.

## Project Structure

```text
aws-serverless-greeting-service/
│
├── README.md
│
├── documentation/
│   ├── AWS Lambda documentation
│   ├── Amazon API Gateway documentation
│   ├── Assignment documentation
│   └── Reflection
│
└── screenshots/
    ├── Lambda screenshots
    ├── API Gateway screenshots
    ├── CloudWatch screenshots
    ├── Invocation URL screenshots
    └── AWS region screenshot
```

## Author

**Manas Samant**

Matriculation Number: **227129**

M.Sc. Software Engineering
Hochschule Heilbronn

---

## License

This repository was created for academic purposes as part of a Cloud Computing assignment.
