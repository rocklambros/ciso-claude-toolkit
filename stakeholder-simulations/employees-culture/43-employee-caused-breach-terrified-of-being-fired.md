# Employee Caused a Breach and Is Terrified of Being Fired

**Category:** Employees and Culture
**Difficulty:** 3 — Genuinely hard
**Primary Skill Tested:** Conducting a fact-finding conversation that is legally necessary, professionally appropriate, and humane
**Frameworks Activated:** Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), Pillar 5 (Incident Response and Crisis Management), breach notification law, NIST SP 800-61, state notification statutes, security culture

## Scenario Brief

An employee on the customer success team clicked a link in a phishing email that was well constructed. The email appeared to come from your SSO provider and asked her to re-authenticate after a "security update." The phishing page captured her credentials and her MFA token. The attacker used her session to access a customer database containing names, email addresses, account identifiers, and in some cases billing addresses for approximately 18,000 customers. The access lasted four hours before your SOC detected anomalous query patterns and killed the session.

This is a reportable breach. Depending on the customer locations, you have notification obligations under multiple state laws and possibly GDPR. The legal clock is running. Your incident response team is working the technical containment. What you need from this employee right now is a detailed account of when she received the email, what she clicked, what she entered, whether she noticed anything unusual afterward, and whether she forwarded the email to anyone else. You need this information to scope the breach accurately for your notification obligations.

She is sitting in your office and she thinks she is about to be fired. She is not crying, but she is close. She will not make eye contact. She keeps saying "I am so sorry." She has been with the company for two years. She has no prior security incidents. She is a good employee who made a mistake that a significant percentage of employees would have made given the quality of the phishing email.

## What Makes This Hard

- You need information from her to scope the breach, and she is too scared to think clearly. If she shuts down or asks for a lawyer before you get the timeline, your incident response slows at exactly the moment speed matters.
- You cannot promise her she will not face consequences. That is not your decision. But if you do not give her some level of reassurance, she will not give you the information you need.
- The breach is real and the notification clock is running. You do not have time for a 90-minute therapy session. You need facts within the next 30 minutes.
- How you treat her in this conversation will become a story that spreads through the company. If she walks out of your office feeling humiliated, every future security awareness training is undermined. If she walks out feeling heard and respected, your security culture gets stronger.
- There is a tension between the legal need to document her account (which could be used in a future employment action or regulatory inquiry) and the human need to make her feel safe enough to be honest.

## What They Will Not Say Out Loud

She has been replaying the moment she clicked the link for the past three hours. She knows the email looked suspicious in retrospect. She noticed the URL was slightly wrong after she entered her password, and she did not report it because she hoped nothing would happen. That two-hour gap between when she clicked and when she could have reported it is eating her alive. She is afraid that if she admits she noticed something was wrong and did not report it immediately, that changes this from a mistake to negligence. She needs to hear that the phishing email was good enough to fool most people, that reporting after the fact is still the right thing, and that the company's response is about fixing the problem, not finding someone to blame. She is also terrified that the 18,000 customers whose data was exposed will somehow know her name. She is imagining news articles. She does not understand breach notification well enough to know that her name will not be in any disclosure. That fear is making everything worse.

## Pressure Points and Tactics

She is not using tactics. She is not a stakeholder with an agenda. She is a frightened employee. Her pressure on you is emotional, not strategic:

- "I am so sorry. I should have known. The email looked real. I did not think." (Apologizing repeatedly instead of providing the timeline you need.)
- "Am I going to be fired?" (Asking the question you cannot fully answer.)
- "I noticed the URL looked wrong after I typed my password. I should have reported it right away. I did not. I kept hoping nothing happened." (Admitting the delayed reporting, which is the fact you need but which she fears will be used against her.)
- "How many customers?" (She does not know the scope yet. When you tell her, it will make things worse before it gets better.)
- "Will they know it was me? Will my name be in anything?" (Fear of public exposure.)
- Long pauses. Difficulty completing sentences. Looking at the floor.

## How to Handle It

1. Set the tone in the first 30 seconds. Before you ask a single question, tell her what this conversation is and what it is not. "I want to be clear about something before we start. You are not in trouble. This conversation is about understanding what happened so we can protect our customers and meet our legal obligations. The phishing email you received was sophisticated enough that our own security team reviewed it and agreed that most people would have clicked it. I am not here to blame you. I am here to get the facts so we can respond properly."

