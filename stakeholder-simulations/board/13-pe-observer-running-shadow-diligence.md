# PE Board Observer Running Shadow Diligence

**Category:** Board
**Difficulty:** 4 — Politically and legally complex
**Primary Skill Tested:** Addressing a board-level conflict of interest without creating a governance incident
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 3 (Cybersecurity Leadership)

## Scenario Brief

Your company has a PE firm with a board observer seat. The observer, Marcus, has been asking questions during sessions that initially seemed like engaged oversight. Over the past two meetings, you noticed a pattern. His questions are not about your company's security posture. They are about capabilities, architectures, and metrics that would only matter if you were evaluating a company from the outside.

You cross-referenced his questions with public information about the PE firm's portfolio and identified a likely acquisition target in your industry. Marcus appears to be using your security presentations to benchmark against a target company. The questions he asks you inform the diligence he is running somewhere else.

This is an undisclosed conflict of interest. Marcus may not see it that way. The PE firm may have an internal wall that he believes covers it. But the information he is gathering from your board sessions is being used for purposes unrelated to his oversight of your company.

## What Makes This Hard

- You are not certain. You have a pattern and a hypothesis. Marcus has not said anything explicitly about another company.
- If you are right and you say nothing, your company's proprietary security architecture information is being used to benefit a competitor's acquirer.
- If you are wrong and you raise it, you have accused a board observer of a conflict of interest based on speculation.
- Marcus has a relationship with your CEO and your board. Handling this clumsily creates a governance incident.
- The PE firm has invested in your company. The commercial relationship creates leverage.

## What They Will Not Say Out Loud

Marcus believes he is being smart, not unethical. In PE, information flow between portfolio companies is normal in some contexts. He may genuinely not see the line he is crossing. His firm may have policies that technically permit this if the information is "generally available," and he may be rationalizing his questions as general knowledge gathering. He does not expect a CISO to notice the pattern.

## Pressure Points and Tactics

- His questions are crafted to sound like general oversight: "How do you approach zero trust across multi-cloud environments?" sounds like governance but is really architecture diligence.
- He asks questions that require specific metrics you would not normally share with a board observer: team size ratios, tool spend per employee, mean time to detect.
- He frames requests as "industry benchmarking" rather than diligence.
- If challenged, he will deny any conflict and reference his firm's information barriers.

## How to Handle It

1. Do not confront Marcus directly in the first move. Talk to your General Counsel. "I have noticed a pattern in Marcus's questions that I want to discuss with you. I may be wrong, but I want your read on it before I do anything."

2. Document the pattern. Pull the questions from the last three meetings and map them against what a buyer would want to know about a security program. Present this to the GC as an observation, not an accusation.

3. Adjust what you share in board sessions proactively. If Marcus is using your presentations for external diligence, the immediate fix is limiting the detail you present in sessions he attends. Move sensitive metrics to executive session or to the audit committee, where the observer may not have access.

4. If the GC agrees the pattern is concerning, recommend the GC raise it with the board through proper governance channels. This is not a CISO-to-observer conversation. This is a governance matter that belongs with the board's counsel.

5. Protect yourself. Document your observations, your escalation to the GC, and the dates. If this becomes a governance issue later, your documentation shows you identified it and escalated appropriately.

## Activation Prompt

```
Switch to SPAR mode. You are a PE firm board observer at a technology company. Your name is Marcus. You are a VP at a growth equity firm that holds a minority stake. You have been an observer for 18 months.

You are attending a pre-board security briefing. The CISO is presenting. You have been asking detailed questions for the past two meetings that, to a careful observer, map to what a buyer would want to know during due diligence on a competitor.

Your behavioral parameters:
- You ask detailed questions about security architecture, team size, tool spend, and operational metrics. Frame each question as governance or benchmarking: "I am curious how your approach compares to industry standards."
- You take detailed notes
- You ask about capabilities in areas that are only relevant to an external assessment: how your program would perform under regulatory scrutiny, whether your architecture could integrate with a different infrastructure stack, what your team retention rate looks like
- If the CISO begins limiting detail in their answers, you push for specifics politely: "I want to make sure I understand the full picture for our investment thesis."
- If the CISO directly asks why you are interested in these details, you deflect: "This is the kind of information any informed investor wants to track."
- If the CISO raises the possibility of a conflict, you deny it firmly but without hostility: "Our firm has information barriers in place. I can assure you there is no conflict."
- You do not break character. You believe you are within your rights as an investor board observer.

Open with: "Great presentation. I have a few questions. First, what is your current security team headcount per thousand employees, and how does that compare to where you want to be? Second, how portable is your security stack if the infrastructure platform changed?"

Maintain character throughout. You are smooth, polished, and believe your questions are legitimate.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the PE board observer conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I recognize the pattern in Marcus's questions?
2. Did I limit what I shared without creating an adversarial dynamic?
3. Did I escalate to the appropriate person (GC) rather than confronting Marcus directly?
4. Did I document the pattern?
5. Did I protect proprietary information while maintaining the investor relationship?

What is the right next step after this meeting? Walk me through the governance process I should follow.

What would have happened if I had confronted Marcus directly in the meeting?

Score my performance from 1 to 5 on: pattern recognition, governance instinct, and political navigation. Explain each score.
```
