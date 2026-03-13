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

1. **Creation of buckets in different regions**  
   `step-01-create-s3-buckets-cross-region.png`
2. **Accessing replication configuration settings**  
   `step-02-open-s3-replication-configuration.png`
3. **Setup of cross-region replication rule**  
   `step-03-create-cross-region-replication-rule.png`
4. **Confirmation replication rule enabled**  
   `step-04-cross-region-replication-rule-enabled.png`
5. **Test object uploaded to source bucket**  
   `step-05-object-uploaded-to-source-bucket.png`
6. **Object replicated to destination bucket**  
   `step-06-object-replicated-to-destination-bucket.png`

---

✅ **Result:** Cross-Region Replication successfully configured and verified between:

- Source: `source-s3-bucket-01-2026` (us-east-1)  
- Destination: `destination-s3-bucket-02-2026` (us-east-2)
