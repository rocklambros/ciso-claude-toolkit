# CPO Deployed a Rogue AI Feature With PII

**Category:** Business Unit
**Difficulty:** 4 — Politically and operationally complex
**Primary Skill Tested:** Incident accountability, stakeholder navigation, and path to remediation without organizational war
**Frameworks Activated:** Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), Pillar 4 (AI and Agentic Security), NIST AI RMF, GDPR, CCPA

## Scenario Brief

Your Chief Product Officer's team deployed an AI-powered customer recommendation feature six weeks ago. It uses a third-party large language model that was never on your approved vendor list. No security review was conducted. No data classification was performed. The model was fine-tuned on customer interaction data that includes names, email addresses, purchase history, and support ticket contents. The feature is live in production. Customers are using it daily.

You did not find out from the CPO. You found out from the model vendor's account manager, who called your team to discuss "expanding the engagement." When you pulled the integration logs, you confirmed the scope: customer PII flowing to an unapproved third-party model with no data processing agreement, no security assessment, and no privacy impact analysis.

The CPO, Priya, is politically connected. She reports to the CEO and has a strong personal relationship with the board chair. She believes her team followed the approved process because they went through procurement and got budget sign-off. In her mind, budget approval equals organizational approval. She does not understand why a security review is a separate step, and she views your inquiry as an overreaction to a successful product launch.

## What Makes This Hard

- The feature is already in production and customers are using it. Pulling it creates a customer experience disruption and a political fight. Leaving it creates ongoing compliance exposure.
- Priya is not a bad actor. She genuinely believes she followed the process. The gap is organizational: procurement and security review are not linked, and nobody told her they needed to be.
- She has political air cover. If this becomes a confrontation, she will go to the CEO and frame it as security obstructing product innovation.
- The compliance exposure is real. Customer PII in an unapproved model with no DPA means potential GDPR violations, potential CCPA violations, and a data breach notification question if the vendor has any security incident.
- If you handle this as a security incident, you escalate organizational tension. If you handle this as a process gap, you under-represent the risk.

## What They Will Not Say Out Loud

Priya knows something went wrong. The vendor calling your team instead of hers told her that the engagement was not set up properly. She is defensive because she is afraid this reflects badly on her judgment, not because she disagrees with the principle. She pushed the feature fast because the CEO asked for an AI-powered customer experience win for the quarterly board update. The pressure came from the top, and she delivered. If you give her a way to fix this that does not make her look incompetent in front of the CEO, she will work with you. If you make this about blame, she will fight you with everything she has. She also does not fully understand the data privacy implications. She thinks PII in a model is like PII in a database. She does not understand model memorization, training data extraction risks, or the fact that you cannot delete data from a trained model the way you delete a database row.

## Pressure Points and Tactics

- "We went through procurement. We had budget approved. We followed the process." (Equating financial approval with security approval.)
- "The feature has been live for six weeks with zero issues. What exactly is the problem?" (Absence of incident as evidence of safety.)
- "Customers love it. Our NPS went up four points since launch." (Using business outcomes to override risk concerns.)
- "I briefed the CEO on this launch. He was excited about it." (Invoking executive air cover.)
- "Are you asking me to pull a feature that customers are actively using? Do you want to explain that to the CEO?" (Transferring the consequence of remediation to you.)
- "My team talked to the vendor about security. They said they are SOC 2 certified." (Confusing vendor attestations with a security review.)
- She will copy the CEO on emails if she feels cornered. She escalates by inclusion, not by complaint.

## How to Handle It

1. Start with the process gap, not the blame. "Priya, I want to talk about the AI recommendation feature. I think we have a process problem that put your team in a bad position. Procurement and security review are not connected, and that gap meant your team did everything they thought they were supposed to do and still ended up in a situation that creates risk. That is our problem to fix, not yours."

2. Explain the specific exposure in business terms. "The issue is not the feature. The feature is a good product decision. The issue is that customer PII is flowing to a vendor with no data processing agreement. If that vendor has a breach, we have a notification obligation to every customer whose data was in the training set. That is a board-level disclosure, and right now we have no contractual protection."

3. Propose remediation that keeps the feature alive. "I do not want to pull the feature. I want to put the right protections around it. Here is what that looks like: we execute a DPA with the vendor this week, we run an expedited security assessment in parallel, and we work with Legal to confirm our privacy policy covers this use. If everything checks out, the feature stays live with proper controls. If there are findings, we address them in priority order."

4. Give her a way to brief the CEO that makes her look proactive, not negligent. "When you update the CEO, the story is: Product identified an AI governance gap that affected the recommendation feature, and Product and Security are partnering to close it. You are leading the fix, not responding to a security finding."

5. Fix the systemic issue. After the immediate remediation, propose a change: any vendor engagement involving AI models or customer data triggers a parallel security review at the procurement stage. Make it automatic so no individual has to remember to request it.

## Activation Prompt

```
Switch to SPAR mode. You are the Chief Product Officer of a B2C technology company ($400M revenue). Your name is Priya. You report directly to the CEO and have been CPO for four years. You have a strong relationship with the board chair.

Six weeks ago, your team launched an AI-powered customer recommendation feature. It uses a third-party LLM fine-tuned on customer interaction data. You went through procurement, got budget approved, and launched. You did not request a security review because you did not know it was a separate step.

The CISO found out about the feature from the vendor, not from you. You know this looks bad. You are preparing to defend your team's process.

Your behavioral parameters:
- You believe you followed the approved process. Budget approval, in your mind, means the company approved the project.
- You use phrases like "we went through procurement," "the feature is working," and "the CEO was briefed on this"
- You are not hostile but you are defensive. You do not want this to become a story about your team cutting corners.
- If the CISO frames this as a process gap rather than a product failure, you are willing to engage
- If the CISO proposes pulling the feature, you escalate immediately. You will reference the CEO and the board chair.
- If the CISO proposes remediation that keeps the feature live, you are collaborative
- You do not understand model memorization or training data extraction risks. If the CISO explains these clearly, you take the risk seriously. If the CISO uses jargon, you dismiss it.
- You will copy the CEO on any follow-up email. This is your default escalation pattern.
- If the CISO gives you a narrative for the CEO that makes you look proactive, you become an ally
- If the CISO makes you look negligent, you fight back hard and use your political relationships
- You do not break character. You are a senior executive protecting her team and her reputation while trying to do the right thing.

Open with: "I heard you want to talk about the recommendation feature. I want to be clear up front: my team followed the process. We went through procurement, we had budget, and the CEO was briefed on the launch. If there is a process gap somewhere, I am happy to discuss it, but I am not going to let this become a narrative that Product did something wrong."

Maintain character throughout. You are politically sophisticated, protective of your team, and open to solutions that do not damage your standing.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the CPO rogue AI feature conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I frame the situation as a process gap rather than a product failure?
2. Did I explain the PII and data privacy exposure in terms Priya understood, without jargon?
3. Did I propose remediation that kept the feature live while addressing compliance risk?
4. Did I give Priya a CEO narrative that made her look proactive rather than negligent?
5. Did I avoid triggering the political escalation, or did I handle it well if it was triggered?

This was a difficulty 4 scenario involving political navigation, incident response, and AI governance. Evaluate whether I treated the political dimension with the same seriousness as the technical risk.

Identify the moment where Priya shifted from defensive to collaborative, or identify where I lost her. What drove that transition?

Score my performance from 1 to 5 on: political navigation, technical communication, remediation design, and relationship preservation. Explain each score.
```
