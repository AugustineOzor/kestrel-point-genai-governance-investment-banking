# 01 · AI Use Case Inventory

| Field | Value |
|---|---|
| Document ID | KPC-AIG-INV-001 |
| As at | 30 September 2026 |
| Owner | AI Governance Lead |
| Attestation | Business owners attest quarterly (control C-04) |

## How the inventory was built

1. **Survey:** a front-office survey in February 2026 (412 responses).
2. **Network evidence:** web proxy logs for AI domains over 90 days.
3. **Procurement and expenses:** card spend and purchase orders mentioning AI.
4. **Model inventory:** a reconciliation with Model Risk's model inventory.
5. **Workshops:** one 60-minute workshop per business area to confirm each use case.

The search found **14 business use cases**, **4 platforms** and **3 unapproved tools** bought on corporate cards. The unapproved tools were decommissioned by 30 April 2026, and their use cases moved to Kestrel Assist.

## Inventory

| ID | Use case | AI route | Business owner | Highest data class | Tier | Status |
|---|---|---|---|---|---|---|
| UC-01 | Market and industry intelligence | Kestrel Assist | Head of Coverage | Internal | 3 | Approved |
| UC-02 | Financial document analysis | Kestrel Assist | Head of Advisory | Confidential | 2 | Approved |
| UC-03 | Content generation and pitching | Kestrel Assist | Head of Advisory | MNPI-Restricted | 1 | Approved |
| UC-04 | Due diligence automation | VaultLens via Kestrel Assist gateway | Head of Advisory | MNPI-Restricted | 1 | Approved |
| UC-05 | Strategic sourcing and screening | Kestrel Assist | Head of Coverage | Confidential | 2 | Approved |
| UC-06 | Financial modelling support | Kestrel Assist | Head of Leveraged Finance | Confidential | 2 | Approved |
| UC-07 | Meeting and relationship management | NoteStream, M365 Copilot (Teams) | COO Front Office | MNPI-Restricted | 1 | Approved with conditions |
| UC-08 | Valuation benchmarking | Kestrel Assist | Head of Advisory | Confidential | 2 | Approved |
| UC-09 | Executive outreach and personalisation | Kestrel Assist | Head of Coverage | Confidential | 2 | Approved |
| UC-10 | Regulatory and internal compliance review | Kestrel Assist | Head of Compliance | MNPI-Restricted | 2 | Approved |
| UC-11 | Market sentiment analysis | SignalCurrent | Head of Markets | Confidential | 1 | Approved with conditions |
| UC-12 | AI-driven risk management | In-house ML models | Chief Risk Officer | MNPI-Restricted | 1 | Approved |
| UC-13 | Financial statement analysis | Kestrel Assist | Head of Leveraged Finance | MNPI-Restricted | 2 | Approved |
| UC-14 | Smart daily priorities | M365 Copilot | COO Front Office | MNPI-Restricted | 2 | Pilot |

**Totals:** 14 use cases. Tier 1: 5. Tier 2: 8. Tier 3: 1.

| Status | Count | Use cases |
|---|---|---|
| Approved | 11 | UC-01 to UC-06, UC-08 to UC-10, UC-12, UC-13 |
| Approved with conditions | 2 | UC-07, UC-11 |
| Pilot | 1 | UC-14 |

## Conditions on approval

| Use case | Condition | Due | Linked item |
|---|---|---|---|
| UC-07 | NoteStream to move EU client meeting data to EU hosting. Recording notice to be shown in every external meeting invite | 31 Dec 2026 | [Vendor review](../05-third-party/01-ai-vendor-due-diligence.md) |
| UC-11 | SignalCurrent model documentation to be received and independently validated before signals are used for position sizing | 31 Jan 2027 | Finding F-04 |
| UC-14 | Copilot rollout beyond 60 pilot users gated on the SharePoint oversharing clean-up | 31 Dec 2026 | Finding F-02 |

## Inventory record fields

Each use case has a full record in the AI register with these fields:

| Field | Example (UC-04) |
|---|---|
| Purpose | First-pass review of VDR contracts for change-of-control, MFN and non-compete clauses |
| Users | Deal teams (about 140 users), external counsel excluded |
| Inputs | Target contracts uploaded to the VDR (MNPI-Restricted) |
| Outputs | Clause extraction table with document and section references, risk rating |
| Decision supported | Which contracts go to lawyers for full review, and issues list for the client |
| Human in the loop | Associate reviews every hit. Lawyer review of all High items |
| Model and provider | VaultLens clause model plus Kestrel Assist LLM for summaries |
| Data location | Kestrel Azure tenant (UK South), VaultLens EU region |
| Retention | Prompts and outputs 7 years in records archive |
| Impact assessment | [UC-04 impact assessment](../03-risk-assessment/03-impact-assessment-uc04-due-diligence.md) |
| Risks | R-01, R-02, R-05, R-11, R-12 |
| Key controls | C-06, C-07, C-11, C-14, C-23, C-25 |
| Last reviewed | 15 September 2026 |

<!-- nav -->
---

[← Regulatory and Framework Landscape](../00-programme/03-regulatory-landscape.md) · [Home](../README.md) · [Risk Tiering Methodology →](02-risk-tiering-methodology.md)
<!-- /nav -->
