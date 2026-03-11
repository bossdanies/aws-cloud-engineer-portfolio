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
- **step1-intelligent-tiering-empty.png** – Shows the initial state with no Intelligent-Tiering configurations.  
- **step2-intelligent-tiering-setup.png** – Shows the configuration setup before saving.  
- **step3-intelligent-tiering-enabled.png** – Shows confirmation that the Intelligent-Tiering configuration is active.
