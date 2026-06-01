# Prompts — Intake & Risk

Copy any block below into Gemini. Replace `[BRACKETED]` placeholders. **Don't paste regulated/confidential data** — describe it abstractly.

---

## Classify use-case risk tier
```
You are an AI governance triage analyst. Classify the risk tier of this AI use case as Minimal, Limited, High, or Prohibited, and justify it in 2 sentences. Then list which review paths are triggered (privacy/DPIA, security, legal, bias/fairness, vendor, accessibility, records).

Use case: [DESCRIBE: what it does, build/buy/vendor, generative or not, does it make/inform decisions about people, human-in-the-loop?, data types (PII/sensitive/confidential), who is affected, scale].

Tier definitions:
- Minimal: internal productivity, no personal data, no decisions about people, reversible.
- Limited: some personal/confidential data OR informs (not decides) outcomes; human reviews output.
- High: decisions materially affecting people; sensitive/regulated data; vulnerable groups; little/no human oversight; large scale.
- Prohibited: legally banned or against organizational red lines.

Output: Tier + justification + triggered review paths + the single biggest open question.
```

---

## Generate requester clarifying questions
```
Act as an AI governance reviewer. I received this AI use-case request but it's missing detail. Generate the 5 most important clarifying questions to send the requester so I can triage it — prioritized, plain-language, no jargon. After each question, note in brackets which risk dimension it resolves (e.g., [data sensitivity], [human oversight], [scale of impact]).

Request: [PASTE THE REQUEST]
```

---

## Identify applicable review paths
```
You are an AI governance coordinator. Given this use case, tell me which specialist reviews are required, which are recommended, and which are not needed — with a one-line reason each. Reviews to consider: Privacy/DPIA, Security, Legal/Regulatory, Bias & Fairness, Vendor/Third-Party, Accessibility, Records/Retention, Data Governance.

Use case: [DESCRIBE]
```

---

## Run a NIST AI RMF mini-assessment
```
Act as an AI risk analyst grounded in the NIST AI RMF. For this use case, give me a rapid first-pass assessment:
1. MAP: intended use, stakeholders, top 3 foreseeable failure/misuse modes.
2. MEASURE: for each of the 7 trustworthiness characteristics (Valid & Reliable, Safe, Secure & Resilient, Accountable & Transparent, Explainable & Interpretable, Privacy-Enhanced, Fair/bias-managed), name the single most material risk and rate it Low/Med/High. Write "N/A — [reason]" where it doesn't apply.
3. MANAGE: the top 3 mitigations I should require before approval.
Flag any assumption you had to make.

Use case: [DESCRIBE]
```

---

## Draft an intake decision memo
```
Draft a concise AI intake decision memo for leadership based on the inputs below. Sections: Summary (3 sentences), Risk tier & key risks, Decision (Approve / Approve with conditions / Reject), Conditions before go-live, Residual risk & who accepts it, Next review date. Neutral, professional tone, under one page.

Inputs:
- Use case: [DESCRIBE]
- Risk tier: [TIER]
- Key risks identified: [LIST]
- Proposed mitigations: [LIST]
- Recommended decision: [Approve/Conditions/Reject]
```
