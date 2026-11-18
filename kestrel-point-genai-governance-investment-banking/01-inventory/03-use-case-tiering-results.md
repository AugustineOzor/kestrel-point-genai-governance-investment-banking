# 03 · Use Case Tiering Results

Scored with the [risk tiering methodology](02-risk-tiering-methodology.md). Reviewed by the AI Use Case Review Panel and confirmed by the AIGC on 12 May 2026.

| ID | Use case | D | E | I | A | R | Total | Tier | Main driver |
|---|---|---|---|---|---|---|---|---|---|
| UC-01 | Market and industry intelligence | 1 | 1 | 1 | 2 | 1 | **6** | 3 | Public data, internal use |
| UC-02 | Financial document analysis | 2 | 1 | 2 | 1 | 2 | **8** | 2 | Client financials in private mandates |
| UC-03 | Content generation and pitching | 3 | 3 | 2 | 1 | 3 | **12** | **1** | MNPI in CIMs, external material, FINRA 2210 and COBS 4 |
| UC-04 | Due diligence automation | 3 | 1 | 3 | 2 | 3 | **12** | **1** | MNPI and deal-breaker decisions |
| UC-05 | Strategic sourcing and screening | 2 | 1 | 2 | 2 | 2 | **9** | 2 | Web data sourcing, wall-crossing risk |
| UC-06 | Financial modelling support | 2 | 1 | 3 | 1 | 2 | **9** | 2 | Model error in LBO outputs |
| UC-07 | Meeting and relationship management | 3 | 2 | 1 | 3 | 3 | **12** | **1** | Records every meeting, personal data, MNPI, recordkeeping |
| UC-08 | Valuation benchmarking | 2 | 2 | 2 | 1 | 2 | **9** | 2 | Feeds client valuation materials |
| UC-09 | Executive outreach | 2 | 3 | 1 | 1 | 2 | **9** | 2 | External emails, personal data on executives |
| UC-10 | Compliance review | 3 | 1 | 2 | 1 | 3 | **10** | 2 | Missed issues let non-compliant material out |
| UC-11 | Market sentiment analysis | 2 | 1 | 3 | 3 | 3 | **12** | **1** | Feeds trading decisions continuously, MAR |
| UC-12 | AI-driven risk management | 3 | 1 | 3 | 2 | 3 | **12** | **1** | VaR, stress and credit outputs, SR 11-7 |
| UC-13 | Financial statement analysis | 3 | 2 | 2 | 1 | 2 | **10** | 2 | Credit memos on private targets |
| UC-14 | Smart daily priorities | 3 | 1 | 1 | 2 | 2 | **9** | 2 | Reads inboxes that hold MNPI |

## Distribution

| Tier | Count | Use cases |
|---|---|---|
| Tier 1 | 5 | UC-03, UC-04, UC-07, UC-11, UC-12 |
| Tier 2 | 8 | UC-02, UC-05, UC-06, UC-08, UC-09, UC-10, UC-13, UC-14 |
| Tier 3 | 1 | UC-01 |

## Panel challenges recorded

| Use case | Challenge | Outcome |
|---|---|---|
| UC-14 | Business proposed Tier 3 as "personal productivity" | Rejected. Copilot reads every email the user can access, including MNPI. Scored D = 3 and kept at Tier 2 |
| UC-10 | Compliance proposed Tier 1 because it is a control | Kept at Tier 2. A compliance officer reviews every flagged and unflagged slide. Residual risk tracked as R-18 |
| UC-12 | Risk asked whether credit scoring is high-risk under the EU AI Act | Not high-risk: the model scores corporate counterparties, not natural persons. Annual re-check added because Annex III applies from 2 December 2027 |
| UC-01 | Should the morning "macro pulse" checklist be separate? | Folded into UC-01. It uses public market data only |

<!-- nav -->
---

[← Risk Tiering Methodology](02-risk-tiering-methodology.md) · [Home](../README.md) · [Generative AI Acceptable Use Policy →](../02-policies/01-genai-acceptable-use-policy.md)
<!-- /nav -->
