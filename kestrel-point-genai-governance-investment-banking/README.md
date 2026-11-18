<p align="center">
<img width="2560" height="840" alt="kestrel-point-banner" src="https://github.com/user-attachments/assets/a84ed4af-2e60-45cc-aa1f-a1160c971a7c" />

</p>

# Kestrel Point Capital · Generative AI Governance for Investment Banking

An end-to-end AI governance programme for a fictional mid-market investment bank that is rolling out generative AI across 14 deal-lifecycle use cases, from pitchbooks and due diligence to sentiment signals and risk models.

The work shows how a second-line AI governance function lets bankers use AI **without leaking MNPI, breaching market abuse rules or sending wrong numbers to clients**.

![NIST AI RMF](https://img.shields.io/badge/NIST-AI%20RMF%201.0-1f3a5f)
![NIST AI 600-1](https://img.shields.io/badge/NIST-AI%20600--1%20GenAI-1f3a5f)
![ISO/IEC 42001](https://img.shields.io/badge/ISO%2FIEC-42001-2d6a4f)
![EU AI Act](https://img.shields.io/badge/EU-AI%20Act-003399)
![SR 11-7](https://img.shields.io/badge/Fed-SR%2011--7-6b4f1d)
![MAR](https://img.shields.io/badge/EU%2FUK-MAR-7a1f2b)
![FINRA 2210](https://img.shields.io/badge/FINRA-2210-444)
![DORA](https://img.shields.io/badge/EU-DORA-003399)

> **Fictional case study.** Kestrel Point Capital, its staff, vendors (VaultLens, NoteStream, SignalCurrent), figures and incidents are invented. The use cases are based on common industry guidance on AI for investment bankers. Regulations and frameworks are real. Nothing here is legal advice.

---

## The problem

In early 2026, 41% of Kestrel's front-office staff were using public AI chatbots for work and 12% had pasted client or deal information into one. Copilot was in pilot with no permissions review, and the Risk team was testing a machine-learning stress model that Model Risk had never seen.

The Board asked for a programme that would let bankers use AI safely instead of banning it.

## What was delivered

| Deliverable | Result |
|---|---|
| AI use case inventory | 14 use cases, 4 AI routes, 3 shadow tools decommissioned |
| Risk tiering | 5 Tier 1, 8 Tier 2, 1 Tier 3 |
| Policies | Acceptable Use Policy plus MNPI, output review and prompt library standards |
| Risk register | 18 risks. Inherent: 1 Critical, 13 High. Residual: 0 Critical, 1 High |
| Control library | 30 controls mapped to NIST AI RMF, ISO/IEC 42001, EU AI Act, MAR, FINRA, SEC, SR 11-7, GDPR and DORA |
| Control testing | 8 key controls: 4 Effective, 4 Partially effective, 4 findings |
| Impact assessments | Due diligence AI (UC-04) and risk models (UC-12) |
| Monitoring | 12 KRIs, incident playbook, Project KINGFISHER tabletop |
| Board reporting | Q3 2026 Board AI risk report and remediation roadmap |

## Repository structure

| # | Section | Documents |
|---|---|---|
| 00 | **Programme** | [Scenario and context](00-programme/01-scenario-and-context.md) · [Governance charter](00-programme/02-governance-charter.md) · [Regulatory landscape](00-programme/03-regulatory-landscape.md) |
| 01 | **Inventory** | [AI use case inventory](01-inventory/01-ai-use-case-inventory.md) · [Risk tiering methodology](01-inventory/02-risk-tiering-methodology.md) · [Tiering results](01-inventory/03-use-case-tiering-results.md) |
| 02 | **Policies** | [GenAI Acceptable Use Policy](02-policies/01-genai-acceptable-use-policy.md) · [MNPI and data protection standard](02-policies/02-mnpi-and-data-protection-standard.md) · [Output review and human oversight](02-policies/03-output-review-and-human-oversight-standard.md) · [Prompt library governance](02-policies/04-prompt-library-governance-standard.md) |
| 03 | **Risk assessment** | [Methodology](03-risk-assessment/01-risk-assessment-methodology.md) · [AI risk register](03-risk-assessment/02-ai-risk-register.md) · [Impact assessment: UC-04 due diligence](03-risk-assessment/03-impact-assessment-uc04-due-diligence.md) · [Impact assessment: UC-12 risk models](03-risk-assessment/04-impact-assessment-uc12-risk-models.md) |
| 04 | **Controls** | [Control library](04-controls/01-control-library.md) · [Framework crosswalk](04-controls/02-framework-crosswalk.md) · [Q3 2026 control testing](04-controls/03-control-testing-workpapers.md) |
| 05 | **Third parties** | [AI vendor due diligence](05-third-party/01-ai-vendor-due-diligence.md) |
| 06 | **Monitoring** | [KRI framework](06-monitoring/01-monitoring-and-kri-framework.md) · [AI incident response playbook](06-monitoring/02-ai-incident-response-playbook.md) |
| 07 | **Reporting** | [Board AI risk report Q3 2026](07-reporting/01-board-ai-risk-report-q3-2026.md) · [Remediation roadmap](07-reporting/02-remediation-roadmap.md) · [Maturity and lessons learned](07-reporting/03-maturity-assessment-and-lessons.md) |

**Start here:** read the [scenario](00-programme/01-scenario-and-context.md), then jump to the [Board report](07-reporting/01-board-ai-risk-report-q3-2026.md) for the outcome. Every document links to the next one at the bottom.

## The 14 use cases

| Tier 1 (high) | Tier 2 (elevated) | Tier 3 (standard) |
|---|---|---|
| UC-03 Pitchbooks and CIMs | UC-02 Financial document analysis | UC-01 Market and industry intelligence |
| UC-04 Due diligence automation | UC-05 Sourcing and screening | |
| UC-07 Meeting transcription | UC-06 Financial modelling support | |
| UC-11 Market sentiment analysis | UC-08 Valuation benchmarking | |
| UC-12 AI risk and credit models | UC-09 Executive outreach | |
| | UC-10 Compliance review | |
| | UC-13 Financial statement analysis | |
| | UC-14 Smart daily priorities | |

## How the pieces connect

```
Use case (UC-xx) ──► Tier ──► Risks (R-xx) ──► Controls (C-xx) ──► Tests ──► Findings (F-xx) ──► Actions (RA-xx) ──► Board report
                                    │                 │
                                    └── KRIs ◄────────┘
```

Every ID is used consistently across documents, so a reviewer can trace a Board-level risk back to the control test that supports its rating.

## Skills demonstrated

- AI governance operating model design (three lines of defence, RACI, SM&CR accountability)
- AI inventory, risk tiering and impact assessment
- GenAI risk assessment with NIST AI RMF and NIST AI 600-1
- Control design and multi-framework mapping (ISO/IEC 42001 Annex A, EU AI Act, MAR, FINRA, SEC, SR 11-7, DORA, GDPR)
- Control testing, findings and remediation tracking
- Model risk management for AI and ML models
- AI third-party risk management
- KRIs, incident response and Board reporting


