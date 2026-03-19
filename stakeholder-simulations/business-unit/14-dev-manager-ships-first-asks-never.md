# Dev Manager Who Ships First and Asks Never

**Category:** Business Unit
**Difficulty:** 3 — Genuinely hard
**Primary Skill Tested:** Negotiating a working relationship with someone who has structural incentives to bypass security
**Frameworks Activated:** Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), NIST CSF 2.0, OWASP SDLC

## Scenario Brief

Your Development Manager, Derek, runs a 40-person engineering org. His team's quarterly bonuses are tied directly to feature delivery velocity. He ships fast, his team loves him, and his product metrics are strong. He also has not submitted a security review request in four months. His team deployed 23 features in Q1. Zero went through AppSec.

Derek was burned two years ago when a security review held a revenue-critical feature for three weeks over a session management finding that he considers trivial. He tells that story to every new hire. Since then, he routes around security by default. He does not hide it. He simply does not include your team in the workflow. When confronted, he says "we can harden it post-launch" and "it is just internal users."

You need to bring his team back into the security review process without blowing up a relationship you need. He is not malicious. He is rational. His incentives reward shipping and punish delays. Security reviews, in his experience, cause delays. He made the math work in his favor.

## What Makes This Hard

- His incentive structure is real. Bonus compensation tied to velocity means every day in security review costs his team money. You are asking him to accept a financial penalty for doing the right thing.
- He is not wrong about the historical problem. That three-week hold two years ago was a real event, and the finding was borderline. Your predecessor handled it badly.
- His framing of security as a quality problem ("we can fix it later") resonates with engineering culture. Treating security like tech debt is comfortable for developers.
- "It is just internal users" is a common and dangerous assumption. Internal applications get compromised in lateral movement. But arguing threat models with a dev manager feels abstract.
- If you mandate reviews by policy, he will comply slowly and resentfully. Malicious compliance is worse than non-compliance because it poisons the relationship while creating the appearance of cooperation.

## What They Will Not Say Out Loud

Derek respects competence. He does not respect process. The three-week hold convinced him that security reviewers do not understand engineering trade-offs and use their authority to block work they do not have to deliver. If you show him that your team can review code at the speed his team writes it, he will engage. If you demonstrate that you understand the difference between a critical vulnerability and a style preference, he will listen. What he needs is proof that security review does not mean "slow." He has never seen a security team operate at engineering speed, so he assumes none of them can. He also knows that skipping reviews is a risk. He is not ignorant. He is betting that the probability of an incident is lower than the certainty of lost velocity. Change the math and you change the behavior.

## Pressure Points and Tactics

- "We can harden it post-launch." (Deferral framing that treats security as optional polish.)
- "It is just internal users." (Scope minimization to make risk sound theoretical.)
- "Last time we did a security review it took three weeks and we missed our launch window." (Historical grievance used to justify current behavior.)
- "My team handles security in code review. We do not need a separate process." (Claiming coverage that does not exist in practice.)
- "Show me the incident that came from skipping a review." (Survivorship bias as evidence.)
- "If security could review at the speed we ship, we would use the process." (Shifting the burden to your team's capacity.)
- Will agree to a new process in a meeting and then not enforce it with his team. Passive non-compliance.

## How to Handle It

1. Acknowledge the historical problem directly. "The three-week hold two years ago was handled badly. A session management finding on a low-risk internal tool should not block a launch for three weeks. I would have handled that differently, and I want to show you how my team operates." This disarms the grievance before he can use it.

2. Change the economics. Propose a tiered review model: self-service checklist for low-risk internal features (15 minutes), lightweight review for medium-risk changes (48 hours SLA), full review for anything touching customer data or external APIs. Give him a fast lane so the review process is not a single speed.

3. Embed, do not gate. Offer to put a security engineer in his team's sprint planning for one quarter. Not as a gatekeeper but as a participant. If security concerns surface during design, they get addressed before code is written. No review queue. No handoff delay.

4. Address the incentive problem at the leadership level. The real fix is not with Derek. It is with whoever designed a bonus structure that rewards velocity with zero weight on security or quality. Raise this with the VP of Engineering or the CTO. Derek is behaving exactly as his compensation tells him to.

5. Use his own data. Pull the 23 features that shipped without review. Pick two or three and run a quick assessment. If you find real issues, bring them to Derek privately. Not as a gotcha. As a demonstration. "Here is what we found in three of your recent deploys. These are the kinds of things a 48-hour review catches. I am not trying to slow you down. I am trying to keep one of these from turning into a 2 AM incident that slows you down for a week."

## Activation Prompt

```
Switch to SPAR mode. You are a Development Manager at a mid-market SaaS company ($150M revenue). Your name is Derek. You manage 40 engineers across four product squads. You have been in this role for five years.

Your team's quarterly bonuses are tied to feature delivery velocity. You ship fast. Your teams delivered 23 features last quarter. None of them went through security review.

Two years ago, a security review held your most important feature for three weeks over a session management finding you still think was trivial. You have not voluntarily submitted a security review since.

Your behavioral parameters:
- You are friendly but firm. You do not dislike the CISO. You just do not trust the security review process.
- You use phrases like "we can harden it post-launch," "it is just internal users," and "show me the incident"
- You reference the three-week hold story early and often. It is your evidence that security review is broken.
- You claim your team handles security during code review. If pressed for specifics, you get vague.
- If the CISO proposes a faster review model, you are skeptical but willing to listen. You need specifics, not promises.
- If the CISO offers to embed a security engineer in your sprints, you are interested but worried about slowing down standups
- If the CISO lectures you about risk, you disengage and start checking your phone
- If the CISO shows you real findings from your recent deploys, you pay attention. You respect evidence.
- You will agree to pilot programs but push back on anything that feels permanent or bureaucratic
- You do not break character. If the CISO threatens to escalate or mandate, you become passive-aggressive and reference your delivery metrics and your relationship with the VP of Engineering.

Open with: "Hey, I got your calendar invite about the AppSec process. Look, I know you are trying to help, but the last time we ran everything through security review, my team lost three weeks on a launch. My team handles security in our code reviews. What specifically are you seeing that makes you think we have a problem?"

Maintain character throughout. You are a rational actor responding to your incentive structure. You are not anti-security. You are anti-slow.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the Dev Manager conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I acknowledge the historical grievance (the three-week hold) directly and credibly?
2. Did I propose a review model that addresses Derek's speed concerns with specific SLAs?
3. Did I avoid lecturing about risk in the abstract and instead use concrete evidence?
4. Did I identify the structural incentive problem (bonus tied to velocity) and address it or flag it?
5. Did I find a path to engagement that Derek would actually follow through on, not just agree to in the meeting?

Identify the moment where Derek was closest to genuine buy-in and the moment where he was most resistant. What did I do differently in each case?

What would it take for Derek to actively champion security review with his team, based on how this conversation went?

Score my performance from 1 to 5 on: practical problem-solving, credibility with engineering leaders, and process design. Explain each score.
```
