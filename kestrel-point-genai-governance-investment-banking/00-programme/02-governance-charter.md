# 02 · AI Governance Charter

| Field | Value |
|---|---|
| Document ID | KPC-AIG-CH-001 |
| Version | 1.0 |
| Owner | Chief Risk Officer |
| Approved by | Board Risk Committee, 24 March 2026 |
| Next review | March 2027 |

## 1. Purpose

This charter sets out who decides, who does the work and who checks it for all use of artificial intelligence at Kestrel Point Capital and its subsidiaries.

## 2. Principles

1. **Client confidentiality comes first.** MNPI and client data are only processed in approved, isolated AI environments.
2. **A banker owns every output.** AI drafts; a named person reviews, signs off and is accountable.
3. **Controls follow risk.** Oversight scales with the use case's tier (see [risk tiering](../01-inventory/02-risk-tiering-methodology.md)).
4. **Models are models.** Any AI that produces numbers used in risk, valuation or credit decisions is governed under model risk management.
5. **If it is not recorded, it did not happen.** Prompts, outputs and approvals are retained as business records.

## 3. Governance structure

```
Board of Directors
 └── Board Risk Committee  ── quarterly AI risk report
      └── AI Governance Committee (AIGC)  ── monthly
           ├── AI Use Case Review Panel  ── fortnightly intake
           ├── Model Risk Committee  ── AI models (UC-06, UC-11, UC-12)
           └── Data Governance Council  ── data classes, MNPI handling
```

### AI Governance Committee

| Item | Detail |
|---|---|
| Chair | Chief Risk Officer |
| Members | COO Front Office, Head of Compliance, Group DPO, CISO, Head of AI Platform, Head of Model Risk, General Counsel (or delegate) |
| Observer | Head of Internal Audit |
| Quorum | Chair or delegate plus four members, including Compliance and one first-line member |
| Decides | Approval of Tier 1 use cases, AI policies, risk acceptance up to "High", exceptions over 90 days |
| Escalates to BRC | Residual risks rated High above appetite, Sev-1 AI incidents, regulatory findings |

## 4. Three lines of defence

| Line | Who | AI responsibilities |
|---|---|---|
| **1st** | Business heads, deal teams, AI Platform team | Own use cases and risks, follow policy, review outputs, run controls, report incidents |
| **2nd** | Risk (AI Governance), Compliance, DPO, Model Risk, CISO | Set policy and risk appetite, approve tiers, challenge, test key controls, monitor KRIs, report to the Board |
| **3rd** | Internal Audit | Independent assurance over the AI governance framework (first audit planned Q2 2027) |

## 5. RACI

R = Responsible, A = Accountable, C = Consulted, I = Informed

| Activity | Business owner | AI Platform | AI Governance | Compliance | DPO | Model Risk | AIGC | Internal Audit |
|---|---|---|---|---|---|---|---|---|
| Submit use case | R/A | C | I | I | I | I | I | – |
| Risk tiering | C | C | R | C | C | C | A | I |
| Approve Tier 1 use case | C | C | R | C | C | C | A | I |
| Approve Tier 2 use case | C | C | A/R | C | C | C | I | – |
| DPIA | C | C | C | C | R/A | – | I | – |
| Model validation | C | C | I | – | – | R/A | I | I |
| Operate technical controls | I | R/A | C | I | I | – | – | – |
| Test key controls | C | C | R/A | C | C | C | I | I |
| AI incident response | R | R | A | R | R | C | I | I |
| Board AI risk report | C | C | R | C | C | C | A | I |
| Independent audit | I | I | I | I | I | I | I | R/A |

## 6. Accountability under SM&CR

Under the FCA Senior Managers and Certification Regime, the **Chief Risk Officer (SMF4)** holds documented responsibility for AI risk management. The **Chief Operations function (SMF24)** is responsible for the operational resilience of AI services. Both responsibilities are recorded in their Statements of Responsibilities.

## 7. Risk appetite for AI

| Risk area | Appetite | Meaning |
|---|---|---|
| MNPI or client data leaving approved environments | **Zero** | No tolerance; any instance is an incident |
| Inaccurate content in client or external materials | **Low** | Every external output has human sign-off |
| Model error in risk, valuation or credit outputs | **Low** | Independent validation before use |
| Productivity use of AI on internal, non-confidential work | **Moderate** | Encouraged inside approved tools |

A residual risk rated **High** or above sits outside appetite and needs a remediation plan approved by the AIGC, or formal acceptance by the CRO with a review date.

## 8. Documents under this charter

| ID | Document |
|---|---|
| KPC-AIG-POL-001 | [Generative AI Acceptable Use Policy](../02-policies/01-genai-acceptable-use-policy.md) |
| KPC-AIG-STD-002 | [MNPI and Data Protection Standard for AI](../02-policies/02-mnpi-and-data-protection-standard.md) |
| KPC-AIG-STD-003 | [AI Output Review and Human Oversight Standard](../02-policies/03-output-review-and-human-oversight-standard.md) |
| KPC-AIG-STD-004 | [Prompt Library Governance Standard](../02-policies/04-prompt-library-governance-standard.md) |

<!-- nav -->
---

[← Scenario and Context](01-scenario-and-context.md) · [Home](../README.md) · [Regulatory and Framework Landscape →](03-regulatory-landscape.md)
<!-- /nav -->
