# AWS VPC Peering Connection Setup

## 📌 Project Overview
This project demonstrates how to create two Virtual Private Clouds (VPCs) and establish a VPC Peering connection between them.

VPC Peering enables private communication between VPCs without using the public internet, improving security and performance.

This setup follows AWS networking best practices by isolating environments while allowing controlled communication between them.

---

## 🏗️ Architecture
```
│▼ VPC 1 (10.0.0.0/24)
│▼ VPC Peering Connection  
│▼ VPC 2 (172.31.0.0/16)
```
---

## ⚙️ AWS Services Used

- Amazon VPC  
- VPC Peering  
- Route Tables  
- AWS Networking  

---

## 📊 Configuration Details

| Resource | Name |
|--------|--------|
| VPC 1 | north-vpc-03-20-26 |
| VPC 2 | east-vpc-03-20-26 |
| CIDR VPC 1 | 10.0.0.0/24 |
| CIDR VPC 2 | 172.31.0.0/16 |
| Peering Connection | first-peering-03-26 |

---

## 🚀 Deployment Steps

### Step 1 — Search VPC Service
Navigate to the AWS console and search for the VPC service.

![Step 1](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step01-search-vpc-service.png)

---

### Step 2 — Create First VPC
Create the first VPC with CIDR block 10.0.0.0/24.

![Step 2](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step02-create-first-vpc.png)

---

### Step 3 — First VPC Created
Verify that the first VPC is successfully created.

![Step 3](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step03-first-vpc-created.png)

---

### Step 4 — Create Second VPC
Create the second VPC with CIDR block 172.31.0.0/16.

![Step 4](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step04-create-second-vpc.png)

---

### Step 5 — Second VPC Created
Verify that the second VPC is successfully created.

![Step 5](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step05-second-vpc-created.png)

---

### Step 6 — Create Peering Connection
Create a VPC Peering connection between both VPCs.

![Step 6](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step06-create-peering-connection.png)

---

### Step 7 — Peering Request Pending
The peering connection is created and waiting for acceptance.

![Step 7](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step07-peering-request-pending.png)

---

### Step 8 — Accept Peering Request
Accept the peering request to establish the connection.

![Step 8](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step08-accept-peering-request.png)

---

### Step 9 — Confirm Peering
Confirm the connection details and finalize the setup.

![Step 9](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step09-peering-confirmation.png)

---

### Step 10 — Peering Active
The VPC Peering connection is now active.

![Step 10](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/347619b85789a5bfabd6f3e1863d6bb27565ab42/08-vpc-peering-connection/step10-peering-active.png)

---

## Important Note

To enable full communication between VPCs, route tables must be updated in both VPCs to include routes pointing to the peering connection.

Without route table configuration, the peering connection will not allow traffic flow.

---

## 💥 Result

Two VPCs were successfully created and connected using VPC Peering.

The environments remain isolated but can communicate privately through AWS internal networking.

---

## 🎯 Skills Demonstrated

- VPC Creation  
- CIDR Block Configuration  
- VPC Peering Setup  
- AWS Networking Fundamentals  
- Route Table Awareness  
- Cloud Architecture Design  
