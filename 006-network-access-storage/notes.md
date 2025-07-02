# Notes - Network Access to Storage Accounts Lab

## Key Concepts

### What is a Private Endpoint?
- A private endpoint provides a **private IP address** in your VNet for a specific Azure service.
- This allows secure, internal-only access to services like Storage, SQL, and others—without exposing them publicly.

### Why Use a Private Endpoint for Storage?
- Improves security posture by eliminating public endpoint access.
- Ensures that traffic stays within the Microsoft backbone network.
- Supports compliance scenarios where public access must be disabled.

## Storage Access Flow
1. Storage account created with public access disabled.
2. Private endpoint connects storage to VNet.
3. VM in the same subnet accesses storage using internal DNS name and connection string.

## Tools Used
- **Azure Storage Explorer**: GUI tool to browse Azure storage from inside the VM.
- **PowerShell nslookup**: Validates that the blob endpoint resolves to a private IP.

## Gotchas
- Ensure VM and storage are in the **same region** and **same VNet/subnet** for private endpoint to work.
- Make sure public access is disabled or you'll break the isolation.
- Use incognito to avoid login conflicts during labs.

## Validation Checks
- VM successfully RDPs and resolves storage via private DNS
- Storage Explorer connects via connection string
- `$logs` blob container is visible
