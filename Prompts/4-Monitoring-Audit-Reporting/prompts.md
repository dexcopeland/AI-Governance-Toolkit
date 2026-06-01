# Prompts — Monitoring, Audit & Reporting

Copy any block into Gemini. Never let the model invent metrics — give it real numbers; it will flag gaps with `[NEEDS DATA]`.

---

## Draft an executive / board summary
```
You are an AI governance reporting assistant writing for a [board / executive committee]. Turn the inputs below into a one-page summary: headline (1 sentence), 3-5 key points (risk, progress, decisions needed), and explicit asks. Plain language, quantify where possible, no jargon. If any input is missing, insert [NEEDS DATA: …] rather than guessing.

Inputs (period [Qx YYYY]): [PASTE metrics, decisions, incidents, notable changes]
```

---

## Build a metrics narrative
```
Act as an AI governance analyst. Given this metrics table, write a short narrative that explains what the numbers mean and why the trends matter — not just restating them. Call out anomalies, overdue items, and what's being done about them. Then suggest 2-3 metrics we're not tracking but should.

Metrics: [PASTE TABLE: intake volume, tiers, decision times, approvals/rejections, overdue reviews, incidents, training completion, open gaps]
```

---

## Prepare audit evidence for a control
```
You are an audit-evidence preparer. For the control/requirement below, produce: (1) a plain-language statement of the control, (2) the types of evidence that demonstrate it operating, (3) where that evidence typically lives, (4) the NIST AI RMF function and/or ISO/IEC 42001 clause it maps to, (5) common gaps an auditor would probe. 

Control/requirement: [e.g., "Human oversight is applied before high-risk AI outputs are actioned" or "ISO 42001 Clause 9.2 internal audit"]
```

---

## Draft an AI incident report
```
You are an AI governance incident analyst. Draft an incident report from the facts below. Sections: What happened (timeline), Systems & data involved, Impact (who/what, severity), Root cause (or hypothesis), Immediate actions taken, Corrective & preventive actions (with owners), Lessons learned, Standards reference (NIST MANAGE / ISO 42001 Clause 10 improvement). Factual and non-blaming. Mark unknowns clearly.

Facts: [DESCRIBE what happened, when, systems, impact, response so far]
```

---

## Triage an AI incident & build a response plan
```
You are an AI incident response lead. Triage the incident below and produce an action plan. Steps:
1. Classify the AI incident TYPE (harmful/biased output, hallucination, prompt injection/jailbreak, data leakage/privacy, model/vendor degradation, loss of human oversight, shadow AI, IP/confidentiality, security compromise, safety).
2. Assign SEVERITY (SEV-1 Critical / SEV-2 High / SEV-3 Moderate / SEV-4 Low-near-miss) with reasoning.
3. List immediate CONTAINMENT actions (e.g., switch to human-only, disable feature, roll back model version, revoke keys, take offline).
4. State who to NOTIFY and any likely regulatory/contractual obligations to check.
5. List EVIDENCE to preserve before anything is changed.
6. Give the next 3 investigation questions to find root cause — both technical and "why didn't oversight catch it?"

Incident: [DESCRIBE what happened, the system & model/version, data & people involved, what's been done so far]
```

---

## Run an AI incident post-incident review
```
Act as an AI governance facilitator running a blameless post-incident review. From the facts below, produce: (1) a clear timeline, (2) technical root cause, (3) PROCESS root cause — why existing controls/oversight failed to prevent or catch it, (4) impact summary, (5) corrective actions (fix this incident) with owners, (6) preventive actions (stop recurrence: control, policy, training, or monitoring changes) with owners, (7) which policies or risk assessments should be updated as a result. Map lessons to NIST AI RMF MANAGE and ISO/IEC 42001 Clause 10 (improvement).

Incident facts & response taken: [PASTE]
```

---

## Summarize a period for stakeholders
```
Write a concise AI governance program update for [AUDIENCE]. Cover: what we reviewed this period, key decisions, current risk posture, open issues & overdue items, and what's next. Use a metrics table for the numbers and short prose for the narrative. Tone: transparent, including problems. Flag missing data as [NEEDS DATA].

Inputs: [PASTE]
```
