# 01 · AI Vendor Due Diligence

| Field | Value |
|---|---|
| Document ID | KPC-AIG-TPR-001 |
| Owner | Head of Procurement, with AI Governance and Information Security |
| Controls | C-25 (due diligence), C-26 (contract clauses), C-29 (continuity and exit) |

## 1. When AI due diligence applies

Standard third-party risk management applies to every vendor. The **AI supplement** applies when a vendor:

- provides an AI model or AI feature that processes Kestrel data, or
- adds AI features to a service Kestrel already uses (embedded AI).

Existing vendors that switch on AI features must be reassessed before the feature is enabled.

## 2. AI supplement questionnaire (extract)

| # | Area | Question | Evidence expected |
|---|---|---|---|
| 1 | Data use | Is customer data used to train or improve any model, including foundation models from your providers? | Contract clause, data flow diagram |
| 2 | Retention | How long are prompts, files and outputs kept? Can we set zero retention? | Configuration screenshot, policy |
| 3 | Location | Where are data processed and stored, including sub-processors? | Sub-processor list, region settings |
| 4 | Models | Which models do you use, from whom, and how do you manage version changes? | Model card, change notification process |
| 5 | Performance | How do you measure accuracy for our use case? Will you share test results? | Validation report, benchmark on sample data |
| 6 | Security | How do you protect against prompt injection, data leakage between customers and model theft? | Pen test or red team summary, OWASP LLM controls |
| 7 | Assurance | Do you hold SOC 2 Type II, ISO/IEC 27001 or ISO/IEC 42001? | Current report or certificate |
| 8 | Transparency | Can you explain how outputs are produced to the level our model risk team needs? | Model documentation |
| 9 | Incidents | Will you notify us of AI incidents within 24 hours? | Contract clause |
| 10 | Exit | How do we get our data back and confirm deletion at exit? | Exit plan, deletion certificate process |

## 3. Assessments completed

### VaultLens (UC-04 VDR contract review)

| Area | Finding | Rating |
|---|---|---|
| Data use | No training on customer data, confirmed in contract | ✔ |
| Retention | Deleted 30 days after project close | ✔ |
| Location | EU (Ireland). No sub-processors outside EU | ✔ |
| Performance | Shared benchmark; Kestrel ran its own recall test (96.1%) | ✔ |
| Security | SOC 2 Type II (Mar 2026), annual pen test, prompt injection testing | ✔ |
| Transparency | Model card provided, version change notice 30 days | ✔ |
| **Decision** | **Approved.** Critical ICT provider for the GmbH: added to DORA register of information | |

### NoteStream (UC-07 meeting transcription)

| Area | Finding | Rating |
|---|---|---|
| Data use | No training on customer data | ✔ |
| Retention | Configurable; set to 90 days for audio | ✔ |
| Location | **US only today.** EU region launching Q4 2026 | ⚠ |
| Security | SOC 2 Type II (Jan 2026) | ✔ |
| Transparency | Speaker identification accuracy published | ✔ |
| **Decision** | **Approved with conditions.** EU client meetings stay on Teams transcription until NoteStream EU hosting is live (due 31 Dec 2026). Standard contractual clauses in place | |

### SignalCurrent (UC-11 market sentiment)

| Area | Finding | Rating |
|---|---|---|
| Data use | Kestrel sends no data; receives signals only | ✔ |
| Data sources | Social media and news. Vendor confirms licensed sources; legal review completed (C-28) | ✔ |
| Performance | Marketing back-tests only. No independent validation | ⚠ |
| Transparency | **Model documentation refused** as proprietary | ✘ |
| Assurance | ISO/IEC 27001 certificate | ✔ |
| **Decision** | **Approved with conditions.** Signals are information only and cannot drive position sizing until Model Risk validates them (finding F-04). If documentation is not provided by 31 Jan 2027, Markets will move to an alternative vendor | |

### Microsoft 365 Copilot (UC-07, UC-14)

Assessed as an extension of the existing Microsoft 365 relationship. Enterprise data protection terms confirm prompts and responses are not used to train foundation models. The main risk is internal (oversharing), not the vendor, so the key control is C-08.

## 4. Contract clause checklist (C-26)

| Clause | VaultLens | NoteStream | SignalCurrent |
|---|---|---|---|
| No training on Kestrel data | ✔ | ✔ | n/a (no data sent) |
| Retention and deletion terms | ✔ | ✔ | n/a |
| Sub-processor approval | ✔ | ✔ | ✔ |
| Audit and information rights | ✔ | ✔ | ✔ |
| 24-hour incident notice | ✔ | ✔ | ✔ |
| Model change notice | ✔ 30 days | ✔ 14 days | ✘ Under negotiation |
| Exit and data return | ✔ | ✔ | ✔ |
| DORA Article 30 provisions (GmbH) | ✔ | ✔ | ✔ |

<!-- nav -->
---

[← Control Testing Workpapers: Q3 2026](../04-controls/03-control-testing-workpapers.md) · [Home](../README.md) · [AI Monitoring and Key Risk Indicators →](../06-monitoring/01-monitoring-and-kri-framework.md)
<!-- /nav -->
