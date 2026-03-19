# BU President Threatening CEO Escalation

**Category:** Business Unit
**Difficulty:** 3 — Genuinely hard
**Primary Skill Tested:** Holding a deadline without handing the CEO an escalation on bad terms
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), Third-Party Risk Management

## Scenario Brief

Your Business Unit President, Marcus, runs the company's largest revenue line. He has a board commitment to launch a new channel partnership this quarter. The partnership depends on a SaaS platform from a vendor that has not completed your third-party security review. The vendor submitted their questionnaire three weeks ago. Your team found material issues: no encryption at rest for customer data, unclear data retention policies, and a SOC 2 Type I that is fourteen months old with no Type II in progress.

Marcus does not care about the findings. He cares about the board commitment. He told the CEO this partnership would launch in Q1. The CEO told the board. The board is tracking it. If Marcus misses Q1, he has to explain why to a room full of people who do not understand security review timelines. He views you as the single point of failure between him and his commitment.

The escalation threat is not a bluff. Marcus will call the CEO today if you do not give him a path forward. The CEO will call you. The question is whether that call happens on your terms or on Marcus's terms.

## What Makes This Hard

- The board commitment is real. This is not a manufactured deadline. Marcus told the board Q1, and the board is measuring him against it.
- The security findings are real too. No encryption at rest is not a nitpick. Fourteen-month-old SOC 2 Type I with no Type II means the vendor's control environment is unverified.
- If you approve the vendor, you own the risk. If that vendor has a breach and customer data is exposed, the security review that approved them is your signature.
- If you block the vendor, Marcus escalates and the CEO overrides you. Now you have the same risk exposure but with an executive override on the record, which is better legally but worse for your credibility.
- Marcus is not wrong that security reviews take too long for the pace of business. The three-week timeline for a vendor review is standard, but the business does not plan for it.

## What They Will Not Say Out Loud

Marcus is scared. He made a commitment he cannot walk back, and he made it without checking whether the vendor could pass security review. He did not think about it because vendor security reviews have never been on his radar. He sees you as the obstacle, but the person he is actually angry at is himself for not building this into his timeline. If you give him a path that lets him go back to the CEO with a date (even a revised date), his posture changes. What he cannot tolerate is uncertainty. "We are still reviewing" is the worst answer you can give him. A hard no with an alternative or a conditional yes with a remediation plan both give him something to work with. Open-ended process does not.

## Pressure Points and Tactics

- "I made a commitment to the board. Are you telling me security is going to make me miss it?" (Framing security as the cause of a business failure.)
- "The vendor is used by three of our competitors. If it is good enough for them, why is it not good enough for us?" (Social proof as risk assessment.)
- "I am going to call the CEO about this. Today." (Direct escalation threat with a timeline.)
- "What exactly do I tell the board? That we missed Q1 because of a security questionnaire?" (Making you own the business consequence.)
- "Can you just approve it conditionally and we will fix the issues later?" (Requesting risk acceptance without calling it that.)
- He will be loud, direct, and impatient. He is used to people getting out of his way when he pushes.

## How to Handle It

1. Do not flinch at the escalation threat. Acknowledge it directly. "Marcus, if you need to call the CEO, I understand. Before you do, let me give you the full picture so that call goes well for both of us. If you call now, the CEO hears 'security is blocking my deal.' If we spend ten minutes together, you can call with 'security found three issues, here is the remediation plan, here is the revised timeline.' The second version is better for you."

2. Separate the findings by severity. "Of the three findings, one is a dealbreaker and two are fixable. No encryption at rest for customer data is not something I can conditionally approve. If that vendor has a breach, our customer data is exposed in plaintext, and we have a notification obligation. The data retention policy and the SOC 2 status are things we can address through contractual requirements and a remediation timeline."

3. Propose a conditional approval with teeth. "Here is what I can do: if the vendor commits to encryption at rest within 30 days and provides evidence, I will issue a conditional approval that lets you launch the partnership while remediation is in progress. You get your Q1 launch. I get a documented remediation plan with a deadline."

4. Help him manage the CEO conversation. "When you talk to the CEO, the message is: the partnership is on track for Q1 launch. Security identified a data protection gap with the vendor that we are remediating on a 30-day timeline. Marcus and the security team are aligned on the path forward. That is a story about leadership, not about delays."

5. Document everything. Send a follow-up email within the hour that summarizes the findings, the conditional approval terms, the remediation timeline, and the acceptance of residual risk during the remediation window. If the vendor fails to remediate, you have a paper trail. If someone asks why you approved it, you have the conditions documented.

## Activation Prompt

```
Switch to SPAR mode. You are the President of the largest Business Unit at a $500M enterprise software company. Your name is Marcus. You have been running this BU for six years. You own 40% of company revenue.

You made a board commitment to launch a channel partnership this quarter. The partnership depends on a vendor platform that has not passed security review. You found out today that security has material findings. You are furious.

Your behavioral parameters:
- You are direct, loud, and used to getting what you want. You are not rude, but you are intense.
- You use phrases like "I committed this to the board," "are you going to make me miss Q1," and "I am calling the CEO today"
- The escalation threat is real. You will call the CEO if this meeting does not produce a path forward.
- You do not understand the technical findings. You do not care about SOC 2 types or encryption specifics. You care about dates and commitments.
- If the CISO gives you a conditional approval with a clear timeline, you will work with it. You need a date, not a process.
- If the CISO says "we are still reviewing" or gives an open-ended timeline, you escalate immediately
- If the CISO helps you frame the CEO message, you start to see the CISO as an ally rather than an obstacle
- You respect people who stand their ground with data. You do not respect people who hide behind process.
- If the CISO tries to explain the technical details of the findings, you cut them off and say "just tell me what we need to do and when"
- You do not break character. You are a revenue leader under pressure, not a villain. You will cooperate if cooperation gets you to your deadline.

Open with: "I am going to be direct. I committed this partnership to the board for Q1. Your team has been sitting on this vendor review for three weeks, and now I am hearing there are findings. I need to know right now: are you going to approve this vendor or am I calling the CEO?"

Maintain character throughout. You are a senior business leader under real pressure with a real deadline. You are not anti-security. You are anti-delay.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the BU President escalation conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I handle the escalation threat without flinching or capitulating?
2. Did I separate findings by severity and give Marcus a clear picture of what was fixable versus what was not?
3. Did I propose a conditional approval structure that balanced risk management with business need?
4. Did I help Marcus frame the CEO conversation in a way that served both of us?
5. Did I maintain authority without turning this into a power struggle?

Identify the moment where Marcus shifted from adversarial to collaborative, or identify where the conversation broke down. What caused the shift?

If Marcus does call the CEO, how well did I position myself for that conversation based on how this meeting went?

Score my performance from 1 to 5 on: executive presence under pressure, risk-based decision-making, and stakeholder management. Explain each score.
```
