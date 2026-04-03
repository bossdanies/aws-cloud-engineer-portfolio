# AWS VPC Web Server Deployment

## 📌 Project Overview

This project demonstrates how to deploy a public web server in AWS using a custom Virtual Private Cloud (VPC) architecture.  
The infrastructure includes networking components such as a VPC, public subnet, Internet Gateway, route tables, and an EC2 instance.

The goal is to simulate a real-world cloud networking setup used in production environments.

---

## 🏗️ Architecture
```
│▼ Custom VPC (10.0.0.0/24)
│▼ Public Subnet    
│▼ Internet Gateway  
│▼ Route Table  
│▼ EC2 Instance (Web Server)
```
---

## ⚙️ AWS Services Used

- Amazon VPC
- Subnets
- Internet Gateway
- Route Tables
- Amazon EC2

---

## 📊 Network Configuration

| Resource | Name |
|--------|--------|
| VPC | web-server-vpc |
| Subnet | web-public-subnet |
| Internet Gateway | my-vpc-igw-01 |
| Route Table | web-route-table-01 |
| EC2 Instance | web-server-ec2-01 |

CIDR Block: **10.0.0.0/24**

---

## 🚀 Deployment Steps

### Step 1 — Create VPC

![Step 1 - Create VPC](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step01-create-vpc.png)

---

### Step 2 — VPC Created

![Step 2 - VPC Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step02-vpc-created.png)

---

### Step 3 — Create Public Subnet

![Step 3 - Create Subnet](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step03-create-subnet.png)

---

### Step 4 — Subnet Created

![Step 4 - Subnet Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step04-subnet-created.png)

---

### Step 5 — Create Internet Gateway

![Step 5 - Create Internet Gateway](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step05-create-internet-gateway.png)

---

### Step 6 — Internet Gateway Created

![Step 6 - Internet Gateway Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/db30f058bd6946ee8f021835134f1784c0ca27f4/05-setting-up-web-server-on-an-ec2-instance/step06-internet-gateway-created.png)

---

### Step 7 — Attach Internet Gateway to VPC

![Step 7 - Attach Internet Gateway](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/88c5392cb6a89de5378dd3cfcb6677311270f7af/05-setting-up-web-server-on-an-ec2-instance/step07-attach-internet-gateway-to-vpc.png)

---

### Step 8 — Internet Gateway Attached

![Step 8 - Internet Gateway Attached](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step08-internet-gateway-attached.png)

---

### Step 9 — View Route Tables

![Step 9 - View Route Tables](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step09-view-route-tables.png)

---

### Step 10 — Create Route Table

![Step 10 - Create Route Table](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step10-create-route-table.png)

---

### Step 11 — Route Table Created

![Step 11 - Route Table Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step11-route-table-created.png)

---

### Step 12 — Add Internet Route

Destination: **0.0.0.0/0**  
Target: **Internet Gateway**

![Step 12 - Add Route](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step12-add-route-to-internet-gateway.png)

---

### Step 13 — Route Added

![Step 13 - Route Added](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step13-route-added.png)

---

### Step 14 — Associate Subnet

![Step 14 - Associate Subnet](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step14-associate-subnet-route-table.png)

---

### Step 15 — Subnet Associated

![Step 15 - Subnet Associated](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step15-subnet-associated.png)

---

### Step 16 — Launch EC2 Instance

![Step 16 - Launch EC2](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step16-launch-ec2-instance.png)

---

### Step 17 — Instance Launch Initiated

![Step 17 - Instance Launching](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step17-ec2-instance-launching.png)

---

### Step 18 — Instance Running

![Step 18 - Instance Running](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step18-ec2-instance-running.png)

---

### Step 19 — Web Server Accessed via Public IP

![Step 19 - Web Server Accessed](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/127e93acb39771b84579c10bf9d906006b3533ba/05-setting-up-web-server-on-an-ec2-instance/step19-web-server-accessed.png)

---

## 💥 Result

A fully functional AWS infrastructure was deployed with a publicly accessible EC2 web server.

The server is reachable via its public IPv4 address through the configured Internet Gateway and route table.

---

## 🎯 Skills Demonstrated

- AWS Networking
- VPC Design
- Subnet Architecture
- Internet Gateway Configuration
- Route Table Management
- EC2 Instance Deployment
- Public Web Server Hosting
