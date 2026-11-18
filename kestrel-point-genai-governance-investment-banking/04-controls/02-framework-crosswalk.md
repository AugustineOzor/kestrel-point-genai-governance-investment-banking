# 02 · Framework Crosswalk

Maps each Kestrel control to the frameworks and rules it supports. One control can satisfy several obligations, which avoids duplicate controls and duplicate testing.

**Key:** AI RMF = NIST AI RMF 1.0 subcategory. 42001 = ISO/IEC 42001:2023 Annex A control. EU AI Act applies to the Frankfurt entity. FS rules = financial services obligations from the [regulatory landscape](../00-programme/03-regulatory-landscape.md).

| Control | NIST AI RMF | ISO/IEC 42001 Annex A | EU AI Act | FS rules and other |
|---|---|---|---|---|
| C-01 Approved tools, public GenAI blocked | GOVERN 1.6, MAP 4.1 | A.9.2, A.9.4 | – | MAR Art. 16 (systems to prevent insider dealing), s15(g) |
| C-02 DLP to AI domains | MANAGE 2.4, MEASURE 2.10 | A.7.2, A.9.2 | – | MAR, GDPR Art. 32, OWASP LLM02 |
| C-03 Use case intake and approval | GOVERN 1.3, MAP 1.1 | A.5.2, A.6.1.3 | – | SM&CR accountability |
| C-04 AI inventory and attestation | GOVERN 1.6 | A.4.2, A.6.2.7 | – | FINRA RN 24-09 (supervision of AI use) |
| C-05 AI training | GOVERN 2.2 | A.4.6 | **Art. 4 AI literacy** | FCA SYSC 5 (competence) |
| C-06 Kestrel Assist gateway | MEASURE 2.7, MANAGE 4.1 | A.6.2.6, A.6.2.8 | – | GDPR Art. 32, DORA Art. 9 |
| C-07 Entitlement-aware retrieval | MAP 4.2, MEASURE 2.10 | A.7.4, A.9.2 | – | Information barriers: SYSC 10, s15(g), MAR |
| C-08 Copilot oversharing review | MANAGE 1.3 | A.4.4, A.9.2 | – | SYSC 10, MAR |
| C-09 Sensitivity labels | MAP 4.2 | A.7.4, A.7.5 | – | GDPR Art. 25 |
| C-10 Prompt library governance | GOVERN 1.4, MANAGE 2.4 | A.6.2.3, A.6.2.5 | – | FINRA 3110 (supervision of templates) |
| C-11 Human review and sign-off | GOVERN 3.2, MAP 3.5 | A.9.3, A.9.4 | Art. 26(2) human oversight (good practice; required only for high-risk) | FINRA 3110, COBS 4 |
| C-12 Compliance pre-use review | GOVERN 1.1 | A.8.5, A.9.2 | – | **FINRA 2210**, COBS 4 |
| C-13 Claim substantiation | MEASURE 2.5 | A.8.2 | – | FINRA 2210(d), COBS 4 |
| C-14 Due diligence recall testing | MEASURE 2.3, MEASURE 2.5 | A.6.2.4 | – | – |
| C-15 EUC register and model check | MEASURE 2.5 | A.6.2.4 | – | SR 11-7 (model use) |
| C-16 Model validation | MEASURE 2.3, MEASURE 2.5 | A.6.2.4, A.6.2.5 | – | **SR 11-7**, PRA SS1/23 |
| C-17 Performance and drift monitoring | MEASURE 3.1, MANAGE 4.1 | A.6.2.6 | Art. 26(5) monitoring (good practice) | SR 11-7, SS1/23 |
| C-18 Credit model fairness testing | MEASURE 2.11 | A.5.4, A.7.4 | Annex III 5(b) watch | Equality and fair treatment principles |
| C-19 Sentiment signals in surveillance | MEASURE 3.1 | A.6.2.8 | – | **MAR Art. 16** |
| C-20 Restricted and watch list check | MANAGE 1.3 | A.9.2 | – | MAR, SYSC 10, s15(g) |
| C-21 Records retention | GOVERN 1.1, MEASURE 3.1 | A.6.2.8 | Art. 26(6) logs (good practice) | **SEC 17a-4**, FCA SYSC 9 and 10A |
| C-22 DPIA and recording notice | MAP 5.1, MEASURE 2.10 | A.5.4, A.8.2 | Art. 26(9) uses GDPR DPIA | **GDPR Art. 13, 35** |
| C-23 Prompt injection filter | MEASURE 2.7 | A.6.2.6 | – | OWASP LLM01 |
| C-24 AI red team | MEASURE 2.7 | A.6.2.4 | – | OWASP LLM Top 10 |
| C-25 AI vendor due diligence | GOVERN 6.1, MANAGE 3.1 | A.10.3 | – | **DORA Art. 28**, SYSC 8 outsourcing |
| C-26 AI contract clauses | GOVERN 6.1 | A.10.2, A.10.3 | – | DORA Art. 30, GDPR Art. 28 |
| C-27 Tier-based oversight in tool | GOVERN 3.2 | A.9.3 | – | FINRA 3110 |
| C-28 Data source legal review | MAP 4.1 | A.7.3, A.7.5 | – | Copyright, website terms |
| C-29 AI service continuity | GOVERN 6.2, MANAGE 2.4 | A.4.5 | – | **DORA Art. 11, 28**, FCA operational resilience |
| C-30 AI incident management | MANAGE 4.3 | A.3.3, A.8.4 | – | GDPR Art. 33, DORA Art. 17–19 |

## Coverage check

| Framework area | Covered by | Gap |
|---|---|---|
| NIST AI RMF GOVERN | C-01, C-03, C-04, C-05, C-10, C-11, C-12, C-21, C-25, C-26, C-27, C-29 | None |
| NIST AI RMF MAP | C-01, C-03, C-07, C-09, C-11, C-22, C-28 | None |
| NIST AI RMF MEASURE | C-02, C-06, C-07, C-13 to C-19, C-21, C-22, C-23, C-24 | None |
| NIST AI RMF MANAGE | C-02, C-06, C-08, C-10, C-17, C-20, C-25, C-29, C-30 | None |
| ISO/IEC 42001 Annex A.10 third parties | C-25, C-26 | A.10.4 (customers) not applicable: Kestrel does not supply AI systems to clients |
| ISO/IEC 42001 Annex A.5 impact assessment | C-03, C-18, C-22 | Societal impact (A.5.5) assessed as low for all use cases; documented in each impact assessment |

> Clause and subcategory references were checked against the published texts in May 2026. Note that some EU AI Act deployer duties in Article 26 apply in law only to high-risk systems. Kestrel adopts them as good practice for its Tier 1 use cases.

<!-- nav -->
---

[← AI Control Library](01-control-library.md) · [Home](../README.md) · [Control Testing Workpapers: Q3 2026 →](03-control-testing-workpapers.md)
<!-- /nav -->
