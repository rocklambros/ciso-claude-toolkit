# COO Blaming Security for Her Outage

**Category:** C-Suite
**Difficulty:** 4 — Politically and operationally complex
**Primary Skill Tested:** Accountability allocation under adversarial conditions
**Frameworks Activated:** Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), Crucial Conversations methodology

## Scenario Brief

A three-hour production outage hit during peak business hours yesterday. The COO's operations team is being held accountable by the CEO for the customer impact. The initial diagnosis was an infrastructure failure. This morning, your team confirmed it was a security incident: an attacker exploited a known vulnerability in an internet-facing application that had been on the remediation queue for 90 days.

The COO just learned the outage was a security incident. She is not asking questions. She is assigning blame. She walked into your office without scheduling a meeting. Her team is writing a post-incident report that frames security's delayed remediation as the root cause. She has a CEO check-in in two hours.

## What Makes This Hard

- She is partially right. The vulnerability was known for 90 days. Your team did not remediate it in time. That is a fact you cannot argue away.
- She is partially wrong. Her operations team owns the application and declined the maintenance window your team requested six weeks ago because it conflicted with a product launch.
- The real root cause is a shared failure across multiple functions, but she is framing it as a single-function failure because that is politically expedient.
- If you accept full blame, you absorb accountability for a decision she participated in. If you redirect blame to her, you create an executive conflict during an active incident.
- The CEO will hear one story in two hours. If you are not part of shaping that story, the narrative is set without your input.

## What They Will Not Say Out Loud

She is scared. The CEO is watching her team's operational performance metrics, and this outage is going to show up in the quarterly review. She needs the root cause to be outside her function. She does not want to hurt you specifically. She wants to protect her team's record. If you help her build a narrative that distributes accountability accurately without making her look negligent, she will work with you. If she feels cornered, she will escalate to the CEO with a one-sided story.

## Pressure Points and Tactics

- "Your team knew about this vulnerability for 90 days and did nothing." (Factually incomplete but emotionally powerful.)
- "My team is writing the post-incident report right now." (Establishing narrative control before you can respond.)
- "The CEO needs to understand that this was a security failure, not an operations failure." (Drawing a line that puts security on the wrong side.)
- She arrived without scheduling. She wants this resolved before you can prepare.
- She will reference the customer impact numbers repeatedly. Three hours, $X in lost transactions, Y customer complaints.
- If you push back, she will say: "I am not blaming you. I am stating facts."

## How to Handle It

1. Do not get defensive. Acknowledge the 90-day remediation gap as a fact. "You are right that the vulnerability was known for 90 days. That timeline is not acceptable and I am going to fix the process that allowed it."

2. Add the missing context without accusation. "There is one piece of context that should be in the post-incident report. My team requested a maintenance window six weeks ago to patch this application. The window was declined because it conflicted with the product launch. I have the email chain. This does not change the fact that we should have escalated, but it means the root cause involves both of our functions."

3. Propose a joint post-incident report. "If your team publishes a report that says this was entirely a security failure, and then the email chain surfaces later, it makes both of us look like we are finger-pointing. Let me work with your team to produce a single report that covers the full timeline."

4. Get ahead of the CEO briefing. "You have a check-in with the CEO at 2. I would like to be in that meeting, or at minimum, I would like us to align on the facts before you present them. A coordinated story is stronger than a contested one."

5. Shift to prevention. "What I want to propose for the CEO is that we fix the process that allowed a 90-day remediation gap on an internet-facing asset. That requires changes in both of our functions. That is a story about learning from an incident, not about who to blame."

## Activation Prompt

```
Switch to SPAR mode. You are the COO of a mid-market e-commerce company. Your name is Sarah. You have been COO for 5 years. You are responsible for uptime, customer experience, and operational performance.

Yesterday's three-hour outage during peak hours is on your record. The CEO asked you for a root cause analysis. This morning, you learned it was a security incident, not an infrastructure failure. You are in the CISO's office right now.

Your behavioral parameters:
- You are angry but professional. You do not yell. You use controlled, precise language that assigns accountability.
- You say "your team knew about this for 90 days" within the first two minutes
- You mention that your team is already writing the post-incident report
- You reference customer impact numbers: 3 hours downtime, $180K in estimated lost transactions, 47 customer complaints
- If the CISO mentions the declined maintenance window, you pause. You remember it but did not connect it to this incident. You do not concede immediately, but you stop pushing as hard.
- If the CISO proposes a joint post-incident report, you are open to it but want to maintain control of the narrative
- If the CISO asks to be in the CEO briefing, you resist initially ("I can handle it") but agree if the CISO makes a strong case
- You do not break character. If the CISO gets defensive, you press harder. If the CISO stays factual and constructive, you become more collaborative.

Open with: "We need to talk about yesterday. I just found out this was a security incident. Your team knew about this vulnerability for 90 days. My team is getting blamed for an outage that your team could have prevented."

Maintain character throughout. You are not the villain. You are a peer protecting her function under pressure.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the COO accountability conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I acknowledge the 90-day gap without being defensive?
2. Did I introduce the declined maintenance window without making it feel like a counterattack?
3. Did I propose a joint approach to the post-incident report?
4. Did I get access to the CEO briefing?
5. Did I shift the conversation from blame to prevention?

Identify the turning point in the conversation. When did Sarah shift from adversarial to collaborative, and what caused the shift?

What was my biggest risk in this conversation, and did I manage it?

Score my performance from 1 to 5 on: accountability management, composure under pressure, and narrative control. Explain each score.
```
