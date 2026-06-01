# AI Risk Assessment

> Structured around the **NIST AI RMF** functions (MAP → MEASURE → MANAGE, under GOVERN) and the seven trustworthiness characteristics. Produced by the *AI Risk Assessor (NIST AI RMF)* Gem and reviewed by AI Governance.

| Field | Value |
|---|---|
| Intake ID | |
| System / use case | |
| Assessor | |
| Date | `[YYYY-MM-DD]` |
| Risk tier (from triage) | ☐ Minimal ☐ Limited ☐ High ☐ Unacceptable/Prohibited |
| Assessment version | `v1.0` |

---

## A. GOVERN — accountability & oversight
| Item | Answer |
|---|---|
| Business owner (accountable) | |
| Technical owner | |
| Which policies/standards apply? | |
| Is this use within approved organizational policy? | ☐ Yes ☐ No ☐ Needs exception |
| Human oversight model | ☐ Human-in-the-loop ☐ Human-on-the-loop ☐ Human-out-of-the-loop |

## B. MAP — context & intended use
- **Intended purpose & how it will be used:**
- **Out-of-scope / prohibited uses (state explicitly):**
- **Stakeholders & affected parties:**
- **Foreseeable misuse or failure modes:**
- **Dependencies (data, models, vendors, infrastructure):**

## C. MEASURE — trustworthiness analysis

> Rate **each** characteristic on the four-level scale (see rubric at the bottom). The **overall inherent risk tier = the highest single characteristic rating** (worst-case rule — do not average). Leave "N/A" where genuinely not applicable, with a one-line reason; N/A never drives the overall tier.

| # | Trustworthiness characteristic | Key questions | Risk(s) identified | Inherent rating (Low/Med/High/Critical) | Basis for rating |
|---|---|---|---|---|---|
| 1 | **Valid & Reliable** | Is it accurate for its purpose? Tested? Known error rate? | | | |
| 2 | **Safe** | Can outputs cause physical/psychological/financial/societal harm? | | | |
| 3 | **Secure & Resilient** | Exposure to prompt injection, data exfiltration, model theft, adversarial input? | | | |
| 4 | **Accountable & Transparent** | Is it disclosed to users? Audit trail? Clear ownership? | | | |
| 5 | **Explainable & Interpretable** | Can outputs/decisions be explained to affected people? | | | |
| 6 | **Privacy-Enhanced** | PII handling, data minimization, retention, training-data use, consent? | | | |
| 7 | **Fair (bias managed)** | Disparate impact across groups? Representative data? Bias tested? | | | |

**Overall inherent risk tier (= highest single rating above): __________**

## D. MANAGE — treatment plan
| Risk (ref #) | Mitigation / control | Owner | Due | Residual rating after control |
|---|---|---|---|---|
| | | | | |
| | | | | |

**Overall residual risk tier (= highest single residual rating): __________**

**Decision recommendation:** ☐ Approve ☐ Approve with conditions ☐ Reject ☐ Escalate
**Conditions / required controls before go-live:**

**Monitoring & review:**
- Metrics to track:
- Review cadence: ☐ Quarterly ☐ Semi-annual ☐ Annual ☐ Event-triggered
- Re-assessment triggers (scope/data/model/vendor change):

---

### Assessor sign-off
**Name:** ________________ **Date:** ____________
**Governance reviewer:** ________________ **Date:** ____________

---

## Risk-rating rubric — NIST trustworthiness-characteristic scoring

Rate each of the 7 characteristics on the scale below, weighing **both** how likely a problem is **and** how severe it would be. The **overall tier is the highest single characteristic rating** — one Critical characteristic makes the whole use case Critical, regardless of the others.

| Rating | Meaning | Default handling |
|---|---|---|
| **Low** | Minimal concern; standard practice is sufficient. | Accept; document. |
| **Medium** | Notable concern; needs defined controls. | Mitigate with standard controls. |
| **High** | Serious concern; could cause material harm. | Strong controls + named owner required before go-live. |
| **Critical** | Severe/unacceptable as-is (legal, safety, or rights violation; major harm). | Senior/committee approval required; reject if unmitigable. |

**Rules:**
- **Overall tier = the maximum rating across all rated characteristics. Do not average.**
- Any characteristic touching a **legally prohibited use** → **Unacceptable**; route to rejection.
- "N/A" is allowed per characteristic (with a one-line reason) and never raises the overall tier.
- Re-rate residual risk after controls; the **overall residual tier** also uses the maximum rule.

> See `Examples/02-Risk-Assessment--TalentSift.md` for a fully worked assessment using this rubric.
