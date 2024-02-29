# Orders API using AWS SAM

This project implements an Orders API using AWS Serverless Application Model (SAM). The API allows you to manage orders with basic CRUD operations.

## Table of Contents

- [Image of Flow](#image-of-flow)
- [Prerequisites](#prerequisites)
- [SAM Template Overview](#sam-template-overview)
- [Deployment](#deployment)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [License](#license)


## Prerequisites

Before deploying the Orders API, ensure you have the following:

- [AWS CLI](https://aws.amazon.com/cli/) installed and configured.
- [AWS SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html) installed.
- Java 11 runtime environment.

## SAM Template Overview

The SAM template (`template.yaml`) defines the AWS resources needed for the Orders API. It includes a DynamoDB table for storing orders, Lambda functions for creating and reading orders, and API Gateway configurations.

## Image of Flow

<img src="./APIGW.png" alt="Orders API Flow" width="400">

### Resources

- [OrdersTable](#orderstable): DynamoDB table for storing orders.
- [CreateOrderFunction](#createorderfunction): Lambda function for creating orders.
- [ReadOrdersFunction](#readordersfunction): Lambda function for reading orders.

For more details, refer to the [template.yaml](template.yaml) file.

## Project Structure

[Project Structure](./Project%20Structure.png)

<img src="./Project Structure.png" alt="Project Structure" width="400">

## Deployment

To deploy the Orders API, run the following commands in your terminal:

```bash
sam build
sam deploy --guided