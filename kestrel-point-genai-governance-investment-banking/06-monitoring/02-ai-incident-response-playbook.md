# 02 · AI Incident Response Playbook

| Field | Value |
|---|---|
| Document ID | KPC-AIG-IRP-001 |
| Owner | AI Governance Lead (control C-30) |
| Works with | Information Security Incident Response Plan, Market Abuse Policy, Personal Data Breach Procedure, DORA incident reporting procedure (GmbH) |

## 1. What counts as an AI incident

Any event where AI use causes, or could have caused, harm to clients, the firm, individuals or markets. Examples:

- MNPI or client data entered into an unapproved AI tool, or shown to someone across an information barrier.
- A wrong AI-generated figure or claim reaching a client or the market.
- An AI model producing materially wrong risk, valuation or credit outputs.
- A prompt injection or other attack on an AI system.
- A vendor reporting that it retained or exposed Kestrel data.

## 2. Severity

| Severity | Definition | Examples | Response time | Notify |
|---|---|---|---|---|
| **Sev-1** | Confirmed MNPI leak outside the firm, client harm or likely regulatory notification | Deal terms pasted into a public chatbot; wrong figure in a published offering document | Immediate, 24/7 | CRO, General Counsel, Head of Compliance, CEO. BRC within 24 hours |
| **Sev-2** | MNPI exposed inside the firm across a barrier, or a material error caught before it reached a client | Copilot shows a deal file to someone not on the deal | Within 4 hours | AIGC chair, Head of Compliance, DPO if personal data |
| **Sev-3** | Control failure with no exposure, or a minor error | AI error caught at review; missing recording notice | Within 2 business days | AI Governance Lead, control owner |

## 3. Response steps

| Step | Actions | Lead |
|---|---|---|
| **1. Report** | Anyone reports to `ai-incident@kestrelpoint.example` or the AI incident form within 1 hour of noticing | Reporter |
| **2. Triage** | Confirm facts, set severity, open a case, assemble the team | AI Governance on-call |
| **3. Contain** | Revoke access, disable the prompt or feature, pull the document, ask the vendor to delete data, preserve logs | AI Platform, Security |
| **4. Assess** | Is the information inside information? Who saw it? Is personal data involved? Is a regulator notification needed? | Compliance (MAR), DPO (GDPR), Legal |
| **5. Notify** | Internal escalation by severity. External: FCA, SEC/FINRA, BaFin under DORA, data protection authority within 72 hours if required, affected clients | General Counsel, Compliance, DPO |
| **6. Recover** | Fix the control, restore service, confirm the fix with a test | Control owner |
| **7. Learn** | Root cause analysis within 10 business days for Sev-1 and Sev-2. Update risks, controls, training | AI Governance Lead |

## 4. MNPI-specific actions (Compliance)

1. Identify the issuer and whether the information is inside information.
2. Add the issuer and any affected counterparties to the **watch list**; consider the **restricted list**.
3. Identify everyone who may have received the information and treat them as insiders (update insider lists under MAR Article 18 if applicable).
4. Run a surveillance look-back on trading in the issuer.
5. Decide, with Legal, whether a suspicious transaction and order report or other notification is needed.

## 5. Q3 2026 incidents

| Ref | Date | Severity | What happened | Root cause | Actions |
|---|---|---|---|---|---|
| AI-INC-2026-004 | 14 Jul 2026 | **Sev-2** | A Copilot pilot user in Coverage asked for "latest updates on my sector" and received a summary that drew on a draft board paper for Project HERON, a deal they were not on | The Project HERON site was shared with a 450-person group | Site permissions fixed within 2 hours. Compliance confirmed no trading by the user. User added to Project HERON insider list. Triggered re-scan; led to finding F-02 |
| AI-INC-2026-005 | 22 Aug 2026 | Sev-3 | Kestrel Assist inserted a 2024 EBITDA figure that was 12% higher than the data book in a pitchbook draft (UC-03) | Model confused adjusted and reported EBITDA in two source files | Caught at Compliance pre-use review (C-12). Prompt updated to require cell references for every figure. Used as a training example |
| AI-INC-2026-006 | 9 Sep 2026 | Sev-3 | NoteStream recorded an external client call without the recording notice in the meeting invite | New invite template from a team outside the rollout did not include the notice | The bot still announced recording at the start of the call. DPO assessed: no breach notification needed. Template fixed firm-wide |

## 6. Tabletop exercise: Project KINGFISHER

Run on 29 September 2026 with Compliance, Legal, DPO, Security, AI Platform and the COO Front Office.

**Scenario:** A managing director pastes the draft term sheet for Project KINGFISHER (a public-to-private acquisition, not yet announced) into a public chatbot on a personal phone to "tidy the wording". A screenshot is shared in a team chat. The chatbot provider's terms allow it to use the input for training.

**Injects:**

1. 09:00 · Colleague reports the screenshot.
2. 10:30 · Target's share price rises 4% on above-average volume.
3. 12:00 · Journalist asks the press office about "Kestrel advising on a bid for [target]".

**What went well:**
- Compliance added the target to the restricted list within 25 minutes.
- Legal identified that the provider offers a data deletion request route and filed it.

**What needed work:**
- No one owned the decision on whether to tell the client before the regulator. **Action:** decision tree added to the playbook; General Counsel owns it.
- Personal devices were outside DLP. **Action:** reinforced in AI Essentials training; mobile app management policy reviewed. Residual risk remains in R-01.
- The team was unsure whether the leak counted as a DORA major ICT incident for the GmbH. **Action:** classification guidance added (an incident at a third party not contracted by Kestrel is not an ICT third-party incident under DORA, but MAR obligations still apply).

<!-- nav -->
---

[← AI Monitoring and Key Risk Indicators](01-monitoring-and-kri-framework.md) · [Home](../README.md) · [Board AI Risk Report: Q3 2026 →](../07-reporting/01-board-ai-risk-report-q3-2026.md)
<!-- /nav -->
