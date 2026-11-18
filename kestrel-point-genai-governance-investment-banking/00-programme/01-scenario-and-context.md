# 01 · Scenario and Context

> **Fictional case study.** Kestrel Point Capital, its people, vendors, figures and incidents are invented for this portfolio. Regulations and frameworks referenced are real.

## The firm

**Kestrel Point Capital** is a mid-market investment bank with about **1,150 staff**.

| Entity | Location | Regulator | Activities |
|---|---|---|---|
| Kestrel Point Capital Ltd (group HQ) | London | FCA | M&A advisory, ECM, DCM and leveraged finance, group functions |
| Kestrel Point Securities LLC | New York | SEC, FINRA | US broker-dealer: advisory, capital markets, institutional sales |
| Kestrel Point Capital GmbH | Frankfurt | BaFin | EU advisory and capital markets coverage |

The firm advises corporate and private equity clients on mergers, acquisitions and financing. Its bankers handle **material non-public information (MNPI)** every day: target names, deal terms, client financials and board materials.

## How AI arrived

In late 2025 a widely shared industry guide described 14 tasks where investment bankers could use AI to save time, each with an "advanced power prompt". Kestrel's bankers started using it within weeks.

What the Chief Risk Officer found in a February 2026 survey:

- **41%** of front-office staff had used a public AI chatbot for work in the last month.
- **12%** admitted pasting client or deal information into one.
- Three desks had bought AI tools on corporate cards with no vendor review.
- Microsoft 365 Copilot was in pilot with 60 users, with no check of who could see which SharePoint sites.
- The Markets risk team was testing a machine-learning stress-test model that Model Risk had never seen.

The guide itself warned users never to put MNPI or PII into public AI models, to use enterprise "walled garden" instances, and to review outputs before external use. Nobody at Kestrel owned those rules.

## The mandate

In March 2026 the Board Risk Committee approved **Project LANTERN**: a programme to let bankers use GenAI safely across the deal lifecycle rather than ban it.

The Board asked for five things by Q4 2026:

1. A complete inventory of AI use cases, tiered by risk.
2. Policies that bankers can follow without reading a regulation.
3. A risk register and controls mapped to the frameworks and rules that apply to the firm.
4. Evidence that the key controls work, from independent testing.
5. A quarterly AI risk report to the Board.

## The 14 use cases in scope

| ID | Use case | Primary users |
|---|---|---|
| UC-01 | Market and industry intelligence | Coverage bankers, analysts |
| UC-02 | Financial document analysis (10-K, 10-Q, annual reports) | Analysts, associates |
| UC-03 | Content generation and pitching (pitchbooks, teasers, CIMs) | Deal teams |
| UC-04 | Due diligence automation (virtual data room review) | Deal teams, legal |
| UC-05 | Strategic sourcing and target screening | Coverage, PE coverage |
| UC-06 | Financial modelling support (LBO, formulas, VBA/Python) | Analysts, associates |
| UC-07 | Meeting and relationship management (transcription, follow-ups) | All front office |
| UC-08 | Valuation benchmarking (trading comps) | Analysts, associates |
| UC-09 | Executive outreach and personalisation | Coverage bankers |
| UC-10 | Regulatory and internal compliance review | Compliance |
| UC-11 | Market sentiment analysis | Markets, sales and trading |
| UC-12 | AI-driven risk management (stress testing, credit scoring, fraud) | Risk |
| UC-13 | Financial statement analysis (credit memos, ratio dashboards) | Leveraged finance, analysts |
| UC-14 | Smart daily priorities (inbox, calendar, deal tracker) | All staff |

## The platform decision

The firm chose three routes for AI, and banned everything else:

| Route | What it is | Used for |
|---|---|---|
| **Kestrel Assist** | Enterprise LLM in the firm's own cloud tenant, behind an AI gateway with logging, DLP, zero data retention and entitlement-aware retrieval | UC-01 to UC-06, UC-08 to UC-10, UC-13 |
| **Microsoft 365 Copilot** | Embedded AI across email, calendar, Teams and documents | UC-07 (Teams recap), UC-14 |
| **Approved specialist vendors** | VaultLens (VDR review), NoteStream (meeting transcription), SignalCurrent (sentiment data) | UC-04, UC-07, UC-11 |
| **In-house models** | Machine-learning stress test and corporate credit scoring models built by Risk | UC-12 |

Public AI chatbots are blocked on firm devices.

## Programme team

| Role | Name (fictional) | Line |
|---|---|---|
| Executive sponsor | Chief Risk Officer, Helena Marsh | 2nd |
| Programme lead, AI governance | AI Governance Lead (author of this repository) | 2nd |
| Business owner | Chief Operating Officer, Front Office, David Okafor | 1st |
| Compliance | Head of Compliance, Priya Raman | 2nd |
| Data protection | Group DPO, Lukas Brenner | 2nd |
| Technology | Head of AI Platform, Sam Whitfield | 1st |
| Model risk | Head of Model Risk Management, Ana Ferreira | 2nd |
| Assurance | Head of Internal Audit, Michael Chen | 3rd |

<!-- nav -->
---

[Home](../README.md) · [AI Governance Charter →](02-governance-charter.md)
<!-- /nav -->
