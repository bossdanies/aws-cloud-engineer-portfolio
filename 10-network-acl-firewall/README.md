
# AWS Network ACL Firewall Configuration

## 📌 Project Overview

This project demonstrates how to configure a Network Access Control List (NACL) in AWS to control inbound and outbound traffic at the subnet level.

A Network ACL acts as a stateless firewall, allowing or denying traffic based on defined rules.

The goal is to understand how to implement an additional layer of security in a VPC environment.

---

## 🏗️ Architecture

```
VPC

│
├── Subnet
│ └── Network ACL (Firewall)
│ ├── Inbound Rules
│ └── Outbound Rules
```

---

## ⚙️ AWS Services Used

- Amazon VPC
- Network ACLs (NACL)

---

## 📊 Configuration Details

| Resource     | Name    |
|--------------|--------|
| VPC          | my-vpc-01 |
| Network ACL  | nacl-01   |

---

## 🚀 Deployment Steps

### Step 1 — Create Network ACL  
A new Network ACL is created within the selected VPC.

![Step 1 - Create NACL](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/61e931319dbfeb8be260497aabf6c85a8ef49712/10-network-acl-firewall/step-01-create-nacl.png)

---

### Step 2 — Network ACL Created  
The Network ACL is successfully created and visible in the dashboard.

![Step 2 - NACL Dashboard](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/61e931319dbfeb8be260497aabf6c85a8ef49712/10-network-acl-firewall/step-02-nacl-dashboard.png)

---

## 💥 Result

A Network ACL was successfully created and configured.

The NACL can now be used to control inbound and outbound traffic at the subnet level, adding an extra layer of security to the VPC.

---

## 🎯 Skills Demonstrated

- AWS Network ACL Configuration  
- Subnet-Level Security  
- Inbound and Outbound Rule Management  
- Cloud Network Security Fundamentals 
