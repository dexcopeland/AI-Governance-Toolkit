# AI Use-Case Intake Form

> Completed by the **requester** (with help from the AI Intake & Triage Analyst Gem if needed). This is the front door of the intake review pipeline. Keep it light — depth comes later in the risk assessment.
>
> 📄 Worked example: `Examples/01-Intake-Form--TalentSift.md`

| Field | Value |
|---|---|
| Intake ID | `[AUTO / e.g., AI-2026-001]` |
| Date submitted | `[YYYY-MM-DD]` |
| Requester name & role | |
| Business unit / sponsor | |
| Requested go-live (target) | |

## 1. What are you trying to do?
*Describe the business problem and the proposed AI solution in plain language (no jargon).*



## 2. The AI system
| Question | Answer |
|---|---|
| System / product / model name | |
| Build, buy, or embedded in existing tool? | ☐ Build internally ☐ Buy (vendor) ☐ Feature of existing tool |
| Vendor (if any) | |
| Underlying model(s), if known | `[e.g., Gemini, GPT-4, custom, unknown]` |
| Is this **generative** AI? | ☐ Yes ☐ No ☐ Unsure |
| Will it make or materially inform a **decision about a person**? | ☐ Yes ☐ No ☐ Unsure |
| Is there a **human in the loop** before action is taken? | ☐ Yes, reviews every output ☐ Sometimes / sampled ☐ No, fully automated |

## 3. Data
| Question | Answer |
|---|---|
| What data goes **in** (prompts/inputs/training)? | |
| Does input include **personal data / PII**? | ☐ Yes ☐ No ☐ Unsure |
| Does it include **sensitive / regulated** data (health, financial, biometric, minors, etc.)? | ☐ Yes ☐ No ☐ Unsure |
| Does it include **confidential / non-public** organizational data? | ☐ Yes ☐ No ☐ Unsure |
| Where is data processed/stored? | `[cloud / region / on-prem / vendor]` |
| Will our data be used to **train the vendor's model**? | ☐ Yes ☐ No ☐ Unsure ☐ Contractually prohibited |

## 4. People affected
| Question | Answer |
|---|---|
| Who is affected by the outputs? | ☐ Internal staff ☐ Customers / public ☐ Vulnerable groups ☐ Other: |
| Approx. number of people affected | |
| Could an error cause **harm** (financial, legal, safety, reputational, rights)? | ☐ High ☐ Medium ☐ Low — explain: |

## 5. Context the reviewer needs
- Existing approvals or reviews already done:
- Known constraints (legal, contractual, budget, deadline):
- Anything that worries you about this use case:

---

### Requester attestation
> I confirm the information above is accurate to the best of my knowledge and I will notify AI Governance of material changes to scope, data, or vendor.

**Name:** ________________  **Date:** ____________

---
*Next step: AI Governance triages this form → assigns a risk tier → routes to the appropriate review path. See `Intake-Review-Decision-Record.md`.*
