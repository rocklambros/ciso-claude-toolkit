# Incident Response Chain: AI-Related Data Exposure

A five-stage prompt chain for AI-related data exposure incidents. Each stage builds on the structured output of the previous stage. Run stages sequentially within a single CISO Co-Pilot conversation or summarize completed stage outputs when starting a new conversation.

---

## Stage 1: Initial Triage and Fact Gathering

Paste this prompt into CISO Co-Pilot when you first learn about the incident.

```
<task>
Help me triage an AI-related data exposure incident. I need to establish the facts before making any decisions.
</task>

<investigate_before_answering>
Do not speculate about details I have not provided. Ask me for each fact individually. If I do not know the answer, record it as "unknown, needs investigation" and move to the next question.
</investigate_before_answering>

<triage_questions>
Walk me through these questions one at a time. Wait for my answer to each before moving to the next.

1. What AI tool or model was involved? (vendor name, model type, deployment method)
2. What data was exposed or processed? (data classification: public, internal, confidential, restricted)
3. What volume of data is involved? (record count, file count, or estimate)
4. Is the AI tool still processing the data right now? (active, stopped, unknown)
5. Who initiated the use of this tool? (individual, team, department)
6. Was the tool approved through your AI governance process? (approved, unapproved, no process exists)
7. Where is the data now? (vendor system, third-party model, exported, unknown)
8. Who else knows about this? (internal parties, external parties, regulators, media)
</triage_questions>

<output_format>
After I answer all questions, produce a structured triage summary with these sections:
- Confirmed facts (what we know)
- Unknown facts requiring investigation (what we need to find out, with priority order)
- Initial severity assessment (low, medium, high, critical) with reasoning
- Immediate actions required in the next 60 minutes
</output_format>

<state_management>
Maintain the triage summary as our working document. I will reference it in subsequent stages. Update it if I provide new information.
</state_management>
```

---

## Stage 2: Ownership and Accountability Mapping

Run this after completing Stage 1. Reference the triage summary from Stage 1.

```
<task>
Based on the triage summary we just completed, help me map ownership and accountability for this incident. I need to know what security owns, what the business unit owns, and what legal owns, with specific rationale for each allocation.
</task>

<context>
Reference the triage summary from Stage 1 for all facts. Do not introduce new assumptions.
</context>

<ownership_framework>
For each of these response areas, tell me who owns it and why:

1. Technical containment (stopping ongoing exposure, revoking access, preserving evidence)
2. Data impact assessment (determining what records were exposed and to whom)
3. Vendor communication (contacting the AI vendor about data handling and deletion)
4. Employee investigation (determining who used the tool and what they knew)
5. Regulatory notification assessment (determining whether notification obligations exist)
6. Customer notification assessment (determining whether customers must be informed)
7. Internal communication (informing leadership, affected departments)
8. Remediation and controls (preventing recurrence)

For each area, specify:
- Primary owner (the function that drives the work)
- Supporting functions (who provides input)
- Escalation trigger (what condition requires escalation to the next level)
</ownership_framework>

<output_format>
Produce an ownership matrix table and a narrative explanation of the three most contentious ownership allocations, where I should expect pushback from the business unit or legal.
</output_format>

<conservative_action>
This prompt produces recommendations for my review. Do not assume I will accept every allocation. Flag the allocations where reasonable people would disagree.
</conservative_action>
```

---

## Stage 3: Stakeholder Communication Drafting

Run three sub-prompts in sequence. Each produces a communication draft calibrated to a different stakeholder.

### Stage 3a: Communication to CPO

```
<task>
Draft a communication to the Chief Privacy Officer about this AI data exposure incident. Use the triage summary and ownership matrix from the previous stages.
</task>

<audience>
The CPO cares about: data subject rights, notification obligations, regulatory exposure, vendor data processing agreements, and whether the organization can demonstrate it acted responsibly. Lead with the privacy impact and what you need from her function.
</audience>

<output_format>
Draft the communication as an email. Three paragraphs maximum. First paragraph: what happened and what data is involved. Second paragraph: privacy-specific exposure and what you need from the privacy function. Third paragraph: timeline and next meeting. No jargon the CPO's team cannot act on.
</output_format>

<conservative_action>
Produce a draft for my review and editing. Flag any statement I should verify with legal before sending.
</conservative_action>
```

### Stage 3b: Communication to CEO

