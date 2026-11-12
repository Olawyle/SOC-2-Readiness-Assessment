# CloudBridge Technologies Ltd. – Company Overview

> **Disclaimer:** CloudBridge Technologies Ltd. is a fictional organisation created for a portfolio case study. All details are assumptions, not claims about any real company.

## 1. Business Summary

| Item | Detail |
|---|---|
| Legal name | CloudBridge Technologies Ltd. |
| Industry | Cloud-based Software as a Service (SaaS) |
| Core services | Customer relationship management (CRM) and customer data analytics |
| Customers | Small and medium-sized enterprises (SMEs) and enterprise clients |
| Hosting | Amazon Web Services (AWS) |
| Employees | 45 |
| IT / Engineering team | 8 |
| Security team | 2 |
| Compliance objective | SOC 2 Type 2 readiness |
| Assessment scope | Security (Common Criteria), Availability, Confidentiality |

## 2. Products and Services

1. **CloudBridge CRM** – multi-tenant web application for managing contacts, accounts, sales pipelines, support tickets and communication history.
2. **CloudBridge Insights** – analytics module providing dashboards and reports built on customer CRM data.
3. **CloudBridge API** – REST API enabling customers to integrate CRM data with third-party tools.
4. **Customer Support Portal** – ticketing and knowledge base for customer success.

## 3. Customers and Data

- Approximately 320 customer organisations (about 260 SMEs, 60 enterprise clients).
- Customer data processed: contact records, business records, deal and revenue data, support correspondence and uploaded attachments.
- Some customer records contain personal information (names, business emails, phone numbers). Privacy is considered but outside the initial scope (see scope document).
- Enterprise customers increasingly request a SOC 2 report during procurement and security reviews, which drives the compliance objective.

## 4. Organisation Structure

| Function | Headcount | Notes |
|---|---|---|
| Executive / Management | 4 | CEO, CTO, CFO, COO |
| Engineering / IT | 8 | Development, DevOps, cloud infrastructure, internal IT |
| Security | 2 | Security Lead (acting CISO responsibilities) and Security Analyst |
| Product | 4 | Product management and design |
| Sales and Marketing | 12 | Including pre-sales |
| Customer Success and Support | 11 | Tier 1 and Tier 2 support |
| Finance, HR and Administration | 4 | Includes HR and vendor management |
| **Total** | **45** | |

The Security Lead reports to the CTO. There is no dedicated compliance function; compliance is currently a shared responsibility.

## 5. Current Security and Compliance Posture (Starting Assumptions)

These assumptions are deliberately realistic for a growing SaaS company and will be tested in the later stages.

- Some policies exist (acceptable use, information security) but have not been formally reviewed in over 12 months.
- Access to AWS is managed through IAM with MFA enforced for administrators but not consistently for all staff.
- Code is managed in GitHub with pull request reviews that are not consistently enforced.
- Vulnerability scanning is performed ad hoc, not on a defined schedule.
- Backups are configured, but restoration tests have not been documented.
- An incident response plan exists but has not been exercised.
- Vendor onboarding is informal; no consistent due diligence record is kept.
- Security awareness training is delivered at onboarding only.
- Evidence of control operation is not systematically retained.

## 6. Key Stakeholders

| Role | Responsibility in the engagement |
|---|---|
| CEO | Executive sponsor of SOC 2 initiative |
| CTO | Owner of system and infrastructure controls |
| Security Lead | Day-to-day owner of the SOC 2 programme |
| Head of HR | HR-related controls (onboarding, offboarding, training) |
| Head of Customer Success | Customer commitments and support processes |
| DevOps Lead | Change management, monitoring and backup controls |

## 7. Business Drivers for SOC 2

- Meet enterprise customer procurement requirements.
- Reduce the effort of repeated security questionnaires.
- Demonstrate maturity to investors and partners.
- Establish a repeatable control framework that supports future ISO 27001 alignment.