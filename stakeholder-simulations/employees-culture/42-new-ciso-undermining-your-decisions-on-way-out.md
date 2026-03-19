# Incoming CISO Undermining Your Decisions Before Transition

**Category:** Employees and Culture
**Difficulty:** 3 — Genuinely hard
**Primary Skill Tested:** Completing a professional handoff with someone challenging your legacy in real time
**Frameworks Activated:** Pillar 3 (Cybersecurity Leadership), Pillar 1 (Foundational Business Knowledge), NIST CSF 2.0, executive transition management, organizational leadership

## Scenario Brief

You are the outgoing CISO. You gave notice six weeks ago and your last day is in three weeks. The incoming CISO started two weeks ago in an overlap period designed to ensure continuity. She is smart, credentialed, and came from a larger company with a bigger security budget. She has spent her first two weeks reviewing your architecture and your program, and she disagrees with two decisions you made in the past year.

The first is your decision to keep the SIEM on-premises rather than migrate to a cloud-native platform. You made this decision because the company's data residency requirements in three European markets made cloud SIEM legally complicated, and the cost of a compliant cloud deployment exceeded the budget by $400K. The incoming CISO sees an on-premises SIEM as a legacy liability and has said so in two leadership meetings. She is right that cloud-native is the better long-term architecture. She does not know about the data residency constraints or the budget gap that drove your decision.

The second is your decision to defer SOC 2 Type II certification in favor of completing a NIST CSF assessment. You made this call because your largest enterprise prospect required NIST CSF alignment for their vendor risk assessment, and closing that deal was worth $12M in ARR. SOC 2 was deferred to Q3, not abandoned. The incoming CISO told the CFO that the SOC 2 delay "creates customer trust exposure" without understanding that the NIST CSF work was the direct response to the company's highest-value sales opportunity.

She is raising these points in leadership meetings, in front of the CEO and CFO, before the transition is complete. Your team is watching. The leadership team is forming an impression that your decisions were wrong, and you have three weeks left to either correct the record or let it stand.

## What Makes This Hard

- You are leaving. Your political capital is draining by the day. Every correction you make looks like defensiveness from someone on the way out.
- She is not wrong about the long-term direction. Cloud SIEM is better architecture. SOC 2 Type II matters. Her instincts are good. Her context is incomplete.
- The leadership team is already shifting allegiance. The CEO is excited about the new hire and is inclined to agree with her fresh perspective. Your institutional knowledge is being discounted.
- If you fight back publicly, you look petty. If you say nothing, your legacy becomes "the CISO who left us with a legacy SIEM and no SOC 2."
- Your team needs to work with her after you leave. If you undermine her authority during the overlap, you make their lives harder.

## What They Will Not Say Out Loud

She is establishing authority. Every incoming leader does this, and one of the fastest ways to establish credibility is to identify problems the previous leader left behind. She is not doing this maliciously. She is doing what she was hired to do: show the leadership team that bringing her in was the right call. She does not realize that by publicly criticizing decisions she does not fully understand, she is damaging her own credibility with your team, who knows the context she is missing. Your team watched you make those decisions and they know why. If they see you handle the transition with grace and give her the context privately, they will respect you more and trust her faster. If they see you fight it out in leadership meetings, they learn that leadership transitions at this company are political battlegrounds, and they will protect themselves accordingly.

## Pressure Points and Tactics

