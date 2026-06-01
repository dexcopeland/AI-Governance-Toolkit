# AI Risk Assessment — WORKED EXAMPLE (fictional)

> Reference only. Demonstrates `Templates/AI-Risk-Assessment.md` using **NIST trustworthiness-characteristic scoring** (overall tier = the highest single characteristic rating).

| Field | Value |
|---|---|
| Intake ID | AI-2026-014 |
| System / use case | TalentSift — AI resume screening & shortlisting |
| Assessor | A. Rivera, AI Governance |
| Date | 2026-05-20 |
| Risk tier (from triage) | High (provisional) |
| Assessment version | v1.0 |

---

## A. GOVERN — accountability & oversight
| Item | Answer |
|---|---|
| Business owner (accountable) | VP People |
| Technical owner | HR Systems Manager |
| Policies/standards that apply | AI Acceptable Use Policy; Privacy Policy; EEO/non-discrimination obligations |
| Within approved policy? | Needs exception/committee review (high-risk, decisions about people) |
| Human oversight model | Human-on-the-loop — recruiter reviews shortlist but does not re-read every rejected resume |

## B. MAP — context & intended use
- **Intended purpose:** rank applicants by fit to a job description; generate candidate summaries to speed recruiter review.
- **Out-of-scope / prohibited:** must NOT auto-reject candidates without human review; must NOT be used for promotion/termination decisions; must NOT infer protected characteristics.
- **Stakeholders:** job applicants (external, affected), recruiters (users), HR leadership, Legal.
- **Foreseeable misuse / failure modes:** recruiters rubber-stamp the AI ranking (automation bias); model penalizes employment gaps (proxy for caregiving/disability/age); prompt-injection text hidden in a resume inflates a score; scores treated as objective truth.
- **Dependencies:** vendor model & uptime; quality/representativeness of training data (vendor-controlled); job-description quality.

## C. MEASURE — trustworthiness analysis

| # | Characteristic | Risk(s) identified | Inherent rating | Basis for rating |
|---|---|---|---|---|
| 1 | **Valid & Reliable** | Vendor accuracy claims not validated on *our* roles/applicant pool; "fit score" may not predict job success | **Medium** | Plausible but unproven; testable before/after deployment |
| 2 | **Safe** | Wrongful screening denies livelihood (economic harm to individuals) | **Medium** | Real harm, but mediated by human review |
| 3 | **Secure & Resilient** | Resume text is untrusted input → prompt-injection to game scores; PII in a SaaS | **Medium** | Vendor has SOC 2; injection risk specific to this use, mitigable with input handling |
| 4 | **Accountable & Transparent** | Applicants not told AI is used; limited audit trail of why someone was ranked low | **High** | Transparency to affected people is weak; growing legal expectation of disclosure |
| 5 | **Explainable & Interpretable** | Cannot explain to a rejected applicant *why* they scored low; some jurisdictions require this | **High** | Black-box scoring + potential legal duty to explain adverse decisions |
| 6 | **Privacy-Enhanced** | Sensitive PII; unclear retention; possible training use; cross-border processing | **High** | Large volume of external-individual PII with unresolved retention/training-use questions |
| 7 | **Fair (bias managed)** | Resume screening is a well-documented disparate-impact risk; vendor bias testing is limited and not on our population; proxies (name, gaps, schools) | **Critical** | Direct risk of unlawful discrimination affecting thousands; vendor evidence insufficient |

**Overall inherent risk tier (= highest single rating): Critical** — driven by **Fairness**.

## D. MANAGE — treatment plan
| Risk (ref #) | Mitigation / control | Owner | Due | Residual rating |
|---|---|---|---|---|
| 7 Fair | Independent adverse-impact (4/5ths) analysis before launch + quarterly; remove name/school/photo from model input | AI Gov + HR | Pre-launch | High |
| 7 Fair | Recruiter must review full resume before any rejection of an AI-deprioritized candidate; log rationale | HR | Pre-launch | High |
| 4/5 Transparent/Explainable | Disclose AI use to applicants; provide human contact for adverse-decision questions | HR + Legal | Pre-launch | Medium |
| 6 Privacy | DPA with no-training clause; 12-month retention max; US-only processing; DPIA completed | Privacy | Pre-launch | Medium |
| 1 Valid | Validate scores against recruiter judgment on a pilot set before full rollout | HR Systems | Pilot | Low |
| 3 Secure | Sanitize/limit resume text; vendor confirms injection safeguards | Security | Pre-launch | Low |

**Overall residual risk tier (= highest single residual rating): High** — fairness cannot be reduced below High in this domain; it requires *ongoing* monitoring, not a one-time fix.

**Decision recommendation:** ☒ Approve with conditions (Critical inherent tier → requires committee approval)
**Conditions before go-live:** adverse-impact analysis passed; recruiter-review-before-rejection enforced; applicant disclosure live; DPA with no-training + 12-mo retention signed; pilot validation complete.

**Monitoring & review:**
- Metrics: shortlist selection rates by protected group (4/5ths), override rate, complaint volume, score-vs-hire correlation.
- Cadence: ☒ Quarterly
- Re-assessment triggers: vendor model version change, new job families, expansion beyond shortlisting, any adverse-impact flag.

---
### Sign-off
**Assessor:** A. Rivera **Date:** 2026-05-20
**Governance reviewer:** _pending committee_ **Date:** ____

> *Note the rubric in action: six characteristics are Medium/High, but one **Critical** (Fairness) sets the whole use case to **Critical inherent** — averaging would have wrongly hidden that. Conditions bring residual to **High**, which the accountable owner must formally accept. → see 04.*
