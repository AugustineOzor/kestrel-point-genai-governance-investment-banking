# 01 · AI Risk Assessment Methodology

| Field | Value |
|---|---|
| Document ID | KPC-AIG-MTH-002 |
| Version | 1.0 |
| Aligned to | NIST AI RMF (Map, Measure), NIST AI 600-1, ISO/IEC 42001 clause 6.1, ISO/IEC 23894 |
| Approved by | AI Governance Committee, 14 April 2026 |

## 1. Approach

AI risks are assessed on the same 5x5 scale as the firm's enterprise risk framework, so they can be compared with other risks in Board reporting.

1. **Identify** risks per use case using the NIST AI 600-1 GenAI risk list, OWASP LLM Top 10, regulatory obligations and workshops.
2. **Rate inherent risk:** likelihood x impact with no AI-specific controls.
3. **Map controls** from the [control library](../04-controls/01-control-library.md).
4. **Rate residual risk** after controls, using control test results where available.
5. **Treat:** compare with appetite, then reduce, accept, transfer or avoid.

## 2. Likelihood

| Score | Rating | Guide |
|---|---|---|
| 1 | Rare | Not expected in the next 3 years |
| 2 | Unlikely | Could happen once in 3 years |
| 3 | Possible | Could happen once a year |
| 4 | Likely | Expected several times a year |
| 5 | Almost certain | Expected monthly or more |

## 3. Impact

The highest applicable column sets the score.

| Score | Rating | Financial | Regulatory | Client and reputation | Operational |
|---|---|---|---|---|---|
| 1 | Minimal | < £50k | No regulatory interest | No client impact | < 4 hours disruption |
| 2 | Minor | £50k–£250k | Query from a regulator | One client complaint | One team for a day |
| 3 | Moderate | £250k–£1m | Formal regulatory enquiry | Client relationship damaged | One deal delayed |
| 4 | Major | £1m–£10m | Enforcement investigation | Loss of a mandate, trade press coverage | Several deals delayed |
| 5 | Severe | > £10m | Fine, restriction or individual enforcement under SM&CR | Loss of multiple clients, national press | Firm-wide disruption |

## 4. Risk rating

**Score = Likelihood x Impact**

| Score | Rating | Action |
|---|---|---|
| 17–25 | **Critical** | Stop or restrict the activity. Board Risk Committee informed |
| 10–16 | **High** | Outside appetite. Remediation plan approved by the AIGC, or CRO acceptance with a review date |
| 5–9 | **Medium** | Within appetite with monitoring. Owner reviews quarterly |
| 1–4 | **Low** | Within appetite. Annual review |

## 5. Control effectiveness

Residual likelihood and impact are only reduced for controls that are designed and in operation. Where a control was tested, the result limits the credit given:

| Test result | Credit allowed |
|---|---|
| Effective | Full reduction |
| Partially effective | Half the reduction, rounded down. Finding raised |
| Ineffective | No reduction. Finding raised |
| Not yet tested | Reduction based on design review only, flagged in the register |

## 6. GenAI risk categories used

From NIST AI 600-1, adapted for investment banking:

| Category | Example at Kestrel |
|---|---|
| Confabulation | Invented EBITDA figure in a CIM |
| Data privacy | Personal data of executives in outreach profiling |
| Information security | Prompt injection in a VDR document |
| Information integrity | Misleading sentiment signal from manipulated social media |
| Value chain and component integration | Vendor retains deal data |
| Human-AI configuration | Junior analyst trusts AI comps without checking |
| Intellectual property | Scraped paywalled research used in pitch material |

Plus banking-specific categories: **MNPI and information barriers**, **market abuse**, **model risk**, **recordkeeping**, **communications compliance**.

<!-- nav -->
---

[← Prompt Library Governance Standard](../02-policies/04-prompt-library-governance-standard.md) · [Home](../README.md) · [AI Risk Register →](02-ai-risk-register.md)
<!-- /nav -->
