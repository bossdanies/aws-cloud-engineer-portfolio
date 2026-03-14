# AWS S3 Intelligent-Tiering Setup

## Project Overview

This project demonstrates how to configure an Intelligent-Tiering policy on an Amazon S3 bucket to optimize storage costs.

Amazon S3 Intelligent-Tiering automatically moves objects between storage tiers based on access patterns, helping reduce storage costs for objects that are accessed infrequently.

This feature is commonly used in production environments to manage storage lifecycle and cost optimization without impacting performance.

---

## Architecture

S3 Bucket

│  
└── Intelligent-Tiering Configuration

│  
└── Automatic Tier Management

---

## AWS Services Used

- Amazon S3
- S3 Intelligent-Tiering

---

## Configuration Details

| Resource | Name |
|--------|--------|
| Bucket | example-s3-bucket |
| Configuration Name | IntelligentTiering-Config |
| Prefix | All objects |
| Status | Enabled |
| Archive Access Tier | Disabled |
| Deep Archive Access Tier | Disabled |

---

## Deployment Steps

### Step 1 — Initial State (No Intelligent-Tiering Configuration)

The S3 bucket initially has no Intelligent-Tiering configurations applied.

![Step 1 - Initial State](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/94861cba4e3c5bf30ffaede7f1f020c91e0308d3/03-s3-intelligent-tiering/step1-intelligent-tiering-empty.png)

---

### Step 2 — Configure Intelligent-Tiering Policy

An Intelligent-Tiering configuration is created and applied to the bucket.

![Step 2 - Setup Configuration](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/94861cba4e3c5bf30ffaede7f1f020c91e0308d3/03-s3-intelligent-tiering/step2-intelligent-tiering-setup.png)

---

### Step 3 — Intelligent-Tiering Enabled

The Intelligent-Tiering configuration is successfully created and enabled.

![Step 3 - Intelligent Tiering Enabled](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/94861cba4e3c5bf30ffaede7f1f020c91e0308d3/03-s3-intelligent-tiering/step3-intelligent-tiering-enabled.png)

---

## Result

An Intelligent-Tiering configuration was successfully applied to the S3 bucket.

Objects stored in the bucket will automatically be managed across storage tiers based on access patterns, helping optimize storage costs while maintaining performance.

---

## Skills Demonstrated

- Amazon S3 Storage Management
- Intelligent-Tiering Configuration
- Cloud Storage Cost Optimization
- Automated Storage Tier Management
