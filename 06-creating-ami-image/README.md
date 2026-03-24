# AWS EC2 AMI Image Creation

## 📌 Project Overview

This project demonstrates how to launch an EC2 instance and create a custom Amazon Machine Image (AMI) from it.

An AMI allows engineers to replicate servers quickly by creating a reusable image containing the operating system, installed software, and system configuration.

This practice is commonly used in cloud environments for infrastructure replication, backup strategies, and rapid server deployment.

---

## 🏗️ Architecture

EC2 Instance (Ubuntu)

│  
└── Custom AMI Image

---

## ⚙️ AWS Services Used

- Amazon EC2
- Amazon Machine Image (AMI)
- Elastic Block Store (EBS)

---

## 📊 Instance Configuration

| Resource | Name |
|--------|--------|
| EC2 Instance | my-instance-01 |
| Instance Type | t2.micro |
| Operating System | Ubuntu Server 24.04 LTS |
| Storage | 8 GiB EBS |
| AMI Image | my-instance-ami-image |

---

## 🚀 Deployment Steps

### Step 1 — Launch EC2 Instance

![Step 1 - Launch EC2 Instance](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/f6f392a075aada07dc9d068ddabaa9aa75be0b29/06-creating-ami-image/step1-launch-ec2-instance.png)

---

### Step 2 — Instance Launch Successful

![Step 2 - Instance Launch Successful](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/f6f392a075aada07dc9d068ddabaa9aa75be0b29/06-creating-ami-image/step2-ec2-instance-running.png)

---

### Step 3 — EC2 Instance Running and AMI Creation

![Step 3 - EC2 Instance Running](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/f6f392a075aada07dc9d068ddabaa9aa75be0b29/06-creating-ami-image/step3-create-ami-from-ec2.png)

---

## 💥 Result

A custom Amazon Machine Image (AMI) is created from the EC2 instance.

This AMI can now be used to launch new EC2 instances with the same operating system and configuration.

---

## 🎯 Skills Demonstrated

- EC2 Instance Deployment
- AMI Image Creation
- Ubuntu Server Provisioning
- Infrastructure Replication
- Cloud Backup Strategy
