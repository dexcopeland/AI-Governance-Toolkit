# Prompts — Vendor & Third-Party AI

Copy any block into Gemini. Don't upload NDA materials to a consumer surface unless permitted.

---

## Review a model / system card
```
You are an AI vendor risk reviewer. Analyze this model/system card. Extract and assess: stated intended use & out-of-scope uses, training-data disclosure & limitations, evaluation/benchmark results, known risks/biases, version & deprecation policy. Flag anything missing that I should request. Rate transparency Low/Med/High with reasons. Separate vendor claims (mark "unverified") from independently evidenced facts.

Model/system card: [PASTE OR DESCRIBE]
```

---

## Assess data protection & privacy posture
```
Act as a privacy-focused AI vendor reviewer. Based on the vendor materials below, answer: Is our input data used to train their models (and can we opt out)? Data retention & deletion terms? Processing locations/residency? Sub-processors disclosed? Is a DPA in place? Rate data & privacy risk Low/Med/High and list the exact follow-up questions to send the vendor for anything unclear.

Vendor materials: [PASTE / DESCRIBE]
```

---

## Generate a vendor due-diligence questionnaire
```
Generate an AI vendor due-diligence questionnaire for a [DESCRIBE PRODUCT, e.g., "generative AI writing assistant that will process internal confidential documents"]. Group questions under: Transparency, Data & Privacy, Security & Resilience, Responsible AI, and Contractual. Keep it to the ~20 highest-value questions, phrased so a yes/no or short answer is auditable.
```

---

## Draft a vendor risk write-up
```
You are an AI vendor risk reviewer. Produce a structured risk write-up from the inputs below. Sections: 5 domain ratings (Transparency, Data & Privacy, Security & Resilience, Responsible AI, Contractual) each Low/Med/High with evidence; overall vendor risk; recommendation (Approve / Approve with conditions / Reject / Needs more info); required contractual or technical controls; outstanding questions for the vendor. Mark unverified vendor claims as such.

Inputs:
- Vendor & product: [NAME]
- What we'll use it for & data involved: [DESCRIBE]
- What the vendor provided: [model card / SOC 2 / DPA / terms / nothing — DESCRIBE]
- Known concerns: [LIST]
```

---

## Compare two vendors
```
Compare these two AI vendors for governance risk across Transparency, Data & Privacy, Security, Responsible AI, and Contractual terms. Give a side-by-side table with Low/Med/High per domain, then a recommendation noting the key differentiators and what additional evidence would change the call.

Vendor A: [DESCRIBE]
Vendor B: [DESCRIBE]
```
