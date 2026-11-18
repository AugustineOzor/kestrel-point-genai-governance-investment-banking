# 01 · AI Control Library

| Field | Value |
|---|---|
| Document ID | KPC-AIG-CTL-001 |
| As at | 30 September 2026 |
| Owner | AI Governance Lead |
| Controls | 30 (P = preventive, D = detective, C = corrective) |
| Key controls tested in Q3 2026 | 8, marked ★ |

## Governance and access

| ID | Control | Type | Frequency | Owner | Risks |
|---|---|---|---|---|---|
| C-01 ★ | Only approved AI tools are reachable: public GenAI domains blocked at the web proxy, approved tools list published | P | Continuous | Head of Security Engineering | R-01 |
| C-02 ★ | Endpoint and browser DLP detects MNPI labels and deal codenames in uploads or pastes to AI domains and blocks them | P | Continuous | Head of Security Engineering | R-01 |
| C-03 | AI use case intake: every new use case or material change is tiered and approved before use | P | Per request | AI Governance Lead | All |
| C-04 | AI inventory maintained; business owners attest quarterly that it is complete | D | Quarterly | AI Governance Lead | All |
| C-05 | AI Essentials and AI in Deals training completed before access and annually | P | Annual | Head of Learning | R-01, R-14 |

## Platform and data

| ID | Control | Type | Frequency | Owner | Risks |
|---|---|---|---|---|---|
| C-06 ★ | Kestrel Assist gateway: SSO, zero data retention by provider, tenant isolation, full logging | P | Continuous | Head of AI Platform | R-01, R-12 |
| C-07 | Entitlement-aware retrieval: AI workspaces per project codename, deal team list from entitlement system | P | Continuous | Head of AI Platform | R-02, R-08 |
| C-08 ★ | Copilot readiness: SharePoint and Teams oversharing scan and fix before licences are issued; quarterly re-scan | P/D | Quarterly | Head of IT Infrastructure | R-02 |
| C-09 | Sensitivity labels applied to deal documents automatically in project sites | P | Continuous | Data Governance Lead | R-02, R-10 |
| C-10 | Prompt library: approved prompts versioned, reviewed and read-only | P | Per change | Head of AI Platform | R-03, R-04, R-16, R-18 |
| C-20 | Restricted and watch list check: prompts from public-side users naming listed companies are blocked and alerted | P/D | Continuous | Head of Compliance | R-02, R-08 |
| C-21 ★ | AI prompts, outputs, retrieved document IDs and meeting transcripts archived in the books-and-records system | P | Continuous | Head of Compliance | R-09 |
| C-22 | DPIA completed for AI processing personal data; meeting recording notice in invites and at the start of calls | P | Per use case | Group DPO | R-10 |
| C-23 | Gateway filter detects prompt injection patterns in documents and web content | P | Continuous | Head of AI Platform | R-11 |

## Output quality and oversight

| ID | Control | Type | Frequency | Owner | Risks |
|---|---|---|---|---|---|
| C-11 ★ | Human review and sign-off at the level the Output Review Standard requires, with source citation | P | Per output | Business heads | R-03, R-05, R-13, R-14 |
| C-12 | Compliance pre-use review of external marketing material and outreach templates | P | Per document | Head of Compliance | R-03, R-04, R-18 |
| C-13 | Claim substantiation: superlatives and comparisons footnoted to data | P | Per document | Deal team VP | R-04 |
| C-14 ★ | Due diligence recall testing: 250 clauses sampled monthly from live deals and checked manually; threshold 95% | D | Monthly | Head of Advisory | R-05 |
| C-15 | End-user computing (EUC) register and independent check for client models using AI-suggested logic | D | Per model | Head of Leveraged Finance | R-13 |
| C-27 | Tier-based oversight in tool: Tier 1 outputs cannot be exported until a VP signs off | P | Continuous | Head of AI Platform | R-14 |

## Model risk

| ID | Control | Type | Frequency | Owner | Risks |
|---|---|---|---|---|---|
| C-16 ★ | AI and ML models in risk, valuation or trading decisions are on the model inventory and independently validated before use | P | Per model, annual revalidation | Head of Model Risk | R-06, R-07, R-08 |
| C-17 | Ongoing performance and drift monitoring with thresholds and escalation | D | Monthly | Model owners | R-06, R-18 |
| C-18 | Fairness and consistency testing for credit scoring across sectors and company sizes | D | Annual | Head of Model Risk | R-07 |
| C-19 | Sentiment signals logged and linked to trade surveillance | D | Continuous | Head of Compliance Surveillance | R-08 |

## Security, vendors and resilience

| ID | Control | Type | Frequency | Owner | Risks |
|---|---|---|---|---|---|
| C-24 | AI red team of Tier 1 use cases before go-live and annually | D | Annual | CISO | R-11 |
| C-25 | AI vendor due diligence: questionnaire, SOC 2 or ISO 27001 report, AI-specific review | P | Onboarding, annual | Head of Procurement | R-12, R-15 |
| C-26 | AI contract clauses: no training on firm data, retention limits, sub-processors, audit rights, 24-hour breach notice, exit | P | Per contract | General Counsel | R-12 |
| C-28 | Legal review of data sources for scraping and licensed data | P | Per source | General Counsel | R-15 |
| C-29 | AI service continuity: fallback to manual process, vendor exit plans, DORA register of information | C | Annual test | COO Front Office | R-17 |
| C-30 | AI incident management with severity levels, root cause analysis and KRI reporting | C | Per incident | AI Governance Lead | All |

## Control ownership summary

| Line | Controls |
|---|---|
| 1st line operates (16) | C-01, C-02, C-05, C-06, C-07, C-08, C-09, C-10, C-11, C-13, C-14, C-15, C-17, C-23, C-27, C-29 |
| 2nd line operates (14) | C-03, C-04, C-12, C-16, C-18, C-19, C-20, C-21, C-22, C-24, C-25, C-26, C-28, C-30 |

<!-- nav -->
---

[← AI Impact Assessment: UC-12 AI-Driven Risk Management](../03-risk-assessment/04-impact-assessment-uc12-risk-models.md) · [Home](../README.md) · [Framework Crosswalk →](02-framework-crosswalk.md)
<!-- /nav -->
