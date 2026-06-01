# AI System Inventory

> The living register of every AI system/use case in the organization — your single source of truth. Maps to NIST AI RMF **GOVERN** (maintain an inventory) and ISO/IEC 42001 **A.3 / A.4** (internal organization & resources). An inventory you can't trust undermines every other control, so keep it current.
>
> 📊 **Working copy:** `AI-System-Inventory.csv` — open in Excel or Google Sheets and maintain it there. **This markdown file is the field guide**: column definitions, status meanings, and discovery sources.

---

## Keeping it current (discovery sources)
An inventory built only from voluntary intake will miss **shadow AI**. Reconcile it against multiple sources:
- ☐ **Intake pipeline** — every approved use case auto-adds a row.
- ☐ **Procurement / finance** — flag any purchase of AI-labeled tools or "AI add-on" SKUs.
- ☐ **Periodic survey** — ask each team annually: "What AI tools do you use, and with what data?"
- ☐ **Network / SaaS discovery** — IT reports on AI domains/apps in use (e.g., known GenAI services).
- ☐ **Existing-tool features** — AI features switched on inside tools you already own (often missed).

> Newly discovered systems are added with status **Discovered** and routed retroactively through intake.

---

## Master inventory (one row per system)
| ID | System / use case | Purpose (short) | Business owner | Build/Buy/Embed | Vendor | Model | Gen? | Decisions re people? | Data sensitivity | Risk tier | Intake/Assessment ref | Status | Last reviewed | Next review |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| AI-001 | | | | | | | Y/N | Y/N | Pub/Int/Conf/PII | Min/Lim/High | | | | |
| AI-002 | | | | | | | | | | | | | | |

*(Tip: maintain the master in a spreadsheet/database for filtering & sorting; use the record block below for detail and for systems that need a fuller entry.)*

---

## Detailed system record (per high/limited-tier system)
| Field | Value |
|---|---|
| Inventory ID | |
| System / use case name | |
| Description & business purpose | |
| Business owner (accountable) | |
| Technical owner / admin | |
| Build / Buy / Embedded feature | |
| Vendor (if any) | |
| Underlying model(s) & version | |
| Generative AI? | ☐ Yes ☐ No |
| Makes or informs decisions about people? | ☐ Yes ☐ No |
| Data types & sensitivity | |
| Data residency / processing location | |
| Risk tier | ☐ Minimal ☐ Limited ☐ High ☐ Prohibited |
| Linked artifacts | Intake: __ · Risk/Impact assessment: __ · Vendor assessment: __ · Decision record: __ |
| Human oversight model | ☐ In-the-loop ☐ On-the-loop ☐ Out-of-the-loop |
| Status | (see definitions below) |
| Conditions of approval (if any) | |
| Date added | |
| Last reviewed / Next review due | |
| Notes | |

## Status definitions
| Status | Meaning |
|---|---|
| **Proposed** | In intake, not yet decided |
| **Approved** | Cleared, not yet live |
| **In production** | Live and in use |
| **Discovered** | Found via discovery; pending retroactive intake |
| **Suspended** | Temporarily disabled (e.g., during an incident) |
| **Retired** | Decommissioned (keep the record for audit history) |
| **Rejected** | Not approved for use |

## Maintenance
- **Owner of this inventory:** ____________
- **Reconciliation cadence:** ☐ Quarterly ☐ Semi-annual
- **Per-system review:** driven by each system's *Next review due* date.
- Roll-up counts (by tier / status) feed `Control-Monitoring-and-Reporting.md`.

---
*Inventory owner sign-off:* ____________ *Date:* __________
