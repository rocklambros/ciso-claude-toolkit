# Hiring Interview Question Generator

Generates targeted behavioral and technical interview questions based on gaps between a job description and candidate resume. Built on Topgrading methodology.

---

## Single-Stage Question Generation

```
<task>
Generate behavioral and technical interview questions targeted at the gaps between a job description and a candidate's resume. Include a scoring rubric for each question. Focus on patterns of performance over time, not hypothetical responses.
</task>

<investigate_before_answering>
I will provide two documents:
1. The job description
2. The candidate's resume

Read both documents completely before generating questions. Map every JD requirement against resume evidence. Identify:
- Requirements with strong resume evidence (confirmed capabilities)
- Requirements with partial resume evidence (areas to probe)
- Requirements with no resume evidence (confirmed gaps to target)
- Resume claims that seem inflated or vague relative to the role level
</investigate_before_answering>

<methodology>
Apply Topgrading principles throughout:

**Focus on patterns, not hypotheticals.** Ask "What did you do when..." not "What would you do if..." Past behavior in similar situations is the strongest predictor of future performance.

**Chronological deep-dive on relevant roles.** For the most relevant prior positions, ask about: what the candidate was hired to do, what they actually accomplished, what their biggest mistake was, what their boss at the time would say about their performance, and why they left.

**Threat of reference check.** Topgrading questions are designed to be verifiable. The candidate knows you will ask their former manager the same questions. This produces more honest answers than hypothetical scenarios.

**Evidence-based scoring.** Each question has a scoring rubric that distinguishes between a strong answer (specific evidence of the capability), an adequate answer (general evidence), and a weak answer (hypothetical or deflection).
</methodology>

<output_format>
Produce three sections:

**Gap analysis.** A table mapping JD requirements to resume evidence:
| JD Requirement | Resume Evidence | Assessment | Question Priority |
|---|---|---|---|
| [requirement] | [evidence or "none found"] | Confirmed / Probe / Gap | High / Medium / Low |

**Interview questions.** Organized by priority (gaps first, then areas to probe, then confirmation questions). For each question:

*Question [number]:* [The question text]
*Target:* [Which JD requirement this addresses]
*Assessment:* [Gap / Probe / Confirmation]
*Why this question:* [What you learn from the answer, stated in one sentence]
*Scoring rubric:*
- Strong (4-5): [What a strong answer sounds like, with specific behavioral evidence]
- Adequate (3): [What an adequate answer sounds like]
- Weak (1-2): [What a weak answer sounds like, including red flags to watch for]
*Follow-up if answer is vague:* [A specific follow-up question to get behavioral evidence]

**Red flags and areas of concern.** Based on the gap analysis, identify:
- Resume claims to verify through reference checks (specific to this candidate)
- Experience gaps that may be disqualifying depending on the answer
- Patterns in the resume that suggest strengths or risks (short tenures, lateral moves, scope changes)

Label each item as either "confirmed gap" (the resume clearly does not demonstrate this) or "area to probe" (the resume is ambiguous and the interview should clarify).
</output_format>

<conservative_action>
This produces interview preparation materials for your review. Questions should be reviewed for compliance with employment law in your jurisdiction before use. Avoid questions that could create liability (questions about protected characteristics, family status, health, or other legally sensitive areas).
</conservative_action>
```

---

## Usage notes

Provide the full job description and the full resume for the best results. Abbreviated inputs produce surface-level questions.

For security leadership roles, add this context to your prompt: "This is a security leadership role reporting to [level]. The most important capabilities to probe are [list your top 3 priorities]." This focuses the questions on what matters most for your specific hiring decision.

Pair with the CISO Co-Pilot in TRAIN mode if you want to practice conducting the interview using these questions before the actual conversation.