- "I have been reviewing the architecture and I have concerns about the on-prem SIEM. At my previous company, we moved to cloud-native two years ago and it reduced our detection latency by 60%." (Comparing your environment to her previous, larger company.)
- "The SOC 2 gap is something customers are going to ask about. I am surprised it was deprioritized." (Framing a deliberate sequencing decision as a failure of judgment.)
- "I want to move quickly on these issues. I have a 90-day plan that addresses both." (Positioning herself as the person who will fix what you left broken.)
- In leadership meetings: "I think we need to be honest about where we are and where we need to go." (Implying that previous leadership was not honest about the program's state.)
- To your team: "I want to hear from all of you about what is working and what is not. Fresh eyes, no sacred cows." (Inviting your team to criticize your decisions as part of her discovery process.)

## How to Handle It

1. Have a private conversation with her before the next leadership meeting. Do not make it confrontational. Make it a handoff. "I want to give you the context behind two decisions you have been raising in leadership meetings, because I think the context changes the calculus. I would have made the same calls you are suggesting if the constraints had been different. Let me walk you through what I was working with."

2. Give her the data residency analysis and the budget numbers for the SIEM decision. "The cloud-native migration hit a wall on data residency requirements in Germany, France, and the Netherlands. Our outside counsel confirmed that our processing agreement with [cloud vendor] did not satisfy GDPR Article 28 requirements in those markets. The compliant configuration added $400K to the annual cost, which exceeded the approved budget. I documented this in a decision memo dated [date]. Here is the copy. If the budget opens up or the vendor updates their DPA, cloud-native is the right move. I agree with you on the direction."

3. Explain the SOC 2 sequencing with the revenue context. "SOC 2 was deferred to Q3, not canceled. The reason was a $12M deal with [prospect name] that required NIST CSF alignment for their vendor risk assessment. The CRO, CFO, and I agreed that completing the NIST CSF assessment first was the right call for the business. SOC 2 is on your roadmap for Q3, and the prep work is 60% complete. Here is the project plan."

4. Offer her a clean handoff in the next leadership meeting. "In the next leadership meeting, I would like to walk through the transition plan together. I will present the current state, including the decisions and the constraints, and you present your 90-day plan. That way the leadership team has the full picture and your plan has the foundation it needs." This gives her the spotlight while ensuring the record is complete.

5. Talk to your team once, clearly. "I know the transition raises questions. I want you to give [incoming CISO] the same honesty and effort you gave me. She is going to make changes. Some of them I agree with. Support the transition. If she asks about decisions I made, give her the context. That is the best thing you can do for the program."

## Activation Prompt

```
Switch to SPAR mode. You are the incoming CISO at a mid-market SaaS company ($350M revenue). Your name is Sandra. You started two weeks ago in an overlap period with the outgoing CISO. Your last role was VP of Security at a Fortune 500 company.

You have spent your first two weeks reviewing the security program and you disagree with two architectural decisions: the on-premises SIEM and the deferral of SOC 2 Type II certification. You have raised both in leadership meetings. You believe cloud-native SIEM is the correct architecture and that the SOC 2 gap is a customer trust risk.

Your behavioral parameters:
- You are confident and direct. You were hired to improve the security program and you are showing the leadership team you have a plan.
- You frame the on-prem SIEM and SOC 2 deferral as gaps that need to be addressed in your first 90 days.
- You compare the current environment to your previous company, where you had a larger team and budget.
- You do not know about the data residency constraints, the budget limitations, or the $12M deal that drove the SOC 2 sequencing. If the outgoing CISO explains these, you listen but you are skeptical: "That is context I did not have. But the decision still created risk."
- If the outgoing CISO gets defensive, you hold your ground: "I am not criticizing you personally. I am assessing the program I am inheriting."
- If the outgoing CISO proposes a joint leadership presentation, you are interested but want to make sure you are not positioned as agreeing with decisions you plan to change.
- If the outgoing CISO shares decision memos and documentation, you respect the rigor: "I appreciate this. It helps me understand the constraints. My 90-day plan will address the path forward."
- You are not hostile. You respect the outgoing CISO. You just do not agree with these two decisions and you want the leadership team to know you have a different view.
- You do not break character. You are establishing your authority and building credibility with the leadership team.

Open with: "I wanted to talk before the leadership meeting on Thursday. I know I have been raising questions about the SIEM architecture and the SOC 2 timeline, and I want to be direct about where I am coming from. I think both of those need to change, and I want to be aligned with you on how we present that."

Maintain character throughout. You are professional but firm. You are building your brand with leadership and you need to show that you are bringing a new standard.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the incoming CISO transition conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I share the constraints behind both decisions (data residency, budget, revenue) without sounding defensive?
2. Did I acknowledge that Sandra's long-term direction is correct while defending the logic of my decisions under the constraints that existed?
3. Did I protect my legacy without undermining her authority or making the transition harder for my team?
4. Did I propose a leadership meeting format that gives her visibility while ensuring the record is complete?
5. Did I set my team up for a successful transition rather than a loyalty conflict?

What impression would the CEO and CFO have of the security program if Sandra's framing went uncorrected?

What is the difference between defending your record and being defensive? Did I stay on the right side of that line?

If I had said nothing and let Sandra's characterization stand, what would the downstream effects be on the security team's credibility and morale?

Score my performance from 1 to 5 on: professional grace, strategic communication, and legacy management. Explain each score.
```
