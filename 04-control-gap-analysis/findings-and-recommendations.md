# CloudBridge Technologies Ltd. – Control Assessment Findings and Recommendations

> **Disclaimer:** Fictional case study. This is a readiness assessment, not an audit or attestation. Ratings are simulated from the assumed starting posture and are not the result of real testing.

Supporting workbooks: [`control-assessment.xlsx`](control-assessment.xlsx) and [`gap-register.xlsx`](gap-register.xlsx).

## 1. Scope and approach

All 47 controls defined in Stage 2 were assessed for design, implementation and evidence retention. Each control received an overall status and a Type 2 readiness result, and every control that was not ready was logged as a gap with a severity, linked Stage 3 risk, recommendation, owner and target date.

## 2. Headline results

| Measure | Result |
|---|---|
| Controls designed and implemented | 6 of 47 (13%) |
| Controls partially implemented | 31 of 47 (66%) |
| Controls not implemented | 10 of 47 (21%) |
| Controls ready for a Type 2 observation period | 4 of 47 (9%) |
| Controls with evidence retained | 8 of 47 (17%) |
| Gaps raised | 43 (5 Critical, 22 High, 14 Medium, 2 Low) |
| Gap types | 19 design, 22 implementation, 2 operating evidence |
| In-scope criteria with at least one fully implemented control | 7 of 38 (18%) |

**Overall conclusion:** CloudBridge has a workable foundation in cloud architecture, encryption, backups, HR screening and customer commitments, but is **not yet ready to begin a SOC 2 Type 2 observation period**. Most gaps are about consistency, documentation and evidence rather than missing technology.

## 3. What is working

| Area | Controls | Why it is strong |
|---|---|---|
| Availability engineering | AVL-01, AVL-02 | Multi-AZ database, load balancing and capacity alarms are configured and evidenced (backup monitoring, AVL-03, needs work) |
| Encryption | ACC-06 (with one exception) | KMS encryption at rest and TLS 1.2 or higher on most endpoints; one legacy endpoint accepted TLS 1.0 and has been fixed |
| People and contracts | HR-01, GOV-05 | Screening and customer commitments are documented and retained (HR-04 confidentiality agreements had one exception) |

## 4. Critical findings

| Control | Area | Finding | Recommendation | Target |
|---|---|---|---|---|
| ACC-01 | MFA | MFA is enforced for administrators only | Enforce MFA for all staff on SSO, AWS and GitHub | 11 Dec 2026 |
| CHG-01 | Change approval | Pull request approval and tests are not enforced | Enable branch protection on all production repositories | 11 Dec 2026 |
| OPS-01 | Vulnerability management | Scanning is ad hoc with no timelines | Weekly authenticated scans with severity-based remediation timelines | 18 Dec 2026 |
| ACC-03 | Access review | No periodic access review has ever been performed | Quarterly reviews with signed results and evidenced removals | 15 Jan 2027 |
| AVL-04 | Disaster recovery | No DR plan and no restoration test | Write the DR plan and complete a documented restoration test | 15 Jan 2027 |

These five areas are among the most common causes of exceptions in SOC 2 reports and map to the highest-rated risks in the Stage 3 register (R01, R02, R04, R05, R07).

## 5. Themes across the 43 gaps

1. **Governance is informal.** There is no quarterly management review, policies are stale and unapproved, and no steering group exists (GOV-01, GOV-02, GOV-04).
2. **Evidence is the biggest Type 2 obstacle.** Only 8 controls retain evidence and 15 have none. Without an evidence library and collection schedule, even working controls cannot be proved over time (GOV-07, MON-01, MON-02).
3. **Operational security lacks routine.** Scanning, log alerting, triage, incident exercises and post-incident review are missing or untested (OPS-01 to OPS-05).
4. **Vendor management is absent.** No tiering, due diligence or annual review exists for AWS, GitHub, Google Workspace or Slack (VEN-01 to VEN-03, ACC-07).
5. **Joiner, mover and leaver controls leak.** Access approvals are informal, leaver removal has no deadline and no access reviews are performed (HR-03, ACC-02, ACC-03).
6. **Key-person concentration.** The Security Lead owns 14 of the 43 gaps (33%) and 14 of 47 controls, which is a capacity and continuity risk on its own (R20). The remediation plan moves five of them to other owners.

## 6. Criteria coverage

Only 7 of the 38 in-scope criteria have at least one fully implemented control, and none is yet covered by every mapped control. This strict measure is expected at the start of a readiness engagement. It will improve quickly as the Critical and High gaps close. The per-criterion view is on the **Criteria Coverage** sheet of the control assessment.

## 7. Recommended sequence

| Phase | Window | Focus | Controls with gaps |
|---|---|---|---|
| 1. Quick wins | Dec 2026 | MFA, branch protection, scanning schedule, secret scanning, evidence library | ACC-01, CHG-01, OPS-01, CHG-02, GOV-07 |
| 2. Core controls | Jan 2027 | Access reviews, DR test, management review, IR exercise, control testing, leaver process, penetration test | ACC-03, AVL-04, GOV-04, OPS-04, MON-01, HR-03, MON-03 |
| 3. Process maturity | Feb to Mar 2027 | Policies, vendor programme, logging and alerting, deletion procedure, classification | GOV-01, VEN-01 to VEN-03, OPS-02, CON-01, CON-02 |
| 4. Evidence run-in | After Phase 3 | Run controls on schedule and collect evidence before the observation period starts | All |

A sensible Type 2 observation start is **April 2027**, once Phases 1 to 3 are complete and a few weeks of retained evidence exist.

## 8. Update after the Stage 5 evidence review

Reviewing evidence changed four ratings. Implementation was lowered to partial for ACC-05 (a production bastion allowed SSH from anywhere), ACC-06 (one endpoint accepted TLS 1.0), AVL-03 (three failed backups with no alert) and HR-04 (a contractor started without a signed agreement). Gaps G41 to G43 were added and the ACC-05 gap was revised to High. The workbooks and totals in this document reflect version 0.2.

## 9. Limitations

- Assessment ratings are simulated for a fictional company and rely on the assumptions in the company overview.
- Severity ratings and target dates are assessor proposals and would be agreed with control owners in a real engagement.
- Stage 5 tested the evidence and led to the four changes described in section 8.

## 10. Next steps

- Stage 5 (done): evidence requests and reviews are in `05-evidence-management/`.
- Stage 6 (done): the 43 gaps are converted into a remediation register with ownership, verification and closure records in `06-remediation/`.