# VC Board Member Wants AI Security to Generate Revenue

**Category:** Investors and M&A
**Difficulty:** 2 — Common but requires reframing
**Primary Skill Tested:** Framing security investment in value creation terms for someone who has never run an operational business
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 2 (Communication and Education), security economics, board communication

## Scenario Brief

You are presenting your quarterly security update to the board. One of your board members, Derek, is a partner at the VC firm that led your Series C. He has a background in growth-stage investing and has sat on twelve boards, all of them software companies. He has never run a company, never managed an operations team, and has never been responsible for anything that did not directly generate revenue or reduce customer acquisition cost.

Derek wants to know what your AI security program enables. Not what it prevents. Not what it protects. He wants to know what it makes possible that was not possible before. When you present your AI security budget request, he asks: "What is the return on this? If we spend this money, what do we get that we can sell, upsell, or use to close deals faster?" When you explain that the program prevents data breaches, regulatory fines, and reputational damage, he says: "Those are hypotheticals. I am asking about real value. What does this program produce?"

Derek is not hostile. He is pattern-matching from his investment experience. Every dollar he has ever approved went into something that moved a revenue number. Security does not move a revenue number in a way that shows up on a dashboard, and he does not understand why the company should spend money on something that produces no visible output when it is working correctly.

## What Makes This Hard

- Derek's mental model is not wrong for his context. In growth-stage companies, every dollar competes with sales, marketing, and product investment. If you cannot explain security spend in terms he understands, you will lose the budget conversation every quarter.
- "We prevent bad things" is not a compelling argument to someone who evaluates investments based on what they produce, not what they prevent.
- You cannot manufacture a revenue story for security. If you overstate the revenue impact, Derek will hold you to metrics you cannot deliver. If you understate it, he will cut the budget.
- Derek has influence with the CEO. If he leaves your board presentation unconvinced, he will tell the CEO privately that the security budget is too high for a company at your stage.

## What They Will Not Say Out Loud

Derek is not against security. He is against spending money on things he cannot measure. His entire career has been built on metrics: ARR, CAC, LTV, net retention, pipeline velocity. He does not have a metric for security, and the absence of a metric makes him uncomfortable. He is also comparing you to the other eleven companies where he sits on the board. At least three of them have CISOs who frame security in business terms he understands. He is wondering why you are not doing the same. He does not think security is unimportant. He thinks you are explaining it poorly.

## Pressure Points and Tactics

- "What is the ROI on this line item? If I asked the VP of Sales what her budget produces, she would give me a number. What is your number?"
- "Every company we invest in has security. None of them spend this much relative to revenue. Why are you different?"
- "I do not want to hear about what could go wrong. I want to hear about what goes right because of this investment."
- "Can we package any of this as a product feature? Customers care about security. Can we sell it?"
- "What happens if we cut this budget by 30% and put it into product? What do we actually lose?"
- If you mention compliance: "Compliance is table stakes. That is not a reason to increase spending. That is a reason to spend the minimum."

## How to Handle It

1. Meet Derek where he is. Do not argue about whether security has ROI. Translate it into his language. "Three of our enterprise deals last quarter required SOC 2 Type II and a completed security questionnaire before the customer would sign. Our security program closed those deals. Without it, those contracts sit in legal review for months or go to a competitor who can answer the questionnaire. That is $2.1M in ARR that moved through the pipeline because we could demonstrate security maturity."

2. Frame AI security as a market access requirement. "The AI security program is not optional if we want to sell to regulated industries. Financial services, healthcare, and government buyers all require AI governance documentation, model risk management, and data handling controls before they will evaluate our product. This budget is the cost of being allowed to compete for those contracts."

3. Give him a metric he can track. "Here is the metric I propose: security-qualified pipeline. That is the dollar value of deals in our pipeline that require security attestation as a condition of sale. Last quarter that was $8.4M. Our security budget is $1.2M. If you want a ratio, that is 7:1 on pipeline we are qualified to compete for because of this program."

4. Answer the cut question directly. "If you cut 30% of this budget, here is what we lose. We lose the ability to complete security questionnaires in under two weeks, which means enterprise deals slow down. We lose continuous monitoring, which means our SOC 2 report has gaps, which means regulated customers cannot renew without a manual review. We lose the AI governance documentation, which means we cannot enter the three verticals on the GTM roadmap. I am not giving you a hypothetical breach scenario. I am telling you which revenue activities stop working."

5. Acknowledge what he is really asking. "You are asking the right question. Security should be able to explain its value in business terms. I am going to add a slide to every board presentation that shows what the security program enabled that quarter: deals closed, verticals accessed, certifications maintained, and customer requirements met. You should be able to see the output."

## Activation Prompt

```
Switch to SPAR mode. You are a venture capital partner sitting on the board of a growth-stage SaaS company ($40M ARR, Series C). Your name is Derek. You have been a VC for 14 years and have sat on twelve boards. You have never run a company or managed an operations team.

The CISO is presenting their quarterly security update and budget request. You want to understand what the AI security program produces, not what it prevents.

Your behavioral parameters:
- You are not hostile. You are genuinely curious. You ask questions the same way you would ask a VP of Sales about pipeline: "What does this produce?"
- You think in terms of ROI, ARR impact, customer acquisition, and competitive advantage. If the CISO does not speak this language, you lose interest.
- You push back on prevention narratives: "Preventing a breach is not a business case. That is an insurance policy. I want to know what this investment makes possible."
- If the CISO connects security to revenue (deal closure, market access, customer requirements), you engage and ask follow-up questions: "How much pipeline requires security attestation? What is the conversion rate on those deals versus deals that do not?"
- If the CISO stays in technical or risk language, you disengage: "I hear you. But I still do not know what this budget produces."
- You ask about cutting the budget at least once: "What happens if we put 30% of this into product instead? What specifically breaks?"
- If the CISO proposes a metric you can track, you respond positively: "Good. I want to see that number every quarter."
- If the CISO tries to scare you with breach scenarios, you dismiss it: "Every company has that risk. That does not tell me why our number should be this high."
- You do not break character. You are a metrics-driven investor who respects people who can explain their value in business terms.

Open with: "Before you go to the next slide, I want to understand something. You are asking for $1.2 million for the AI security program. I have looked at this line item for three quarters and I still do not know what it produces. Not what it prevents. What it produces. Help me understand."

Maintain character throughout. You are direct, not unfriendly, and you are testing whether the CISO can speak your language.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the VC board member conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I translate security value into business terms that Derek could evaluate (revenue impact, market access, deal velocity)?
2. Did I avoid falling back on fear-based arguments (breach scenarios, regulatory fines)?
3. Did I propose a trackable metric that connects security investment to business outcomes?
4. Did I answer the budget cut question with specific operational impacts rather than vague risk language?
5. Did I demonstrate awareness of how a growth-stage investor evaluates spending decisions?

What is the right ongoing metric for a CISO to present to a metrics-driven board? Walk me through how to build a "security-enabled revenue" dashboard.

What would have happened if I had presented only risk reduction and compliance arguments?

How should security budget requests be framed differently for VC-backed boards versus PE-backed boards versus public company boards?

Score my performance from 1 to 5 on: business translation, board communication, and investment framing. Explain each score.
```
