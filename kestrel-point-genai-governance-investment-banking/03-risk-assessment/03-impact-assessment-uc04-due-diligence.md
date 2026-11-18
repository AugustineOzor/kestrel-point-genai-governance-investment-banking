# 03 · AI Impact Assessment: UC-04 Due Diligence Automation

| Field | Value |
|---|---|
| Document ID | KPC-AIG-AIA-004 |
| Use case | UC-04 Due diligence automation |
| Tier | 1 |
| Assessor | AI Governance Lead |
| Contributors | Head of Advisory, Legal, Compliance, Head of AI Platform, VaultLens account team |
| Aligned to | ISO/IEC 42001 clause 6.1.4 and Annex A.5, NIST AI RMF Map 1–5 |
| Decision | **Approved** by AIGC, 9 June 2026, with the controls below |

## 1. Description

Deal teams upload a target's contracts to the virtual data room (VDR). VaultLens scans them for change-of-control, most-favoured-nation, non-compete, exclusivity and assignment clauses. Kestrel Assist then summarises each hit, explains the trigger and notice periods, and gives a High, Medium or Low rating with the document name and section number.

**Before AI:** two associates spent about 60 hours reading 400 contracts on a mid-size sell-side deal.
**With AI:** first-pass extraction takes about 2 hours. Associates spend about 14 hours checking hits and samples. Lawyers review all High items.

## 2. Stakeholders and who could be affected

| Stakeholder | How they are affected | Potential harm |
|---|---|---|
| Client (buyer or seller) | Relies on issues list for price and terms | Missed clause leads to a lower price, a broken deal or a post-closing claim |
| Target company | Its contracts are processed by a vendor | Confidentiality breach |
| Counterparties named in contracts | Their contract terms are processed | Confidentiality breach |
| Deal team associates | Do less manual reading | Over-reliance, loss of skill in reading contracts |
| Kestrel | Advice relies on output | Liability claim, reputational damage, MAR breach if MNPI leaks |

## 3. Benefits

- About 75% less time on first-pass review.
- More consistent extraction across hundreds of contracts.
- Earlier visibility of deal-breakers, while there is still time to negotiate.

## 4. Risks

| Risk | Description | Register |
|---|---|---|
| False negatives | The model misses a clause written in unusual language or buried in an amendment | R-05 |
| Confabulation | The summary misstates a notice period or trigger | R-03 |
| MNPI leakage | VDR data leaves approved environments or crosses the wall | R-01, R-02 |
| Vendor data use | VaultLens retains or trains on contracts | R-12 |
| Prompt injection | A contract contains hidden text that changes the AI's behaviour | R-11 |
| Over-reliance | Associates stop reading contracts not flagged | R-14 |

## 5. Testing before approval

| Test | Method | Result |
|---|---|---|
| Recall (clauses found / clauses present) | 3 closed deals, 1,120 contracts, compared with lawyers' original review | **96.1%** overall. Change of control 98.4%, MFN 93.0% |
| Precision (correct hits / all hits) | Same sample | 88.7%. False positives are cheap to dismiss |
| Location accuracy | Document and section reference correct | 99.2% |
| Prompt injection | 12 seeded contracts with hidden instructions in white text and footers | 11 of 12 blocked by gateway filter. 1 changed the summary's tone but not the extraction. Filter rule added and retested: 12 of 12 |
| Entitlements | Non-deal-team user tries to query a project workspace | Blocked in 20 of 20 attempts |

**Acceptance threshold:** recall of at least 95% overall and at least 90% for every clause type. Met.

## 6. Controls required

| Control | How it applies to UC-04 |
|---|---|
| C-06 | Only through Kestrel Assist gateway. No direct VaultLens access |
| C-07 | Workspace per project codename. Deal team list from entitlement system |
| C-11 | Associate reviews every hit. Lawyer reviews all High items |
| C-14 | Monthly recall test: 250 clauses sampled from live deals and checked manually |
| C-23 | Gateway prompt injection filter on all VDR content |
| C-25, C-26 | VaultLens contract: EU hosting, no training, deletion within 30 days of deal close |

## 7. Residual risk and decision

Residual risk for R-05 is **Medium (2 x 4 = 8)** and within appetite with monthly recall testing. The AIGC approved UC-04 on 9 June 2026.

**Conditions:**
1. MFN recall is lower (93.0%). Associates must manually search for "most favoured" and "most favored" in every contract set.
2. Re-test on any VaultLens model update.
3. Review in December 2026.

## 8. Post-launch results (Q3 2026)

| Measure | Target | Q3 result |
|---|---|---|
| Monthly recall test | ≥ 95% | 96.8% (242 of 250 clauses) |
| Deals using UC-04 | – | 17 |
| Material clause missed and found later | 0 | 0 |

<!-- nav -->
---

[← AI Risk Register](02-ai-risk-register.md) · [Home](../README.md) · [AI Impact Assessment: UC-12 AI-Driven Risk Management →](04-impact-assessment-uc12-risk-models.md)
<!-- /nav -->
