Lab Details
In this lab we will walk through the steps to create, manage and assign Azure Policies.

Introduction
What are Azure Policies? 
Azure Policy is a service in Azure which allows you to create policies which enforce and control the properties of a resource. When these policies are used they enforce different rules and effects over the resources, so those resources stay compliant with your IT governance standards.

Azure Policy allows you to ensure that all resources are configured with required services, and will tell you when systems are out of compliance. 
Azure policy is basically 3 components; policy definition, assignment and parameters. Policy definition is the conditions which you want controlled. There are built in definitions such as controlling what type of resources can be deployed to enforce the use of tags on all resources.

Policy assignment is the scope of what the policy definition can take effect around. Scope of assignment can be assigned to an individual, resource, resource group or management group. Policy assignments are inherited by all child resources. Policy parameters help you avoid creating multiple policy definitions by making your policies flexible. For example, you can use parameters to specify allowed VM SKUs or restrict resource deployment to a specific location.

Task Details
Sign in to Azure Portal
Create an Allowed Locations policy assignment
Test the Allowed Locations policy assignment
Delete the resources
