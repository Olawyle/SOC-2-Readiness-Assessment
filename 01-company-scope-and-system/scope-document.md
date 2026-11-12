# CloudBridge Technologies Ltd. – SOC 2 Readiness Scope Document

> **Disclaimer:** Fictional case study. This project is a readiness assessment. It is **not** a SOC 2 examination, attestation or report. Only an independent CPA firm can issue a SOC 2 report.

## 1. Purpose

Define the boundaries, criteria, reporting approach and assumptions for the SOC 2 readiness assessment of CloudBridge Technologies Ltd.

## 2. Assessment Objective

Assess readiness against the selected AICPA Trust Services Criteria, identify control gaps, evaluate available evidence, and produce a prioritised remediation roadmap that prepares the organisation for a future **SOC 2 Type 2** examination.

## 3. Reference Framework

- AICPA 2017 Trust Services Criteria (with revised points of focus, 2022).
- The assessment matrix is original work. Published criteria are referenced, not reproduced wholesale.

## 4. Trust Services Categories

| Category | In scope? | Justification |
|---|---|---|
| Security (Common Criteria) | **Yes** | Mandatory baseline for any SOC 2 report; primary customer concern |
| Availability | **Yes** | SLA commitment of 99.9% uptime; customers rely on the platform for daily operations |
| Confidentiality | **Yes** | Platform stores confidential customer business data subject to contractual confidentiality |
| Processing Integrity | No (considered) | Platform is a data repository and analytics tool rather than a transaction-processing system; accuracy risks are lower than for payment or financial processing. To be reconsidered if analytics outputs become customer-critical |
| Privacy | No (considered) | Personal data is limited to business contact details; privacy obligations are addressed separately (e.g. GDPR / NDPA programmes) and would broaden scope disproportionately at this stage |

## 5. Report Type Approach

| Stage | Focus |
|---|---|
| Readiness assessment (this project) | Control design, implementation and evidence quality |
| Future Type 1 (optional) | Design of controls at a point in time |
| Future Type 2 (target) | Design and operating effectiveness over an observation period (proposed 6 months initially) |

## 6. In-Scope Items

**Services:** CloudBridge CRM, CloudBridge Insights, CloudBridge API.

**Infrastructure and systems:** production AWS accounts and regions, VPC networking, ECS/EC2 workloads, RDS, S3, IAM, CloudWatch, CloudTrail; GitHub repositories and CI/CD pipelines supporting production; internal admin console.

**Supporting corporate systems:** identity provider and SSO/MFA, endpoint management, ticketing (Jira), communications used for incident handling, password manager.

**People:** Engineering, DevOps, Security, Customer Success/Support, HR and management personnel with access to or responsibility for in-scope systems.

**Processes:** access management, change management, vulnerability management, logging and monitoring, incident response, backup and recovery, business continuity, vendor management, HR security, risk management, data classification and retention.

**Locations:** head office and remote workers accessing in-scope systems.

## 7. Out-of-Scope Items

| Item | Reason |
|---|---|
| Staging and development environments with no customer data | No production data; assessed only where they affect production change control |
| Marketing website and CMS | Does not process customer data |
| Sales and marketing tools (e.g. CRM for internal prospecting) | Not part of the service delivered to customers |
| Finance and payroll systems | Not part of the service commitments |
| Processing Integrity and Privacy criteria | See Section 4 |
| Physical data centre controls | Inherited from AWS (subservice organisation carve-out) |

## 8. Subservice Organisations

AWS, GitHub, Google Workspace and Slack are treated using the carve-out method. The readiness assessment will review each provider's available assurance reports and identify complementary subservice organisation controls CloudBridge must operate.

## 9. Assessment Approach

1. Map in-scope criteria to CloudBridge controls (Stage 2).
2. Assess risks using a likelihood × impact methodology (Stage 3).
3. Evaluate control design and implementation, and record gaps (Stage 4).
4. Request and review evidence, including evidence needed to show operation over time (Stage 5).
5. Plan and track remediation with owners and dates (Stage 6).
6. Report progress through eramba and a Power BI dashboard (Stage 7).
7. Publish a readiness report and roadmap (Stage 8).

## 10. Rating Scales (Initial Proposal)

| Rating | Meaning |
|---|---|
| Designed and implemented | Control exists and is in place as described |
| Partially implemented | Control exists but is incomplete or inconsistent |
| Not implemented | No control exists |
| Not applicable | Criterion does not apply, with justification |

Evidence status: Not requested, Requested, Received, Under review, Accepted, Rejected / insufficient.

## 11. Tooling

| Tool | Purpose |
|---|---|
| eramba Community | Control, risk and compliance management |
| Microsoft Excel | Matrices, registers and evidence trackers |
| Power BI | Management dashboard |
| GitHub | Documentation and portfolio publication |

## 12. Assumptions and Limitations

- All organisational facts are fictional assumptions.
- No real customer data, systems or company are assessed.
- Conclusions represent readiness opinions, not audit assurance.
- Scope may be refined as later stages reveal dependencies.

## 13. Document Control

| Version | Date | Author | Change |
|---|---|---|---|
| 0.1 | 2026-11-12 | Project author | Initial draft for Stage 1 |