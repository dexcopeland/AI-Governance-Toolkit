# AI Use-Case Intake Form — WORKED EXAMPLE (fictional)

> Reference only. Demonstrates a completed `Templates/AI-Use-Case-Intake-Form.md`.

| Field | Value |
|---|---|
| Intake ID | AI-2026-014 |
| Date submitted | 2026-05-12 |
| Requester name & role | Jordan Lee — Talent Acquisition Lead |
| Business unit / sponsor | Human Resources (sponsor: VP People) |
| Requested go-live (target) | 2026-08-01 |

## 1. What are you trying to do?
We get ~5,000 applications a year and recruiters can't read them all carefully. We want a tool that reads each resume, scores how well it fits the job description, and gives us a ranked shortlist plus a short summary of each top candidate, so recruiters spend their time on the strongest applicants.

## 2. The AI system
| Question | Answer |
|---|---|
| System / product / model name | TalentSift (SaaS) |
| Build, buy, or embedded? | ☒ Buy (vendor) |
| Vendor | TalentSift Inc. |
| Underlying model(s) | Vendor-hosted LLM (vendor says "proprietary + fine-tuned open model"); exact base unknown |
| Is this **generative** AI? | ☒ Yes (writes candidate summaries) |
| Decision about a **person**? | ☒ Yes — ranks/screens job applicants |
| **Human in the loop**? | ☒ Sometimes — recruiter reviews the shortlist, but ranking strongly steers who gets seen |

## 3. Data
| Question | Answer |
|---|---|
| Data in | Applicant resumes (names, contact, work history, education), the job description |
| Personal data / PII? | ☒ Yes |
| Sensitive / regulated? | ☒ Yes — resumes can reveal/infer protected characteristics (age, sex, national origin, disability) |
| Confidential org data? | ☒ Yes — unposted job requisitions, hiring strategy |
| Where processed/stored? | Vendor cloud, US region (per vendor); to confirm in contract |
| Used to train vendor model? | ☒ Unsure — must confirm and contractually prohibit |

## 4. People affected
| Question | Answer |
|---|---|
| Who is affected? | ☒ Customers/public (job applicants) — external individuals |
| Approx. number affected | ~5,000 applicants/year |
| Could an error cause harm? | ☒ High — a biased or wrong score can deny someone a job opportunity (economic + legal/rights harm) |

## 5. Context the reviewer needs
- Existing approvals: none yet.
- Constraints: HR wants it before fall hiring; budget approved.
- What worries me: I've read that resume-screening AI has gotten companies in trouble for bias. I want to do this right.

---
### Requester attestation
**Name:** Jordan Lee  **Date:** 2026-05-12

---
*Triage outcome → tier: High (provisional); review paths: Privacy/DPIA, Legal/Employment, Bias/Fairness, Vendor, Records. Routed to enhanced review. → see 02.*
