# Notes - Create a Storage Account Lab

## Key Concepts

### Blob Storage
- Used for unstructured data (images, videos, backups, etc.)
- Organized into containers
- Access tiers: Hot (frequent), Cool (infrequent, ≥30 days), Archive (rare, ≥90 days)

### File Share
- Cloud-based SMB/NFS shared folders
- Useful for lift-and-shift workloads or shared drives between systems

### Performance Tiers
- **Standard**: Backed by HDD, lower cost
- **Premium**: SSD-backed, high IOPS

### Redundancy Options
| Type | Description |
|------|-------------|
| LRS  | Locally Redundant (3 copies in one datacenter) |
| ZRS  | Zone Redundant (3 zones in one region) |
| GRS  | Geo Redundant (LRS + async copy to paired region) |
| GZRS | Geo-Zone Redundant (ZRS + async geo copy) |

### Access Tiers
- **Hot**: Frequently accessed
- **Cool**: Infrequent access (≥30 days)
- **Cold**: Rarely accessed, quick access
- **Archive**: Offline tier, manual rehydration needed

## Gotchas
- Can't assign Archive tier during storage account creation; only blob objects can be set to Archive.
- Premium performance tier restricts some redundancy and access tier options.
- Naming requirements: lowercase letters, numbers, 3–24 characters.

## Validation
Check for:
- Storage account with correct redundancy/performance
- Container created with uploaded HTML blob
- File share created and file uploaded
- All resources deleted at the end

## Clean-up Reminder
Delete the resource group to remove all associated resources.