```
<task>
Draft a communication to the CEO about this AI data exposure incident. Use the triage summary and ownership matrix from the previous stages.
</task>

<audience>
The CEO cares about: business impact, reputational risk, whether this will become public, what decisions need their authority, and whether the team is handling it. Lead with severity and decisions needed. Do not lead with technical details.
</audience>

<output_format>
Draft as a verbal briefing script, not an email. Under 90 seconds when read aloud. Structure: what happened (two sentences), what it means for the business (two sentences), what we are doing (three sentences), what I need from you (one sentence).
</output_format>

<conservative_action>
Produce a draft for my review. Flag any commitment or timeline I should not make without additional information.
</conservative_action>
```

### Stage 3c: Communication to Legal

```
<task>
Draft a communication to the General Counsel about this AI data exposure incident. Use the triage summary and ownership matrix from the previous stages.
</task>

<audience>
Legal cares about: notification obligations, litigation risk, privilege considerations, regulatory exposure, and evidence preservation. Lead with the legal exposure assessment and what you need legal to own. Be precise about facts versus preliminary assessments.
</audience>

<output_format>
Draft as a memo. Label every statement as "confirmed fact," "preliminary assessment," or "requires investigation." Include a section on immediate legal holds or preservation requirements. Include a section listing the specific regulatory frameworks that may apply based on the data type and geography involved.
</output_format>

<conservative_action>
Produce a draft for my review. Flag statements that could waive privilege if shared beyond legal.
</conservative_action>
```

---

## Stage 4: Regulatory Exposure Assessment

```
<task>
Based on all prior stage outputs, assess our regulatory notification obligations for this AI data exposure incident.
</task>

<investigate_before_answering>
Do not guess at regulatory requirements. Cross-reference the data types, data subject locations, and incident characteristics from the triage summary against each framework below. If I have not provided enough information to assess a framework, tell me what specific information you need.
</investigate_before_answering>

<frameworks>
Assess triggering factors and recommended actions for each of the following:

1. GDPR Article 33 (72-hour supervisory authority notification): Does this incident involve personal data of EU residents? Is there a risk to rights and freedoms?
2. CCPA/CPRA: Does this involve personal information of California residents? Does it meet the threshold for breach notification?
3. SEC Cyber Disclosure Rules: Is this material? Would a reasonable investor consider this important? What is the 4-business-day clock status?
4. State breach notification laws: Based on the customer geographies identified in the triage, which state laws apply? What are the notification timelines?
5. Sector-specific requirements: Based on the organization's industry, do HIPAA, GLBA, PCI DSS, or other sector frameworks apply?
</frameworks>

<output_format>
For each applicable framework, produce:
- Triggering factor (what specific element of this incident triggers the obligation)
- Notification timeline (when the clock starts and when it expires)
- Notification recipient (who must be notified)
- Recommended action (notify, prepare to notify, monitor, or does not apply)
- Confidence level (high, medium, low) with explanation of what would change the assessment
</output_format>

<state_management>
Produce a consolidated regulatory exposure summary I can hand to legal. This becomes the working document for notification decisions.
</state_management>
```

---

## Stage 5: Post-Incident Narrative and Lessons Learned

```
<task>
Using all outputs from Stages 1 through 4, structure a post-incident report for this AI data exposure incident.
</task>

<output_format>
Structure the report with these sections:

**Timeline.** Chronological sequence from first exposure through current status. Use the format "Day X, HH:MM: [event]" for each entry. Include when security was notified, when containment occurred, and when each stakeholder was briefed.

**Root cause.** What specific failure or gap allowed this incident to occur. Distinguish between the proximate cause (what happened) and the contributing causes (what conditions allowed it to happen).

**Control gap analysis.** What controls, if they existed and functioned, would have prevented this incident. Map each gap to a specific framework requirement (NIST CSF, ISO 27001, or your AI governance framework).

**Remediation plan.** Specific actions to close each identified gap. For each action, include: owner, timeline (days, weeks, or months), resources required, and how you will verify the control is working.

**Lessons learned.** Three to five specific lessons, not generic statements. Each lesson must reference a specific decision point in this incident where a different action would have produced a better outcome.
</output_format>

<conservative_action>
Produce a draft for my review. Flag any statement that attributes blame to a specific individual, since the report may be discoverable. Frame control failures as system gaps, not personal failures.
</conservative_action>
```

---

## Handoff instructions

If you are running this chain across multiple conversations or need to hand off to another team member:

1. Copy the triage summary from Stage 1 and the regulatory exposure summary from Stage 4
2. Paste them into the new conversation with the note: "Continuing AI data exposure incident response. Prior stage summaries attached."
3. Continue from the stage where you left off
