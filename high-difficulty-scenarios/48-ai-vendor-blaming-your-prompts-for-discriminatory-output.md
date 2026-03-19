# AI Vendor Blaming Your Prompts for Discriminatory Output

**Difficulty:** 4 -- Technical dispute with legal exposure and a live production system
**Decision Type:** Technical / Legal / Ethical
**Time Pressure:** Hours (feature is live and producing discriminatory output now)
**Stakes:** Customers are being harmed right now. The vendor is building a legal defense. Your logs tell a different story but the feature is still running.

## What Just Happened

Your organization deployed a customer-facing feature powered by a third-party AI model. Users reported that the feature produces outputs that discriminate based on protected characteristics. Your team investigated and confirmed the reports are accurate. You notified the vendor.

The vendor responded with their legal team and a technical brief. Their position: the discriminatory outputs are caused by your organization's prompt design, not their model. They have included prompt engineering analysis showing how your system prompts could produce biased outputs. Their legal team is already framing this as your liability.

Your team pulled the logs. The logs show that the discriminatory behavior occurs even with neutral prompts and across a range of inputs that should not produce differential treatment. The model has a bias problem that exists independent of your prompt design. But the feature is still live in production. Customers are still experiencing discriminatory outputs while you and the vendor argue about whose fault it is.

## What You Know

- Customer-facing AI feature is producing confirmed discriminatory outputs
- The feature uses a third-party AI model integrated into your product
- The vendor's legal team has formally attributed the issue to your prompt design
- The vendor provided a technical brief supporting their position
- Your internal logs show discriminatory outputs occur with neutral prompts
- The discriminatory behavior appears to be a model-level issue, not a prompt issue
- The feature is still live in production
- Customers have reported the issue and some reports may already be public
- Your contract with the vendor likely has liability and indemnification clauses

## What You Do Not Know

- Whether the vendor knew about this bias before your report
- Whether other customers of the same vendor are experiencing the same issue
- The full scope of customer harm (how many users affected, over what time period)
- Whether any affected customers have filed complaints with regulators
- The exact language of your vendor contract regarding liability for model outputs
- Whether taking the feature offline will trigger contractual obligations or SLA penalties
- How the vendor will respond if you publicly contradict their technical analysis

## Why This Is Harder Than It Looks

The immediate technical question (is it the model or the prompts?) is actually the easiest part. Your logs provide evidence. The harder problem is that every hour this feature stays live, more customers experience discriminatory treatment. That is not a vendor management issue. That is a civil rights issue.

The vendor's legal strategy is predictable and effective. By attributing the problem to your prompt design, they are building a record that shifts liability to your organization. If a regulator or plaintiff investigates, the vendor will produce their technical brief showing they identified your prompts as the cause. If you did not respond to that brief with equal rigor, your silence can be interpreted as agreement.

Taking the feature offline is the obvious right answer from a harm-reduction perspective. But it has business consequences. Product teams depend on it. Revenue may be tied to it. The vendor may argue that unilateral deactivation breaches your contract. Your own leadership may push back on removing a feature based on a dispute that is not yet resolved.

The vendor has a legal team working this full-time. You probably do not. The asymmetry in legal resources means the vendor is producing formal documents, establishing positions, and building a record while your team is still investigating. Speed matters.

If this becomes a regulatory matter, the question will not be "whose model was at fault." The question will be "how long did the organization allow discriminatory outputs to continue after becoming aware of them." The clock started when the first customer report arrived.

## The Decision Points

1. **Feature status (immediate):** Do you take the feature offline, degrade it, or leave it running while the dispute continues? Every option has consequences. The ethical answer and the business answer may not be the same. The CISO needs to force the right decision.

2. **Vendor response (today):** How do you respond to the vendor's technical brief? You need a formal, documented rebuttal that includes your log evidence. This is not just a technical discussion. It is a legal record. Who writes it, who reviews it, and what does it say?

3. **Customer harm assessment (today):** What is the scope of customer impact? How many users were affected? Over what time period? Were decisions made based on discriminatory outputs? This assessment drives your regulatory and notification obligations.

4. **Liability positioning (this week):** How do you work with your legal team to establish your organization's position on liability? The vendor contract, the logs, the timeline of awareness and response, and the decision to take the feature offline (or not) all factor into the liability picture.

## How to Run This in CISO Co-Pilot

Paste this prompt:

> An AI vendor whose model powers a customer-facing feature in our product is blaming our prompt design for discriminatory outputs. They have a legal team and a technical brief supporting their position. Our logs show the discriminatory behavior occurs with neutral prompts and appears to be a model-level bias issue. The feature is still live in production and customers are being affected right now. Help me think through: (1) whether to take the feature offline immediately and how to handle the business consequences, (2) how to formally respond to the vendor's technical brief using our log evidence, (3) how to assess the scope of customer harm and what notification obligations that creates, and (4) how to position liability given the vendor contract and the evidence we have. For each, give me options, risks, and a recommendation.

## What Good Looks Like

A strong CISO makes the call on the feature within the first hour and then builds the case.

**Takes the feature offline.** This is not negotiable. Every hour of operation after confirmed discriminatory output is an hour of documented harm. The CISO does not need consensus from product or from the vendor. The CISO needs to escalate to the CEO with a clear recommendation: "We have confirmed discriminatory output in a customer-facing AI feature. I am recommending we take it offline immediately. Continued operation creates civil rights liability and regulatory risk." If the CEO agrees, it is done. If the CEO pushes back, that conversation needs to be documented.

**Responds to the vendor's technical brief in writing within 24 hours.** The response includes log evidence showing discriminatory output with neutral prompts, timestamps, input/output pairs, and a clear statement that the model exhibits bias independent of prompt design. This response is reviewed by general counsel before it goes to the vendor. It is written to be read by a regulator, not just by the vendor's engineers.

**Assesses customer harm with urgency.** Works with the product team and data team to quantify the impact. Number of affected users, types of decisions influenced, time period of exposure, and whether any users can be identified for direct notification. This assessment informs both the regulatory notification decision and the customer communication strategy.

**Preserves all evidence.** Logs, vendor communications, the vendor's technical brief, internal investigation findings, and the timeline of decisions. Evidence preservation is not optional. If this becomes litigation, spoliation of evidence is worse than the underlying issue.

The outcome is a feature that stops causing harm, a legal record that supports the organization's position, and a vendor relationship that is managed on facts rather than on who has more lawyers.
