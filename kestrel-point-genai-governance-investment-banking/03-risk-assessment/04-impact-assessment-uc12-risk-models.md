# 04 · AI Impact Assessment: UC-12 AI-Driven Risk Management

| Field | Value |
|---|---|
| Document ID | KPC-AIG-AIA-012 |
| Use case | UC-12 AI-driven risk management |
| Tier | 1 |
| Assessor | AI Governance Lead with Model Risk Management |
| Aligned to | Fed SR 11-7, PRA SS1/23 (good practice), NIST AI RMF Measure 2, ISO/IEC 42001 Annex A.6 |
| Decision | **Approved** by AIGC, 21 July 2026, after independent validation |

## 1. Description

Kestrel's Risk team built two machine-learning models:

| Model ID | Name | Purpose | Method |
|---|---|---|---|
| MDL-RSK-031 | Scenario stress engine | Generates and runs macro stress scenarios on the leveraged finance underwriting book and trading inventory, estimating impact on VaR and liquidity | Gradient-boosted trees on 15 years of market and credit data, plus a GenAI layer that drafts scenario narratives |
| MDL-RSK-032 | Corporate counterparty credit score | Scores corporate borrowers in the underwriting pipeline from 1 (strong) to 10 (weak) | Gradient-boosted classifier on financial ratios, sector and market signals |

Outputs go to the Risk Committee and set underwriting limits. A risk manager reviews every output and can override it.

## 2. EU AI Act classification

MDL-RSK-032 scores **companies**, not natural persons. Annex III point 5(b) (creditworthiness of natural persons) does not apply, so the model is not high-risk. The model owner must tell AI Governance if the model is ever used for sole traders or individuals. This would trigger a high-risk assessment before 2 December 2027.

## 3. Model risk assessment

| SR 11-7 element | Evidence |
|---|---|
| Model inventory | Both models on the firm model inventory with owner, tier and use |
| Development documentation | Data lineage, feature list, training approach and limitations documented |
| Conceptual soundness | Reviewed by Model Risk: method suitable, features economically sensible |
| Independent validation | Completed July 2026 by Model Risk (separate reporting line to CRO) |
| Outcomes analysis | Back-test against 2008, 2020 and 2022 stress periods |
| Ongoing monitoring | Monthly drift and performance monitoring (C-17) |
| Limitations and overlays | Documented. Risk managers apply judgement overlays, which are logged |

## 4. Validation results

| Test | Model | Threshold | Result |
|---|---|---|---|
| Back-test: losses under historical stress within predicted range | MDL-RSK-031 | ≥ 90% of periods | 94% |
| Discriminatory power (AUC) on hold-out data | MDL-RSK-032 | ≥ 0.75 | 0.81 |
| Stability (Population Stability Index) | MDL-RSK-032 | < 0.10 | 0.04 |
| Consistency across sectors (difference in default prediction error) | MDL-RSK-032 | < 5 percentage points between any two sectors | 3.2 pp maximum |
| GenAI scenario narratives match the numbers | MDL-RSK-031 | 100% of sampled narratives | 47 of 50. Three narratives misstated a rate shock. **Fixed:** narratives are now generated from the numeric output only and checked by the risk manager |

## 5. Risks and controls

| Risk | Register | Controls |
|---|---|---|
| Wrong stress or VaR outputs | R-06 | C-16 validation, C-17 monitoring, risk manager override |
| Unfair or inconsistent credit scores | R-07 | C-18 sector consistency testing, C-16 |
| Narratives misstate numbers (confabulation) | R-03 | C-11 risk manager review |
| Model used outside approved scope | R-06 | Model inventory scope statement, quarterly attestation |

## 6. Decision

Approved for use from 1 August 2026. Residual risk R-06 **Medium (8)**, R-07 **Low (4)**.

**Conditions:**
1. Revalidate annually or on any material change to features or training data.
2. Report overrides above 20% of outputs in a month to the Model Risk Committee (an override rate that high suggests the model is not trusted or not working).
3. GenAI narratives cannot be sent outside Risk without the numeric output attached.

<!-- nav -->
---

[← AI Impact Assessment: UC-04 Due Diligence Automation](03-impact-assessment-uc04-due-diligence.md) · [Home](../README.md) · [AI Control Library →](../04-controls/01-control-library.md)
<!-- /nav -->
