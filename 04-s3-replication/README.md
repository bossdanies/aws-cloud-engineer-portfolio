# Amazon S3 Cross-Region Replication (CRR) Setup

## Objective
Configure **Cross-Region Replication (CRR)** between two Amazon S3 buckets to automatically replicate objects from a source bucket in one AWS region to a destination bucket in another region.

---

## Buckets Created

- **Source Bucket:** `source-s3-bucket-01-2026`  
  - Region: `us-east-1 (N. Virginia)`  
- **Destination Bucket:** `destination-s3-bucket-02-2026`  
  - Region: `us-east-2 (Ohio)`  

> **Note:** Versioning is enabled on both buckets (required for replication).

---

## Replication Rule Configuration

- **Rule Name:** `s3-region-replication-2026`
- **Scope:** Entire bucket
- **Destination Bucket:** `destination-s3-bucket-02-2026`
- **Destination Region:** `us-east-2 (Ohio)`
- **Storage Class:** Same as source
- **Replica Owner:** Same as source
- **Replication Time Control:** Disabled
- **KMS-encrypted objects:** Do not replicate
- **Replica modification sync:** Disabled

✅ Replication rule successfully **created and enabled**.

---

## Test Replication

1. Upload a test object: `aws-s3-object.txt` to the source bucket.
2. Verify that it is **automatically replicated** to the destination bucket.

---

## Screenshots
### Step 1: Create Buckets in Different Regions
Shows the creation of buckets in different AWS regions.  
![Step 1 - Create Buckets](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-01-create-s3-buckets-cross-region.png)

### Step 2: Access Replication Configuration
Shows accessing the replication configuration settings in the source bucket.  
![Step 2 - Open Replication Configuration](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-02-open-s3-replication-configuration.png)

### Step 3: Setup Cross-Region Replication Rule
Shows the setup of the replication rule.  
![Step 3 - Create Replication Rule](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-03-create-cross-region-replication-rule.png)

### Step 4: Confirm Replication Rule Enabled
Shows confirmation that the replication rule was successfully created and enabled.  
![Step 4 - Replication Rule Enabled](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-04-cross-region-replication-rule-enabled.png)

### Step 5: Upload Test Object to Source Bucket
Shows the test object uploaded to the source bucket.  
![Step 5 - Object Uploaded](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-05-object-uploaded-to-source-bucket.png)

### Step 6: Verify Object Replication in Destination Bucket
Shows that the object has been automatically replicated to the destination bucket.  
![Step 6 - Object Replicated](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/269dbfc769ae52bcfdbb96853c05970c846306d5/04-s3-replication/step-06-object-replicated-to-destination-bucket.png)

✅ **Result:** Cross-Region Replication successfully configured and verified between:

- Source: `source-s3-bucket-01-2026` (us-east-1)  
- Destination: `destination-s3-bucket-02-2026` (us-east-2)
