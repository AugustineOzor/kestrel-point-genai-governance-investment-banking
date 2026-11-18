# 02 · AI Risk Register

| Field | Value |
|---|---|
| Document ID | KPC-AIG-REG-001 |
| As at | 30 September 2026 (after Q3 control testing) |
| Owner | AI Governance Lead |
| Scale | 5x5, see [methodology](01-risk-assessment-methodology.md). L = likelihood, I = impact |

## Summary

| Rating | Inherent | Residual |
|---|---|---|
| Critical (17–25) | 1 | 0 |
| High (10–16) | 13 | 1 |
| Medium (5–9) | 4 | 12 |
| Low (1–4) | 0 | 5 |
| **Total** | **18** | **18** |

One residual risk (R-01) remains **High** and outside appetite. Its remediation is tracked in the [remediation roadmap](../07-reporting/02-remediation-roadmap.md).

## Register

| ID | Risk | Use cases | Inherent L x I | Inherent | Key controls | Residual L x I | Residual | Owner | Treatment |
|---|---|---|---|---|---|---|---|---|---|
| R-01 | Staff enter MNPI or client data into public or unapproved AI tools (shadow AI) | All | 4 x 5 = 20 | **Critical** | C-01, C-02, C-05, C-06 | 2 x 5 = 10 | **High** | CISO | Reduce: extend DLP to unmanaged browser profiles (F-01) |
| R-02 | AI retrieval or Copilot surfaces deal information across an information barrier | UC-03, UC-04, UC-14 | 3 x 5 = 15 | High | C-07, C-08, C-09, C-20 | 2 x 4 = 8 | Medium | Head of Compliance | Reduce: finish oversharing clean-up (F-02) |
| R-03 | Confabulated figures or facts reach client deliverables (pitchbooks, CIMs) | UC-02, UC-03, UC-08, UC-13 | 4 x 4 = 16 | High | C-10, C-11, C-12 | 2 x 4 = 8 | Medium | COO Front Office | Reduce: improve sign-off evidence (F-03) |
| R-04 | AI-drafted communications are unbalanced or misleading (FINRA 2210, COBS 4) | UC-03, UC-09 | 3 x 4 = 12 | High | C-10, C-12, C-13 | 2 x 3 = 6 | Medium | Head of Compliance | Accept with monitoring |
| R-05 | Due diligence AI misses a material clause (false negative) | UC-04 | 3 x 5 = 15 | High | C-11, C-14 | 2 x 4 = 8 | Medium | Head of Advisory | Accept with monthly recall testing |
| R-06 | Unvalidated or drifting AI model produces wrong stress test, VaR or liquidity outputs | UC-12 | 3 x 5 = 15 | High | C-16, C-17 | 2 x 4 = 8 | Medium | Head of Model Risk | Accept with monitoring |
| R-07 | Credit scoring model treats counterparties unfairly or inconsistently | UC-12 | 2 x 4 = 8 | Medium | C-16, C-18 | 1 x 4 = 4 | Low | Chief Risk Officer | Accept |
| R-08 | AI-derived signals lead to trading on inside information or manipulated sentiment | UC-11 | 2 x 5 = 10 | High | C-07, C-19, C-20 | 1 x 5 = 5 | Medium | Head of Markets | Reduce: validate vendor model (F-04) |
| R-09 | AI prompts, outputs or transcripts not kept as business records (SEC 17a-4, FCA) | UC-03, UC-07, UC-09 | 3 x 4 = 12 | High | C-21 | 1 x 4 = 4 | Low | Head of Compliance | Accept |
| R-10 | Personal data processed without lawful basis or transparency (recordings, executive profiling) | UC-07, UC-09 | 3 x 4 = 12 | High | C-09, C-22 | 2 x 3 = 6 | Medium | Group DPO | Accept with monitoring |
| R-11 | Prompt injection through VDR documents or web content changes AI behaviour or leaks data | UC-01, UC-04, UC-05 | 3 x 4 = 12 | High | C-23, C-24 | 2 x 3 = 6 | Medium | Head of AI Platform | Accept with annual red team |
| R-12 | AI vendor retains, reuses or trains on firm data | UC-04, UC-07, UC-11 | 3 x 5 = 15 | High | C-25, C-26 | 1 x 5 = 5 | Medium | Head of Procurement | Accept |
| R-13 | AI-suggested spreadsheet logic introduces errors into client models | UC-06 | 3 x 4 = 12 | High | C-11, C-15 | 2 x 3 = 6 | Medium | Head of Leveraged Finance | Accept |
| R-14 | Automation bias: staff accept AI outputs without proper checking | All | 4 x 3 = 12 | High | C-05, C-11, C-27 | 3 x 3 = 9 | Medium | COO Front Office | Reduce: targeted training and sampling |
| R-15 | Web scraping or licensed data use breaches terms of use or copyright | UC-05, UC-11 | 3 x 3 = 9 | Medium | C-25, C-28 | 2 x 2 = 4 | Low | General Counsel | Accept |
| R-16 | Unapproved changes to shared prompts alter outputs (prompt drift) | All | 3 x 3 = 9 | Medium | C-10 | 1 x 3 = 3 | Low | Head of AI Platform | Accept |
| R-17 | Outage of an AI service disrupts deal timelines (DORA ICT risk) | UC-04, UC-07 | 2 x 3 = 6 | Medium | C-29 | 2 x 2 = 4 | Low | COO Front Office | Accept |
| R-18 | Compliance review AI misses non-compliant content (false negatives) | UC-10 | 3 x 4 = 12 | High | C-10, C-12, C-17 | 2 x 3 = 6 | Medium | Head of Compliance | Accept with sampling |

## Notes on Q3 test results

- **R-01:** C-02 was rated Partially effective (F-01). Residual likelihood was kept at 2 rather than 1.
- **R-02:** C-08 was rated Partially effective (F-02). Copilot rollout paused at 60 users until fixed.
- **R-03:** C-11 was rated Partially effective (F-03). Residual stays Medium.
- **R-08:** C-16 was rated Partially effective for UC-11 (F-04). Signals cannot be used for position sizing until validated.

## Risk acceptance log

| Risk | Residual | Accepted by | Date | Review |
|---|---|---|---|---|
| R-01 | High | **Not accepted.** Remediation required | – | AIGC monthly |
| R-04, R-05, R-06, R-10, R-11, R-12, R-13, R-18 | Medium | Risk owner | 30 Sep 2026 | Quarterly |
| R-07, R-09, R-15, R-16, R-17 | Low | Risk owner | 30 Sep 2026 | Annually |

<!-- nav -->
---

[← AI Risk Assessment Methodology](01-risk-assessment-methodology.md) · [Home](../README.md) · [AI Impact Assessment: UC-04 Due Diligence Automation →](03-impact-assessment-uc04-due-diligence.md)
<!-- /nav -->
