# Templates — Index

Ten fill-in templates covering the full AI governance lifecycle. Grab the one you need; each maps to NIST AI RMF and/or ISO/IEC 42001 and has a worked example where noted.

## By lifecycle stage

| # | Template | What it's for | Duty area | Tier / when | Standard | Worked example |
|---|---|---|---|---|---|---|
| 1 | `AI-Use-Case-Intake-Form.md` | Front-door request capture for any new AI use case | Intake | **All** — every request | RMF MAP | `Examples/01` |
| 2 | `Lightweight-Impact-Assessment.md` | Fast, proportionate screen with an escalation gate | Intake / Risk | **Minimal / Limited** only | ISO A.5 / 6.1.4 | — |
| 3 | `AI-Risk-Assessment.md` | Deep NIST RMF assessment; characteristic scoring (tier = highest single rating) | Risk | **High** (or any escalated case) | RMF MAP/MEASURE/MANAGE | `Examples/02` |
| 4 | `Vendor-AI-Assessment.md` | Third-party/SaaS AI risk review | Vendor | Any **buy/embedded** AI | RMF GOVERN · ISO A.10 | `Examples/03` |
| 5 | `Intake-Review-Decision-Record.md` | Authoritative decision + conditions + residual-risk acceptance | Intake | **All** decisions | RMF GOVERN | `Examples/04` |
| 6 | `AI-System-Inventory.csv` (+ `.md` field guide) | Living register of all AI systems + shadow-AI discovery | Monitoring | **Ongoing** (all approved systems) | RMF GOVERN · ISO A.3/A.4 | — |
| 7 | `Control-Monitoring-and-Reporting.md` | Program metrics, deployed-system monitoring, audit-evidence index | Monitoring / Reporting | **Ongoing** (periodic) | RMF MEASURE/MANAGE · ISO 9 | `Examples/05` |
| 8 | `AI-Incident-Response-Playbook.md` | AI-specific incident triage, containment, post-incident review | Monitoring / Manage | **On incident / near-miss** | RMF MANAGE · ISO 10 | (see `Examples/05` near-miss) |
| 9 | `Policy-Gap-Analysis-NIST-and-ISO42001.md` | Dual-standard maturity crosswalk & gap register | Policy | **Periodic** program review | RMF + ISO 42001 (full) | `Examples/06` |
| 10 | `Policy-Revision-Worksheet.md` | Controlled, traceable policy change | Policy | **On change** (gap / incident / reg / standard update) | RMF GOVERN · ISO 10 | — |

## Pick-by-question

- **A new request came in** → 1 (Intake Form), then triage.
- **It's clearly low-risk** → 2 (Lightweight Impact Assessment). *Any red flag → escalate to 3.*
- **It's high-risk / decides about people** → 3 (AI Risk Assessment).
- **It's a vendor/SaaS tool** → 4 (Vendor Assessment) alongside 2 or 3.
- **Time to record the decision** → 5 (Decision Record).
- **Need to log/track what we run** → 6 (AI System Inventory).
- **Quarterly metrics / board report / audit prep** → 7 (Control Monitoring & Reporting).
- **Something went wrong** → 8 (Incident Response Playbook).
- **Checking program against the standards** → 9 (Gap Analysis).
- **Changing a policy** → 10 (Policy Revision Worksheet).

## How they connect
```
Intake (1) → triage
   ├─ low tier → Lightweight Impact Assessment (2)
   └─ high tier → AI Risk Assessment (3)   [+ Vendor Assessment (4) if applicable]
            → Decision Record (5) → AI System Inventory (6)
                  → ongoing: Control Monitoring (7)
                  → on incident: Incident Response (8) → may feed → Policy Revision (10)
   Program-level, periodic: Gap Analysis (9) → Policy Revision (10)
```

> Gems in `../Gemini Gems/` produce drafts directly into these templates — each Gem's `knowledge-files.md` lists the matching template to upload. Single-shot prompts live in `../Prompts/`.
