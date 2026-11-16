# SOC 2 Readiness Assessment & Gap Analysis

Practical compliance assessment for a fictional SaaS company, **CloudBridge Technologies Ltd.**

> **Disclaimer:** CloudBridge is a fictional organisation created for portfolio purposes. This project demonstrates a SOC 2 *readiness assessment*. It is **not** a SOC 2 audit, attestation or report; only an independent CPA firm can issue those. All company details are assumptions.

## Objective

Take a fictional SaaS company from initial compliance assessment through gap identification, evidence evaluation, remediation and management reporting, preparing it for a future **SOC 2 Type 2** examination.

## Case Study

| Item | Detail |
|---|---|
| Company | CloudBridge Technologies Ltd. (fictional) |
| Business | Cloud-based CRM and customer data analytics (SaaS) |
| Customers | SMEs and enterprise clients |
| Infrastructure | AWS |
| Size | 45 employees (8 IT/engineering, 2 security) |
| Objective | SOC 2 Type 2 readiness |

## Scope

| Trust Services Category | Status |
|---|---|
| Security | In scope |
| Availability | In scope |
| Confidentiality | In scope |
| Processing Integrity | Considered, out of scope (justified) |
| Privacy | Considered, out of scope (justified) |

See the [scope document](02-scope-and-criteria/scope-document.md) for justification.

## Tools

- **eramba Community**: GRC and control management
- **Microsoft Excel**: assessment, evidence and remediation registers
- **Power BI**: management dashboard
- **GitHub**: documentation and portfolio presentation

## Project Stages

| # | Stage | Deliverables | Status |
|---|---|---|---|
| 1 | Company profile, scope and system description | [Company overview](01-company-profile/company-overview.md), [System description](01-company-profile/system-description.md), [Scope document](02-scope-and-criteria/scope-document.md) | Complete |
| 2 | Criteria and control mapping | Control matrix, criteria-to-control mapping, ownership register | Complete |
| 3 | Risk assessment | Risk register, methodology, treatment plan | Complete |
| 4 | Control assessment and gap analysis | Control assessment, gap register, findings | Not started |
| 5 | Evidence collection and evaluation | Evidence request register, review log, status tracker | Not started |
| 6 | Remediation management | Remediation register, ownership matrix, closure records | Not started |
| 7 | GRC implementation and dashboard | eramba workflow, Power BI dashboard | Not started |
| 8 | Final readiness report | Executive summary, readiness report, remediation roadmap | Not started |

## Repository Structure

```
SOC-2-Readiness-Assessment/
├── README.md
01-company-scope-and-system/
├── company-overview.md
├── system-description.md
└── scope-document.md
02-criteria-mapping/
└── criteria-mapping.xlsx
├── 03-risk-assessment/
│   └── risk-register.xlsx
├── 04-control-gap-analysis/
│   ├── control-assessment.xlsx
│   └── gap-register.xlsx
├── 05-evidence-management/
│   ├── evidence-request-register.xlsx
│   └── evidence-review-log.xlsx
├── 06-remediation/
│   └── remediation-register.xlsx
├── 07-management-reporting/
│   └── dashboard/
├── 08-final-report/
│   └── readiness-report.md
└── screenshots/
```

## How to Use This Repository

1. Start with the [company overview](01-company-profile/company-overview.md) and [scope document](02-scope-and-criteria/scope-document.md) to understand the scenario.
2. Follow the stage folders in numerical order; each builds on the one before.
3. Read the final report in `08-final-report/` for the consolidated findings and roadmap (available once Stage 8 is complete).

## Approach

- **Type 2 oriented:** controls are assessed for design and implementation first, then for the evidence and operating history a Type 2 examination would require.
- **Original matrix:** the control mapping is original work that references, and does not reproduce, AICPA material.
- **Evidence quality:** evidence is evaluated for whether it actually supports the control claim, not only whether it exists.
- **Accountability:** every gap has an owner, a target date and a verification step.

## References

- [AICPA 2017 Trust Services Criteria (revised points of focus 2022)](https://www.aicpa-cima.com/resources/article/2017-trust-services-criteria-with-revised-points-of-focus-2022)
- [AICPA SOC Resource Library](https://www.aicpa-cima.com/resources/landing/system-and-organization-controls-soc-suite-of-services)

## Author

**Olawale Akinbola**
GRC and Cybersecurity Compliance | TPRM · Risk Assessment · ISO 27001 · SOC 2

[LinkedIn](https://www.linkedin.com/in/olawale-akinbola-tprm) · [GitHub](https://github.com/Olawyle)
