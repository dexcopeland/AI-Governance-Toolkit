# AI Incident Response Playbook

> AI-specific incident response — the failure modes a generic IT/security IR plan misses (biased output, hallucination, prompt injection, data leakage via prompts, model degradation, loss of human oversight). Maps to NIST AI RMF **MANAGE** (respond & recover) and ISO/IEC 42001 **Clause 10 (improvement / nonconformity & corrective action)**.
>
> **Use this as an addendum to — not a replacement for — your existing security incident response plan.** A confirmed data breach or system compromise also triggers that plan.

---

## ⏱️ First 30 minutes (quick reference)
1. **Don't delete anything.** Preserve prompts, outputs, logs, and the model/version in use (see Evidence checklist).
2. **Identify the AI system, owner, and what it touches** (people, data, decisions).
3. **Assess immediate harm** — is a person being harmed *right now* (wrong decision, exposed data, unsafe output)?
4. **Contain** — if harm is active, switch the system to human-only, disable the feature, or take it offline (see Containment options).
5. **Assign an Incident Lead** and open an incident record.
6. **Classify severity** (table below) — this sets who's notified and how fast.

---

## 1. Scope — what counts as an AI incident
Any event where an AI system causes, or risks causing, harm or a control failure — whether or not data/security is involved. Includes near-misses (treat seriously; they're free lessons).

## 2. AI incident taxonomy & first response
| Type | Example | AI-specific first response |
|---|---|---|
| **Harmful / biased output** | Screening tool disadvantages a protected group; offensive generated content | Pause affected decisions; preserve inputs/outputs; pull affected population sample for adverse-impact check |
| **Hallucination / factual error** | AI gave a customer wrong policy/legal/medical info acted upon | Correct the affected record/person; identify scope of others affected; add disclaimer/human check |
| **Prompt injection / jailbreak** | Hidden instruction in input made the system bypass rules or exfiltrate data | Treat as security event too; capture the malicious input; restrict input sources; check what was exposed/done |
| **Data leakage (privacy)** | PII/confidential data appeared in an output, log, or was sent to a vendor/training | Trigger privacy/breach process; identify data + individuals; stop further exposure (disable logging/training) |
| **Model / vendor degradation or outage** | Quality silently dropped after a vendor model update; service down | Roll back to prior model version if possible; switch to fallback/manual; notify vendor; invoke SLA |
| **Loss of human oversight / automation failure** | System acted autonomously where review was required | Halt automated action; revert to manual; audit decisions made without oversight |
| **Unauthorized / shadow AI** | Staff used an unapproved tool with confidential data | Stop usage; assess data exposed; route to intake retroactively |
| **IP / confidentiality exposure** | Confidential input used to train a vendor model; output infringes IP | Legal engaged; invoke contract terms; assess remediation |
| **Security compromise** | Model theft, data poisoning, credential/API-key leak | Full security IR plan; rotate keys; preserve forensic evidence |
| **Safety / physical harm** | AI in a physical or safety-critical process caused/risked harm | Stop the system immediately; safety team + escalation; preserve everything |

## 3. Severity classification
| Severity | Criteria | Target response | Notify |
|---|---|---|---|
| **SEV-1 Critical** | Active harm to people, confirmed data breach, safety event, or unlawful outcome at scale | Immediate (≤1 hr) | Exec/committee, Legal, Privacy, Security, CISO |
| **SEV-2 High** | Material harm likely, limited data exposure, high-risk system affected | Same business day | AI Gov lead, business owner, relevant specialists |
| **SEV-3 Moderate** | Contained issue, low/no individual harm, single system | ≤2 business days | AI Gov, system owner |
| **SEV-4 Low / Near-miss** | No harm occurred; caught before impact | Log & review | AI Gov |

## 4. Roles & responsibilities
| Role | Responsibility |
|---|---|
| **Incident Lead** | Coordinates response, owns the timeline & decisions |
| **AI Governance** | Classifies, ensures process followed, owns post-incident review |
| **System / business owner** | Operational facts, authorizes containment, accepts residual risk |
| **Security** | Compromise/injection/forensics |
| **Privacy / DPO** | Data exposure, breach notification obligations |
| **Legal** | Regulatory/contractual/liability, disclosure decisions |
| **Comms** | Internal/external messaging (if needed) |
| **Vendor contact** | For third-party AI: invoke notification SLA, get fixes |

## 5. Response lifecycle (checklist)
- ☐ **Detect & report** — how was it found? logged with timestamp.
- ☐ **Triage** — type, severity, systems, data, people affected.
- ☐ **Contain** — stop ongoing harm (see options below).
- ☐ **Investigate** — root cause (technical + process); what failed and why oversight didn't catch it.
- ☐ **Remediate / eradicate** — fix the cause; correct affected records/people.
- ☐ **Recover** — restore safe operation; verify the fix; decide on re-enabling.
- ☐ **Notify** — affected individuals, regulators, vendor, leadership as required.
- ☐ **Post-incident review** — lessons, corrective & preventive actions.

### Containment options (AI-specific)
- Switch system to **human-only / manual** mode.
- **Disable the AI feature** while keeping the rest of the product running.
- **Roll back** to a prior, known-good model version.
- **Revoke API keys / access**; block the malicious input source.
- **Kill switch** / take offline (for SEV-1 or safety).
- **Quarantine** affected outputs/decisions pending review.

## 6. Notification & regulatory considerations
- Personal-data exposure → privacy breach assessment & statutory notification clocks (jurisdiction-dependent).
- Decisions about people → consider duty to inform/remediate affected individuals.
- Third-party AI → vendor contractual notification obligations both ways.
- **Don't over- or under-disclose** — Legal decides external messaging.

## 7. Evidence to preserve (don't delete!)
- The exact **prompt(s)/input(s)** and **output(s)** involved.
- **Model name + version**, configuration/settings, and timestamps.
- **System & access logs**, user/session involved.
- Decisions/actions taken as a result.
- Screenshots and the affected records.
- Who did what, when (response timeline).

## 8. Post-incident review
| Item | Notes |
|---|---|
| What happened (timeline) | |
| Root cause (technical) | |
| Root cause (process — why didn't oversight/controls catch it?) | |
| Impact (people, data, decisions, reputation) | |
| What worked / what didn't in the response | |
| Corrective actions (fix this incident) | owner + due |
| Preventive actions (stop recurrence — control/policy/training changes) | owner + due |
| Policy/standard updates needed → log in `Policy-Revision-Worksheet.md` | |
| Risk assessment to update? → re-open `AI-Risk-Assessment.md` for the system | |

---

## Incident log / register
| ID | Date | System | Type | Severity | Status | Owner | Corrective action ref |
|---|---|---|---|---|---|---|---|
| INC-2026-001 | | | | | ☐Open ☐Closed | | |

---
### Sign-off
**Incident Lead:** ____________ **Date:** ______
**AI Governance review:** ____________ **Date:** ______

> 📄 The fictional incident in `Examples/05-Executive-Summary--Quarterly.md` (prompt-injection near-miss) is the kind of SEV-4 entry this log captures.
