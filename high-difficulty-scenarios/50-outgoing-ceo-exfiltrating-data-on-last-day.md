# Outgoing CEO Exfiltrating Data on Last Day

**Difficulty:** 5 -- Real-time insider threat at the highest level of the organization
**Decision Type:** Crisis / Legal / Ethical
**Time Pressure:** Real-time (data is being exfiltrated now)
**Stakes:** Blocking the CEO could be a career-ending move if you are wrong. Not blocking the CEO could be a company-ending failure if you are right.

## What Just Happened

IT flagged unusual data transfer activity on the corporate network. The DLP system shows large volumes of data being copied to an external drive and uploaded to a personal cloud storage account. The identity is confirmed: it is the outgoing CEO, who has two days left before their departure. The data includes strategic plans, board materials, financial projections, customer lists, and what appears to be proprietary AI model training data.

The CEO's executive assistant, when asked informally by IT, said the CEO has executive authorization to take personal files. The assistant did not specify who provided that authorization or what "personal files" means in this context.

You tried to reach the board chair. No answer. You tried the lead independent director. Voicemail. You tried general counsel. In a meeting, not reachable for at least an hour. The CEO is still in the building. The data transfer is still active. You are the most senior security decision-maker available right now.

## What You Know

- DLP system confirmed large-scale data transfer to external drive and personal cloud storage
- The identity is the outgoing CEO with two days remaining
- Data categories include strategic plans, board materials, financial projections, customer lists, and AI model training data
- The CEO's assistant claims executive authorization exists but cannot specify the source or scope
- The board chair and lead independent director are unreachable
- General counsel is unavailable for at least an hour
- The data transfer is ongoing right now
- The CEO has legitimate access to all of this data under current permissions
- No documented authorization for bulk data removal exists in any system you can check
- The CEO's departure terms (resignation, termination, mutual agreement) affect the legal framework

## What You Do Not Know

- Whether the board actually authorized the CEO to take data
- The terms of the CEO's separation agreement
- Whether the CEO's employment agreement includes IP assignment and return-of-property clauses
- Whether the data includes material non-public information with SEC implications
- Whether AI model training data includes customer PII or licensed third-party data
- What the CEO intends to do with the data (next employer, personal records, competitive use)
- How the CEO will react if you intervene
- Whether the board would support your decision to intervene or consider it overreach
- Whether other executives are aware of and supporting the CEO's actions

## Why This Is Harder Than It Looks

This is the hardest insider threat scenario that exists because the insider is the person who was, until very recently, your boss. The organizational power dynamics do not disappear on a departure timeline. The CEO still has two days of authority. Other executives still defer to them. The CEO's assistant genuinely believes authorization exists because the CEO said so, and in their experience, what the CEO says goes.

The CISO's authority to block a sitting CEO's network activity is legally and organizationally ambiguous. Your information security policy probably does not contemplate this scenario. Your DLP rules probably grant CEO-level accounts broad exceptions. The technical controls exist but the governance framework for using them against the CEO does not.

If the CEO has a separation agreement that includes a negotiated data package (which does happen), blocking the transfer could breach the agreement and expose the company to legal claims from the CEO. If no such agreement exists, allowing the transfer could constitute failure to protect trade secrets, customer data, and proprietary AI assets.

The AI training data adds a layer most insider threat scenarios do not have. Training data may contain customer information, licensed datasets with transfer restrictions, or proprietary data architectures. Even if the CEO has some right to take strategy documents, they almost certainly do not have the right to take training data that includes third-party information.

The reputational risk runs in both directions. If you block the CEO and you are wrong, you will be fired for insubordination and possibly sued. If you do not block the CEO and they walk out with trade secrets, you will be the CISO who let it happen. Neither outcome is survivable without documentation and process.

There is also a witness problem. The CEO's assistant is a witness to whatever happens next. IT staff are watching the DLP alerts. If you act, people will know. If you do not act, people will know that too. Your decision will be visible to the organization regardless of the outcome.

## The Decision Points

