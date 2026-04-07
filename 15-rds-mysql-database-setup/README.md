# AWS RDS MySQL Database Deployment

## 📌 Project Overview

This project demonstrates how to create and configure a MySQL database using Amazon RDS in AWS.

Amazon RDS simplifies database management by handling provisioning, backups, patching, and scaling.

The goal is to deploy a relational database inside a custom VPC using proper subnet configuration across multiple Availability Zones.

---

## 🏗️ Architecture
```
│▼ VPC
│▼ Subnet (AZ-1)
│▼ Subnet (AZ-2)
│▼ DB Subnet Group
│▼ Amazon RDS (MySQL)
```

---

## ⚙️ AWS Services Used

- Amazon RDS  
- Amazon VPC  
- Subnets  
- DB Subnet Group  
- Security Groups  

---

## 📊 Configuration Details

| Resource            | Name        |
|---------------------|------------|
| DB Instance         | database-2 |
| Engine              | MySQL      |
| Instance Class      | db.t3.micro |
| Deployment Type     | Single-AZ  |
| VPC                 | Custom VPC |
| Subnet Group        | default    |
| Public Access       | Disabled   |

---

## 🚀 Deployment Steps

### Step 1 — Create Database

![Step 1](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c0cf4f134ab399be327e790ad7d113ca4ffff56f/15-rds-mysql-database-setup/step-01-create-database.png)

---

### Step 2 — Select MySQL Engine

![Step 2](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c0cf4f134ab399be327e790ad7d113ca4ffff56f/15-rds-mysql-database-setup/step-02-engine-selection.png)

---

### Step 3 — Configure DB Instance

![Step 3](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c0cf4f134ab399be327e790ad7d113ca4ffff56f/15-rds-mysql-database-setup/step-03-db-settings.png)

---

### Step 4 — Configure Networking and Subnets

![Step 4](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c0cf4f134ab399be327e790ad7d113ca4ffff56f/15-rds-mysql-database-setup/step-04-network-config.png)

---

### Step 5 — Database Successfully Created

![Step 5](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c0cf4f134ab399be327e790ad7d113ca4ffff56f/15-rds-mysql-database-setup/step-05-database-created.png)

---

## 🎯 Skills Demonstrated

- How to deploy a MySQL database using Amazon RDS  
- Understanding of DB Subnet Groups  
- Multi-AZ subnet configuration requirements  
- VPC networking integration with RDS  
- Basic database architecture in AWS  
