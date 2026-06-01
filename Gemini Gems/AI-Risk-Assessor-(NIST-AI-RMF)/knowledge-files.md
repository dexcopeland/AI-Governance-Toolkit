# Knowledge files — AI Risk Assessor (NIST AI RMF)

| File | Why | Priority |
|---|---|---|
| `Templates/AI-Risk-Assessment.md` | So output lands in your exact assessment structure & rubric | **Required** |
| `NIST.AI.100-1.pdf` (NIST AI RMF core) | Authoritative grounding for functions & trustworthiness characteristics | **Required** |
| NIST AI RMF **Playbook** (if you have it) | Suggested actions per subcategory → richer mitigations | Recommended |
| Your org's **AI policy & risk appetite statement** | Calibrates what "acceptable residual risk" means | Recommended |
| Completed sample assessment (a good past one) | Few-shot example of the depth/tone you want | Recommended |
| Sector/regulatory guidance relevant to you | Sharpens legal/compliance risk calls | Optional |

## Notes
- This Gem uses **NIST trustworthiness-characteristic scoring**: rate each of the 7 characteristics Low/Med/High/Critical, and the overall tier = the highest single rating. If you change the scoring model, update **both** this Gem's instruction and the template, then re-upload — keep them consistent.
- The NIST RMF PDF you already have (`Regs and Frameworks/NIST.AI.100-1.pdf`) is the primary source; point the upload there.
