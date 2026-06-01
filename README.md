# AI Governance Toolkit

A working toolkit for an AI Governance Manager, built around **NIST AI RMF (AI 100-1)** and **ISO/IEC 42001:2023**. Everything here is generic best-practice and portable across organizations — no org-specific policy language baked in.

It contains three things:

| Folder | What it is | How you use it |
|---|---|---|
| **Prompts/** | Single-shot prompts | Copy/paste into a normal Gemini chat for a one-off task. |
| **Gemini Gems/** | Reusable AI assistants | Each folder holds a paste-ready *system instruction* + a *knowledge-files manifest*. Recreate the Gem once in Gemini, reuse forever. |
| **Templates/** | Fill-in documents | The artifacts you produce — intake forms, risk assessments, gap analyses, vendor reviews, reports. |
| **Examples/** | Worked, filled-in samples | A connected fictional scenario (intake → risk → vendor → decision) plus reporting & gap-analysis examples, showing the depth expected. |

---

## How the three pieces work together

A typical intake flows through all three:

```
New AI request
   │
   ├─ Templates/AI-Use-Case-Intake-Form.md      ← requester (or you) fills this in
   │
   ├─ Gem: AI Intake & Triage Analyst            ← classifies tier, flags review paths
   │     (or Prompts/1-Intake-and-Risk/*)
   │
   ├─ Low tier (Minimal/Limited)?
   │     → Templates/Lightweight-Impact-Assessment.md  ← fast, proportionate screen
   │
   ├─ High tier → Gem: AI Risk Assessor (NIST AI RMF) ← deep risk assessment
   │     → produces Templates/AI-Risk-Assessment.md
   │
   ├─ (if a vendor) Gem: Vendor & Third-Party AI Reviewer
   │     → produces Templates/Vendor-AI-Assessment.md
   │
   ├─ Templates/Intake-Review-Decision-Record.md  ← your decision + conditions
   │
   ├─ Templates/AI-System-Inventory.md            ← every approved system is logged here
   │
   └─ Gem: Governance Reporting & Audit Assistant ← exec summary, metrics, audit evidence
```

---

## Setting up a Gemini Gem (one time per Gem)

1. In Gemini, open **Gems → New Gem** (Gem manager).
2. Name it to match the folder (e.g., *AI Risk Assessor (NIST AI RMF)*).
3. Open the Gem's `system-instruction.md`, copy the whole thing, paste it into the Gem's **Instructions** field.
4. Open `knowledge-files.md` and upload the listed knowledge files (your policies, the NIST/ISO PDFs, your templates) to the Gem.
5. Save. Reuse it any time without re-pasting.

> **Tip:** Upload the matching file from `Templates/` as a knowledge file so the Gem produces output already in your template format.

---

## A note on tool choice & data handling

- Treat every prompt as if its contents may be retained by the model provider. **Do not paste regulated, confidential, or personal data** into a consumer Gemini surface unless your organization has an enterprise agreement that permits it. Use placeholders (`[SYSTEM NAME]`, `[VENDOR]`) and redact.
- AI output is a **first draft for a human governance professional**, never the decision itself. Every artifact here has a human sign-off line for that reason.

---

## Standards quick-reference

**NIST AI RMF — four functions**
- **GOVERN** — culture, policies, accountability, roles (cross-cutting).
- **MAP** — context, intended use, stakeholders, potential impacts.
- **MEASURE** — analyze, assess, benchmark, and monitor risks.
- **MANAGE** — prioritize, respond to, and recover from risks.

**NIST AI RMF — trustworthiness characteristics**
Valid & Reliable · Safe · Secure & Resilient · Accountable & Transparent · Explainable & Interpretable · Privacy-Enhanced · Fair (with Harmful Bias Managed).

**ISO/IEC 42001:2023 — management-system clauses**
4 Context · 5 Leadership · 6 Planning (incl. AI risk assessment, risk treatment, AI system impact assessment) · 7 Support · 8 Operation · 9 Performance evaluation · 10 Improvement.

**ISO/IEC 42001:2023 — Annex A control areas**
A.2 Policies · A.3 Internal organization · A.4 Resources · A.5 Impact assessment · A.6 AI system life cycle · A.7 Data for AI · A.8 Information for interested parties · A.9 Use of AI systems · A.10 Third-party & customer relationships.

---
*Generic best-practice toolkit. Not legal advice. Adapt to your jurisdiction and organizational policy before use.*
