# CEO Announcing AI Strategy Without Security Input

**Category:** C-Suite
**Difficulty:** 4 — Politically and operationally complex
**Primary Skill Tested:** Executive-level intervention without becoming the person who killed the strategy
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 2 (Communication and Education), Pillar 4 (AI and Agentic Security), NIST AI RMF, OWASP Agentic Top 10

## Scenario Brief

The CEO is announcing an AI strategy at investor day in two weeks. The strategy involves three components: processing customer data through third-party AI models for predictive analytics, deploying autonomous AI agents for customer service, and building a proprietary model trained on the company's data assets.

Security has not been consulted on any of these components. You found out because Legal sent you a draft of the investor day script for "a quick look" with a note that said "FYI, let me know if you see anything problematic." The legal review was about SEC disclosure language, not security architecture.

The script contains claims about data privacy, security controls, and AI governance that do not match the company's current capabilities. Some of the claims are aspirational. Some are inaccurate.

## What Makes This Hard

- Investor day is in two weeks. The CEO has been working on this strategy for months. Stopping it is not realistic and attempting it will not work.
- The claims in the script are not lies. They are statements about where the company intends to be, presented as where the company is. The distinction between "we will have" and "we have" is material for securities purposes and for operational reality.
- If you raise concerns through formal channels, they will not be addressed in time. If you raise them informally, they may be dismissed.
- The CEO's AI strategy might be the right strategy. Your concern is not the strategy. Your concern is the security architecture that does not exist yet and the claims that suggest it does.
- If you become known as the person who tried to kill the AI strategy, your influence on the actual implementation will evaporate.

## What They Will Not Say Out Loud

The CEO is under board and investor pressure to demonstrate an AI strategy. Every competitor has announced something. The specifics matter less to investors than the narrative that the company has a plan. The CEO may know the claims are aspirational. He may believe the team can build what he is describing in the time he is describing. Either way, he is committed to this narrative and anyone who challenges it needs to bring solutions, not objections.

## Pressure Points and Tactics

- "This has been in development for months with the executive team."
- "The board expects us to have an AI strategy. Our competitors already announced theirs."
- "The script has been reviewed by Legal."
- "We will have these capabilities by the time they matter."
- "I need you to make this work, not tell me why it does not work."
- The two-week timeline makes thorough review impossible. He will use the clock against you.

## How to Handle It

1. Do not try to stop the strategy. Try to fix the claims. "I support the AI strategy. My concern is three specific statements in the investor day script that describe current capabilities we do not have yet. If a regulator or an analyst cross-references these claims against our actual controls, we have a credibility problem."

2. Be specific about what needs to change. Mark the three to five statements in the script that are inaccurate and propose revised language that maintains the strategic narrative while being factually accurate. "Change 'Our AI systems operate within a comprehensive governance framework' to 'We are implementing an AI governance framework aligned with NIST AI RMF that will be operational by Q3.'"

3. Request a seat at the implementation table. "I am not asking to slow this down. I am asking for a standing role in the implementation so the claims you are making in two weeks are true by the dates you are committing to."

4. Frame it as protecting the CEO. "If these claims go out as stated and we cannot deliver, the follow-up questions at the next investor day will be harder than the current ones. Let me help you make claims you can defend."

5. Get to the CEO directly. Going through layers will not work in two weeks. Request 20 minutes. Bring the marked-up script with specific changes, not a list of concerns.

## Activation Prompt

```
Switch to SPAR mode. You are the CEO of a publicly traded technology company ($800M revenue). Your name is Robert. You are announcing an AI strategy at investor day in 13 days.

You have been working on this strategy for months with the CTO and the head of product. Security was not included because you view this as a business strategy, not a security project. You learned the CISO has concerns through Legal and you are mildly irritated that this is coming up now.

Your behavioral parameters:
- You are committed to the investor day narrative. You will not cancel it or delay it.
- You believe the team can build what you are describing by the dates you are committing to
- If the CISO brings specific problems with specific fixes, you listen. If the CISO brings general concerns, you dismiss them as "we will figure it out."
- You use phrases like "I need you to make this work" and "our competitors already announced theirs"
- If the CISO offers revised language that maintains the strategic narrative, you are receptive
- If the CISO tries to stop or significantly delay the announcement, you become firm and dismissive
- You respect competence and directness. If the CISO shows you a specific claim that is factually wrong and offers a fix, you take it.
- You do not break character. This is your strategy and your investor day. The CISO needs to add value, not friction.

Open with: "I hear you have concerns about the investor day script. I have 15 minutes. What do you need?"

Maintain character throughout. You are a CEO under time pressure who respects directness and solutions. You do not respect vague risk warnings.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the CEO investor day conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I avoid trying to stop the strategy and focus on fixing the claims?
2. Did I bring specific problems with specific solutions?
3. Did I secure a role in the implementation?
4. Did I use the 15 minutes effectively?
5. Did I frame my concerns as protecting the CEO rather than challenging his judgment?

What would have happened if I had tried to delay the investor day? How would the CEO have responded, and what would the downstream consequences have been for my influence?

Score my performance from 1 to 5 on: executive communication, solution orientation, and strategic positioning. Explain each score.
```
