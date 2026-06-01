# Prompts — Policy & Standards Alignment

Copy any block into Gemini. These align to **NIST AI RMF** and **ISO/IEC 42001:2023**. Note: aligning as best-practice, not seeking certification.

---

## Map a policy to NIST AI RMF + ISO 42001
```
You are an AI governance policy expert. Map the policy text below to (a) NIST AI RMF functions (GOVERN/MAP/MEASURE/MANAGE) and trustworthiness characteristics, and (b) ISO/IEC 42001 clauses (4-10) and Annex A control areas (A.2-A.10). Produce a table: Policy provision | NIST mapping | ISO 42001 mapping. Then list what important standard outcomes are NOT addressed by this policy.

Policy text: [PASTE]
```

---

## Gap analysis against both standards
```
Act as an AI management-system auditor (advisory, not certification). Assess how well the material below covers NIST AI RMF and ISO/IEC 42001. For each standard area, score maturity 0-4 (0 Absent, 1 Ad hoc, 2 Defined, 3 Managed, 4 Optimized), cite the evidence, and state the gap. End with a prioritized gap register (gap | standard ref | severity H/M/L | recommended action | quick-win?).

Cover NIST: GOVERN, MAP, MEASURE, MANAGE.
Cover ISO 42001 clauses 4-10 and Annex A areas A.2-A.10.

Material: [PASTE POLICIES / PROGRAM DESCRIPTION]
```

---

## Draft or revise policy language
```
You are an AI governance policy writer. Draft policy language for: [TOPIC, e.g., "acceptable use of generative AI by staff" / "human oversight requirements for high-risk AI"].

Requirements:
- Clear, enforceable, auditable. Use "must/shall" for requirements; define key terms.
- Each requirement states who, what, the trigger, and how compliance is evidenced.
- Assign roles/responsibilities.
- Add a short crosswalk noting which NIST function(s) and ISO 42001 clause/Annex A control each section supports.
- Flag anything that needs legal review.

Context: [ORG TYPE, EXISTING POLICIES, CONSTRAINTS]
```

---

## Stress-test existing policy
```
Critique this AI policy as a skeptical reviewer. Identify: (1) vague or unenforceable statements, (2) ambiguity that could be read two ways, (3) missing edge cases or scenarios, (4) conflicts with typical privacy/security/records policies, (5) requirements with no way to verify compliance. For each issue, propose a specific fix.

Policy: [PASTE]
```

---

## Turn a standard into a requirements checklist
```
Convert the following standard/section into a practical, auditable checklist for our AI program. For each item: the requirement in plain language, what evidence would demonstrate it, and a suggested owner role.

Standard/section: [e.g., "ISO/IEC 42001 Annex A.6 — AI system life cycle" or "NIST AI RMF MEASURE function"]
```
