### **Module 3: Azure Storage Services**

## Storage Types
1. **Blob Storage**: For unstructured data (images, backups)
   - Access tiers: Hot (frequent), Cool (infrequent), Archive (rare)
2. **File Storage**: SMB/NFS file shares
3. **Table Storage**: NoSQL key-value store

## Key Features
- **Replication Options**:
  - LRS (Locally-redundant)
  - GRS (Geo-redundant)
- **Shared Access Signatures (SAS)**: Time-limited access tokens

## Lab Results
- Created storage account with:
  ```bash
  az storage account create --name hmaccount \
  --resource-group learn-123 --sku Standard_LRS
