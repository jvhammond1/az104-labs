## 🧪 Lab: Azure Resource Locks

### 📋 Summary
In this lab, you will learn how to prevent users from accidentally deleting or modifying resources using Azure Resource Locks.

---

### 🎯 Learning Objectives
- Understand the purpose and types of Azure resource locks.
- Apply `Delete` and `Read-only` locks at various levels (resource, resource group).
- Practice lock management through the Azure Portal.

---

### 🧰 Tools Used
- Azure Portal

---

### 📚 Key Concepts

**What are Azure Resource Locks?**  
Azure resource locks provide a way to safeguard critical Azure resources by preventing accidental deletion or modification. Unlike RBAC, which controls *who* can do *what*, locks enforce restrictions *regardless of role*.

There are two types:
- `CanNotDelete` (Delete Lock): Resource can be read or modified, but not deleted.
- `ReadOnly`: Resource can be read only — no modifications or deletions allowed.

These appear in the Azure Portal as **Delete** and **Read-only**.

---

### ✅ Task Outline
1. Sign in to Azure Portal
2. Deploy a Virtual Machine
3. Create a Delete Lock
4. Create a Read-only Lock
5. Remove Locks
6. Validation Test
7. Delete the Virtual Machine

---

### 🔗 Related Docs
- [Lock resources to prevent changes](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/lock-resources)

