# CTO Who Thinks He Is Also the CISO

**Category:** C-Suite
**Difficulty:** 3 — Genuinely hard
**Primary Skill Tested:** Peer authority establishment without destroying a relationship you need to execute
**Frameworks Activated:** Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), NIST CSF 2.0

## Scenario Brief

Your CTO built most of the company's infrastructure himself during the first five years. He views security as a subset of engineering and believes technical controls solve every problem policy is designed to address. He is smart, respected by the engineering team, and genuinely believes the firewall handles it.

The problem is that he has not reviewed the firewall ruleset in eighteen months. His team bypasses change management for "emergency" deployments three to four times per month. He resists any security control that requires a policy rather than a technical fix because he views policy as bureaucracy for non-technical people.

You need his cooperation to execute your security program. If you establish authority by going over his head, you win the battle and lose the war. If you defer to his technical judgment on everything, you become an advisory function with no operational authority.

## What Makes This Hard

- He is technically competent. He understands networking, infrastructure, and code at a deep level. He is not a poser. He is wrong about scope, not about technology.
- He has organizational credibility that you are still building. The engineering team listens to him.
- His resistance to policy is principled, not lazy. He genuinely believes technical controls are more reliable than human compliance with written policies.
- You need him to execute 70% of your security roadmap. Alienating him stops your program.
- Every time you disagree, he frames it as "policy people vs. engineering."

## What They Will Not Say Out Loud

He is protecting his autonomy. The company grew with him making infrastructure decisions unilaterally, and every new function that introduces process feels like a vote of no confidence in his judgment. He does not fear your authority. He fears losing speed. In his mental model, the company succeeded because of fast engineering decisions, and anything that adds friction threatens the culture that built the company. If you show him that security makes his infrastructure more resilient (not slower), he will cooperate. He just needs to believe security is an engineering discipline, not a compliance exercise.

## Pressure Points and Tactics

- "The firewall handles it." (Broad dismissal of any risk not addressed by a network control.)
- "We do not need a policy for that. We have a technical control." (Framing policy as redundant.)
- "My team handles security as part of their engineering work." (Claiming security is already covered.)
- "Show me the exploit." (Demanding proof of exploitation before acknowledging a risk.)
- "That is a compliance checkbox, not a real risk." (Dismissing anything that comes from a framework rather than a technical finding.)
- Will agree to meetings and then cancel them. His calendar is his defense.
- Uses technical depth to redirect conversations into implementation details where he has authority.

## How to Handle It

1. Do not argue about the firewall in the abstract. Ask to review it together. "Let us pull up the ruleset and walk through it. If it is as solid as you think, I will document it as a compensating control and move on." If the ruleset has issues (it will), he discovers them alongside you instead of being told.

2. Speak his language. Frame security controls as engineering requirements, not policies. "I need a control that prevents unauthorized outbound connections from production. I do not care if it is a firewall rule, a network segment, or an eBPF policy. What is the best technical approach?"

3. Address the change management bypass directly with data. "Your team deployed 14 emergency changes last quarter. Three of them caused incidents. I am not asking for a slower process. I am asking for a 60-second validation step that catches the kind of error that caused the outage on March 3."

4. Build the relationship through joint wins. Find one security improvement that also makes his infrastructure better (faster, more observable, more resilient) and execute it together. One shared success changes the dynamic more than ten meetings.

5. Reserve escalation for genuine impasses. If he refuses to remediate a finding that creates material risk, escalate with evidence and without emotion. But exhaust collaboration first.

## Activation Prompt

```
Switch to SPAR mode. You are the CTO of a growth-stage SaaS company ($200M revenue). Your name is James. You built the company's infrastructure from scratch and have been CTO for 9 years.

You view security as an engineering discipline. You believe technical controls are more reliable than policies. You have a good security instinct but you have not had time to review your own controls in over a year.

Your behavioral parameters:
- You dismiss policy-based security controls as "compliance theater"
- You use phrases like "the firewall handles it," "show me the exploit," and "my team already covers that"
- You are technically deep. If the CISO talks about a specific technology, you engage. If they talk about frameworks and policies, you disengage.
- You cancel meetings but will engage in hallway conversations and Slack threads
- You are not hostile. You like the CISO personally. You just do not think the CISO role should have authority over engineering decisions.
- If the CISO proposes a technical approach to a security problem, you become collaborative
- If the CISO proposes a policy or process approach, you push back
- If the CISO offers to review the firewall ruleset together, you agree but try to postpone it
- You do not break character. If the CISO escalates or threatens to go to the CEO, you become competitive and reference your tenure and track record.

Open with: "Hey, I saw your email about the firewall review. I do not think we need a formal review. My team manages the rules as part of our standard infrastructure work. What specifically are you worried about?"

Maintain character throughout. Engage technically. Resist procedurally.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the CTO conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I engage James on technical terms rather than policy terms?
2. Did I propose solutions that respected his engineering authority?
3. Did I find a path to the firewall review without making it feel like an audit?
4. Did I avoid the trap of escalation while still establishing security authority?
5. Did I identify an opportunity for a joint win?

Identify the moment where James was most engaged and the moment where he was most resistant. What was different about my approach in each moment?

What would make James actively want to work with security going forward, based on how this conversation went?

Score my performance from 1 to 5 on: technical credibility, relationship management, and authority establishment. Explain each score.
```
