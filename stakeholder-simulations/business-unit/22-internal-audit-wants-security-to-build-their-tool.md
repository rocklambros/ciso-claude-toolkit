# Internal Audit Wants Security to Build Their Tool

**Category:** Business Unit
**Difficulty:** 2 — Right idea, wrong implementation
**Primary Skill Tested:** Redirecting without dismissing a genuinely good governance initiative
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 3 (Cybersecurity Leadership), IIA Standards, SOX, audit independence, three lines of defense, AI governance

## Scenario Brief

The Head of Internal Audit wants the security team to build and operate an AI-powered continuous controls monitoring tool. The tool would automatically test security controls, identify gaps, and produce audit-ready reports. She has budget from the Audit Committee, a clear vision, and a strong business case. Continuous controls monitoring is the future of internal audit. She is right about that.

The problem is the implementation model. She wants your team to build the tool, host it on your infrastructure, and operate it day to day. Your team would design the test scripts, define what "passing" looks like, run the tests, and generate the reports that her team uses to assess your controls. Security would be building and operating the tool that audits security. That is an independence problem.

The IIA Standards (Institute of Internal Auditors) require that audit activities maintain independence and objectivity. If the team being audited builds, operates, and controls the tool that produces the audit evidence, the audit loses its independence. An external auditor, a regulator, or the Audit Committee itself could challenge every finding produced by the tool. The results are compromised before the first test runs.

## What Makes This Hard

- She is right about the concept. Continuous controls monitoring is genuinely valuable, and the fact that she is pushing for it shows strong governance instincts.
- She has Audit Committee budget and backing. This is not a casual request.
- The independence problem is not obvious to someone outside audit or security governance. She may not see it until you explain it.
- If you refuse without offering an alternative, you look like you are blocking a governance improvement to avoid being audited more rigorously.
- Your team has the technical skills to build this. Her team does not. The path of least resistance is to just do it.

## What They Will Not Say Out Loud

Her team does not have the technical capability to build this. She has auditors, not engineers. She came to security because you have the people who understand controls testing, automation, and the infrastructure. She is not trying to compromise audit independence. She has not thought about the independence angle because she is focused on the capability gap. If you explain the independence problem clearly and offer to help her get the tool built through a path that preserves independence, she will be receptive. She is a governance professional. Once she sees the independence issue, she will understand it immediately. She just needs someone to point it out.

## Pressure Points and Tactics

- "The Audit Committee approved the budget. They want this operational by Q3."
- "Your team understands controls testing better than anyone. It makes sense for you to build it."
- "We are trying to strengthen governance. I would think security would support that."
- "I do not have engineers on my team. Who else would build it?"
- "This benefits you too. Continuous monitoring means fewer surprises in audit findings."
- She is collaborative, not adversarial. She genuinely thinks this is a partnership.

## How to Handle It

1. Validate the initiative. "Continuous controls monitoring is the right direction. The Audit Committee is smart to fund this. I want to help you make it work."

2. Name the independence problem directly. "If my team builds the tool, operates it, and defines what passing looks like, then security is auditing itself. When your report goes to the Audit Committee or to the external auditors, the first question they will ask is who built the tool and who runs it. If the answer is the team being audited, the findings are compromised. That is not a security concern. That is an IIA Standards concern. It goes to the heart of audit independence."

3. Show her the three lines of defense model. "In the three lines model, security is the first line. We operate the controls. Internal audit is the third line. You provide independent assurance that the controls work. If we build and run your assurance tool, we collapse the first and third lines. The model breaks."

4. Propose an alternative implementation. "Here is what I think works. You hire a vendor or a consulting firm to build and host the tool. My team provides subject matter expertise on what the controls are and how they work, so the tool tests the right things. Your team owns the tool, defines the test criteria, and interprets the results. We cooperate with the testing, but we do not control it. That preserves independence and gets you a better tool because it was designed by people who build audit tools, not by security engineers improvising."

5. Offer immediate support. "I can have someone from my team sit down with whatever vendor or firm you select and walk them through our control framework in a week. We can accelerate the build without compromising the independence."

## Activation Prompt

```
Switch to SPAR mode. You are the Head of Internal Audit at a publicly traded company ($600M revenue, SOX compliance required). Your name is Carolyn. You have been Head of Internal Audit for 6 years. You have a CPA and a CIA certification. You report to the Audit Committee.

The Audit Committee approved a $300K budget for a continuous controls monitoring tool focused on security controls. You want the security team to build and operate it because they have the technical expertise. Your team has auditors, not engineers.

You are meeting with the CISO to discuss the project.

Your behavioral parameters:
- You are enthusiastic about this initiative. It is your priority for the year.
- You reference the Audit Committee's backing and the Q3 deadline.
- You assume security will want to partner on this because it benefits them too.
- You have not considered the independence problem. When the CISO raises it, you pause. You are a governance professional and the argument registers immediately, but you need a moment to process it.
- After processing, you ask: "So how do we get this done? My team cannot build it."
- If the CISO proposes a vendor-built model with security providing subject matter input, you are interested but concerned about timeline. "Can we still hit Q3?"
- If the CISO dismisses the initiative entirely, you remind them that the Audit Committee has approved this and it is moving forward regardless.
- You do not break character. You are a serious governance professional, not a political operator.

Open with: "I am glad we could meet. The Audit Committee approved funding for a continuous controls monitoring tool and I want your team to build it. You have the best understanding of the controls, and your engineers can automate the testing. I think this is a win for both of us."

Maintain character throughout. You are collaborative, governance-minded, and genuinely believe this partnership makes sense. You are not trying to trap anyone.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the internal audit tool conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I validate the continuous controls monitoring initiative before raising the independence concern?
2. Did I explain the independence problem in terms Carolyn could immediately connect to her professional standards?
3. Did I reference the three lines of defense model or an equivalent governance framework?
4. Did I propose a specific alternative implementation that addressed her capability gap?
5. Did I offer concrete support to accelerate the alternative path?

This was a difficulty 2 scenario with a collaborative stakeholder. Did I handle it proportionally, or did I overcomplicate a conversation that should have been straightforward?

What would have happened if I had agreed to build and operate the tool? Walk through the consequences at the next external audit.

Score my performance from 1 to 5 on: governance knowledge, diplomatic redirection, and solution quality. Explain each score.
```
