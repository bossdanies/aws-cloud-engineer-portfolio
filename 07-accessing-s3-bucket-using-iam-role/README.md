# AWS IAM Role for EC2 S3 Access

## 📌 Project Overview

This project demonstrates how to create an IAM Role that allows an EC2 instance to securely access Amazon S3 resources.

Instead of storing credentials directly on the server, an IAM role is attached to the EC2 instance to grant temporary permissions.

This is a best practice in AWS security architecture because it eliminates the need to manage access keys on servers.

---

## 🏗️ Architecture
```
│▼ EC2 Instance
│▼ IAM Role
│▼ Amazon S3 Read Access
```
---

## ⚙️ AWS Services Used

- AWS Identity and Access Management (IAM)
- Amazon EC2
- Amazon S3
- AWS CloudShell

---

## 📊 Configuration Details

| Resource | Name |
|--------|--------|
| IAM Role | s3-access-01 |
| Trusted Entity | EC2 |
| Permission Policy | AmazonS3ReadOnlyAccess |
| EC2 Instance | my-instance-01 |
| S3 Bucket | bucket-aws-01-2026 |

---

## 🚀 Deployment Steps

### Step 1 — Create IAM Role for EC2

An IAM role is created with **EC2 as the trusted entity**, allowing EC2 instances to assume the role.

![Step 1 - Create IAM Role](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step01-create-iam-role.png)

---

### Step 2 — Attach S3 Read Policy

The **AmazonS3ReadOnlyAccess** managed policy is attached to the role.

![Step 2 - Attach Policy](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step02-attach-policy.png)

---

### Step 3 — Configure Role Name

The role is named **s3-access-01** and the configuration is reviewed before creation.

![Step 3 - Role Configuration](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step03-role-configuration.png)

---

### Step 4 — IAM Role Created

The IAM role is successfully created and available in the IAM roles list.

![Step 4 - Role Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step04-role-created.png)

---

### Step 5 — Attach IAM Role to EC2 Instance

The IAM role is attached to the EC2 instance using the **Modify IAM Role** option.

![Step 5 - Attach Role to EC2](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step05-attach-role-ec2.png)

---

### Step 6 — Role Successfully Attached

The role is successfully attached to the running EC2 instance.

![Step 6 - Role Attached](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step06-role-attached.png)

---

### Step 7 — Create S3 Bucket

An S3 bucket is created to store objects.

![Step 7 - Create Bucket](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step07-create-bucket.png)

---

### Step 8 — Access Bucket Objects

The bucket is opened and ready for object upload.

![Step 8 - Open Bucket](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step08-open-bucket.png)

---

### Step 9 — Upload Test File

A test file (**Hello.txt**) is uploaded to the S3 bucket.

![Step 9 - Upload File](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step09-upload-file.png)

---

### Step 10 — Upload Successful

The object upload is confirmed.

![Step 10 - Upload Success](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step10-upload-success.png)

---

### Step 11 — Verify Access from EC2

Using AWS CloudShell, the command `aws s3 ls` is executed to verify access to the S3 bucket.

![Step 11 - Verify Access](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/5bced0329bfd3ae1fa0f061aa54d9c55d8decbbd/07-accessing-s3-bucket-using-iam-role/step11-verify-access.png)

---
## 🎯 Skills Demonstrated

- IAM Role Creation
- EC2 Instance Role Attachment
- AWS Security Best Practices
- Amazon S3 Access Management
- Cloud Identity and Access Management