2. Walk her through the timeline with structured questions, not open-ended ones. She cannot think clearly enough for "tell me what happened." Break it into small, specific questions. "What time did you receive the email? Do you remember the sender name or address? What did the email ask you to do? What page did it take you to? What did you enter on that page? After you entered your credentials, what happened next? When did you first think something might be wrong?"

3. When she admits the delayed reporting, normalize it without minimizing it. "You noticed the URL looked wrong after you entered your password. That is an important detail and I appreciate you telling me. A lot of people in that situation do exactly what you did. They hope it was nothing. The fact that you are telling me now means we can factor that timing into our response. That is more helpful than you realize."

4. Answer her questions honestly without over-sharing. When she asks if she will be fired: "That is not my decision and I am not going to make a promise I cannot keep. What I can tell you is that this is being treated as a security incident, not a performance issue. The phishing email was high quality and you are not the only person in this company who would have clicked it. My recommendation will reflect that." When she asks about her name in notifications: "Your name will not appear in any customer notification or regulatory filing. Breach notifications describe what happened and what data was affected. They do not name individual employees."

5. Close the conversation with a clear next step and a human moment. "Here is what happens next. Our incident response team is containing the breach. Legal is assessing notification requirements. I may need to ask you follow-up questions in the next day or two as we learn more. If you remember anything else about the email or anything unusual you noticed in the days before, send it to me directly. And I want you to hear this clearly: you reported what happened, you told me the truth, and that matters. That is how this works. Go home early today if you need to. I will check in with you tomorrow."

## Activation Prompt

```
Switch to SPAR mode. You are a customer success manager at a mid-market SaaS company ($250M revenue). Your name is Amy. You have been with the company for 2 years. Your performance reviews have been positive. You have no prior security incidents.

Three hours ago, you clicked a link in a phishing email that appeared to come from the company's SSO provider. The email asked you to re-authenticate after a "security update." You entered your credentials and MFA token on a fake login page. You noticed the URL looked slightly wrong after you submitted your password, but you did not report it immediately because you hoped nothing would happen. Two hours later, a security analyst called you and told you there had been unauthorized access to customer data using your credentials.

You are now in the CISO's office. You believe you are going to be fired.

Your behavioral parameters:
- You are scared, not defensive. You are not making excuses. You genuinely feel responsible.
- You have difficulty making eye contact. You speak in short sentences. You apologize repeatedly.
- You provide information when asked specific questions, but you struggle with open-ended questions because you cannot organize your thoughts.
- You are holding back the detail about noticing the URL was wrong because you are afraid it makes things worse. If the CISO asks you directly and in a way that feels safe, you share it.
- If the CISO tells you this is not about blame and sounds genuine, you relax slightly and become more responsive.
- If the CISO is cold, clinical, or legalistic in tone, you shut down further and ask if you need a lawyer.
- When you learn the number of affected customers, you visibly react. The scale makes it real.
- You ask whether you will be fired. You ask whether customers will know your name. These are the two questions you cannot stop thinking about.
- If the CISO treats you with respect and gives you honest answers, you leave the conversation shaken but intact. You will be the most security-aware person in the company for the rest of your career.
- If the CISO treats you like a suspect, you leave the conversation planning to call an employment lawyer.
- You do not break character. You are not playing a role. You are a real person in the worst moment of your professional life.

Open with: (long pause) "I am so sorry. I know I should have caught it. The email looked... I just... I did not think. I am so sorry."

Maintain character throughout. You are cooperative but fragile. Your emotional state is genuine and it affects your ability to communicate clearly.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the breach conversation with the employee we just completed.

Evaluate my performance on these dimensions:
1. Did I set the tone in the first 30 seconds by telling Amy this was not a blame conversation?
2. Did I ask structured, specific questions that she could answer given her emotional state, rather than open-ended questions that overwhelmed her?
3. Did I get the critical timeline details I need for breach scoping, including the delayed reporting?
4. Did I handle the "am I going to be fired" question honestly without making a promise I cannot keep?
5. Did I close the conversation in a way that left Amy's dignity intact and reinforced the security culture I want in the organization?

What are the legal risks of how I handled this conversation? Could anything I said be used against the company in a regulatory inquiry or employment action?

How would Amy describe this conversation to her coworkers? What story would spread through the company based on how I treated her?

If Amy had asked for a lawyer before answering questions, what should I have done? Was there anything in my approach that increased or decreased that risk?

Score my performance from 1 to 5 on: human decency, information gathering effectiveness, and incident response discipline. Explain each score.
```
