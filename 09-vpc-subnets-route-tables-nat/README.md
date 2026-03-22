# AWS VPC Subnets, Route Tables and NAT Gateway

## Project Overview

This project demonstrates how to configure a complete AWS VPC networking architecture, including public and private subnets, Internet Gateway, route tables, and a NAT Gateway.

The goal is to simulate a real-world cloud network where public resources have direct internet access and private resources securely access the internet through a NAT Gateway.

This setup follows AWS best practices for secure and scalable infrastructure design.

---

## Architecture

Custom VPC (10.0.0.0/24)

│
├── Public Subnet (10.0.0.0/25)
│   ├── Internet Gateway
│   └── NAT Gateway
│
└── Private Subnet (10.0.0.128/25)
└── Route Table → NAT Gateway

---

## AWS Services Used

* Amazon VPC
* Subnets
* Internet Gateway
* NAT Gateway
* Route Tables

---

## Network Configuration

| Resource              | Name              |
| --------------------- | ----------------- |
| VPC                   | my-vpc-01         |
| Public Subnet         | public-subnet-01  |
| Private Subnet        | private-subnet-01 |
| Internet Gateway      | my-igw-01         |
| NAT Gateway           | nat-gateway-01    |
| Route Table (Public)  | public-rt-01      |
| Route Table (Private) | private-rt-01     |

CIDR Block: **10.0.0.0/24**

---

## Deployment Steps

## ![Step 1 - Create VPC](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-01-create-vpc.png)

## ![Step 2 - VPC Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-02-vpc-created.png)

## ![Step 3 - VPC Dashboard](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-03-vpc-dashboard.png)

## ![Step 4 - Edit VPC Settings](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-04-edit-vpc-settings.png)

## ![Step 5 - Enable DNS Hostnames](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-05-enable-dns-hostnames.png)

## ![Step 6 - Create Internet Gateway](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-06-create-internet-gateway.png)

## ![Step 7 - Internet Gateway Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-07-internet-gateway-created.png)

## ![Step 8 - Attach Internet Gateway to VPC](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-08-attach-internet-gateway.png)

## ![Step 9 - Internet Gateway Attached](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-09-internet-gateway-attached.png)

## ![Step 10 - Create Public Subnet](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-10-create-public-subnet.png)

## ![Step 11 - Public Subnet Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-11-public-subnet-created.png)

## ![Step 12 - Create Private Subnet](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-12-create-private-subnet.png)

## ![Step 13 - Private Subnet Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-13-private-subnet-created.png)

## ![Step 14 - Create Route Table](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-14-create-route-table.png)

## ![Step 15 - Route Table Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-15-route-table-created.png)

## ![Step 16 - Associate Public Subnet](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-16-associate-public-subnet.png)

## ![Step 17 - Public Route Table Associated](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-17-public-route-table-associated.png)

## ![Step 18 - Create NAT Gateway](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-18-create-nat-gateway.png)

## ![Step 19 - NAT Gateway Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-19-nat-gateway-created.png)

## ![Step 20 - Configure Private Route Table](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-20-configure-private-route.png)

## ![Step 21 - Associate Private Subnet](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/42a88b566001bf885d439dc02418c3b075ee8993/09-vpc-subnets-route-tables-nat/step-21-private-route-table-associated.png)

## Result

A fully functional AWS VPC networking architecture was successfully deployed.

* Public subnet has direct internet access via Internet Gateway
* Private subnet accesses the internet securely through NAT Gateway
* Proper routing ensures secure and controlled traffic flow

---

## Skills Demonstrated

* AWS VPC Networking
* Public and Private Subnet Design
* Internet Gateway Configuration
* NAT Gateway Deployment
* Route Table Management
* Secure Cloud Architecture

