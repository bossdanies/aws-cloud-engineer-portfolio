# AWS VPC Flow Logs Monitoring

## 📌 Project Overview

This project demonstrates how to enable and configure VPC Flow Logs in AWS to capture network traffic information.

Flow logs provide visibility into the IP traffic going to and from network interfaces in a VPC, allowing monitoring, troubleshooting, and security analysis.

The goal is to implement network monitoring and store logs in Amazon S3 for further analysis.

---

## 🏗️ Architecture

```
│▼ VPC
│▼ Flow Logs
│▼ Amazon S3 Bucket
│▼ AWSLogs/
```

---

## ⚙️ AWS Services Used

- Amazon VPC  
- VPC Flow Logs  
- Amazon S3  

---

## 📊 Configuration Details

| Resource       | Name             |
|----------------|------------------|
| VPC            | my-vpc-01        |
| Flow Log       | flow-log-01      |
| Destination    | Amazon S3        |
| S3 Bucket      | demon-bucket-001 |

---

## 🚀 Deployment Steps

### Step 1 — Select VPC  
The VPC is selected to enable flow logs.

![Step 1 - Select VPC](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/ae895b841a691fdb63deedea372cc376738e0385/11-vpc-flow-logs-monitoring/step-01-select-vpc.png)

---

### Step 2 — Create Flow Log  
A flow log is configured to capture all traffic and send it to an S3 bucket.

![Step 2 - Create Flow Log](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/ae895b841a691fdb63deedea372cc376738e0385/11-vpc-flow-logs-monitoring/step-02-create-flow-log.png)

---

### Step 3 — Flow Log Created  
The flow log is successfully created and becomes active.

![Step 3 - Flow Log Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/ae895b841a691fdb63deedea372cc376738e0385/11-vpc-flow-logs-monitoring/step-03-flow-log-created.png)

---

### Step 4 — Verify Logs in S3  
The logs are delivered to the S3 bucket under the AWSLogs directory.

![Step 4 - S3 Logs](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/ae895b841a691fdb63deedea372cc376738e0385/11-vpc-flow-logs-monitoring/step-04-s3-logs.png)

---
## 🎯 Skills Demonstrated

- VPC Flow Logs Configuration  
- Network Traffic Monitoring  
- AWS Logging and Observability  
- S3 Integration for Log Storage  
- Cloud Security and Troubleshooting  


