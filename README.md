# Microsoft 365 Administration Homelab

A hands-on Microsoft 365 and Microsoft Entra administration portfolio developed within a realistic, scenario-based enterprise homelab.

This repository documents practical administration, security, identity management and cloud administration projects completed using a progressively developed Microsoft 365 environment based on the fictional organisation **Bright Horizons Health**.

---

## Lab Scenario — Bright Horizons Health

**Bright Horizons Health** is a fictional healthcare organisation created to provide a realistic business context for this Microsoft 365 administration homelab.

The tenant includes users across multiple departments, job roles and business functions. User identities, organisational attributes, security groups and Microsoft 365 groups are progressively developed and reused throughout the projects.

Rather than treating each project as an isolated exercise, the environment evolves in the same way a production Microsoft 365 tenant grows over time.

Example organisational areas include:

- Clinical
- Reception
- Finance
- Human Resources
- Information Technology
- Procurement
- Management

---

## Portfolio Highlights

This portfolio currently demonstrates practical implementation of:

- Microsoft Entra ID administration
- Identity lifecycle management
- Microsoft 365 and Security Group administration
- Dynamic group membership
- Administrative Roles and Role-Based Access Control (RBAC)
- Multi-Factor Authentication (MFA)
- Microsoft Entra Privileged Identity Management (PIM)
- Just-In-Time (JIT) administration
- Approval workflows for privileged access
- Audit logging and administrative activity validation

Additional projects covering Identity Governance, Conditional Access and Enterprise Applications will continue to expand the environment.

---

## Project Roadmap

The projects build progressively on the same Microsoft 365 tenant. Identities, attributes, groups and configurations created in earlier projects are reused in later projects.

| Project | Focus | Status |
|---|---|---|
| [Project 01 — User Lifecycle Management](Project-01-User-Lifecycle/README.md) | User creation, identity attributes, MFA, session management, deletion, restoration and auditing | ✅ Complete |
| [Project 02 — Group Management](Project-02-Group-Management/README.md) | Microsoft 365 groups, Security Groups, assigned and dynamic membership, rule validation and group ownership | ✅ Complete |
| [Project 03 — Administrative Roles & RBAC](Project-03-Administrative-Roles-RBAC/README.md) | Administrative roles, least privilege, role assignment and delegated administration | ✅ Complete |
| Project 04 — Authentication & Security Defaults | Authentication methods, MFA configuration and tenant-wide Security Defaults | Planned |
| Project 05 — Conditional Access | Access policies, MFA controls, exclusions, testing and safe policy deployment | Planned |
| Project 06 — Enterprise Applications & App Registrations | Enterprise applications, application registrations, permissions and service principals | Planned |
| [Project 07 — Privileged Identity Management (PIM)](Project-07-Privileged-Identity-Management/README.md) | Eligible administrator assignments, Just-In-Time (JIT) activation, approval workflows, activation policies and audit logging | ✅ Complete |
| [Project 08 — Identity Governance](Project-08-Identity-Governance/README.md) | Access Reviews, Entitlement Management, Access Packages, guest access and lifecycle governance | 🚧 In Progress |

---

## Progressive Lab Approach

This portfolio is designed as a connected administration environment rather than a collection of unrelated exercises.

**Identity lifecycle management → Group administration → Administrative Roles & RBAC → Authentication & Security Defaults → Conditional Access → Enterprise Applications → Privileged Identity Management (PIM) → Identity Governance**

Each project extends the existing environment and introduces additional Microsoft 365 and Microsoft Entra administration capabilities.

For example:

- Users and organisational attributes created during **Project 01** are reused in **Project 02** to automate group membership based on Department and Job Title.
- Groups created during **Project 02** support delegated administration scenarios in **Project 03**.
- Administrative roles configured in **Project 03** are secured through Microsoft Entra **Privileged Identity Management (PIM)** in **Project 07**.
- Future Identity Governance projects will build upon the privileged access model implemented in Project 07.

This progressive approach reflects how Microsoft 365 environments evolve in production rather than treating each topic as an isolated exercise.

---

## Technologies and Administration Areas

- Microsoft Entra ID
- Microsoft 365 Administration
- User lifecycle management
- Identity attributes
- Multi-Factor Authentication (MFA)
- Sign-in logs
- Audit logs
- Microsoft 365 Groups
- Security Groups
- Assigned group membership
- Dynamic group membership
- Dynamic membership rules
- Group ownership
- Administrative roles
- Role-Based Access Control (RBAC)
- Microsoft Entra Privileged Identity Management (PIM)
- Just-In-Time (JIT) administration
- Eligible administrator assignments
- Approval workflows
- Activation policies
- Authentication methods
- Security Defaults
- Conditional Access
- Enterprise Applications
- Application registrations
- Identity Governance
- Access Reviews
- Entitlement Management

---

## Portfolio Purpose

This homelab supports my continued development toward Microsoft 365 Administrator, Systems Administrator, Infrastructure Engineer and Modern Workplace administration roles.

The projects document practical configuration, testing, troubleshooting, security controls, auditing and operational administration within a progressively developed Microsoft cloud environment.

As additional projects are completed, this portfolio will continue to expand into broader Microsoft Entra Identity Governance, Microsoft Intune and Microsoft 365 administration capabilities.
