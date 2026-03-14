# S3 Intelligent-Tiering Setup

## Objective
Configure an Intelligent-Tiering policy on an existing S3 bucket to optimize storage costs for objects that are infrequently accessed.

## Tasks Completed
1. Opened the S3 bucket and verified no existing Intelligent-Tiering configurations.  
2. Created an Intelligent-Tiering configuration with:  
   - **Configuration Name:** `IntelligentTiering-Config`  
   - **Prefix:** empty (applies to all objects in the bucket)  
   - **Status:** Enabled  
   - **Archive Access tier and Deep Archive tier:** disabled  
3. Confirmed that the Intelligent-Tiering configuration was successfully created and is active.

## Screenshots

### Step 1: Initial State – No Intelligent-Tiering Configurations
Shows the initial state with no Intelligent-Tiering configurations.  
![Step 1 - Initial State](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/94861cba4e3c5bf30ffaede7f1f020c91e0308d3/03-s3-intelligent-tiering/step1-intelligent-tiering-empty.png)

### Step 2: Setup Intelligent-Tiering Configuration
Shows the configuration setup before saving.  
![Step 2 - Setup Configuration](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/94861cba4e3c5bf30ffaede7f1f020c91e0308d3/03-s3-intelligent-tiering/step2-intelligent-tiering-setup.png)

### Step 3: Intelligent-Tiering Enabled
Shows confirmation that the Intelligent-Tiering configuration is active.  
![Step 3 - Configuration Enabled](https://github.com/bossdanies/aws-cloud-engineer-portfolio/blob/94861cba4e3c5bf30ffaede7f1f020c91e0308d3/03-s3-intelligent-tiering/step3-intelligent-tiering-enabled.png)
