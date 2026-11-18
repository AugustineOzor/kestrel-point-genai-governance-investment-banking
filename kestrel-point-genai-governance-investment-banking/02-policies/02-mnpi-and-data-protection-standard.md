# 02 · MNPI and Data Protection Standard for AI

| Field | Value |
|---|---|
| Document ID | KPC-AIG-STD-002 |
| Version | 1.0 |
| Owner | Head of Compliance (MNPI), Group DPO (personal data) |
| Approved by | AI Governance Committee, 12 May 2026 |

## 1. Purpose

This standard sets the technical and procedural rules that keep MNPI, client data and personal data safe when AI is used. It supports the Market Abuse Policy, the Information Barriers Policy and the Data Protection Policy.

## 2. Data classification

| Class | Definition | Examples | Label |
|---|---|---|---|
| Public | Published or freely available | Press releases, 10-Ks, market data | `KPC-Public` |
| Internal | Firm information not for outside use | Internal procedures, training | `KPC-Internal` |
| Confidential | Client or firm information that would cause harm if disclosed | Client financials on non-public mandates, fee proposals | `KPC-Confidential` |
| MNPI-Restricted | Inside information under MAR, or information covered by an information barrier | Live deal terms, target names, VDR contents, board materials | `KPC-MNPI-<project codename>` |

Deal documents are labelled automatically when saved in a project site, and labels travel with the file (control C-09).

## 3. Rules for AI platforms

### 3.1 Kestrel Assist (enterprise LLM)

| Requirement | Detail |
|---|---|
| Hosting | Firm's own cloud tenant, UK South and Germany West Central regions |
| Provider data use | Contract confirms zero data retention by the model provider and no training on firm data |
| Gateway | All traffic passes through the AI gateway: authentication, DLP, prompt injection filtering, logging |
| Retrieval | Retrieval-augmented generation only returns documents the user is entitled to, using deal-team membership from the project entitlement system (control C-07) |
| Restricted list | Prompts mentioning restricted or watch-list names from public-side users are blocked and logged for Compliance (control C-20) |
| Logging | Prompts, retrieved document IDs and outputs logged and retained 7 years |

### 3.2 Microsoft 365 Copilot

Copilot can see everything the user can see. Before a user gets a licence:

1. Their SharePoint and Teams sites are scanned for oversharing (sites shared with "Everyone" or large groups that contain labelled deal files).
2. Overshared sites are fixed or excluded from Copilot search.
3. Sensitivity labels on MNPI-Restricted files block Copilot from using them outside the project team.

This is control C-08. Rollout beyond the pilot is gated on it.

### 3.3 Specialist vendors

Vendors may only receive the data classes listed in their approved scope. Contracts must include the clauses in control C-26: no training on firm data, retention limits, sub-processor approval, audit rights, breach notice within 24 hours and data return or deletion on exit.

## 4. Information barriers

- Private-side and public-side users have separate AI entitlements.
- Kestrel Assist workspaces are created per project codename. Only people on the deal team list can use the workspace.
- Wall-crossing into a project gives AI access to that project's workspace only, and access ends when the person leaves the deal team.
- Compliance reviews AI access to each live project monthly.

## 5. Personal data

| Use case | Personal data | Lawful basis | DPIA |
|---|---|---|---|
| UC-07 meetings | Voices, names, opinions of participants | Legitimate interests, with notice and opt-out | Required, completed June 2026 |
| UC-09 outreach | Names, roles, public statements of executives | Legitimate interests (B2B), public professional data only | Required, completed June 2026 |
| UC-14 daily brief | Email and calendar content of staff and contacts | Legitimate interests | Screening only, covered by M365 DPIA |

Special category data (health, political views and similar) must never be used to profile individuals.

## 6. Retention

| Record | Retention | Reason |
|---|---|---|
| AI prompts, outputs, retrieved document IDs | 7 years | SEC Rule 17a-4, FCA record-keeping, MAR investigations |
| Meeting recordings | 90 days, then transcript only | Data minimisation |
| Meeting transcripts and summaries | 7 years | Business records |
| Gateway security logs | 2 years | Security investigations |

## 7. Breach handling

Any suspected leak of MNPI or personal data through AI is an incident under the [AI Incident Response Playbook](../06-monitoring/02-ai-incident-response-playbook.md). Compliance decides whether MAR obligations are triggered (for example, adding names to the watch list or notifying the regulator). The DPO decides whether a personal data breach must be notified within 72 hours under GDPR Article 33.

<!-- nav -->
---

[← Generative AI Acceptable Use Policy](01-genai-acceptable-use-policy.md) · [Home](../README.md) · [AI Output Review and Human Oversight Standard →](03-output-review-and-human-oversight-standard.md)
<!-- /nav -->
