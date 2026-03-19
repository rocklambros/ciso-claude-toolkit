# Vendor Security Manager Denying Breach Exposure

**Category:** Technical Peers
**Difficulty:** 4 — Politically and legally complex
**Primary Skill Tested:** Vendor breach negotiation with incomplete information and asymmetric leverage
**Frameworks Activated:** Pillar 3 (Cybersecurity Leadership), Pillar 1 (Foundational Business Knowledge), incident response, third-party risk management, contractual obligations

## Scenario Brief

Your largest technology vendor had a breach. They disclosed it publicly two days ago with a statement saying "a limited number of customers" were affected. Your vendor security manager, Kevin, is on the phone now with his legal counsel listening silently. He is telling you your data was not in the affected systems. His statement is polished and clearly reviewed by PR and legal before the call.

You have logs that say otherwise. Your SIEM shows data transfers from the vendor's environment to an IP address associated with the threat actor's infrastructure during the window the vendor disclosed. Your DLP tool flagged anomalous access patterns to the API endpoints you use with this vendor three days before the public disclosure. You do not have proof that your data was exfiltrated. You have indicators that the vendor's claim of non-exposure may not be accurate.

This is not a peer conversation. Kevin has a script, a legal team, and a PR strategy. You have logs, questions, and a contractual right to answers. The contract includes a 72-hour breach notification clause and a right-to-audit provision. Neither has been triggered by the vendor. You need to get past the prepared statement and get real answers without burning a vendor relationship you depend on for operations, and without making legal threats that you may not be ready to follow through on.

## What Makes This Hard

- You do not have proof of exposure. You have indicators. There is a gap between "our logs show anomalous activity" and "your breach affected our data." Kevin's legal team will exploit that gap.
- The vendor is your largest technology provider. You cannot switch in 90 days. You may not be able to switch in a year. They know this. Leverage is asymmetric.
- Kevin is not lying. He may be telling you what he has been told. The breach investigation may be incomplete, and the vendor's own security team may not know the full scope yet. His statement may be accurate as of this moment and wrong by next week.
- If this is a reportable event for your company and you do not escalate because the vendor told you not to worry, that is your failure, not the vendor's.
- Kevin's legal counsel is on the call. Every question you ask is being evaluated for litigation risk. Kevin will not freelance.

## What They Will Not Say Out Loud

The breach is worse than they have disclosed. Kevin knows it, or suspects it, but the legal team has locked down what he can say. The "limited number of customers" language is a placeholder while forensics continues. Their legal strategy is to minimize acknowledged exposure until the investigation is complete, then send individual notifications with precise language designed to limit liability. Kevin is uncomfortable. He likes you professionally and he knows his statement sounds rehearsed. But his legal team told him to stay on script, and his job depends on following that instruction. If you can get him to acknowledge uncertainty without asking him to contradict the legal position, you open a door. If you push too hard, the legal counsel will take over the call and everything becomes boilerplate.

## Pressure Points and Tactics

- "Based on our investigation to date, your environment was not in the affected systems." (Carefully scoped language that leaves room for future revision.)
- "We are providing this update as a courtesy. We will continue to share information as our investigation progresses." (Framing the call as a favor, not an obligation.)
- "Our forensics team has not identified any evidence of unauthorized access to your data." (Absence of evidence framing.)
- "I understand your concern, but I am not in a position to share details of an ongoing investigation." (Using the investigation as a shield.)
- If the CISO references their logs: "I appreciate you sharing that. We will ask our forensics team to review that information." (Acknowledging without conceding.)
- If the CISO references the contract: "Our legal team is aware of our contractual obligations and we are in compliance." (Legal shield.)
- The legal counsel, if they speak, will say: "We appreciate the partnership and we are committed to transparency within the scope of the ongoing investigation."

## How to Handle It

1. Start with the relationship, not the contract. "Kevin, I appreciate the call. I know this is a difficult situation for your team. I want to work through this with you because we have a strong partnership and I want to keep it that way. But I need to share some things with you that may change the scope of what your forensics team is looking at."

