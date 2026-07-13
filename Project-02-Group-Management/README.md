# Project 02 – Microsoft Entra Group Management

## Project Overview

This project demonstrates the design, configuration and validation of Microsoft Entra ID groups within the fictional **Bright Horizons Health** environment.

The project focused on using Microsoft 365 groups and security groups to support collaboration, access management and administrative efficiency. Both assigned and dynamic membership models were implemented and tested.

Dynamic membership rules were created using user attributes such as department and job title. The project also included rule validation, live attribute-change testing, automated group assignment for a newly created user, and an investigation of group ownership and delegated management.

---

## Business Scenario

Bright Horizons Health has employees working across multiple business areas, including Clinical, Finance, Human Resources, Procurement, Reception and Information Technology.

Manually maintaining group membership would increase administrative effort and create a risk that access becomes outdated when employees join the organisation, change departments or move into management positions.

The organisation therefore required a structured group-management model that could:

- Support collaboration through Microsoft 365 groups
- Support access control through security groups
- Automatically assign users to appropriate groups based on identity attributes
- Reduce repetitive manual administration
- Respond to changes in employee information
- Support delegated group management through group ownership

---

## Project Objectives

The objectives of this project were to:

- Understand the differences between Microsoft 365 groups and security groups
- Configure groups using consistent naming conventions
- Compare assigned and dynamic membership
- Create department-based dynamic membership rules
- Create a management group using department and job-title attributes
- Validate dynamic membership rules before relying on them
- Verify that users were assigned to the expected groups
- Test how a department change affects dynamic membership
- Test automated group assignment for a newly created employee
- Investigate group ownership and delegated group management
- Document findings and lessons learned

---

## Environment

| Component | Configuration |
|---|---|
| Organisation | Bright Horizons Health |
| Identity platform | Microsoft Entra ID |
| Tenant type | Cloud-based Microsoft Entra tenant |
| Administration portal | Microsoft Entra admin centre |
| User environment | Fictional healthcare organisation |
| Group types | Microsoft 365 groups and security groups |
| Membership types | Assigned and dynamic user membership |
| Dynamic attributes | Department and job title |

---

## Group Design

Groups were created to represent business departments, collaboration requirements and administrative functions.

Examples included:

| Group | Group Type | Membership Model | Purpose |
|---|---|---|---|
| `M365-Clinical` | Microsoft 365 | Dynamic | Collaboration for Clinical employees |
| `M365-Reception` | Microsoft 365 | Dynamic | Collaboration for Reception employees |
| `M365-Procurement` | Microsoft 365 | Dynamic | Collaboration for Procurement employees |
| `M365-HR` | Microsoft 365 | Dynamic | Collaboration for Human Resources employees |
| `M365-Finance` | Microsoft 365 | Assigned | Finance collaboration with manually managed membership |
| `SG_IT_Admins` | Security | Dynamic | Security grouping for IT management personnel |
| `SG_IT_ServiceDesk` | Security | Dynamic | Security grouping for IT employees |
| `SG_Managers` | Security | Dynamic | Organisation-wide management grouping |

The naming convention used:

- `M365-` for Microsoft 365 collaboration groups
- `SG_` for security groups

This made the purpose and group type easier to identify in the Entra admin centre.

---

## Microsoft 365 Groups

Microsoft 365 groups are primarily designed to support collaboration.

A Microsoft 365 group can provide shared services such as:

- Group email and conversations
- Shared calendar
- SharePoint resources
- Microsoft Teams integration
- Shared collaboration resources

In this project, Microsoft 365 groups were used to represent departmental collaboration requirements.

---

## Security Groups

Security groups are primarily used to manage access to resources, applications and services.

Rather than assigning permissions separately to individual users, permissions can be assigned to a security group and inherited by its members.

Security groups in this project were used to represent access-oriented and administrative groupings, including IT employees, IT administrators and managers.

---

## Assigned and Dynamic Membership

Two membership approaches were implemented.

### Assigned Membership

With assigned membership, an administrator or authorised group owner manually adds and removes members.

`M365-Finance` was configured with assigned membership, and its Finance users were added manually.

Assigned membership may be appropriate when:

- Membership is based on business decisions that cannot be represented reliably by user attributes
- Membership requires manual approval
- The group contains a small or specialised set of users
- Direct administrative control is required

### Dynamic Membership

Dynamic membership automatically evaluates user attributes against a membership rule.

When a user satisfies the rule, Microsoft Entra ID automatically adds the user to the group. If the user no longer satisfies the rule, the user is automatically removed.

Dynamic membership can reduce repetitive administration and help keep group membership aligned with current identity information.

---

## Dynamic Membership Rules

Department attributes were used to automate membership for departmental groups.

An example department-based rule was:

```text
(user.department -eq "Clinical")
