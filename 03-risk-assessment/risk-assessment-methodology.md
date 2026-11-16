# CloudBridge Technologies Ltd. – Risk Assessment Methodology

> **Disclaimer:** Fictional case study. This is a readiness assessment, not an audit or attestation. All values are assumptions.

## 1. Purpose

Identify and rate risks to CloudBridge's Security, Availability and Confidentiality commitments, and decide how each risk will be treated. This supports the SOC 2 risk assessment criteria (CC3.1 to CC3.4) and business disruption and vendor risk (CC9.1, CC9.2). The working register is in [`risk-register.xlsx`](risk-register.xlsx).

## 2. Approach

| Step | Activity |
|---|---|
| 1. Identify | Draw risks from the system description, the starting security posture, the Stage 2 control set and common SaaS threats |
| 2. Inherent risk | Rate likelihood and impact assuming no controls |
| 3. Current risk | Rate again with controls as they operate today (refined after Stage 4 and Stage 5) |
| 4. Evaluate | Compare the current rating with the thresholds and risk appetite |
| 5. Treat | Choose Mitigate, Accept, Transfer or Avoid; assign owner, date and target score |
| 6. Review | Management reviews quarterly and after significant change |

## 3. Likelihood (next 12 months)

| Score | Level | Description |
|---|---|---|
| 1 | Rare | Under 5%; no history in comparable companies |
| 2 | Unlikely | 5% to 20% |
| 3 | Possible | 20% to 50%; has occurred in similar organisations |
| 4 | Likely | 50% to 80%; expected given current controls |
| 5 | Almost certain | Over 80%; occurring or near certain |

## 4. Impact (worst realistic outcome)

| Score | Level | Customer data and security | Availability | Financial (USD, assumed) | Compliance and reputation |
|---|---|---|---|---|---|
| 1 | Minimal | No customer data affected | Under 15 min | Under 5,000 | No attention |
| 2 | Minor | Internal data only | 15 min to 1 hour | 5,000 to 25,000 | Minor customer queries |
| 3 | Moderate | One customer's limited data exposed | 1 to 4 hours | 25,000 to 100,000 | Complaints; SLA credits |
| 4 | Major | Several customers' data exposed | 4 to 8 hours (RTO at risk) | 100,000 to 500,000 | Contract breach; escalations |
| 5 | Severe | Large breach or permanent data loss | Over 8 hours or data loss | Over 500,000 | Key customer loss; failed SOC 2 outcome |

## 5. Rating and required response

Score = likelihood x impact (1 to 25).

| Rating | Score | Required response |
|---|---|---|
| Low | 1 to 5 | Accept and monitor |
| Medium | 6 to 11 | Accept or mitigate; owner reviews at least twice a year |
| High | 12 to 19 | Treatment plan with owner and date; quarterly management reporting |
| Critical | 20 to 25 | Immediate treatment; executive attention; monthly reporting |

**Risk appetite:** management accepts Low and Medium residual risk. High and Critical current risks require a treatment plan.

## 6. Treatment options

- **Mitigate:** add or improve controls to reduce likelihood or impact.
- **Accept (monitor):** formally accept within appetite and keep under review.
- **Transfer:** share the risk, for example through insurance or contract terms.
- **Avoid:** stop the activity that creates the risk.

## 7. Limitations

- Current scores rely on the starting posture assumed in the [company overview](../01-company-scope-and-system/company-overview.md). Stage 4 will test whether controls are designed and implemented, and scores will be updated.
- Likelihood and impact values are judgement-based and are fictional for this case study.
- Risk owners are roles, not named individuals.

## 8. Results summary (draft 0.1)

| Rating | Inherent | Current | Target |
|---|---|---|---|
| Critical | 6 | 0 | 0 |
| High | 11 | 14 | 0 |
| Medium | 5 | 8 | 16 |
| Low | 0 | 0 | 6 |

22 risks were assessed; 14 currently rate High and each has a treatment plan, giving an expected reduction in average score of about 47% once the plan is complete.