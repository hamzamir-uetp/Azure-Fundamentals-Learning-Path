# **Module 4: Security & Identity**

## Core Services
- **Azure Active Directory (AAD)**: Cloud identity provider
- **Role-Based Access Control (RBAC)**:
  - Roles: Owner, Contributor, Reader
  - Scope: Management group → Resource
- **Azure Security Center**: Unified security management

## Key Concepts
1. **Multi-Factor Authentication (MFA)**: Requires 2+ verification methods
2. **Conditional Access**: Context-aware access policies

## Practical Steps
- Assigned VM contributor role:
  ```bash
  az role assignment create --assignee user@domain.com \
  --role "Virtual Machine Contributor" --scope /subscriptions/xxx/resourceGroups/yyy
