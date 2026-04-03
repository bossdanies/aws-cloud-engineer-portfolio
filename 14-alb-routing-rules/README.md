# AWS Application Load Balancer - Routing Rules

## 📌 Project Overview

This project demonstrates how to create and configure routing rules in an Application Load Balancer (ALB) in AWS.

Routing rules allow you to control how incoming traffic is directed to different target groups based on conditions such as source IP, path, or host.

The goal is to simulate real-world traffic control and routing behavior used in production environments.

---

## 🏗️ Architecture
```
│▼ Client Request
│▼ Application Load Balancer (ALB)
│▼ Rule: Source IP (10.0.0.0/16)
│▼ Target Group 1 (EC2)
│▼ Default Rule
│▼ Target Group 2 (EC2)
```

---

## ⚙️ AWS Services Used

- Amazon EC2  
- Application Load Balancer (ALB)  
- Target Groups  
- Amazon VPC  

---

## 📊 Configuration Details

| Resource            | Name        |
|---------------------|------------|
| Load Balancer       | demon-001  |
| Listener            | HTTP:80    |
| Rule Condition      | Source IP (10.0.0.0/16) |
| Target Group        | demon-001  |
| Scheme              | Internet-facing |

---

## 🚀 Deployment Steps

### Step 1 — Select Load Balancer Type

![Step 1](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-01-select-load-balancer-type.png)

---

### Step 2 — Create Application Load Balancer

![Step 2](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-02-create-application-load-balancer.png)

---

### Step 3 — Load Balancer Created

![Step 3](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-03-load-balancer-created.png)

---

### Step 4 — Load Balancer Overview

![Step 4](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-04-load-balancer-overview.png)

---

### Step 5 — View Listeners and Rules

![Step 5](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-05-listeners-and-rules.png)

---

### Step 6 — Add New Rule

![Step 6](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-06-add-rule.png)

---

### Step 7 — Set Rule Priority

![Step 7](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-07-set-rule-priority.png)

---

### Step 8 — Rule Successfully Created

![Step 8](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-08-rule-created.png)

---

### Step 9 — Final Listener Rules

![Step 9](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/c6cffc6533df3722dae02f187d90c1d18e7c209a/14-alb-routing-rules/step-09-final-listener-rules.png)

---

## 🎯 Skills Demonstrated

- How Application Load Balancer routes traffic  
- How to create custom routing rules  
- How rule priority affects request handling  
- How to use Source IP conditions  
- Real-world traffic distribution strategies
