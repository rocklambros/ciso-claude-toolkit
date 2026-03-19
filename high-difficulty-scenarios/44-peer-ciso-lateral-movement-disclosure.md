# Peer CISO Lateral Movement Disclosure

**Difficulty:** 5 -- Crisis management with incomplete information under a hard external deadline
**Decision Type:** Crisis / Legal / Political
**Time Pressure:** Real-time (two hours before partner's public disclosure)
**Stakes:** Your organization may already be compromised, and the window to act before the story goes public is closing fast.

## What Just Happened

A peer CISO at a partner organization just called you directly. Their company is about to announce a breach. Press release drops in two hours. During their forensic investigation, the IR team found lateral movement that may have crossed into your environment through a shared integration. The peer is giving you a heads-up as a professional courtesy. They are not required to. Their legal team does not know they are making this call.

You have no alerts, no indicators of compromise in your environment, and no confirmation that you are affected. You only have the word of a peer under enormous pressure who may or may not have the full picture of their own incident.

## What You Know

- Partner organization confirmed a breach with lateral movement
- Shared integration exists between your environments (API connectivity, shared credentials, or federated access)
- Partner's press release drops in approximately two hours
- Your peer disclosed this outside their own legal guidance
- Your SOC has no current alerts related to this vector
- The partner's forensic investigation is still active and findings are preliminary

## What You Do Not Know

- Whether the lateral movement actually reached your environment
- The scope, timeline, or method of the original compromise at the partner
- Whether the shared integration was the actual attack path or just a theoretical one
- Whether your peer's information is complete or accurate given their own fog of war
- Whether other partner organizations received the same call
- What the partner's press release will say about downstream impact
- Whether your organization will be named or implied in public reporting

## Why This Is Harder Than It Looks

The two-hour window creates a false binary: act now or get caught flat-footed when the story breaks. But acting on unverified information carries its own damage. If you escalate a potential breach to your board and it turns out you were never affected, you burned credibility and created unnecessary panic. If you do not escalate and you were affected, you failed your most basic duty.

The peer CISO acted outside their legal guidance to warn you. That creates an information-handling problem. You now possess material non-public information about another company's security incident. If the partner is publicly traded, there are insider trading implications for anyone you tell. If you are publicly traded, there are disclosure implications for your own organization.

Your SOC showing no alerts means nothing. Absence of evidence is not evidence of absence, especially against an adversary capable of lateral movement across organizational boundaries. A clean dashboard could mean you are fine or could mean the attacker is better at hiding than your tools are at finding.

The peer's legal team does not know about this call. That means the information you received has no legal framework around it. No NDA, no joint defense agreement, no coordinated disclosure plan. You are operating in a gray zone where the information itself is a liability.

When the press release drops, reporters will call your comms team. Your board members will read the news. Regulators will start asking questions about downstream impact. You need a position before any of that happens, and right now you do not have the facts to form one.

## The Decision Points

1. **Immediate response (next 15 minutes):** Do you activate your incident response process based on unverified information from an informal channel? Full activation, limited activation, or investigation-only mode?

2. **Notification chain (next 30 minutes):** Who do you tell, in what order, and what exactly do you say? General counsel needs to know but the information has legal sensitivity. The CEO needs to know but you have nothing confirmed. The board chair may need to know but premature escalation has costs.

3. **Technical action (next 60 minutes):** Do you sever or restrict the partner integration before you have evidence of compromise? Cutting the connection is safe but may disrupt business operations and signal to the partner (and their legal team) that you received advance notice.

4. **External posture (before the press release):** What is your prepared statement if reporters or regulators ask whether you are affected? "Investigating" is honest but sounds bad. "Not affected" may be premature. Silence is not an option once the story breaks.

## How to Run This in CISO Co-Pilot

Paste this prompt:

> A peer CISO at a partner organization just called me directly. Their company is announcing a breach in two hours. Their IR team found lateral movement that may have crossed into our environment through a shared integration. The peer disclosed this outside their own legal guidance as a professional courtesy. My SOC has no current alerts. I have no confirmation we are affected. Help me think through each decision point: (1) whether and how to activate incident response on unverified information, (2) who to notify and in what order given the legal sensitivity of how I received this information, (3) whether to restrict the partner integration before confirming compromise, and (4) what external posture to prepare before the press release drops. For each decision, walk me through the options, the risks of each option, and your recommendation.

## What Good Looks Like

A strong CISO does four things in the first 30 minutes:

**Activates proportionally.** Not full incident response. Not nothing. A scoped investigation with the IR lead and one senior analyst, focused on the specific integration, looking for indicators consistent with what the peer described. This preserves confidentiality while starting the clock on actual evidence gathering.

**Calls general counsel immediately.** Not to ask permission. To inform them that material non-public information about a partner's breach arrived through an informal channel, that it may implicate the organization, and that a coordinated legal and technical response is needed within 90 minutes. The lawyer needs to know the information exists regardless of whether a breach is confirmed.

**Documents everything.** The time of the call, what was said, what was not said, and every decision made from this point forward. If this becomes a regulatory matter or litigation, the decision log is the CISO's best protection.

**Prepares a holding statement without committing to a conclusion.** Something like: "We are aware of reports regarding [partner]. We are actively reviewing our environment and our integration with [partner] as a precautionary measure. We will provide updates as our review progresses." This is honest, measured, and does not reveal advance knowledge or make claims that might need to be walked back.

The outcome is not certainty. The outcome is a defensible process that scales appropriately whether the answer turns out to be "we were compromised" or "we were never touched." The CISO who handles this well is the one whose response looks the same in hindsight regardless of which scenario materialized.
