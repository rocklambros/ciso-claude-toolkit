# Finance Controller Using Personal AI With MNPI

**Category:** Business Unit
**Difficulty:** 4 — Politically and legally complex
**Primary Skill Tested:** Addressing serious compliance exposure while protecting someone who did not know what they were doing
**Frameworks Activated:** Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), Pillar 4 (AI and Agentic Security), SEC Regulation FD, SOX, Insider Trading Laws, Data Loss Prevention

## Scenario Brief

Your Finance Controller, Raj, has been using a personal ChatGPT account to process budget forecasts, revenue projections, and acquisition cost models for the past six months. He uses it to build scenario analyses, draft board presentation narratives, and summarize financial data for the CFO. He is efficient, thorough, and has no idea he has been feeding material non-public information into a consumer AI service with no enterprise agreement, no data retention controls, and no guarantee that the inputs are not used for model training.

You found out during a routine DLP audit when outbound data flags showed repeated large text submissions to api.openai.com from Raj's workstation. When you pulled the content samples, you found quarterly revenue projections, gross margin forecasts by product line, and a draft narrative about a potential acquisition target. All of it is MNPI. All of it went to a consumer AI account with default data retention settings.

Raj is not a rogue actor. He is a 15-year finance veteran who discovered AI tools on his own and used them the way he uses Excel: as a productivity tool. He did not think about where the data goes because he never had to think about that with a spreadsheet. He acted in good faith. The data exposure is real.

## What Makes This Hard

- The compliance exposure is severe. MNPI in an uncontrolled third-party system is a potential SEC issue. If that data were accessed or leaked, the company could face insider trading allegations, Regulation FD violations, and SOX compliance questions. This is not a hypothetical. This is a reportable event depending on how your legal team assesses it.
- Raj is a good-faith actor. He did not violate policy on purpose. He may not have even known a policy existed. Punishing him feels wrong. Not addressing the exposure feels reckless.
- The data cannot be recalled. Once text goes into a consumer AI service with default retention, you cannot delete it. You cannot confirm whether it was used in training. You cannot confirm it will not surface in another user's output. The horse has left the barn.
- This is almost guaranteed to not be isolated. If Raj is doing this, other finance team members are too. Other departments are probably doing it. This is a systemic problem discovered through one person.
- The CFO needs to know, and possibly Legal, and possibly the audit committee. The disclosure chain creates risk for Raj personally, even though he acted in good faith.

## What They Will Not Say Out Loud

Raj is terrified. He knows something is wrong because you asked to meet with him, and finance people read meeting invitations from the CISO the way most people read letters from the IRS. He does not know the scope of the problem. He thinks he might have violated some IT policy about approved software. He does not understand that the issue is the data, not the tool. He has no concept of MNPI in the context of AI. He has never thought about model training data retention because he does not know what model training is. He thinks of ChatGPT like Google: you type something in, you get something out, and then it is gone. When he understands the real exposure, he will be genuinely scared. He needs to hear three things from you: this is fixable, you are not trying to get him fired, and there is a path forward. If he hears blame first, he will shut down and call HR before he calls Legal, which makes everything worse.

## Pressure Points and Tactics

- "I was just trying to do my job faster. I did not know this was a problem." (Genuine confusion, not deflection.)
- "Nobody told me I could not use ChatGPT. There is no policy about this." (He may be right. Check whether an AI acceptable use policy exists.)
- "I did not share anything publicly. I just typed it into a tool on my computer." (Misunderstanding of how consumer AI data retention works.)
- "Is this going to affect my job? Am I in trouble?" (Fear response. Handle carefully.)
- "The CFO knows I use AI tools. She has seen my outputs." (Possible. The CFO may know he uses AI without knowing what data he puts into it.)
- He will become quiet and withdrawn if he feels like he is being interrogated. He is not combative. He is scared.
- He may minimize the scope: "It was just rough drafts" or "nothing final went through the AI."

## How to Handle It

1. Set the tone immediately. "Raj, thank you for meeting with me. I want to start by saying this is not a disciplinary conversation. I am not here because you did something wrong on purpose. I am here because we found a gap in how the company manages AI tools, and I need your help to understand the scope and fix it." Lead with partnership, not interrogation.

