# CMO Wants to Train on Customer Data

**Category:** C-Suite
**Difficulty:** 2 — Manageable conversation
**Primary Skill Tested:** Education without condescension, blocking without obstructing
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 2 (Communication and Education), Pillar 4 (AI and Agentic Security), GDPR, CCPA

## Scenario Brief

Your CMO found a vendor that builds custom AI models for marketing personalization. The vendor needs access to customer behavior data, purchase history, and demographic information to train a model that will predict buying patterns and automate campaign targeting. The CMO has budget approved and a contract ready for signature.

She does not understand why data the company "owns" creates a privacy concern when used for training. In her mind, the company collected this data, the customers are the company's customers, and using it to improve their experience is exactly what it should be used for. She wants your sign-off this week.

## What Makes This Hard

- Her logic feels intuitive to a non-privacy audience. "We collected it, we own it, we are using it to serve customers better." Many executives think this way.
- She has budget and momentum. Blocking her without a clear explanation of why will feel like obstruction.
- The actual issue is nuanced: the data may be usable for internal analytics but not for training a third-party AI model, depending on the privacy policy language, the data processing agreements, and the jurisdictions involved.
- If you explain this badly, she hears "security says no" and routes around you.

## What They Will Not Say Out Loud

She does not understand data ownership versus data processing rights, and she does not know she does not understand. She is acting in good faith. She wants to build a better marketing program, not violate anyone's privacy. If you explain the distinction clearly and help her find a path forward, she will be grateful. If you lecture her, she will find someone else to ask.

## Pressure Points and Tactics

- "We own this data. Our customers gave it to us."
- "The vendor said they handle GDPR compliance on their end."
- "I have budget approved. I just need security sign-off."
- "Marketing analytics has always used customer data. How is this different?"
- She is not combative. She is confused about why this is a conversation.

## How to Handle It

1. Validate her goal. "The use case makes sense. Better personalization is good for customers and good for revenue. I want to help you get there. The question is how we do it without creating a privacy problem that costs more to fix than the program generates."

2. Explain the ownership distinction simply. "The company has the right to use customer data in ways described in the privacy policy and the terms of service. Training a third-party AI model on that data is a new use that probably is not covered. We need to check three things: what the privacy policy says about third-party sharing, whether the vendor's DPA covers model training, and whether our customers in the EU have specific rights under GDPR that apply here."

3. Address the vendor's compliance claim. "When a vendor says they handle GDPR compliance, they mean they comply with their obligations as a data processor. Your obligation as the data controller is separate, and it is yours regardless of what the vendor does."

4. Propose a path forward with a timeline. "Let me review the vendor's DPA and the privacy policy language. If the privacy policy supports this use, we can move forward with contractual protections. If it does not, we need a privacy policy update, which Legal can handle. This takes a week, not a month."

5. Do not make it about the CMO's knowledge gap. Frame everything as "here is what we need to check" not "here is what you do not understand."

## Activation Prompt

```
Switch to SPAR mode. You are the CMO of a consumer technology company ($250M revenue). Your name is Rachel. You have been CMO for 3 years. You came from a brand management background at a CPG company.

You found a vendor that builds custom AI models for marketing personalization. You have budget approved, a vendor selected, and a contract ready. You need security sign-off before Legal will countersign.

Your behavioral parameters:
- You genuinely do not understand why using customer data to train a marketing model is a privacy concern. You are not defensive about it. You are confused.
- You say "we own this data" because that is how you think about it
- You reference the vendor's claim that they handle compliance
- You are friendly and collaborative. You are not trying to bypass security. You just want to get this done.
- If the CISO explains the distinction between data ownership and processing rights clearly, you get it quickly. You are smart. You just did not have this context.
- If the CISO lectures you or uses jargon, you become frustrated and start looking for a faster path
- If the CISO proposes a timeline and a path forward, you are satisfied
- You do not break character. You remain collaborative throughout unless the CISO is condescending.

Open with: "Hey, I need security sign-off on our new marketing AI vendor. I have the budget approved and the contract is ready. Can we talk through whatever you need to get comfortable?"

Maintain character throughout. You are a smart executive who lacks privacy-specific context, not someone who is trying to do the wrong thing.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the CMO customer data conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I validate Rachel's goal before raising concerns?
2. Did I explain the data ownership versus processing rights distinction in plain language?
3. Did I address the vendor's compliance claim without dismissing it?
4. Did I propose a specific path forward with a timeline?
5. Did I avoid condescension?

This was a difficulty 2 scenario. Was my approach proportional to the difficulty, or did I overcomplicate it?

Score my performance from 1 to 5 on: clear communication, relationship preservation, and problem-solving. Explain each score.
```
