# 03 · Control Testing Workpapers: Q3 2026

| Field | Value |
|---|---|
| Document ID | KPC-AIG-TST-2026Q3 |
| Period tested | 1 July – 30 September 2026 |
| Tested by | AI Governance (2nd line), independent of control operators |
| Reviewed by | Head of Compliance Monitoring |
| Scope | 8 key controls (★ in the [control library](01-control-library.md)) |

## Summary

| Control | Design | Operating effectiveness | Result | Finding |
|---|---|---|---|---|
| C-01 Approved tools, public GenAI blocked | Effective | 25 of 25 passed | **Effective** | – |
| C-02 DLP to AI domains | Partially effective | 22 of 25 passed | **Partially effective** | F-01 |
| C-06 Kestrel Assist gateway | Effective | 25 of 25 passed | **Effective** | – |
| C-08 Copilot oversharing review | Effective | 39 of 47 sites fixed | **Partially effective** | F-02 |
| C-11 Human review and sign-off | Effective | 34 of 40 passed | **Partially effective** | F-03 |
| C-14 Due diligence recall testing | Effective | 3 of 3 months performed, threshold met | **Effective** | – |
| C-16 Model validation | Effective | 2 of 3 in-scope models validated | **Partially effective** | F-04 |
| C-21 Records retention | Effective | 40 of 40 passed | **Effective** | – |

**Result: 4 Effective, 4 Partially effective, 0 Ineffective.**

Sample sizes follow the firm's controls testing standard: 25 for continuous automated controls, 40 for manual per-item controls, full population where small.

---

## C-01 · Approved tools, public GenAI blocked

**Test:** From 5 managed laptops in 5 departments, attempted to reach 25 public GenAI domains taken from the proxy's AI category list and recent threat intelligence.
**Result:** 25 of 25 blocked with the firm's "use Kestrel Assist" page. Proxy logs showed 1,284 blocked attempts in Q3, down from 3,906 in Q2.
**Conclusion:** Effective.

## C-02 · DLP to AI domains

**Test:** Seeded 25 test documents with MNPI labels and fake project codenames. Tried to paste or upload them to AI sites allowed for research (for example, translation tools on the approved list) from different browsers and profiles.
**Result:** 22 of 25 blocked. **3 not blocked.** All three were uploads from a second, unmanaged Edge browser profile that users can create themselves. DLP browser extension is only enforced in the managed profile.
**Conclusion:** Partially effective. → **F-01**

## C-06 · Kestrel Assist gateway

**Test:** 25 random sessions from Q3 traced end to end. Checked SSO authentication, DLP scan, logging of prompt, retrieved documents and output, and model provider zero-retention setting in the tenant configuration.
**Result:** 25 of 25 complete. Zero-retention flag confirmed in configuration and contract (clause 7.3).
**Conclusion:** Effective.

## C-08 · Copilot oversharing review

**Test:** Reviewed the oversharing scan from June 2026 and the fixes made by 30 September. Re-scanned the 47 sites flagged as holding MNPI-labelled files shared with "Everyone except external users" or groups of more than 200.
**Result:** 39 of 47 fixed (83%). **8 still overshared**, of which 3 hold live deal files. Copilot is limited to 60 pilot users, none of whom can reach the 8 sites, so no exposure occurred.
**Conclusion:** Partially effective. → **F-02**

## C-11 · Human review and sign-off

**Test:** 40 AI-assisted outputs sampled from Tier 1 and client-facing Tier 2 use cases (UC-03: 15, UC-08: 10, UC-13: 10, UC-04: 5). Checked for L3 sign-off by a VP or above who was not the author, and for source citations.
**Result:** 34 of 40 passed (85%).

| Exception | Count | Detail |
|---|---|---|
| Signed off by the author, not a second person | 4 | All UC-13 credit memos from one team |
| No sign-off record, but email shows review happened | 2 | UC-08 comps in a fairness opinion pack |

No exception led to an error reaching a client.
**Conclusion:** Partially effective. → **F-03**

## C-14 · Due diligence recall testing

**Test:** Re-performed the July, August and September recall tests and checked results.

| Month | Clauses sampled | Found by AI | Recall |
|---|---|---|---|
| July | 80 | 77 | 96.3% |
| August | 85 | 82 | 96.5% |
| September | 85 | 83 | 97.6% |
| **Q3** | **250** | **242** | **96.8%** |

All months met the 95% threshold. The 8 missed clauses were reviewed: 5 were MFN clauses in amendments, which is the known weakness covered by the manual MFN search.
**Conclusion:** Effective.

## C-16 · Model validation

**Test:** Checked the model inventory for AI and ML models used in risk, valuation or trading decisions. Inspected validation reports.

| Model | Use case | Validated? |
|---|---|---|
| MDL-RSK-031 Scenario stress engine | UC-12 | Yes, July 2026 |
| MDL-RSK-032 Corporate credit score | UC-12 | Yes, July 2026 |
| SignalCurrent sentiment model (vendor) | UC-11 | **No.** Vendor has not provided model documentation. Signals in use by the Markets desk as "information only" |

**Conclusion:** Partially effective. → **F-04**

## C-21 · Records retention

**Test:** 40 AI items selected from usage logs (20 Kestrel Assist outputs, 10 NoteStream transcripts, 10 Copilot Teams recaps). Searched for each in the records archive.
**Result:** 40 of 40 found with correct metadata and retention class.
**Conclusion:** Effective.

---

## Findings

| ID | Control | Finding | Rating | Owner | Action | Due |
|---|---|---|---|---|---|---|
| F-01 | C-02 | DLP not enforced in unmanaged browser profiles; 3 of 25 test uploads succeeded | **High** | Head of Security Engineering | Block creation of unmanaged browser profiles by device policy; extend DLP to all profiles | 15 Dec 2026 |
| F-02 | C-08 | 8 of 47 overshared sites not fixed, 3 with live deal files | **High** | Head of IT Infrastructure | Fix remaining sites; exclude from Copilot search until fixed; quarterly re-scan | 31 Dec 2026 |
| F-03 | C-11 | 6 of 40 outputs lacked independent sign-off evidence | Medium | COO Front Office | Make second-person sign-off mandatory in Kestrel Assist for UC-08 and UC-13 exports; brief the credit team | 30 Nov 2026 |
| F-04 | C-16 | Vendor sentiment model not validated | Medium | Head of Markets / Head of Model Risk | Obtain documentation or replace vendor; validate; signals limited to information only until then | 31 Jan 2027 |

<!-- nav -->
---

[← Framework Crosswalk](02-framework-crosswalk.md) · [Home](../README.md) · [AI Vendor Due Diligence →](../05-third-party/01-ai-vendor-due-diligence.md)
<!-- /nav -->
