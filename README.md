# Secure-File-Services-Deployment
File Sever Deployment with DFS, FSRM, NTFS Permissions and Shadow copies 

Project Overview
This project demonstrates the deployment of a secure, centralized file sharing solution using Windows Server 2016. The key technologies implemented include:

- DFS Namespace for unified and simplified access to shared folders.

- NTFS Permissions to control and secure access to files and folders.

- File Server Resource Manager (FSRM) to enforce storage quotas, restrict unwanted file types, and generate storage usage reports.

- Shadow Copies to enable file versioning and self-service recovery of deleted or modified files.

- The solution is designed for a single-server environment where the Domain Controller (DC) and File Server roles coexist, suitable for lab setups and small environments.

Features
- Centralized namespace for easy access to shared data.

- Granular access control based on Active Directory groups.

- Storage management through quotas and file screening.

- Data protection with periodic shadow copies allowing version recovery.

- Access-Based Enumeration to hide unauthorized folders.

System Requirements
- Windows Server 2016 installed and updated.

- Server promoted as Domain Controller (Active Directory and DNS configured).

- Sufficient disk space (preferably separate data volume) for shared folders and shadow copies.

Administrative privileges.

Setup Instructions
1. Install Required Roles and Features
File Server

DFS Namespaces

File Server Resource Manager

2. Create Active Directory Security Groups
Example: Finance_Read, Finance_Modify

3. Create DFS Namespace
Create a stand-alone namespace (recommended for single-server setups).

Namespace example: \\ServerName\CorpData

4. Create Shared Folders and Configure Permissions
Create folder (e.g., D:\Finance)

Share the folder and assign share permissions to AD groups.

Set NTFS permissions matching group requirements.

5. Configure File Server Resource Manager
Set quotas on shared folders (e.g., 50 GB limit).

Create file screens to block unwanted file types.

Schedule storage reports.

6. Enable Shadow Copies
Enable on the data volume.

Configure schedule and storage limits.

7. Enable Access-Based Enumeration
Enable on DFS Namespace to hide folders users don’t have access to.

Testing
Access the DFS namespace from a domain-joined client.

Verify permissions by logging in as users in different groups.

Test quota limits and file screen blocks.

Create, modify, and delete files; then restore using Shadow Copies.

Notes
This setup is intended for lab or small environment use.

For production, separate the Domain Controller and File Server roles.

DFS Replication requires multiple file servers and is not covered in this single-server setup.

Regular monitoring and maintenance of FSRM reports and shadow copies are recommended.

Shah Azwad Ahnaf 
System Administrator 
shahazwad@keytech.ca
Keytech IT Solutions 


