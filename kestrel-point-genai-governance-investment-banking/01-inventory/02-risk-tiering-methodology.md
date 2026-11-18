# 02 · Risk Tiering Methodology

| Field | Value |
|---|---|
| Document ID | KPC-AIG-MTH-001 |
| Version | 1.0 |
| Owner | AI Governance Lead |
| Approved by | AI Governance Committee, 14 April 2026 |

Tiering decides how much oversight a use case gets. It is done at intake and repeated whenever the use case changes materially (new data, new users, new model or new output channel).

## Five factors

Each factor is scored 1 (low), 2 (medium) or 3 (high).

| Factor | 1 | 2 | 3 |
|---|---|---|---|
| **D · Data sensitivity** | Public or internal only | Confidential client or firm data | MNPI, restricted deal data or special category personal data |
| **E · External exposure** | Internal use only | Output shared with clients after review | Output sent externally or published as firm material |
| **I · Decision impact** | Personal productivity | Informs a business decision, easily checked | Drives deal, credit, risk, valuation or trading decisions |
| **A · Autonomy and integration** | User copies text in and out | Connected to firm data or tools, user triggers each action | Runs continuously, feeds other systems or acts without a prompt |
| **R · Regulatory exposure** | No specific rule engaged | Rules engaged, existing controls cover them | Specific rule engaged with high enforcement risk (MAR, FINRA 2210, SR 11-7, GDPR special data) |

## Tier thresholds

| Total score (5–15) | Tier | Meaning |
|---|---|---|
| **12–15** | **Tier 1** | High risk. AIGC approval, impact assessment, red team before go-live and annually |
| **8–11** | **Tier 2** | Elevated risk. AI Governance Lead approval, standard controls, annual review |
| **5–7** | **Tier 3** | Standard risk. Self-service in approved tools under the Acceptable Use Policy |

**Override rule:** a use case that scores 3 on both Data sensitivity and Decision impact is Tier 1 whatever its total.

## Controls required by tier

| Requirement | Tier 1 | Tier 2 | Tier 3 |
|---|---|---|---|
| Approval | AIGC | AI Governance Lead | Pre-approved |
| AI impact assessment | Full | Short form | Not needed |
| DPIA (if personal data) | Yes | Yes | Screening only |
| Model validation (if numeric outputs used in decisions) | Independent validation | Independent validation | – |
| Human review of outputs | VP or above sign-off | Author review with sign-off | User judgement |
| Red team | Before go-live and annually | On major change | – |
| Monitoring | Monthly KRIs | Quarterly KRIs | Platform-level only |
| Review cycle | 6 months | 12 months | 24 months |

## Worked example

**UC-04 Due diligence automation**

| Factor | Score | Reason |
|---|---|---|
| D | 3 | Target contracts in the VDR are MNPI |
| E | 1 | Outputs go to the deal team first |
| I | 3 | A missed change-of-control clause can change deal value or kill the deal |
| A | 2 | Connected to the VDR, but each run is started by a user |
| R | 3 | MAR, s15(g) MNPI policies and client confidentiality |
| **Total** | **12** | **Tier 1** (the override rule also applies: D = 3 and I = 3) |

Results for all 14 use cases are in [Use case tiering results](03-use-case-tiering-results.md).

<!-- nav -->
---

[← AI Use Case Inventory](01-ai-use-case-inventory.md) · [Home](../README.md) · [Use Case Tiering Results →](03-use-case-tiering-results.md)
<!-- /nav -->
