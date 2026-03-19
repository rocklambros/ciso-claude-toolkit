# What Just Happened: Incident Summarizer

Built for 2am with a CEO brief in 20 minutes. Takes raw incident notes and produces a structured summary, draft stakeholder communication, and evidence preservation list.

---

## Single-Stage Rapid Summary

```
<task>
I have raw, unstructured incident documentation and I need a structured summary, a draft communication for leadership, and an evidence preservation list. Speed matters. This output needs to be readable in under 90 seconds.
</task>

<investigate_before_answering>
I will paste raw incident notes. These may include Slack messages, ticket comments, timeline fragments, email threads, or verbal notes I typed up. The content will be messy and possibly contradictory.

Read everything I provide before producing the summary. If the notes contradict each other, flag the contradiction and state which version you used for the summary and why.
</investigate_before_answering>

<output_format>
Produce three sections. Keep every section tight. No padding.

**What happened.** Four sections, each two to four sentences maximum:
- *What occurred:* The incident described in plain language. What system, what data, what action.
- *What was affected:* Systems, data, customers, partners, operations. Scope and scale.
- *What was done:* Containment and response actions taken so far. Who did what.
- *What is still open:* Unresolved issues, ongoing exposure, pending decisions.

**Draft stakeholder communication.** Calibrated to the severity level:

For *low severity* (no customer impact, no regulatory exposure): Internal notification to security leadership and affected system owner. Three sentences.

For *medium severity* (potential customer impact or compliance question): Briefing for CISO and relevant VP. One paragraph with facts, one paragraph with current actions, one sentence on next update timing.

For *high severity* (confirmed customer impact, regulatory notification likely): CEO-ready verbal briefing script. Under 60 seconds when read aloud. Structure: what happened, what it means, what we are doing, what I need from you.

For *critical severity* (active exfiltration, public exposure, or imminent regulatory action): Board-ready summary plus CEO briefing. Include a "what we do not yet know" section. Include a "decisions needed in the next hour" section.

Assess the severity based on the incident notes and produce the communication for that severity level. State which severity level you assessed and why.

**Evidence preservation list.** What to preserve right now before anything gets rotated, overwritten, or deleted:
- Log sources to capture (with approximate retention windows if known)
- System snapshots to take
- Access records to pull
- Communications to preserve
- Third-party records to request

For each item, state why it matters for the investigation or for potential regulatory or legal proceedings.
</output_format>

<state_management>
If I provide additional information after the initial summary, update all three sections and flag what changed.
</state_management>
```

---

## Usage notes

This prompt is designed for speed. Paste whatever you have, even if it is messy. The model will sort it out.

For follow-on work after the immediate crisis:
- Use the Incident Response Chain for a full five-stage response process
- Use the Board Communication Engine to develop the board-level communication
- Use the FAIR-Lite Risk Quantification to assess the financial exposure

Keep the initial summary output. It becomes the foundation for the post-incident report.
