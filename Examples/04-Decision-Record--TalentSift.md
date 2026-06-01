# Intake Review Decision Record — WORKED EXAMPLE (fictional)

> Reference only. Demonstrates `Templates/Intake-Review-Decision-Record.md`.

| Field | Value |
|---|---|
| Intake ID | AI-2026-014 |
| System / use case | TalentSift — AI resume screening & shortlisting |
| Requester / business unit | Jordan Lee / Human Resources |
| Risk tier | High (residual; Critical inherent) |
| Decision date | 2026-05-27 |
| Decision maker(s) | AI Governance Committee (chaired by CISO; VP People, Legal, Privacy, AI Gov) |
| Linked artifacts | Intake form: ☒ · Risk assessment: ☒ · Vendor assessment: ☒ |

## Triage summary
- **Review path taken:** ☒ Enhanced review + committee
- **Why:** decisions about people at scale, regulated PII, and a Critical inherent fairness risk — exceeds delegated-approval authority, so committee review was required.

## Decision
☒ **Approved with conditions**

**Rationale:** The business value is real and the residual risk is acceptable *only if* the fairness, transparency, and privacy controls operate continuously. The committee is not accepting the Critical inherent risk; it is approving the **High residual** posture created by the conditions, with mandatory monitoring.

## Conditions of approval
| # | Condition | Owner | Due date | Verified |
|---|---|---|---|---|
| 1 | Independent adverse-impact (4/5ths) analysis passed pre-launch | AI Gov | 2026-07-15 | ☐ |
| 2 | Recruiter reviews full resume before rejecting any AI-deprioritized candidate; rationale logged | HR | 2026-07-15 | ☐ |
| 3 | Applicant disclosure of AI use + human contact for adverse-decision queries live | HR + Legal | 2026-07-15 | ☐ |
| 4 | Signed DPA: no-training, 12-month retention, US-only, deletion-on-request | Privacy | 2026-07-01 | ☐ |
| 5 | Pilot validation of scores vs. recruiter judgment completed | HR Systems | 2026-07-22 | ☐ |
| 6 | Name/school excluded from model input | HR Systems | 2026-07-15 | ☐ |

## Residual risk accepted
- **Residual risk statement:** Even with controls, fairness risk remains **High** and requires quarterly adverse-impact monitoring; automation bias remains a standing concern.
- **Risk accepted by:** VP People (accountable business owner)

## Review & expiry
- **Next review date:** 2026-10-27 (quarterly), or earlier on trigger.
- **Early re-review triggers:** any adverse-impact flag, vendor model version change, expansion beyond shortlisting, applicant complaint of discrimination.
- **Approval expires:** at next review or on material change.

---
### Sign-off
| Role | Name | Approval | Date |
|---|---|---|---|
| AI Governance | A. Rivera | Recommended | 2026-05-27 |
| Business owner (risk acceptor) | VP People | Accepted | 2026-05-27 |
| Committee chair | CISO | Approved w/ conditions | 2026-05-27 |
