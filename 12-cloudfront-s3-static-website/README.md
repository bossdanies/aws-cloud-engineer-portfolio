# 🌐 AWS CloudFront + S3 Static Website

## 📌 Project Overview

This project demonstrates how to deploy a **static website using Amazon S3 and Amazon CloudFront**.

Amazon S3 is used to store static files (HTML), while CloudFront is used as a **Content Delivery Network (CDN)** to deliver the website globally with improved performance and security.

This setup follows best practices by using **private S3 access with CloudFront (OAC)** instead of exposing the bucket publicly.

---

## 🏗️ Architecture
```
│▼ User (Browser)
│▼ CloudFront (CDN)
│▼ Amazon S3 (Private Bucket)
│▼ index.html (Static Website)

```
---

## ⚙️ AWS Services Used

- Amazon S3
- Amazon CloudFront
- AWS IAM
- AWS WAF

---

## 📊 Configuration Details

| Resource | Name |
|--------|--------|
| S3 Bucket | demo-08-bucket-02 |
| File | index.html |
| CloudFront Distribution | demo-8-site |
| Origin Type | Amazon S3 |
| Access Control | Origin Access Control (OAC) |
| Default Root Object | index.html |

---

## 🚀 Deployment Steps

### Step 1 — Create S3 Bucket
![Step 1 - Create S3 Bucket](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step01-create-s3-bucket.png)

---

### Step 2 — Bucket Created
![Step 2 - S3 Bucket Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step02-s3-bucket-created.png)

---

### Step 3 — Create Second Bucket
![Step 3 - Create Second Bucket](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step03-create-second-bucket.png)

---

### Step 4 — Second Bucket Created
![Step 4 - Second Bucket Created](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step04-second-bucket-created.png)

---

### Step 5 — Open Bucket
![Step 5 - Open Bucket](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step05-open-bucket.png)

---

### Step 6 — Upload HTML File
![Step 6 - Upload HTML File](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step06-upload-index-file.png)

---

### Step 7 — Upload Successful
![Step 7 - Upload Success](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step07-upload-success.png)

---

### Step 8 — Search CloudFront
![Step 8 - Search CloudFront](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step08-search-cloudfront.png)

---

### Step 9 — CloudFront Setup
![Step 9 - CloudFront Setup](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step09-cloudfront-get-started.png)

---

### Step 10 — Domain Configuration
![Step 10 - Domain Configuration](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step10-configure-domain-warning.png)

---

### Step 11 — Select S3 Origin
![Step 11 - Select S3 Origin](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step11-select-s3-origin.png)

---

### Step 12 — Enable Security
![Step 12 - Enable Security](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step12-enable-security-waf.png)

---

### Step 13 — Review and Create
![Step 13 - Review and Create](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step13-review-and-create-distribution.png)

---

### Step 14 — CloudFront Working
![Step 14 - CloudFront Working](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/845b16d392bcf59b672d14cfda88a86e5bf55c51/12-cloudfront-s3-static-website/step14-cloudfront-working.png)

 
---

## 🎯 Skills Demonstrated

- Deploy static websites using S3 and CloudFront  
- Understand CDN and global content delivery  
- Secure S3 using private access with CloudFront  
  
 
