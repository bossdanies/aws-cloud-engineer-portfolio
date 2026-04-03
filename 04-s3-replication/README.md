# AWS S3 Cross-Region Replication (CRR) Setup

## 📌 Project Overview

This project demonstrates how to configure Cross-Region Replication (CRR) between two Amazon S3 buckets.

Cross-Region Replication automatically replicates objects from a source bucket in one AWS region to a destination bucket in another region. This feature is commonly used for disaster recovery, data redundancy, and compliance requirements.

In this lab, a replication rule is configured to replicate objects uploaded to a source bucket in **us-east-1** to a destination bucket in **us-east-2**.

---

## 🏗️ Architecture
```
│▼ Source S3 Bucket (us-east-1)
│▼ Cross-Region Replication Rule
│▼ Destination S3 Bucket (us-east-2)
```
---

## ⚙️ AWS Services Used

- Amazon S3
- S3 Cross-Region Replication (CRR)
- AWS IAM (Replication permissions)

---

## 📊 Bucket Configuration

| Resource | Name |
|--------|--------|
| Source Bucket | source-s3-bucket-01-2026 |
| Source Region | us-east-1 (N. Virginia) |
| Destination Bucket | destination-s3-bucket-02-2026 |
| Destination Region | us-east-2 (Ohio) |
| Versioning | Enabled on both buckets |

---

## 🚀 Replication Rule Configuration

| Setting | Value |
|--------|--------|
| Rule Name | s3-region-replication-2026 |
| Scope | Entire bucket |
| Destination Bucket | destination-s3-bucket-02-2026 |
| Destination Region | us-east-2 |
| Storage Class | Same as source |
| Replica Owner | Same as source |
| Replication Time Control | Disabled |
| KMS Encrypted Objects | Not replicated |
| Replica Modification Sync | Disabled |

---

## Deployment Steps

### Step 1 — Create S3 Buckets in Different Regions

Two S3 buckets are created in different AWS regions to enable cross-region replication.

![Step 1 - Create Buckets](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-01-create-s3-buckets-cross-region.png)

---

### Step 2 — Access Replication Configuration

The replication configuration settings are accessed in the source bucket.

![Step 2 - Open Replication Configuration](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-02-open-s3-replication-configuration.png)

---

### Step 3 — Create Cross-Region Replication Rule

A replication rule is configured to replicate objects from the source bucket to the destination bucket.

![Step 3 - Create Replication Rule](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-03-create-cross-region-replication-rule.png)

---

### Step 4 — Replication Rule Enabled

The replication rule is successfully created and enabled.

![Step 4 - Replication Rule Enabled](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-04-cross-region-replication-rule-enabled.png)

---

### Step 5 — Upload Test Object to Source Bucket

A test object is uploaded to the source bucket to verify replication.

![Step 5 - Object Uploaded](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-05-object-uploaded-to-source-bucket.png)

---

### Step 6 — Verify Object Replication

The uploaded object is automatically replicated to the destination bucket in the secondary region.

![Step 6 - Object Replicated](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-06-object-replicated-to-destination-bucket.png)

---

## 💥 Result

Cross-Region Replication was successfully configured and verified.

Objects uploaded to the source bucket are automatically replicated to the destination bucket located in another AWS region.

Source: **source-s3-bucket-01-2026 (us-east-1)**  
Destination: **destination-s3-bucket-02-2026 (us-east-2)**

---

## 🎯 Skills Demonstrated

- Amazon S3 Bucket Configuration
- S3 Versioning Management
- Cross-Region Replication Setup
- Multi-Region Data Protection
- Cloud Storage Disaster Recovery Strategy
