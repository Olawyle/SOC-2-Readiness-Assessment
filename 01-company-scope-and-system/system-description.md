# CloudBridge Technologies Ltd. – System Description

> **Disclaimer:** Fictional case study. This is a readiness-oriented system description written for a portfolio project. It is not a SOC 2 Section 3 description prepared for an independent service auditor.

## 1. Overview

The **CloudBridge Platform** is a multi-tenant SaaS system delivering CRM and analytics services to customers over the internet. This document describes the infrastructure, software, people, procedures and data that make up the system within the assessment boundary.

## 2. System Components

### 2.1 Infrastructure

| Component | Description |
|---|---|
| Cloud provider | AWS (primary region eu-west-1; disaster recovery region eu-central-1) |
| Compute | Amazon ECS containers running application services; EC2 for supporting workloads |
| Database | Amazon RDS (PostgreSQL), Multi-AZ, encrypted at rest |
| Storage | Amazon S3 for customer attachments and backups |
| Network | VPC with public, private and database subnets; security groups; AWS WAF in front of the load balancer |
| Load balancing | Application Load Balancer with TLS 1.2+ |
| Identity | AWS IAM with role-based access; MFA for administrators |
| Monitoring | Amazon CloudWatch and CloudTrail; basic alerting to Slack |
| Backups | Daily automated RDS snapshots; S3 versioning |

### 2.2 Software

- Web application (React front end) and API services (Node.js).
- Analytics engine producing customer dashboards.
- Internal admin console used by Support and Engineering.
- GitHub for source control and CI/CD pipelines (GitHub Actions).
- Supporting SaaS tools: Slack, Google Workspace, Jira, a password manager, an endpoint management tool, and a helpdesk platform.

### 2.3 People

| Team | Role in the system |
|---|---|
| Engineering | Develop, test and release the platform |
| DevOps | Operate infrastructure, deployments and monitoring |
| Security | Define security requirements, monitor risks and manage incidents |
| Customer Success / Support | Handle customer requests with limited, role-based data access |
| HR | Onboarding, offboarding and training |

### 2.4 Procedures

Policies and procedures covering information security, access management, change management, incident response, backup and recovery, vendor management, HR security and business continuity. Maturity of these will be assessed in Stage 4.

### 2.5 Data

| Data category | Examples | Classification (proposed) |
|---|---|---|
| Customer business records | Accounts, deals, pipeline data, notes | Confidential |
| Customer contact data | Names, business emails, phone numbers | Confidential |
| Customer attachments | Contracts, proposals, documents | Confidential |
| Authentication data | Hashed passwords, API keys, tokens | Restricted |
| System logs | Access and audit logs | Internal |
| Company data | HR, financial and corporate records | Internal / Confidential |

## 3. Data Flow Summary

1. Customer users authenticate to the CloudBridge web application or API over HTTPS.
2. Requests pass through AWS WAF and the load balancer to application containers in private subnets.
3. Application services read and write customer data in the RDS database and S3 storage.
4. Analytics jobs read customer data and generate dashboards.
5. Backups are written to S3 and replicated to the DR region.
6. Logs flow to CloudWatch and CloudTrail for monitoring and audit.
7. Support staff access customer data through the admin console under role-based permissions.

*A data flow diagram will be added in a later iteration.*

## 4. Service Commitments and System Requirements (Assumed)

| Commitment | Source |
|---|---|
| 99.9% monthly platform availability | Customer contracts / SLA |
| Customer data protected from unauthorised access | Customer contracts, security addendum |
| Customer data treated as confidential and not disclosed except as agreed | Customer contracts, NDAs |
| Security incidents notified to affected customers within 72 hours | Customer contracts |
| RPO of 24 hours and RTO of 8 hours | Internal objectives |

## 5. Subservice Organisations

| Provider | Service | Treatment |
|---|---|---|
| Amazon Web Services | Cloud hosting | Carve-out; rely on AWS SOC 2 report, with Complementary Subservice Organisation Controls (CSOCs) assessed |
| GitHub | Source control, CI/CD | Carve-out; review of vendor assurance |
| Google Workspace | Email and collaboration | Carve-out; review of vendor assurance |
| Slack | Internal communications and alerts | Carve-out; limited data exposure |

## 6. Complementary User Entity Controls (Assumed)

Customers are responsible for managing their own user accounts, enforcing strong passwords and MFA on their tenant, reviewing user access, and protecting API keys.

## 7. System Boundaries

**Included:** production AWS environment, application and API services, databases, storage, CI/CD pipeline, supporting corporate systems that access production, and the people and processes that operate them.

**Excluded:** see the scope document for out-of-scope items and justification.