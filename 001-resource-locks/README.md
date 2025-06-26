Lab Details
In this lab, you will learn how to prevent users to accidently delete resources using Azure resource locks.

Introduction
What are Azure resource locks?
Azure resource locks prevent users in an organization from accidently deleting or modifying critical resources. Azure locks are different from role-based access control in a way that using these locks you can apply restrictions across all users and roles. Users can apply locks on resource level, resource group level or subscription level.

There are two types of locks available in Azure:
CanNotDelete: If this lock is applied to any of the resources, the user can still read or modify the resource but cannot delete it.
ReadOnly: As the name suggests, with this lock applied, a user can only read the resource without causing any modifications or deletions.
In the Azure portal, these locks are called Delete and Read-only.

Task Details
Sign in to Azure Portal
Deploying a Virtual Machine
Creating a Delete Lock
Creating a Read-Only Lock
Deleting the Locks
Validation Test
Deleting the Virtual Machine