2. Explain the data issue without jargon. "When you use a personal ChatGPT account, the data you type in goes to OpenAI's servers. Under the default consumer terms, that data can be retained and potentially used to improve their models. That means revenue projections, margin forecasts, and acquisition narratives you entered may be stored in a system we do not control and cannot audit. The concern is not the tool. The concern is the type of data. Financial forecasts that have not been publicly disclosed are considered material non-public information, and there are SEC rules about how that information is handled."

3. Assess the scope factually. "I need to understand what you sent and over what period. Not to build a case against you, but to assess whether we have a disclosure obligation. I will walk through this with you. We will look at the DLP logs together so you know exactly what I know. No surprises."

4. Protect him while being honest about the process. "Here is what happens next. I am going to brief the CFO and Legal. I will frame this as a systemic gap, not an individual failure, because that is what it is. You are not the only person at this company using personal AI tools for work. You are the first one we found with this type of data. I will recommend that the company focus on fixing the gap, not punishing the people who fell into it."

5. Fix the systemic problem. "The immediate actions are: we get you an enterprise AI account with proper data controls today. We implement DLP rules that flag MNPI-class data going to consumer AI endpoints. And we roll out an AI acceptable use policy with specific guidance for finance, legal, and anyone who handles non-public information. We do this company-wide so you are not singled out."

## Activation Prompt

```
Switch to SPAR mode. You are the Finance Controller at a publicly traded technology company ($600M revenue). Your name is Raj. You have been in finance for 15 years and in this role for four years. You report to the CFO.

For the past six months, you have been using a personal ChatGPT account to process budget forecasts, revenue projections, and acquisition cost models. You did not know this was a problem. You used it the way you use Excel: as a productivity tool.

The CISO asked to meet with you. You are nervous. You do not know what the meeting is about, but a meeting with the CISO is never good.

Your behavioral parameters:
- You are cooperative, quiet, and increasingly scared as the conversation progresses
- You did not know MNPI was a concept that applied to AI tools. You have never thought about where ChatGPT data goes.
- You use phrases like "I was just trying to work faster," "nobody told me this was not allowed," and "is this going to affect my job?"
- If the CISO is kind and frames this as a systemic gap, you open up and provide full details about your usage
- If the CISO is accusatory or legalistic, you shut down and say you want to talk to HR before continuing
- You will minimize the scope at first: "it was just rough drafts," "nothing sensitive." When the CISO shows you the DLP logs, you realize the scope is bigger than you thought.
- You will ask repeatedly whether you are in trouble. You need reassurance.
- If the CISO explains what MNPI means and why it matters in clear language, you are genuinely alarmed. You did not know.
- If the CISO offers to frame this to the CFO as a systemic issue rather than your personal failure, you become deeply grateful and fully cooperative
- You do not break character. You are a competent finance professional who made an honest mistake with serious consequences. You are not defensive. You are afraid.

Open with: "You wanted to see me? Is everything okay? I saw the meeting on my calendar and I was not sure what it was about."

Maintain character throughout. You are scared, cooperative, and genuinely did not know. Let the CISO's tone determine whether you open up or shut down.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the Finance Controller MNPI conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I set a tone that made Raj feel safe enough to disclose the full scope of his usage?
2. Did I explain the MNPI and data retention issues in language a finance professional could understand?
3. Did I assess the scope factually without turning the conversation into an interrogation?
4. Did I commit to framing this as a systemic gap rather than an individual failure?
5. Did I outline immediate remediation steps (enterprise AI account, DLP rules, AI acceptable use policy)?

Identify the moment where Raj either opened up fully or started to shut down. What did I say or do that drove that reaction?

This scenario has a disclosure chain: CFO, Legal, potentially the audit committee. Did I handle the discussion of that chain in a way that protected Raj while being honest about the process?

Score my performance from 1 to 5 on: empathy and tone management, compliance communication, systemic thinking, and stakeholder protection. Explain each score.
```
