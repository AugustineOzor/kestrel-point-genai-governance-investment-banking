# 03 · Maturity Assessment and Lessons Learned

| Field | Value |
|---|---|
| Assessed | October 2026 |
| Method | Self-assessment by AI Governance, challenged by Compliance Monitoring |
| Scale | 1 Initial · 2 Developing · 3 Defined · 4 Managed · 5 Optimised |

## 1. Maturity by NIST AI RMF function

| Function | Feb 2026 | Oct 2026 | Target Q4 2027 | Evidence | Gap to target |
|---|---|---|---|---|---|
| **GOVERN** | 1 | **3** | 4 | Charter, AIGC, policies, SM&CR allocation, training | Metrics-driven policy review; Internal Audit assurance |
| **MAP** | 1 | **3** | 4 | Inventory, tiering, impact assessments for Tier 1 | Impact assessments for all Tier 2 use cases |
| **MEASURE** | 1 | **2** | 4 | 8 key controls tested, recall testing, model validation | Automated quality metrics; validation of vendor models; red team cycle |
| **MANAGE** | 1 | **3** | 4 | Risk register, remediation tracking, incident playbook, KRIs | Close findings; prove incident process in a live Sev-1 or full simulation |

## 2. ISO/IEC 42001 readiness snapshot

| Clause | Status |
|---|---|
| 4 Context of the organisation | ✔ Scope and interested parties defined in charter |
| 5 Leadership and AI policy | ✔ Charter and Acceptable Use Policy approved |
| 6 Planning (risk assessment, impact assessment, objectives) | ✔ Methodologies approved; AI objectives to be set formally |
| 7 Support (competence, awareness, documentation) | ⚠ Training at 94%; document control in place |
| 8 Operation | ✔ Intake, impact assessments, vendor reviews operating |
| 9 Performance evaluation | ⚠ Control testing done; internal audit and management review not yet run |
| 10 Improvement | ⚠ Findings tracked; corrective action process to be formalised |

## 3. Lessons learned

1. **Banning AI did not work; giving people a better tool did.** Blocked public AI attempts fell 67% from Q2 to Q3 once Kestrel Assist launched, not when the block was switched on.
2. **Copilot's biggest risk is the firm's own permissions.** The only Sev-2 incident came from a SharePoint site shared with 450 people. Fixing permissions is a precondition for embedded AI, not a follow-up.
3. **Prompts are controls.** Several prompts from the industry guide asked for persuasive tone, scraped data or final compliance verdicts. Reviewing them removed risk before any output was produced.
4. **Measure what the AI misses, not just what it gets wrong.** Recall testing in due diligence found the weakness on MFN clauses that precision testing would never have shown.
5. **Vendors that will not explain their models cannot feed decisions.** SignalCurrent shows that third-party AI needs the same model risk evidence as in-house AI.
6. **Sign-off needs a second person.** Self-review was the most common control exception. Building the second sign-off into the tool works better than reminding people.

<!-- nav -->
---

[← Remediation Roadmap](02-remediation-roadmap.md) · [Home](../README.md)
<!-- /nav -->
