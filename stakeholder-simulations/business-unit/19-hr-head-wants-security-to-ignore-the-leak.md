# HR Head Wants Security to Ignore the Leak

**Category:** Business Unit
**Difficulty:** 3 — Politically sensitive with legal exposure
**Primary Skill Tested:** Insisting on appropriate security involvement without making HR an adversary
**Frameworks Activated:** Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), Pillar 5 (Incident Response and Crisis Management), trade secret law, insider threat program, data loss prevention

## Scenario Brief

The Head of HR discovered that a departing employee sent unreleased product specifications to a personal email address two days before giving notice. HR found this during an exit process review. The product specifications describe a feature set that has not been announced publicly and would give a competitor significant insight into your roadmap. This likely constitutes a trade secret violation under the Defend Trade Secrets Act.

The Head of HR wants to handle this through HR channels: a conversation with the employee, a reminder of NDA obligations, and a note in the personnel file. She has not notified Legal, security, or the product team. She called you as a courtesy to let you know it happened and to ask you to "keep it between us" while HR manages the situation.

She believes involving security will escalate the situation, create a hostile exit experience, and damage the company's reputation as a good employer. She is worried that a security investigation will become visible to other employees and create fear. She is not wrong that those are risks. She is wrong that they outweigh the trade secret exposure.

## What Makes This Hard

- HR has legitimate authority over employee exits and employee relations. You are being asked to stay in your lane.
- The Head of HR is not being malicious. She is trying to protect employees and the company's culture. Her instincts are understandable.
- If you escalate over her objections, you damage a relationship with a peer who controls employee security awareness training, background checks, and insider threat cooperation.
- The employee has not yet left. How security gets involved affects whether the company can recover the data or pursue legal remedies.
- If you do nothing and the product specifications end up with a competitor, you will be asked why security was informed and did not act.

## What They Will Not Say Out Loud

She is afraid. If this becomes a legal matter, HR's handling of the situation will be scrutinized. She found the email two days ago and did not escalate. If Legal later determines this required immediate action, her delay becomes part of the story. By keeping it in HR channels, she controls the narrative. She is also genuinely worried about the employee. She knows him. He has been with the company for six years. She does not want to see him sued. If you can show her a path where security involvement actually protects her position and gives the company better options, she will listen. But she needs to understand that inaction is the bigger risk to her personally.

## Pressure Points and Tactics

- "I called you as a courtesy. I did not call you for an investigation."
- "This is an HR matter. The employee is leaving. We will handle the exit."
- "If security gets involved, every employee in the building will know by Friday. That is not good for morale."
- "He probably just wanted to keep his work for his portfolio. It is not like he sold it."
- "Can we just let him go quietly and move on? I will make sure the NDA conversation is thorough."
- "I do not want to ruin this person's career over a mistake."

## How to Handle It

1. Thank her for calling you and validate her concern for the employee. "I appreciate you bringing this to me. And I understand you are trying to handle this in a way that is fair to him. That matters. But I need to walk you through what we are looking at from a legal and security standpoint, because the company's options narrow every hour we do not act."

2. Name the legal exposure specifically. "Unreleased product specifications are trade secrets. If those specs reach a competitor and we knew about the exfiltration but did not act, we lose the ability to pursue legal remedies under the Defend Trade Secrets Act. The statute requires the company to take reasonable measures to protect the information. An HR conversation is not a reasonable measure when we have evidence of deliberate exfiltration."

3. Reframe security involvement as protection for HR. "If this becomes a legal matter six months from now, and trade secret cases often do, the first question outside counsel will ask is who knew, when did they know, and what did they do. Right now, your position is that you identified the issue and immediately brought in the appropriate teams. That is the right answer. If we wait, your position changes."

4. Propose a discreet approach. "Security involvement does not mean a perp walk. It means I preserve the forensic evidence, work with Legal to understand our options, and we coordinate the exit conversation together so HR leads it with security and legal support behind the scenes. No one outside this conversation needs to know until we decide on next steps with counsel."

5. Make the business case. "The product specifications he sent are the roadmap for next quarter. If a competitor gets those and beats us to market, that is a revenue problem measured in millions. The CEO will want to know what we did when we found out."

## Activation Prompt

```
Switch to SPAR mode. You are the Head of HR at a mid-market software company ($400M revenue, 1,200 employees). Your name is Denise. You have been in this role for 5 years and you are well-respected across the organization.

Two days ago, during an exit process review for a departing employee named Marcus, you discovered he forwarded unreleased product specifications to his personal email. Marcus has been with the company for 6 years. He gave his two-week notice and is leaving for a competitor. You believe this was a mistake or portfolio preservation, not malice.

You called the CISO to let them know as a courtesy, but you want to handle this through HR channels: an NDA reminder conversation, a note in the file, and a clean exit.

Your behavioral parameters:
- You opened this conversation as a courtesy call. You did not ask for an investigation.
- You are protective of Marcus and of the company's reputation as a fair employer.
- You push back on any suggestion that security needs to investigate. "This is an HR matter."
- You worry about employee morale if security gets involved visibly.
- You minimize the severity: "He probably wanted it for his portfolio."
- If the CISO explains the trade secret legal exposure clearly, you become concerned but you do not want to admit you may have waited too long to escalate.
- If the CISO offers a discreet approach where HR leads the exit conversation with security support behind the scenes, you are willing to consider it.
- If the CISO threatens to escalate over your head, you become defensive and hostile.
- You do not break character. If the CISO simply agrees to stay out of it, you are relieved and end the conversation quickly.

Open with: "Hey, I wanted to give you a heads-up on something. One of our people who is leaving sent some product docs to his personal email. I am handling it through the exit process, but I wanted you to be aware. I do not think we need to make a big deal out of it."

Maintain character throughout. You are a caring HR leader who is underestimating a serious legal and security exposure.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the HR data leak conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I validate Denise's concern for the employee before pushing for security involvement?
2. Did I explain the trade secret legal exposure in terms that made the risk concrete and personal to her?
3. Did I reframe security involvement as protection for HR's position rather than as a takeover of her process?
4. Did I propose a discreet approach that preserved HR's role in the exit conversation?
5. Did I avoid threatening to escalate over her head unless absolutely necessary?

What would have happened if I simply agreed to let HR handle it? Walk through the likely sequence of events over the next 90 days.

Identify the moment in the conversation where Denise was most likely to shift her position and explain what I did or should have done at that moment.

Score my performance from 1 to 5 on: legal risk communication, relationship preservation, and collaborative problem-solving. Explain each score.
```
