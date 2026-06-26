# AWS Highly Available Web App with Auto Scaling

## 📌 Project Overview
This project demonstrates how to deploy a highly available web application on AWS using a custom VPC, EC2, NGINX, Target Groups, an Application Load Balancer (ALB), Amazon Machine Images (AMI), Launch Templates, and Auto Scaling Groups.

## 🏗️ Architecture
```
│▼ Custom VPC
│▼ 2 Public Subnets
│▼ Internet Gateway
│▼ Route Table
│▼ EC2 Instances
│▼ NGINX Web Server
│▼ Target Group
│▼ Application Load Balancer
│▼ AMI
│▼ Launch Template
│▼ Auto Scaling Group
```
---

## Technologies
- AWS EC2
- AWS VPC
- AWS ALB
- AWS Auto Scaling
- AWS AMI
- AWS Launch Templates
- Amazon Linux
- NGINX
- 
---
## 🚀 Deployment Steps

## Step 1 - Create the custom VPC.

![Step 1](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/ceaf051aed1f4c093208c5fc61d1feb339971127/16-aws-highly-available-web-app/step01-create-vpc.png)

## Step 2 - Verify the VPC creation.

![Step 2](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step02-vpc-created.png)

## Step 3 - Create Public Subnet A.

![Step 3](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step03-create-public-subnet-a.png)

## Step 4 - Verify Public Subnet A.

![Step 4](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step04-public-subnet-a-created.png)

## Step 5 - Create Public Subnet B.

![Step 5](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step05-create-public-subnet-b.png)

## Step 6 - Verify Public Subnet B.

![Step 6](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step06-public-subnet-b-created.png)

## Step 7 - Create Internet Gateway.

![Step 7](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step07-create-internet-gateway.png)

## Step 8 - Verify Internet Gateway.

![Step 8](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step08-internet-gateway-created.png)

## Step 9 - Attach Internet Gateway.

![Step 9](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step09-attach-internet-gateway-to-vpc.png)

## Step 10 - Verify attachment.

![Step 10](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step10-internet-gateway-attached-to-vpc.png)

## Step 11 - Create public route table.

![Step 11](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step11-create-public-route-table.png)

## Step 12 - Verify route table.

![Step 12](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step12-public-route-table-created.png)

## Step 13 - Associate public subnets.

![Step 13](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step13-associate-public-subnets-with-route-table.png)

## Step 14 - Verify associations.

![Step 14](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step14-public-route-table-associations-completed.png)

## Step 15

Add default route.

![Step 15](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step15-add-default-route-to-internet-gateway.png)

## Step 16 - Verify route.

![Step 16](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step16-public-route-table-route-added.png)

## Step 17 - Launch EC2 Instance A.

![Step 17](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step17-launch-ec2-instance-a.png)

## Step 18 - Verify Instance A.

![Step 18](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step18-ec2-instance-a-launched.png)

## Step 19 - Connect using SSH.

![Step 19](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step19-connect-to-ec2-instance-a.png)

## Step 20 - Install NGINX.

![Step 20](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step20-install-nginx-on-ec2-instance-a.png)

## Step 21 - Enable NGINX.

![Step 21](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step21-enable-nginx-service-on-ec2-instance-a.png)

## Step 22 - Verify NGINX.

![Step 22](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step22-verify-nginx-on-ec2-instance-a.png)

## Step 23 - Launch EC2 Instance B.

![Step 23](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step23-launch-ec2-instance-b.png)

## Step 24 - Verify Instance B.

![Step 24](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step24-ec2-instance-b-launched.png)

## Step 25 - Connect to Instance B.

![Step 25](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step25-connect-to-ec2-instance-b.png)

## Step 26 - Install NGINX.

![Step 26](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step26-install-nginx-on-ec2-instance-b.png)

## Step 27 - Enable NGINX.

![Step 27](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step27-enable-nginx-service-on-ec2-instance-b.png)

## Step 28 - Verify NGINX.

![Step 28](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step28-verify-nginx-on-ec2-instance-b.png)

## Step 29 - Create Target Group.

![Step 29](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step29-create-target-group.png)

## Step 30 - Register EC2 instances.

![Step 30](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step30-register-targets.png)

## Step 31 - Review Target Group.

![Step 31](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step31-review-target-group-configuration.png)

## Step 32 - Create Target Group.

![Step 32](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step32-create-target-group.png)

## Step 33 - Create ALB.

![Step 33](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step33-create-application-load-balancer.png)

## Step 34 - Verify ALB.

![Step 34](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step34-application-load-balancer-created.png)

## Step 35 - Verify target health.

![Step 35](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step35-verify-target-group-health.png)

## Step 36 - Verify load balancer.

![Step 36](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step36-verify-load-balancer-status.png)

## Step 37 - Test ALB DNS.

![Step 37](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step37-verify-load-balancer-dns.png)

## Step 38 - Create AMI.

![Step 38](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step38-create-ami.png)

## Step 39 - AMI creation in progress.

![Step 39](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step39-ami-creation-in-progress.png)

## Step 40 - Launch instance from AMI.

![Step 40](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step40-launch-instance-from-ami.png)

## Step 41 - Create Launch Template.

![Step 41](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step41-create-launch-template.png)

## Step 42 - Verify Launch Template.

![Step 42](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step42-launch-template-created.png)

## Step 43 - Launch Template list.

![Step 43](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step43-launch-template-list.png)

## Step 44 - Create Auto Scaling Group.

![Step 44](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step44-create-auto-scaling-group.png)

## Step 45 - Select VPC and subnets.

![Step 45](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step45-select-vpc-and-subnets.png)

## Step 46 - Configure Auto Scaling capacity.

![Step 46](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step46-configure-auto-scaling-capacity.png)

## Step 47 - Review Auto Scaling Group.

![Step 47](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step47-review-auto-scaling-group.png)

## Step 48 - Auto Scaling Group created.

![Step 48](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step48-auto-scaling-group-created.png)

## Step 49 - Instances launched automatically.

![Step 49](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step49-auto-scaling-instances-running.png)

## Step 50 - Register Auto Scaling instances.

![Step 50](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step50-register-target-group-targets.png)

## Step 51 - Review Target Group.

![Step 51](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step51-review-target-group-auto-scaling.png)

## Step 52 - Target Group created.

![Step 52](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step52-target-group-created-auto-scaling.png)

## Step 53 - Create ALB for Auto Scaling.

![Step 53](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step53-create-load-balancer-with-auto-scaling.png)

## Step 54 - Verify ALB.

![Step 54](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step54-load-balancer-created.png)

## Step 55 - Test application through ALB.

![Step 55](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step55-test-load-balancer-dns.png)

## Step 56 - Verify healthy targets.

![Step 56](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/1fc036f0d403021ce266be63d0eede162a7ca963/16-aws-highly-available-web-app/step56-target-group-healthy.png)

---

## 🎯 Skills Demonstrated

The project successfully deploys a highly available AWS web application using:
- Multiple EC2 instances
- NGINX
- Application Load Balancer
- Target Groups
- AMI
- Launch Templates
- Auto Scaling Group

The application remains available even when new instances are launched automatically by Auto Scaling.
