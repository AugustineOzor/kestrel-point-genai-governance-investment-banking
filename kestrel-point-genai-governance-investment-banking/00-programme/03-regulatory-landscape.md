# 03 · Regulatory and Framework Landscape

Kestrel operates in the UK, US and EU. No single law covers its AI use, so the programme combines AI-specific frameworks with the financial services rules that already apply.

## AI frameworks adopted

| Framework | How Kestrel uses it |
|---|---|
| **NIST AI RMF 1.0** and the **Generative AI Profile (NIST AI 600-1)** | Programme structure: Govern, Map, Measure, Manage. GenAI risks such as confabulation, information security and data privacy shape the risk register |
| **ISO/IEC 42001:2023** | Management system design: policy, roles, risk assessment, impact assessment, Annex A controls. Certification readiness targeted for 2027 |
| **OWASP Top 10 for LLM Applications (2025)** | Technical risks for Kestrel Assist: prompt injection, sensitive information disclosure, excessive agency |

## AI regulation

| Rule | Applies to | What it means for Kestrel |
|---|---|---|
| **EU AI Act** (Regulation (EU) 2024/1689) | Kestrel Point Capital GmbH as a **deployer** | **Article 4 AI literacy** applies now: staff using AI must have sufficient AI literacy. None of the 14 use cases is a prohibited practice under Article 5. Creditworthiness assessment of **natural persons** is high-risk under Annex III point 5(b), but UC-12 scores **corporate** counterparties only, so it is not high-risk. Kestrel keeps this assessment under review, because Annex III obligations apply from **2 December 2027** following the Digital Omnibus amendments |

## Financial services rules that apply to AI use

| Rule | Jurisdiction | AI relevance | Use cases |
|---|---|---|---|
| **Market Abuse Regulation** (EU MAR and UK MAR): Art. 7 inside information, Art. 14 insider dealing, Art. 16 surveillance | EU, UK | MNPI in prompts, AI-derived trading signals, information barriers | UC-04, UC-05, UC-11, UC-14 |
| **Securities Exchange Act s15(g)** | US | Broker-dealers must keep written policies to prevent misuse of MNPI | UC-03, UC-04, UC-07 |
| **FINRA Rule 2210** (communications with the public) and **Rule 3110** (supervision) | US | AI-drafted pitch and outreach material must be fair and balanced and supervised | UC-03, UC-09 |
| **FINRA Regulatory Notice 24-09** | US | Reminds firms that existing rules apply to GenAI and that supervision and recordkeeping must cover it | All |
| **SEC Rule 17a-4** | US | Business communications, including AI-generated ones, must be retained | UC-03, UC-07, UC-09 |
| **FCA COBS 4** (fair, clear and not misleading) and **SYSC 10** (conflicts of interest) | UK | Client communications and information barriers | UC-03, UC-09, UC-14 |
| **Fed SR 11-7** (model risk management) and **PRA SS1/23** | US, UK | AI and ML models used in risk and valuation need inventory, validation and monitoring. SS1/23 is adopted as good practice | UC-06, UC-11, UC-12 |
| **GDPR** and **UK GDPR** | EU, UK | Lawful basis and DPIAs for meeting recordings, executive profiling and outreach | UC-07, UC-09 |
| **DORA** (Regulation (EU) 2022/2554) | Kestrel Point Capital GmbH | AI vendors that support critical functions go in the ICT third-party register of information, with exit plans | UC-04, UC-07, UC-11 |

## Summary: which obligations drive which controls

| Obligation | Main controls |
|---|---|
| Protect MNPI and keep information barriers | C-01, C-02, C-06, C-07, C-08, C-09, C-20 |
| Fair, accurate and supervised communications | C-11, C-12, C-13 |
| Model risk management | C-15, C-16, C-17, C-18 |
| Recordkeeping | C-21 |
| Data protection | C-09, C-22 |
| Third-party and ICT risk | C-25, C-26, C-29 |
| AI literacy | C-05 |

The full mapping is in the [framework crosswalk](../04-controls/02-framework-crosswalk.md).

> This is a portfolio summary, not legal advice. Each obligation was confirmed with Legal and Compliance before controls were designed.

<!-- nav -->
---

[← AI Governance Charter](02-governance-charter.md) · [Home](../README.md) · [AI Use Case Inventory →](../01-inventory/01-ai-use-case-inventory.md)
<!-- /nav -->
