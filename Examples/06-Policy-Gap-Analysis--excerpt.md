# Policy Gap Analysis (excerpt) — WORKED EXAMPLE (fictional)

> Reference only. Demonstrates `Templates/Policy-Gap-Analysis-NIST-and-ISO42001.md`. Shows a few rows filled to illustrate the depth of evidence and gaps expected. **Illustrative.**

| Field | Value |
|---|---|
| Program / policy under review | AI Acceptable Use Policy v1.2 + intake process |
| Reviewer | A. Rivera | 
| Date | 2026-04-30 |

## Maturity scale
0 Absent · 1 Ad hoc · 2 Defined · 3 Managed · 4 Optimized

## NIST AI RMF (excerpt)
| Function | Outcome | Maturity | Evidence | Gap / action |
|---|---|---|---|---|
| GOVERN | AI policy, roles, risk tolerance | **3** | Policy v1.2 approved; RACI exists; risk tiers defined | Risk-tolerance statement is qualitative only → quantify thresholds |
| GOVERN | Inventory of AI systems | **2** | Spreadsheet inventory exists | Not reconciled to procurement; shadow AI likely → adopt `Templates/AI-System-Inventory.md` with its discovery sources |
| MEASURE | Ongoing monitoring of deployed systems | **1** | Some teams self-report | No standard metrics or cadence → define monitoring template (done: see Control-Monitoring template) |
| MANAGE | Incident response for AI | **1** | General IT IR plan exists | No AI-specific playbook (bias, hallucination, injection) → addressed: `Templates/AI-Incident-Response-Playbook.md` |

## ISO/IEC 42001 (excerpt)
| Area | Intent | Maturity | Evidence | Gap / action |
|---|---|---|---|---|
| Clause 6 — Planning | AI risk assessment, treatment, **impact assessment** | **2** | Risk assessment template in use | Impact-on-individuals assessment not consistently done → make it mandatory for High tier |
| A.5 — Impact assessment | Assess impacts on individuals & society | **2** | Covered for High-risk only | Addressed: `Templates/Lightweight-Impact-Assessment.md` extends a proportionate check to Min/Limited tier |
| A.7 — Data for AI | Data quality/provenance governed | **1** | Privacy review covers PII | No data-provenance/quality checks for training data → add to vendor & build checklists |
| A.10 — Third-party | Supplier AI responsibilities allocated | **3** | Vendor assessment + DPA process | Strong; formalize re-assessment triggers in contract templates |

## Gap register (roll-up, excerpt)
| # | Gap | Standard ref | Severity | Action | Owner | Target |
|---|---|---|---|---|---|---|
| 1 | No AI-specific incident playbook | NIST MANAGE; ISO 10 | High | ✓ Drafted (`Templates/AI-Incident-Response-Playbook.md`); socialize & test | AI Gov + Security | Q3 |
| 2 | Inventory misses shadow AI | NIST GOVERN; ISO A.3 | High | Roll out `AI-System-Inventory.md`; discovery via procurement + survey | AI Gov | Q3 |
| 3 | No standard deployed-system monitoring | NIST MEASURE; ISO 9 | Med | Roll out monitoring template | AI Gov | Q3 |
| 4 | Risk tolerance qualitative | NIST GOVERN | Med | Define quantitative thresholds | AI Gov + Risk | Q4 |

## Summary
- **Overall maturity:** ~2 (Defined), strong on GOVERN/third-party, weak on MEASURE/MANAGE operations.
- **Top 3 priority gaps:** AI incident playbook, shadow-AI discovery, deployed-system monitoring.
- **Quick wins (≤30 days):** publish monitoring template; add mandatory impact check for High tier.
