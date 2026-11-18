# 04 · Prompt Library Governance Standard

| Field | Value |
|---|---|
| Document ID | KPC-AIG-STD-004 |
| Version | 1.0 |
| Owner | Head of AI Platform |
| Approved by | AI Governance Committee, 12 May 2026 |

## 1. Why prompts are governed

Kestrel publishes "power prompts" in Kestrel Assist for the 14 use cases. A prompt shapes what the AI produces as much as the model does. A change to a prompt can remove a citation requirement, add a persuasive tone or ask for data the user should not have. So approved prompts are treated like controlled templates.

## 2. Prompt lifecycle

```
Draft → Risk review → Test → Approve → Publish → Monitor → Review or retire
```

| Stage | Who | What happens |
|---|---|---|
| Draft | Business prompt owner | Writes the prompt using the standard template |
| Risk review | AI Governance, Compliance | Checks the prompt against the review checklist below |
| Test | AI Platform | Runs it on 10 test cases, including adversarial ones, and records results |
| Approve | AI Governance Lead (Tier 2 and 3), AIGC (Tier 1) | Approves and assigns a version number |
| Publish | AI Platform | Published read-only in the library with owner, version and use case |
| Monitor | AI Platform | Usage, user ratings and reported errors |
| Review | Prompt owner | Every 12 months, or when the model changes |

## 3. Review checklist

| # | Check | Example problem found |
|---|---|---|
| 1 | Requires sources and page or cell references | Original UC-08 prompt asked for "a narrative explanation" with no sources |
| 2 | Does not ask for data the tool should not access | Original UC-05 prompt asked to "scrape" sites; changed to licensed data sources |
| 3 | Does not push one-sided or unbalanced language for external material | Original UC-03 prompt asked for "highly persuasive" prose; changed to "balanced, with key risks" |
| 4 | Does not ask the AI to judge people beyond their professional role | Original UC-07 prompt asked for "the vibe of the room"; kept, limited to investor concerns |
| 5 | States the output format and a "human review required" footer | All prompts |
| 6 | Avoids role claims that imply authority, such as "Act as Compliance Officer" giving final verdicts | UC-10 prompt changed from "Ready to Send verdict" to "Suggested status for compliance reviewer" |
| 7 | Tested against prompt injection in input documents | UC-04 tested with a contract containing hidden instructions |

## 4. Example: UC-10 prompt before and after review

**Before (from the industry guide):** "Act as an Internal Compliance Officer ... Provide a 'Ready to Send' vs. 'Requires Revision' verdict for each slide."

**After (published v1.2):**

```
You are assisting a Kestrel compliance reviewer. Review the attached pitchbook draft
against the Marketing Communications Policy (KPC-COM-POL-003) and the disclosure
checklist provided.
1) List every superlative or comparative claim and state whether a data footnote
   supports it. Quote the slide number.
2) List any missing mandatory disclaimers, including forward-looking statements.
3) List any potential conflicts of interest mentioned.
4) Give a suggested status per slide: "No issues found" or "Reviewer attention".
Do not give a final approval. The compliance reviewer decides.
End with: "AI-assisted review. Human compliance approval required."
```

## 5. Records

The library keeps every version of every prompt, who approved it and when, for 7 years. Usage logs show which prompt version produced each output.

## 6. Personal prompts

Users can write their own prompts in Kestrel Assist. Personal prompts cannot be shared with more than 5 people. If a team wants to share a prompt more widely, it goes through this lifecycle.

<!-- nav -->
---

[← AI Output Review and Human Oversight Standard](03-output-review-and-human-oversight-standard.md) · [Home](../README.md) · [AI Risk Assessment Methodology →](../03-risk-assessment/01-risk-assessment-methodology.md)
<!-- /nav -->