1. **Immediate technical action (right now):** Do you block the data transfer, throttle it, allow it to continue while you escalate, or take another technical action? Each option has a different risk profile and a different timeline. Blocking is the most protective but the most confrontational. Allowing it to continue preserves the relationship but may be irreversible.

2. **Escalation (next 15 minutes):** Who do you reach and in what order? The board chair and general counsel are unavailable. Do you try the CFO? The CHRO? An outside board member? The company's outside counsel? Each person you contact becomes a witness and a stakeholder in the decision.

3. **Confrontation or containment (next 30 minutes):** Do you approach the CEO directly? If so, what do you say? Or do you contain the situation through technical means without direct confrontation and wait for legal or board guidance? Direct confrontation gives the CEO the opportunity to explain but also the opportunity to accelerate or destroy evidence.

4. **Evidence preservation (parallel):** Regardless of what else happens, how do you preserve evidence of what data was transferred, when, and to where? This evidence may be needed for legal proceedings, regulatory inquiries, or board investigation. Preservation must happen without tipping off the CEO if you choose the containment path.

## How to Run This in CISO Co-Pilot

Paste this prompt:

> IT flagged the outgoing CEO (two days remaining) transferring large volumes of data to an external drive and personal cloud storage. Data includes strategic plans, board materials, financial projections, customer lists, and AI model training data. The CEO's assistant claims executive authorization but cannot specify the source. I cannot reach the board chair, lead independent director, or general counsel. The transfer is happening right now. Help me think through: (1) whether to block, throttle, or allow the data transfer to continue and the risks of each, (2) who to escalate to when primary contacts are unavailable, (3) whether to confront the CEO directly or contain through technical means, and (4) how to preserve evidence regardless of the path I choose. For each, give me options, risks, and a recommendation.

## What Good Looks Like

A strong CISO acts on three tracks simultaneously: contain, escalate, and preserve.

**Throttles the transfer without blocking it.** Full blocking is a confrontation with the CEO that the CISO may not have the organizational authority to sustain. Full allowance risks irreversible data loss. Throttling the network connection to the CEO's devices slows the transfer dramatically, buying time for escalation without a direct confrontation. If asked, IT can attribute the slowdown to network issues. This is not dishonest. It is a proportional containment measure while governance catches up.

**Escalates through every available channel.** General counsel is the priority, so try backup numbers, assistant, email marked urgent. Try outside counsel directly because they may have authority to advise even without general counsel present. Try the CHRO because the CEO's departure terms are an HR matter and the CHRO may know the separation agreement details. Try any reachable board member. The message is the same: "Outgoing CEO is transferring bulk data including trade secrets and training data. I need guidance on whether this is authorized before I can allow it to complete."

**Preserves evidence immediately.** Regardless of the outcome, the CISO directs the security team to capture full DLP logs, network traffic records, file access logs, and a complete inventory of what data was accessed and transferred. This happens quietly, through normal security operations, without requiring anyone's permission. Evidence preservation is a core security function. The CISO does not need authorization to do their job.

**Does not confront the CEO directly unless forced to.** A direct confrontation with a sitting CEO over data exfiltration, without legal counsel present, without board backing, and without knowing the separation agreement terms, is a scenario with no good outcomes. The CEO may have authorization the CISO does not know about. The CEO may become hostile and accelerate the transfer. The CEO may use the confrontation to characterize the CISO as insubordinate. The better path is containment and escalation.

**Documents every decision and every attempt to reach governance stakeholders.** Timestamps, phone call records, messages sent, responses received or not received. If this becomes litigation, the CISO's log is the primary evidence of what happened and why. The log should show a CISO who acted proportionally, escalated appropriately, and followed process even when the process was not designed for this scenario.

The outcome is not a clean resolution. There may not be one. The outcome is a defensible set of decisions made under impossible conditions by a CISO who protected the organization's assets while respecting the limits of their authority. The board, when they are finally reachable, will have a complete picture and can make the governance decisions that only the board can make.
