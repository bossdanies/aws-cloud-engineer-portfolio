# AWS Application Load Balancer with EC2

## 📌 Project Overview

This project demonstrates how to configure an **Application Load Balancer (ALB)** in AWS to distribute incoming traffic across multiple EC2 instances.

The architecture ensures **high availability, fault tolerance, and load distribution** by routing traffic to healthy targets using a target group.

The goal is to simulate a real-world production setup where multiple web servers handle traffic behind a load balancer.

---

## 🏗️ Architecture


Internet

│
▼
Application Load Balancer (ALB)
│
▼
Target Group
│
▼
 EC2 Instance 1 (Nginx)
│
▼
 EC2 Instance 2 (Nginx)


---

## ⚙️ AWS Services Used

- Amazon EC2  
- Application Load Balancer (ALB)  
- Target Groups  
- Amazon VPC  
- Security Groups  

---

## 📊 Configuration Details

| Resource              | Name                |
|----------------------|---------------------|
| VPC                  | my-vpc-number-01    |
| Target Group         | target-number-01    |
| Load Balancer        | my-alb-number-01    |
| Protocol             | HTTP (Port 80)      |
| Instances            | real-01, real-02    |

---

## 🚀 Deployment Steps

### Step 1 — Target Groups Dashboard  
Access the Target Groups section in EC2.

![Step 1](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-01-target-groups-dashboard.png)

---

### Step 2 — Create Target Group  
Start creating a new target group.

![Step 2](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-02-create-target-group.png)

---

### Step 3 — Configure Target Group  
Select instance type, HTTP protocol, and port 80.

![Step 3](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-03-target-group-settings.png)

---

### Step 4 — Review Target Group  
Verify configuration before creation.

![Step 4](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-04-review-target-group.png)

---

### Step 5 — Target Group Created  
The target group is successfully created.

![Step 5](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-05-target-group-created.png)

---

### Step 6 — Register Targets  
Begin registering EC2 instances.

![Step 6](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-06-register-targets.png)

---

### Step 7 — Select Instances  
Select both EC2 instances.

![Step 7](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-07-select-instances.png)

---

### Step 8 — Add Targets  
Add selected instances to the target group.

![Step 8](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-08-add-targets.png)

---

### Step 9 — Targets Registered  
Instances are successfully registered.

![Step 9](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-09-targets-registered.png)

---

### Step 10 — Load Balancer Dashboard  
Navigate to Load Balancers.

![Step 10](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-10-load-balancers-dashboard.png)

---

### Step 11 — Select Load Balancer Type  
Choose Application Load Balancer.

![Step 11](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-11-select-load-balancer-type.png)

---

### Step 12 — Create Application Load Balancer  
Configure the ALB as internet-facing.

![Step 12](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-12-create-application-load-balancer.png)

---

### Step 13 — Configure Network Mapping  
Select VPC and public subnets in different AZs.

![Step 13](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-13-configure-network-mapping.png)

---

### Step 14 — Load Balancer Created  
The ALB is successfully created.

![Step 14](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-14-load-balancer-created.png)

---

### Step 15 — Healthy Targets  
Both EC2 instances pass health checks.

![Step 15](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-15-healthy-targets.png)

---

### Step 16 — Final Result  
Accessing the Load Balancer DNS displays the Nginx web server.

![Step 16](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/df8b9da038c5a672bfaa1c7130e2de7cb2e9bab5/13-application-load-balancer/step-16-final-nginx-output.png)

---

## 💥 Result

The Application Load Balancer successfully distributes incoming traffic across multiple EC2 instances.

Both instances are healthy and serving web content, ensuring high availability and load distribution.

---

## 🎯 Skills Demonstrated

- Application Load Balancer Configuration  
- Target Group Management  
- EC2 Integration with Load Balancing  
- Health Checks Configuration  
- High Availability Architecture  
- Troubleshooting (Unhealthy Targets → Healthy)  

