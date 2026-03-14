# AWS S3 Bucket Versioning Setup

## Project Overview

This project demonstrates how to enable versioning on an existing Amazon S3 bucket.

S3 Versioning allows multiple versions of an object to be stored in the same bucket. This feature helps protect data from accidental deletion or overwrites by preserving previous object versions.

Versioning is commonly used in production environments for data protection, recovery, and change tracking.

---

## Architecture

S3 Bucket

│  
└── Versioning Enabled

│  
└── Multiple Object Versions Stored

---

## AWS Services Used

- Amazon S3
- S3 Versioning

---

## Configuration Details

| Resource | Name |
|--------|--------|
| Bucket | example-s3-bucket |
| Versioning | Enabled |
| Object Protection | Multiple versions maintained |

---

## Deployment Steps

### Step 1 — Select S3 Bucket

The S3 bucket is selected from the bucket list to configure versioning.

![Step 1 - Select Bucket](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/902ad70d0123bccc5960fb625cebf52b9f0f7f06/02-configuring-s3-versioning/step1-select-bucket.png)

---

### Step 2 — Enable Versioning

Versioning is enabled from the bucket properties section and successfully activated.

![Step 2 - Enable Versioning](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/902ad70d0123bccc5960fb625cebf52b9f0f7f06/02-configuring-s3-versioning/step2-versioning-enabled.png)

---

## Result

S3 Versioning was successfully enabled on the bucket.

New versions of objects uploaded to the bucket will now be stored, allowing recovery of previous versions if objects are modified or deleted.

---

## Skills Demonstrated

- Amazon S3 Bucket Configuration
- S3 Versioning Management
- Data Protection Strategies
- Cloud Storage Version Control
