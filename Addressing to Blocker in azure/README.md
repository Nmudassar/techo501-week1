# README for Addressing Blockers in Azure Resource Management

## Overview

This document focuses on common blockers encountered during Azure resource management and provides practical solutions for each. The goal is to assist in identifying and resolving issues efficiently while working with Azure environments.

---

# Blockers and Solutions

## 1. **Permission Issues**

- **Description**: Users may face errors accessing resource groups or creating resources due to insufficient permissions.
- **Symptoms**:
  - Errors when selecting resource groups.
  - Limited functionality in the Azure portal.
- **Solutions**:
  - Verify user roles in "Access Control (IAM)."
  - Contact the admin to ensure appropriate permissions are granted.

## 2. **Browser Compatibility**

- **Description**: Certain Azure features may not function correctly in specific browsers, such as Chrome.
- **Symptoms**:
  - Errors during resource creation or deletion.
  - UI elements not displaying as expected.
- **Solutions**:
  - Use alternative browsers such as Microsoft Edge or Firefox.
  - Clear the browser cache and retry operations.

## 3. **Resource Deletion Errors**

- **Description**: Issues occur when attempting to delete resources or resource groups.
- **Symptoms**:
  - Partial deletion of resources.
  - Failure messages when deleting resource groups.
- **Solutions**:
  - Ensure all dependent resources are stopped or deleted first.
  - Delete resources individually before deleting the entire group.
  - Avoid selecting "Delete Resource Group" unless absolutely necessary.

## 4. **Configuration Errors**

- **Description**: Misconfigurations can lead to resource creation or operation failures.
- **Symptoms**:
  - Resource creation fails due to invalid names or settings.
  - Network or connectivity issues within VNets.
- **Solutions**:
  - Adhere to naming conventions (e.g., `Tech501-Name-vnet`).
  - Double-check configurations during the review step before creating resources.
  - Validate VNet address spaces and subnet configurations.

## 5. **SSH Key Issues**

- **Description**: Problems generating or using SSH keys for virtual machines.
- **Symptoms**:
  - Errors when connecting to VMs via SSH.
  - Missing private or public key files.
- **Solutions**:
  - Generate SSH key pairs correctly using `ssh-keygen`.
  - Store the private key securely in the `.ssh` folder.
  - Upload the public key to Azure for VM access.

---

# Best Practices

## Troubleshooting Steps

- Retry operations after refreshing the Azure portal.
- Check logs and notifications in the portal for specific error details.
- Ensure all resources and configurations are properly reviewed before finalizing.

## Use Tags

- Add tags such as `owner` with your name to resources for easier identification and management.

## Secure Resources

- Always secure private keys and avoid sharing them.
- Use public keys only for uploading to Azure or sharing with trusted platforms.

## Minimize Costs

- Stop unused virtual machines to reduce expenses.
- Avoid assigning public IPs unless required for external access.

---

# Additional Resources

- [Azure Fundamentals](https://learn.microsoft.com/en-us/azure/)
- [Managing Permissions in Azure](https://learn.microsoft.com/en-us/azure/role-based-access-control/)
- [SSH Key Generation Guide](https://www.ssh.com/academy/ssh/keygen)
- [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/)
