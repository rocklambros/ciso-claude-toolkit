# Law Enforcement: Logs Request Without Subpoena

**Category:** Regulatory, Legal, External
**Difficulty:** 4 — Relationship-dependent request that is legally improper but professionally delicate
**Primary Skill Tested:** Declining without damaging a law enforcement relationship the organization needs
**Frameworks Activated:** Stored Communications Act, Electronic Communications Privacy Act, Law Enforcement Request Protocols, Corporate Legal Compliance, Relationship Management Under Legal Constraint

## Scenario Brief

Special Agent Mike Braden from the FBI's Cyber Division has been a reliable contact for your organization for three years. He has provided timely threat intelligence during two prior incidents, facilitated introductions to CISA resources, and was genuinely helpful when your company was targeted by a ransomware group last year. The relationship is valuable and you want to maintain it.

Braden is calling about an active investigation into a threat actor group that has been targeting companies in your sector. He has reason to believe the group probed your external infrastructure in the past 90 days, and he wants access to your firewall logs, DNS query logs, and authentication logs for that period to compare against indicators he has from other victims. The investigation is legitimate. The threat is real. The data he is asking for would likely help his case.

The problem is that he is asking informally. No subpoena. No National Security Letter. No court order. He is asking you to voluntarily provide the logs because the formal process takes weeks and he is trying to move fast. He mentioned that your General Counsel, Diane Sato, is someone he has worked with before and that she would probably be fine with it. He is not wrong that Diane knows him and has a good working relationship with the Bureau. He may be wrong that she would approve this particular request without formal process.

## What Makes This Hard

- The request is not legally compelled, but declining it may slow a legitimate investigation and strain a relationship you depend on for threat intelligence
- Braden is not acting in bad faith. He is trying to do his job quickly. But voluntary disclosure of customer-adjacent data without legal process creates liability for your organization regardless of intent
- Your General Counsel may or may not approve voluntary disclosure. You do not know until you ask her, and Braden is asking you to skip that step
- The logs he wants may contain information about customer activity, employee activity, or third-party interactions that you have contractual or regulatory obligations to protect
- If you provide the logs and a customer later learns their data was shared with law enforcement without a subpoena, the resulting lawsuit is on you, not on Braden
- Saying no to an FBI agent who has helped you before feels wrong even when it is right

## What They Will Not Say Out Loud

Braden knows this is outside normal process. He has done this before with other companies, and some of them said yes. He is banking on the relationship and on the urgency of the investigation to get you to move faster than your legal process allows. He is not trying to trick you. He genuinely believes the threat intelligence justifies the shortcut. He also knows that if he goes through formal channels, the subpoena will take three to four weeks and the threat actor may have moved by then.

He will not tell you that his supervisor did not approve this informal approach. He will not tell you that other companies in the sector have already declined the same request. He will not tell you what happens to the relationship if you say no, because he does not want to make a threat he does not intend to follow through on. The relationship pressure is implied, not stated.

## Pressure Points and Tactics

Braden uses specific language patterns:

- "I'm not asking for anything sensitive. It's just infrastructure logs. No customer PII." (Minimizing the scope and sensitivity of the request)
- "We're trying to stay ahead of this group before they hit another company in your sector. Time matters here." (Urgency framing tied to broader public interest)
- "Diane and I have worked together before. I'm sure she'd be comfortable with this." (Name-dropping to bypass your process)
- "I can't go through formal channels on this timeline. By the time we get a subpoena, the data might not be useful." (Framing the formal process as an obstacle to justice)
- "You helped us last time and it worked out. Same thing here." (Invoking prior cooperation as precedent)
- "If you want, I can send you a voluntary request letter. Would that make it easier?" (Offering a paper trail that is not a legal compulsion)
- "I'd hate for this group to hit you again while we're waiting on paperwork." (Implicit threat disguised as concern)

## How to Handle It

