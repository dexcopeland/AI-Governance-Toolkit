# Lightweight AI Impact Assessment

> A **proportionate**, one-page screen for **Minimal and Limited tier** use cases — so you capture impact on individuals without running a full NIST RMF assessment on low-risk tools. Maps to ISO/IEC 42001 **A.5 / Clause 6.1.4** (AI system impact assessment) at a depth matched to the risk.
>
> ⛔ **Not for High-tier or decisions-about-people use cases** — those go to the full `AI-Risk-Assessment.md`. If any red-flag below is "Yes," **escalate** rather than completing this form.

| Field | Value |
|---|---|
| Intake ID | |
| System / use case | |
| Assessor | |
| Date | `[YYYY-MM-DD]` |
| Provisional tier | ☐ Minimal ☐ Limited |

---

## 1. Red-flag screen (escalation triggers)
If **any** answer is **Yes**, stop and escalate to a full risk assessment / re-tier — this use case is not low-risk.

| # | Question | Answer |
|---|---|---|
| 1 | Does it **make or materially inform a decision about a person** (hiring, benefits, access, eligibility)? | ☐ Yes ☐ No |
| 2 | Does it process **sensitive/regulated data** (health, financial, biometric, minors, protected characteristics)? | ☐ Yes ☐ No |
| 3 | Does it affect **vulnerable groups** or the **public** at scale? | ☐ Yes ☐ No |
| 4 | Does it operate **without a human reviewing outputs** before action? | ☐ Yes ☐ No |
| 5 | Could a failure cause **legal, safety, financial, or rights harm**? | ☐ Yes ☐ No |
| 6 | Is it **novel, high-visibility, or reputationally sensitive**? | ☐ Yes ☐ No |

**Screen result:** ☐ All "No" → continue below · ☐ One or more "Yes" → **escalate to `AI-Risk-Assessment.md`** (stop here)

## 2. Condensed impact check
*Brief note + Low/Medium rating per area. If anything reaches "High," escalate.*

| Area | Note | Rating |
|---|---|---|
| **Accuracy / reliability** — is it fit for purpose? | | Low / Med |
| **Privacy** — what data, retention, vendor use? | | Low / Med |
| **Fairness** — any group treated differently? | | Low / Med |
| **Transparency** — do users know AI is involved? | | Low / Med |
| **Security** — data exposure / misuse risk? | | Low / Med |

## 3. Proportionate controls
*The few light controls appropriate for a low-risk tool (e.g., usage guidance, "don't input confidential data," human spot-check, disclosure).*
-
-

## 4. Decision
☐ **Proceed** (Minimal) ☐ **Proceed with light conditions** (Limited) ☐ **Escalate to full assessment**

**Conditions (if any):**
**Next review:** ☐ Annual ☐ On material change
**Add to `AI-System-Inventory.md`?** ☐ Yes (always, once approved)

---
### Sign-off
**Assessor:** ____________ **Date:** ______
**Governance reviewer (Limited tier):** ____________ **Date:** ______
