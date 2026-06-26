# AWS Lambda Function and CloudWatch Logs

## 📌 Project Overview

This project demonstrates how to create an AWS Lambda function using Python, execute a test event, and monitor its execution through Amazon CloudWatch Logs.

AWS Lambda is a serverless compute service that automatically runs code in response to events without provisioning or managing servers. Amazon CloudWatch automatically captures execution logs, making it easy to monitor and troubleshoot Lambda functions.

The goal of this lab is to create a Lambda function, validate its execution, and verify that execution logs are successfully generated in CloudWatch.

---

## 🏗️ Architecture

```
│▼ AWS Lambda
│   ▼ Python Function
│
│▼ Test Event
│
│▼ Amazon CloudWatch
│   ▼ Log Group
│   ▼ Log Stream
```

---

## ⚙️ AWS Services Used

- AWS Lambda
- Amazon CloudWatch
- CloudWatch Logs
- IAM (Execution Role)

---

## 📊 Configuration Details

| Resource | Name |
|----------|------|
| Lambda Function | lambdademo |
| Runtime | Python 3.13 |
| Trigger | Manual Test Event |
| Execution Role | Default Lambda Execution Role |
| Log Group | /aws/lambda/lambdademo |
| Monitoring Service | Amazon CloudWatch Logs |

---

## 🚀 Deployment Steps

### Step 1 — Create Lambda Function

![Step 1](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/49909dec8c6700ff92d8e9e059b2c26c14c8f420/17-aws-lambda-cloudwatch-monitoring/step01-create-lambda-function.png)

---

### Step 2 — Review the Lambda Function

![Step 2](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/49909dec8c6700ff92d8e9e059b2c26c14c8f420/17-aws-lambda-cloudwatch-monitoring/step02-lambda-function-created.png)

---

### Step 3 — Create and Execute a Test Event

![Step 3](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/49909dec8c6700ff92d8e9e059b2c26c14c8f420/17-aws-lambda-cloudwatch-monitoring/step03-create-test-event.png)

---

### Step 4 — Verify the CloudWatch Log Group

![Step 4](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/49909dec8c6700ff92d8e9e059b2c26c14c8f420/17-aws-lambda-cloudwatch-monitoring/step04-cloudwatch-log-group.png)

---

### Step 5 — Review CloudWatch Log Events

![Step 5](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/49909dec8c6700ff92d8e9e059b2c26c14c8f420/17-aws-lambda-cloudwatch-monitoring/step05-cloudwatch-log-events.png)

---

## 🎯 Skills Demonstrated

- Creating an AWS Lambda function from scratch
- Configuring a Python runtime environment
- Executing Lambda functions using test events
- Understanding Lambda execution responses
- Monitoring Lambda execution with Amazon CloudWatch Logs
- Navigating CloudWatch Log Groups and Log Streams
- Verifying successful serverless function execution
