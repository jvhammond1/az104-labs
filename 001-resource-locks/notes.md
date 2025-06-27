## 📝 Lab Notes: Azure Resource Locks

### 🗓️ Date: June 27, 2025  
**Lab Topic**: Preventing accidental changes using Azure resource locks.

---

### 🔧 Steps Performed

1. **Signed into Azure Portal**
2. **Deployed a VM** named `az104-locktest-vm` in resource group `az104-rg1`
3. **Created a Delete Lock**:
   - Lock name: `PreventDelete`
   - Type: `CanNotDelete`
   - Applied at: VM level
4. **Created a Read-only Lock**:
   - Lock name: `PreventChanges`
   - Type: `ReadOnly`
   - Applied at: Resource Group level
5. **Attempted to delete VM** — blocked as expected
6. **Removed locks** to allow cleanup
7. **Deleted VM** successfully after lock removal

---

### 💻 Commands Used (CLI, if applicable)
```bash
# Example CLI if used
az lock create --name PreventDelete --lock-type CanNotDelete --resource myVM --resource-type Microsoft.Compute/virtualMachines --resource-group az104-rg1

🧠 Gotchas & Notes
Locks override user permissions: even owners can't delete a locked resource.
Lock types show as Delete and Read-only in Azure Portal.
Always remove locks before automating deletions in scripts or templates.

✅ Test Result
Lock behavior tested and confirmed working. Resources protected and only removable after lock deletion.
