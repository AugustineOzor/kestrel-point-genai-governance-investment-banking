# 01 · AI Monitoring and Key Risk Indicators

| Field | Value |
|---|---|
| Document ID | KPC-AIG-KRI-001 |
| Owner | AI Governance Lead |
| Reported to | AIGC monthly, Board Risk Committee quarterly |

## 1. What is monitored

| Layer | Signals | Source | Watched by |
|---|---|---|---|
| Access | Blocked public AI attempts, new AI domains | Web proxy | Security Operations |
| Data | DLP blocks, restricted list hits, cross-project retrieval denials | AI gateway, DLP | Security Operations, Compliance |
| Usage | Users, use cases, prompts used, sign-off rates | Kestrel Assist | AI Platform, AI Governance |
| Quality | Recall tests, sampled error rate, user error reports | C-14, C-11 testing, feedback button | AI Governance |
| Models | Drift, performance, override rates | Model monitoring (C-17) | Model Risk |
| Markets | Sentiment signals linked to trades | Surveillance (C-19) | Compliance Surveillance |

## 2. KRIs and thresholds

Green is within appetite. Amber needs owner action. Red is escalated to the AIGC.

| KRI | Green | Amber | Red | Q3 2026 | Status |
|---|---|---|---|---|---|
| KRI-01 Confirmed MNPI exposures to unapproved AI | 0 | – | ≥ 1 | 0 | 🟢 |
| KRI-02 Blocked public GenAI attempts per month | < 300 | 300–600 | > 600 | 428 average (1,284 in quarter) | 🟠 |
| KRI-03 DLP blocks on AI uploads per month | < 10 | 10–25 | > 25 | 12 average (37 in quarter) | 🟠 |
| KRI-04 Restricted list hits from public-side users | < 5 | 5–10 | > 10 | 3 | 🟢 |
| KRI-05 Independent sign-off rate in sampled outputs | ≥ 95% | 85–94% | < 85% | 85% (34 of 40) | 🟠 |
| KRI-06 Due diligence recall | ≥ 95% | 90–94% | < 90% | 96.8% | 🟢 |
| KRI-07 AI models in use without validation | 0 | 1 | ≥ 2 | 1 (SignalCurrent) | 🟠 |
| KRI-08 Overshared sites with MNPI files | 0 | 1–10 | > 10 | 8 | 🟠 |
| KRI-09 AI incidents, Sev-1 or Sev-2 | 0 | 1 | ≥ 2 | 1 (Sev-2) | 🟠 |
| KRI-10 AI training completion | ≥ 95% | 90–94% | < 90% | 94% (1,081 of 1,150) | 🟠 |
| KRI-11 AI vendor reviews overdue | 0 | 1 | ≥ 2 | 0 | 🟢 |
| KRI-12 Risk model override rate | < 10% | 10–20% | > 20% | 7% | 🟢 |

**Q3 summary:** 5 green, 7 amber, 0 red.

## 3. Trend: blocked public GenAI attempts

| Month | Attempts |
|---|---|
| April 2026 (block switched on) | 1,742 |
| May 2026 | 1,198 |
| June 2026 | 966 |
| July 2026 | 512 |
| August 2026 | 401 |
| September 2026 | 371 |

The fall follows the launch of Kestrel Assist in June. The remaining attempts are concentrated in two teams that have not yet moved to Kestrel Assist.

## 4. How KRIs link to risks

| KRI | Risks |
|---|---|
| KRI-01, KRI-02, KRI-03 | R-01 |
| KRI-04, KRI-08 | R-02, R-08 |
| KRI-05 | R-03, R-14 |
| KRI-06 | R-05 |
| KRI-07, KRI-12 | R-06, R-08 |
| KRI-09 | All |
| KRI-10 | R-01, R-14 |
| KRI-11 | R-12 |

<!-- nav -->
---

[← AI Vendor Due Diligence](../05-third-party/01-ai-vendor-due-diligence.md) · [Home](../README.md) · [AI Incident Response Playbook →](02-ai-incident-response-playbook.md)
<!-- /nav -->
