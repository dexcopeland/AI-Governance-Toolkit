# Getting Started

A practical walkthrough for using this toolkit day-to-day. If you read nothing else, read the **5-minute quick start** and the **intake walkthrough**.

---

## What this toolkit is
Three reusable assets that work together:
- **Prompts** — copy/paste into a Gemini chat for one-off tasks.
- **Gemini Gems** — saved AI assistants you build once and reuse (each is a system instruction + knowledge files).
- **Templates** — the documents you actually produce and keep as records.

Plus **Examples/** (worked samples) and this guide. Everything aligns to **NIST AI RMF** and **ISO/IEC 42001** — see `README.md` for the standards quick-reference.

---

## 5-minute quick start
1. Open `Templates/README.md` — that's your map to all 10 templates ("pick-by-question" section).
2. Open `Templates/AI-System-Inventory.csv` in Excel or Google Sheets. **Delete the two EXAMPLE rows.** This is now your live inventory.
3. Skim one worked example end-to-end: `Examples/01` → `02` → `03` → `04` (the TalentSift scenario). This shows the depth expected.
4. Build your first Gem (next section).

---

## Build your first Gem (one time, ~5 min)
Start with the **AI Intake & Triage Analyst** — it's the front door.
1. In Gemini: **Gems → New Gem**.
2. Name it `AI Intake & Triage Analyst`.
3. Open `Gemini Gems/AI-Intake-Triage-Analyst/system-instruction.md`, copy everything below the divider, paste into the Gem's **Instructions**.
4. Open the matching `knowledge-files.md` and upload the listed files (at minimum your intake form + your AI policy).
5. Save. Repeat later for the other four Gems as you need them.

> Don't have an AI policy yet? The Gem still works using its built-in tier definitions — just upload your policy later when it exists.

---

## The intake workflow (the core loop)
A new AI request lands. Here's the path:

1. **Capture it** → requester fills `Templates/AI-Use-Case-Intake-Form.md` (paste it to them, or fill it together).
2. **Triage it** → run it through the *Intake & Triage Analyst* Gem (or `Prompts/1-Intake-and-Risk/`). You get a provisional tier + which reviews are needed.
3. **Assess it — proportionate to tier:**
   - **Minimal / Limited** → `Templates/Lightweight-Impact-Assessment.md` (fast). *If any red flag trips → escalate.*
   - **High** → *AI Risk Assessor* Gem → `Templates/AI-Risk-Assessment.md` (deep).
   - **Vendor/SaaS involved?** → also run *Vendor & Third-Party AI Reviewer* → `Templates/Vendor-AI-Assessment.md`.
4. **Decide it** → record the outcome + conditions in `Templates/Intake-Review-Decision-Record.md`. The accountable owner signs off on residual risk.
5. **Log it** → add the approved system to `Templates/AI-System-Inventory.csv`.
6. **Watch it** → track metrics in `Templates/Control-Monitoring-and-Reporting.md`; review on the system's next-review date.

If something goes wrong later → `Templates/AI-Incident-Response-Playbook.md`. Lessons feed `Templates/Policy-Revision-Worksheet.md`.

---

## Program-level work (not tied to one request)
- **Quarterly health check** → `Policy-Gap-Analysis-NIST-and-ISO42001.md` to score maturity against both standards (see `Examples/06`).
- **Board / exec reporting** → *Governance Reporting & Audit Assistant* Gem + `Control-Monitoring-and-Reporting.md` (see `Examples/05`).
- **Policy change** → `Policy-Revision-Worksheet.md` keeps it traceable to a driver.

---

## A maintenance rhythm that works
| Cadence | Do this |
|---|---|
| **Per request** | Intake → triage → assess → decide → log to inventory |
| **Monthly** | Reconcile inventory; check overdue reviews & open conditions |
| **Quarterly** | Metrics report; adverse-impact checks on high-risk systems; shadow-AI discovery sweep |
| **Quarterly/Semi-annual** | Gap analysis; review the AI policy |
| **On event** | Incident response; re-assess on any model/vendor/scope change |

---

## ⚠️ Data-handling rule (read once, remember always)
Treat anything you paste into a consumer Gemini surface as potentially retained. **Don't paste regulated, confidential, or personal data** unless your org has an enterprise agreement that permits it. Use placeholders (`[SYSTEM]`, `[VENDOR]`) and describe data abstractly. AI output is always a **draft for a human** — every template has a sign-off line for that reason.

---

## Make the inventory spreadsheet nicer (optional)
The CSV opens in Excel/Google Sheets as-is. To level it up:
- **Freeze the header row** (View → Freeze).
- **Add dropdowns** (Data → Data validation) for: Risk Tier (Minimal/Limited/High/Prohibited), Status (Proposed/Approved/In production/Discovered/Suspended/Retired/Rejected), Data Sensitivity (Public/Internal/Confidential/Regulated-PII).
- **Conditional formatting** on Risk Tier (red = High) and Next Review (red if past due).
- Column definitions & status meanings live in `Templates/AI-System-Inventory.md` (the field guide).

---

## FAQ
**Where do I start each day?** `Templates/README.md` → pick-by-question.
**Which assessment — light or full?** Tier decides. Limited/Minimal → lightweight; High or any red flag → full.
**Can I change the risk-scoring model?** Yes — but update both `AI-Risk-Assessment.md` and the Risk Assessor Gem so they stay consistent.
**No policy yet?** The toolkit works without one; the gap analysis will help you build toward it.
