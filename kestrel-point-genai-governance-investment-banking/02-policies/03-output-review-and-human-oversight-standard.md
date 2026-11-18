# 03 · AI Output Review and Human Oversight Standard

| Field | Value |
|---|---|
| Document ID | KPC-AIG-STD-003 |
| Version | 1.0 |
| Owner | COO Front Office |
| Approved by | AI Governance Committee, 12 May 2026 |

## 1. Purpose

GenAI writes fluently and can be confidently wrong. This standard says who must check AI outputs, how, and what evidence to keep.

## 2. Review levels

| Level | When it applies | Who reviews | Evidence |
|---|---|---|---|
| **L1 · User check** | Internal, personal-use outputs (Tier 3, UC-14 briefs) | The user | None required |
| **L2 · Author sign-off** | Internal analysis used in a business decision (Tier 2) | The author, against sources | Sign-off tick in Kestrel Assist with source links |
| **L3 · Senior sign-off** | Anything going to a client or used in a deal, credit, risk or valuation decision (Tier 1 and client-facing Tier 2) | VP or above, not the author | Sign-off record in Kestrel Assist plus deal file note |
| **L4 · Compliance pre-use review** | External marketing and communications: pitchbooks, teasers, CIMs, outreach templates | Compliance (supervisory principal for US broker-dealer material) | Compliance approval record (FINRA 2210, COBS 4) |

## 3. Minimum checks for every reviewer

1. **Numbers:** every figure traces to a cited source document, page or cell. AI-calculated ratios are recalculated for at least the headline figures.
2. **Sources:** citations exist and say what the output claims.
3. **Claims:** superlatives ("market leader", "best-in-class") are backed by data with a footnote.
4. **Completeness:** for extraction tasks (UC-02, UC-04), a sample is checked for missed items, not just wrong items.
5. **Confidentiality:** the output contains no information from other deals or clients.
6. **Tone and balance:** external material presents risks as well as benefits.

## 4. Use case specific rules

| Use case | Additional rule |
|---|---|
| UC-03 Pitching and CIMs | No AI-generated financial figure enters a CIM without L3 sign-off against the model or data book |
| UC-04 Due diligence | Every High-rated clause is read in full by a lawyer. Monthly recall testing (C-14) |
| UC-06 Modelling | AI-suggested formulas are independently checked before a model goes to a client. Model logged on the EUC register |
| UC-08 Valuation | Comps outputs used in a fairness opinion are re-pulled from the market data terminal |
| UC-11 Sentiment | Signals inform decisions; traders do not trade automatically on them |
| UC-12 Risk models | Outputs only used from validated models. Overrides by risk managers are logged with a reason |

## 5. Automation bias

Junior bankers are most likely to trust AI outputs without checking. To reduce this:

- Kestrel Assist shows a "check before use" banner and source links on every analytical output.
- Monthly sampling of signed-off outputs by AI Governance (control C-11 testing).
- "AI in Deals" training uses real examples of AI errors caught at Kestrel.

## 6. Disclosure of AI use

Kestrel does not label every AI-assisted document. It does disclose AI use when a client asks, when a contract requires it, or when content would otherwise mislead a reader about how it was made.

<!-- nav -->
---

[← MNPI and Data Protection Standard for AI](02-mnpi-and-data-protection-standard.md) · [Home](../README.md) · [Prompt Library Governance Standard →](04-prompt-library-governance-standard.md)
<!-- /nav -->
