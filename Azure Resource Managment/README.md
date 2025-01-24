# README for Azure Resource Management

## Overview

This document is a practical guide for managing Azure resources, including resource groups, virtual networks, and virtual machines (VMs). It highlights key practices, configurations, and management techniques for cloud-based environments.

---

# Azure Fundamentals

## Resource Groups

- Resource groups are containers for managing and organizing Azure resources.
- All resources must belong to a resource group.
- Example: Use the `Tech 501` resource group for this exercise.

## Virtual Networks (VNet)

- **Purpose**: VNets act as virtual spaces to host and connect resources securely.
- **Naming Convention**: Start names with `Tech 501` followed by your first name and `vnet` (e.g., `Tech501-Name-vnet`).
- **Region**: Set to `UK South` (or specified region).
- **Best Practice**: Add descriptive tags like `owner` to resources for easier management.

### Subnets

- VNets are divided into subnets, functioning like "rooms" in an "apartment building."
- **Types of Subnets**:
  - Public Subnet: Allows external access.
  - Private Subnet: Internal communication only.
- **Address Space**:
  - Public Subnet: `10.0.2.0/24` (256 IP addresses)
  - Private Subnet: `10.0.3.0/24` (256 IP addresses)

### Planning

- Always plan the VNet address space to avoid conflicts and simplify scaling.
- Use CIDR notation for address allocation (e.g., `/16`, `/24`).

---

# Managing Virtual Machines

## Key Steps

1. **Select a VNet**: Virtual machines must reside in a virtual network.
2. **Assign IP Addresses**:
   - Private IP (mandatory): Allocated automatically from the subnet's range.
   - Public IP (optional): Needed for external access.

## Cost Management

- **Public IP Addresses**: Chargeable resources; assign them only when necessary.
- **Virtual Machine States**:
  - Running VMs incur higher costs.
  - Stop VMs when not in use to save costs.

---

# Blockers

## Common Challenges and Solutions

### 1. **Permission Issues**

- **Description**: Users may encounter errors when accessing resource groups or creating resources.
- **Solution**:
  - Verify permissions in the Azure portal under "Access Control (IAM)."
  - Contact the admin to ensure correct roles are assigned.

### 2. **Browser Compatibility**

- **Description**: Certain features may not work properly in specific browsers like Chrome.
- **Solution**:
  - Use alternative browsers such as Edge or Firefox.
  - Clear browser cache and retry.

### 3. **Resource Deletion Errors**

- **Description**: Deleting resources or resource groups might fail or partially complete.
- **Solution**:
  - Ensure no dependent resources are still active.
  - Delete resources individually before deleting the group.

### 4. **Configuration Errors**

- **Description**: Incorrect naming conventions or unplanned configurations can lead to issues.
- **Solution**:
  - Follow naming conventions strictly (e.g., `Tech501-Name-vnet`).
  - Double-check configurations during the review step before creation.

---

# Tips and Best Practices

## Naming Conventions

- Use descriptive names for resources to make their purpose clear.
  - Example: `Tech501-Name-test-vnet` for a test virtual network.

## Troubleshooting

- **Common Issues**: Permission errors, incorrect resource groups, or browser-related bugs.
- **Solution**:
  - Retry operations after refreshing the portal.
  - Switch browsers if needed (e.g., use Edge instead of Chrome).

## Tags

- Add tags like `owner` with your name to resources for better identification.

## Deleting Resources

- Use the "Delete" button on individual resources.
- Avoid "Delete Resource Group" to prevent unintended deletions.
- Confirm all selections carefully before finalizing deletions.

---

# Additional Resources

- [Azure Fundamentals](https://learn.microsoft.com/en-us/azure/)
- [CIDR Notation Guide](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)
- [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/)