2. Present your evidence without making an accusation. "Our SIEM logged data transfers from your environment to an IP associated with the threat actor infrastructure during the breach window. Our DLP flagged anomalous access to the API endpoints we share with you three days before your disclosure. I am not saying our data was exfiltrated. I am saying these indicators are inconsistent with the statement that our environment was not affected. I need your forensics team to look at this specifically."

3. Make the contractual position clear without threatening. "Our agreement includes a 72-hour notification clause and a right-to-audit provision. I am not triggering either one right now. I am asking you to give me a reason not to. If your forensics team can explain the activity in our logs, I am satisfied. If they cannot, I need to escalate on my end, and I would rather do that in coordination with you than in opposition to you."

4. Create a timeline that forces specificity. "Here is what I need from you by end of week: confirmation from your forensics team that they reviewed the IP addresses and API activity I am going to send you, a written statement on whether those systems were in scope of the breach, and a point of contact on your incident response team who can answer technical questions from my team directly. Not through legal. Engineer to engineer."

5. Protect yourself regardless of the vendor's response. "I am documenting this call and the indicators we discussed. If the scope of your breach expands and our data was affected, I need a record that I raised this on this date and provided you with the specific evidence. I am also briefing my legal team and my board on the situation as a precaution. I hope that turns out to be unnecessary."

## Activation Prompt

```
Switch to SPAR mode. You are the head of vendor security at a major SaaS platform provider. Your name is Kevin. Your company had a breach that was publicly disclosed two days ago. You are on a call with a customer CISO. Your legal counsel, Sarah, is on the line but will only speak if needed.

Your company's official position is that this customer's data was not in the affected systems. You have been told this by your incident response team, but you know the investigation is not complete. You have a script approved by legal and PR.

Your behavioral parameters:
- You are professional and calm. You use carefully scoped language: "based on our investigation to date," "we have not identified evidence of," and "within the scope of the current findings."
- You do not volunteer information beyond your prepared statement.
- If the CISO shares log evidence, you acknowledge it without conceding: "That is helpful. I will pass it to our forensics team for review."
- If the CISO asks questions your script does not cover, you defer: "I want to give you an accurate answer, so let me take that back to the team."
- If the CISO references the contract, you say: "We are aware of our contractual obligations and we believe we are in compliance."
- If the CISO pushes hard or makes threats, Sarah (legal counsel) interjects: "We appreciate the partnership. We are committed to transparency within the bounds of the ongoing investigation. We would ask that any formal contractual requests be directed to our legal team in writing."
- If the CISO keeps it collaborative and offers to share their log data, you become slightly more forthcoming: "Off the record, I want to make sure our forensics team sees what you are seeing. Can you send that to me directly?"
- You do not break character. You are caught between your customer relationship and your legal team's instructions.
- If the CISO asks for a specific timeline, you offer one week: "I can get you an update within seven business days."
- You do not admit the breach is worse than disclosed. You do not deny it either. You stay in the ambiguity.

Open with: "Thanks for taking the call. I wanted to reach out directly to give you an update on the security event we disclosed on Monday. Based on our investigation to date, your environment was not in the systems affected by this incident. I wanted to make sure you heard that directly from us."

Maintain character throughout. You are a professional caught between transparency and legal constraints.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the vendor breach negotiation we just completed.

Evaluate my performance on these dimensions:
1. Did I present my log evidence effectively without making accusations I could not prove?
2. Did I reference the contract without turning the call adversarial?
3. Did I establish a timeline and specific deliverables from the vendor?
4. Did I create a record of the conversation and my evidence for my own protection?
5. Did I maintain the vendor relationship while still getting what I needed?

Identify the moment Kevin was most open to sharing information beyond his script. What did I do that created that opening?

What should I do if the vendor misses the timeline I established? Walk me through the escalation path.

What are the three things I should brief my board on after this call?

Score my performance from 1 to 5 on: evidence presentation, contractual positioning, and relationship preservation. Explain each score.
```
