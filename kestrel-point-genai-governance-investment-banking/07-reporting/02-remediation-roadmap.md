# 02 · Remediation Roadmap

| Field | Value |
|---|---|
| As at | 15 October 2026 |
| Owner | AI Governance Lead |
| Tracked at | AIGC monthly |

## Open actions

| ID | Source | Action | Owner | Due | Status | Risk impact when done |
|---|---|---|---|---|---|---|
| RA-01 | F-01 | Block creation of unmanaged browser profiles on all firm laptops by device policy | Head of Security Engineering | 30 Nov 2026 | In progress | R-01 likelihood 2 → 1 |
| RA-02 | F-01 | Extend DLP browser extension to all supported browsers and profiles; retest 25 samples | Head of Security Engineering | 15 Dec 2026 | Not started | R-01 residual High (10) → Medium (5) |
| RA-03 | F-02 | Fix the 8 remaining overshared sites; exclude any unfixed site from Copilot search | Head of IT Infrastructure | 30 Nov 2026 | In progress | R-02 stays Medium, unblocks rollout |
| RA-04 | F-02 | Automate a quarterly oversharing scan with alerts to site owners | Head of IT Infrastructure | 31 Dec 2026 | Not started | Keeps KRI-08 at 0 |
| RA-05 | F-03 | Make second-person sign-off mandatory before export for UC-08 and UC-13 in Kestrel Assist | Head of AI Platform | 30 Nov 2026 | In progress | KRI-05 to ≥ 95% |
| RA-06 | F-03 | Brief the credit team on L3 review and re-sample 20 outputs in December | COO Front Office | 15 Dec 2026 | Not started | Confirms fix |
| RA-07 | F-04 | Obtain SignalCurrent model documentation, or select an alternative vendor | Head of Markets | 31 Jan 2027 | In progress | R-08 stays Medium |
| RA-08 | F-04 | Validate the sentiment model before signals are used for position sizing | Head of Model Risk | 31 Mar 2027 | Not started | KRI-07 to 0 |
| RA-09 | R-14 | Add AI error case studies to AI in Deals training; monthly sampling of signed-off outputs | Head of Learning | 31 Jan 2027 | Not started | R-14 likelihood 3 → 2 |
| RA-10 | Tabletop | Add client-notification decision tree to the incident playbook | General Counsel | 31 Oct 2026 | Complete | – |
| RA-11 | UC-07 | Move NoteStream EU meetings to EU hosting | COO Front Office | 31 Dec 2026 | In progress | Lifts UC-07 condition |
| RA-12 | Programme | ISO/IEC 42001 gap assessment | AI Governance Lead | 31 Mar 2027 | Not started | Certification readiness |

## Timeline

```
Oct 2026   ■ RA-10 decision tree (done)
Nov 2026   ■ RA-01 browser profiles   ■ RA-03 sites   ■ RA-05 mandatory sign-off
Dec 2026   ■ RA-02 DLP retest   ■ RA-04 scan automation   ■ RA-06 re-sample   ■ RA-11 EU hosting
           → Copilot rollout to 400 users if RA-03 complete
Jan 2027   ■ RA-07 vendor decision   ■ RA-09 training update
Mar 2027   ■ RA-08 validation   ■ RA-12 ISO/IEC 42001 gap assessment
```

## Projected residual risk after actions

| Rating | Now | After RA-01 to RA-09 |
|---|---|---|
| Critical | 0 | 0 |
| High | 1 | 0 |
| Medium | 12 | 13 |
| Low | 5 | 5 |

- **R-01** moves from High (10) to Medium (5) and back within appetite.
- **R-14** falls from 9 to 6 but stays Medium.
- No risk would remain outside appetite.

<!-- nav -->
---

[← Board AI Risk Report: Q3 2026](01-board-ai-risk-report-q3-2026.md) · [Home](../README.md) · [Maturity Assessment and Lessons Learned →](03-maturity-assessment-and-lessons.md)
<!-- /nav -->
