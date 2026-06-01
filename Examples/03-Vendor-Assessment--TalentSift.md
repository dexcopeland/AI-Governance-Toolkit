# Vendor / Third-Party AI Assessment — WORKED EXAMPLE (fictional)

> Reference only. Demonstrates `Templates/Vendor-AI-Assessment.md`.

| Field | Value |
|---|---|
| Vendor | TalentSift Inc. |
| Product / service | TalentSift resume screening & shortlisting (SaaS) |
| Model(s) underneath | Vendor "proprietary + fine-tuned open model"; base undisclosed |
| Assessment date | 2026-05-18 |
| Reviewer | A. Rivera, AI Governance |
| Data sensitivity involved | ☒ Regulated/PII (applicant resumes) |

## 1. Vendor & model transparency
| Question | Answer | Risk |
|---|---|---|
| Model/system card? | Partial marketing one-pager; no full system card | Med |
| Training-data sources disclosed? | No — "proprietary"; sources & demographics unknown | High |
| Accuracy / eval results? | Vendor-stated 92% "recruiter agreement" *(unverified, not on our data)* | Med |
| Intended & out-of-scope uses stated? | Intended use yes; out-of-scope guidance thin | Med |
| Version & deprecation policy? | 30-day notice of model updates *(vendor-stated)* | Low |

## 2. Data protection & privacy
| Question | Answer | Risk |
|---|---|---|
| Our data used to train their models? | Default yes; **opt-out available by contract** | High → Med (if contracted out) |
| Retention & deletion? | Default 24 months; deletion-on-request supported | Med (push to 12 mo) |
| Processing locations? | US-only available on enterprise tier | Low (if enterprise) |
| Sub-processors disclosed? | Yes, list provided | Low |
| DPA in place? | ☒ Available, not yet signed | Pending |

## 3. Security & resilience
| Question | Answer | Risk |
|---|---|---|
| Certifications? | SOC 2 Type II (current); no ISO 27001/42001 | Low–Med |
| Pen-test program? | Annual third-party pen test *(attestation provided)* | Low |
| Prompt-injection / abuse safeguards? | "Input sanitization" claimed *(unverified)* | Med |
| Incident notification SLA? | 72-hour notification in contract | Low |
| Uptime commitment? | 99.5% SLA | Low |

## 4. Responsible AI & compliance
| Question | Answer | Risk |
|---|---|---|
| Bias / fairness testing? | Internal testing only; not on our population; methodology not shared | High |
| Content safety / guardrails configurable? | Limited configurability | Med |
| Human oversight & override? | Yes — shortlist is advisory, recruiter overrides | Low |
| Explainability features? | "Top factors" shown per candidate; shallow | Med |
| Regulatory posture? | Aware of employment-AI laws; compliance is *customer's* responsibility per terms | Med |
| Indemnification for outputs? | Limited; caps liability | Med |

## 5. Risk summary
| Domain | Rating | Key concerns |
|---|---|---|
| Transparency | High | Opaque training data; partial documentation |
| Data & privacy | Med | Fixable via DPA: no-training + 12-mo retention + US-only |
| Security | Low–Med | SOC 2 good; injection safeguards unverified |
| Responsible AI | High | Bias testing not on our data; shallow explainability |
| Contractual | Med | Liability caps; compliance pushed to us |

**Overall vendor risk:** ☒ High (driven by transparency + bias evidence gaps)

## 6. Recommendation
☒ Approve with conditions

**Required controls:** sign DPA (no-training, 12-mo retention, US-only, deletion-on-request); obtain bias-testing methodology + agree to our independent adverse-impact testing; written confirmation of injection safeguards; capture employment-law compliance as our responsibility in the risk assessment.

**Outstanding questions to vendor:** What base model & version? Demographic representativeness of training data? Can you share third-party bias-audit results? Will you support per-field input control (exclude name/school)?

---
*Reviewer sign-off:* A. Rivera *Date:* 2026-05-18
*Re-assessment due:* on model version change or annually
