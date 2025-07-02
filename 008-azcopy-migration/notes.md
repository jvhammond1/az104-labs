# Notes - Migrate Data to Cloud with AzCopy

## What is AzCopy?
- A command-line tool for transferring data to/from Azure Storage
- Fast, concurrent, and fault-tolerant
- Supports sync and resumable transfers
- Essential for bulk migration or automated backup workflows

## Setup Summary
### Storage Account
- Type: Standard, GRS
- Hierarchical Namespace: Enabled (for Data Lake features)

### Container
- Name: `democontainer`

## AzCopy Commands
### Authenticate:
```sh
azcopy login
Initial Upload:
sh
Copy
Edit
azcopy copy "<local-folder-path>" "https://<storage-account>.blob.core.windows.net/<container>" --recursive=true
Sync Updated Files:
sh
Copy
Edit
azcopy sync "<local-folder-path>" "https://<storage-account>.blob.core.windows.net/<container>" --recursive=true
Schedule Task Script (in script.bat):
bat
Copy
Edit
azcopy sync "<local-folder-path>" "https://<storage-account>.blob.core.windows.net/<container>" --recursive=true
Create Task:
sh
Copy
Edit
schtasks /CREATE /SC minute /MO 5 /TN "AzCopy Script" /TR C:\script.bat
Gotchas
AzCopy is Windows-only for this lab.

Use azcopy sync only after verifying your initial upload worked.

Double-check container and storage URLs—missing or wrong names break uploads.