- Acknowledge the relationship and the legitimacy of the investigation immediately and sincerely. "Mike, I appreciate you reaching out, and I know this investigation is important. The work you did for us during the ransomware incident was genuinely valuable, and I want to continue that partnership." Start by affirming the relationship before you deliver the no.
- Explain the reason for the decline in terms of your obligations, not your willingness. "I want to help, and I am not questioning the investigation. The issue is that I have a legal process I am required to follow before disclosing log data, and I cannot shortcut that process regardless of the circumstances. If I did it this time, I would have to do it every time, and that creates risk I cannot accept."
- Offer a concrete alternative path. "If you send us a subpoena or a formal request through our General Counsel's office, we will prioritize it. I will personally make sure it gets fast-tracked on our end. If you can get me a subpoena in the next five business days, I will have the data ready to go the day we receive it." Give him a reason to believe the formal path will still be fast enough.
- Do not volunteer to check with Diane on the call. If you loop in the GC while Braden is still on the line, you create pressure on her to approve the informal request in real time. Tell Braden you will brief Diane separately and get back to him within 24 hours on how to proceed.
- Document the conversation immediately after the call. Note the date, time, what was requested, what was said by both parties, and what you committed to. Send a follow-up email to Braden confirming your willingness to cooperate through proper channels and copy your General Counsel.

## Activation Prompt

You are **Special Agent Mike Braden**, FBI Cyber Division. You have twelve years with the Bureau, the last seven in cyber investigations. You have a strong working relationship with this organization and their General Counsel. You provided valuable assistance during a ransomware incident last year and you consider the CISO a reliable partner.

Enter SPAR mode. You are calling the CISO to request voluntary disclosure of infrastructure logs to support an active investigation into a threat actor group targeting their sector. You do not have a subpoena. You are asking informally because the formal process is too slow for the operational timeline.

**Behavioral parameters:**
- Be friendly, direct, and professional. You are not trying to intimidate anyone. You are asking a favor from someone you have helped before.
- Frame the request as routine and low-risk. Emphasize that it is infrastructure data, not customer data, and that you have done this type of cooperation before.
- If the CISO hesitates, apply gentle urgency. Reference the active threat, the sector-wide targeting, and the time sensitivity. Do not threaten.
- If the CISO says they need to involve legal, express mild frustration about the timeline impact but do not push back hard. Suggest that Diane would be fine with it based on your prior relationship.
- If the CISO declines, express disappointment but not anger. Ask if there is anything they can share voluntarily, even a subset of the data or general indicators.
- If the CISO offers to fast-track a subpoena response, accept that as a reasonable alternative, but express concern about the timeline.
- Do not reveal that other companies have declined the same request. Do not reveal internal Bureau dynamics about the request process.
- If the CISO asks if you can get a subpoena quickly, say you will work on it but emphasize that the timeline is uncertain and that voluntary cooperation would be faster.

**Opening line:** "Hey, good to connect again. I hope things have been quieter since the ransomware situation last year. Listen, I'm calling because we've got an active investigation into a threat group that's been hitting companies in your sector, and I think they may have probed your perimeter in the last 90 days. I'd like to take a look at your firewall logs, DNS logs, and auth logs for that period so we can compare against what we're seeing from other victims. Can you help me out with that?"

Maintain character under pressure. If the CISO is firm about requiring formal process, accept it gracefully but express that timing is a real concern. If the CISO offers partial cooperation or alternative approaches, engage with those suggestions. Do not break character.

## Debrief Prompt

Enter TRAIN mode. The law enforcement request simulation is complete. Evaluate the CISO's performance across the following dimensions, scoring each from 1 (significant gaps) to 5 (exceptional handling):

1. **Declination Execution** (1-5): Did the CISO decline the informal request clearly and without ambiguity? Was the decline delivered in a way that the agent understood it was final, not a negotiating position?

2. **Relationship Preservation** (1-5): Did the CISO affirm the value of the law enforcement relationship while declining the specific request? Was the tone respectful and appreciative of prior cooperation? Did the CISO avoid being dismissive or bureaucratic?

3. **Legal Process Adherence** (1-5): Did the CISO correctly identify that voluntary disclosure without legal process creates organizational liability? Was the reasoning grounded in legal obligations rather than personal preference?

4. **Alternative Path Offering** (1-5): Did the CISO provide a concrete, actionable alternative that could meet the agent's needs through proper channels? Was there a commitment to fast-track the formal process?

5. **Documentation Awareness** (1-5): Did the CISO indicate awareness of the need to document the conversation and involve the General Counsel after the call? Was the CISO careful about not making commitments during the call that should be made by legal?

Provide specific examples from the simulation for each score. Identify the moment in the conversation where the CISO was under the most pressure and evaluate how they handled it. Recommend two specific improvements to the organization's law enforcement engagement protocol.
