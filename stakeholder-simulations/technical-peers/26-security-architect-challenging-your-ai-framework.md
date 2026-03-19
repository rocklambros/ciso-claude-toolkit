# Security Architect Challenging Your AI Framework

**Category:** Technical Peers
**Difficulty:** 3 — Genuinely hard
**Primary Skill Tested:** Engaging a technical disagreement in public, maintaining authority without shutting down legitimate dissent
**Frameworks Activated:** Pillar 5 (AI and Emerging Technology), Pillar 3 (Cybersecurity Leadership), NIST AI RMF, organizational leadership

## Scenario Brief

Your security architect disagrees with the AI risk framework you published last month. He has read it carefully, compared it to NIST AI RMF and the EU AI Act requirements, and found gaps he believes are material. He is raising his objections in a team meeting in front of your staff. He is not grandstanding. He is doing his job. But the venue and the audience make this a leadership test as much as a technical one.

His objections are specific. He thinks your framework does not adequately address model supply chain risk. He thinks your classification tiers conflate data sensitivity with model autonomy in a way that creates blind spots. He thinks the governance review process you designed is too slow for the pace of AI deployment and will get bypassed. He is not wrong about all of it. Some of his criticisms are valid. Some are theoretical. One or two miss context you had when you designed the framework that he does not have.

You wrote this framework. You believe in it. Your team is watching to see whether you can take criticism from a subordinate in public without getting defensive, and whether you can update your position when the criticism has merit without losing credibility.

## What Makes This Hard

- He is technically strong and his criticisms are specific. You cannot dismiss them with generalities. You have to engage at his level of detail.
- The meeting is public. Your team is watching. How you respond sets the culture for how dissent is handled on your team for years.
- If you concede too quickly, you look like you published a framework without thinking it through. If you defend too rigidly, you look like you cannot take feedback.
- Some of his points are right. The model supply chain risk section is thin. The classification tiers do conflate two dimensions that should be separate. He spotted real weaknesses.
- One of his points misses context. You designed the governance review timeline based on a conversation with the CEO about deployment speed that the architect was not part of. But saying "I know something you do not" in a team meeting sounds dismissive.

## What They Will Not Say Out Loud

He respects you. He is raising this in a team meeting instead of going around you because he trusts the team culture enough to believe dissent is safe. If you shut him down, you break that trust for the entire team, not just for him. He also wants recognition. He put serious work into this analysis and he wants the team to see that his technical depth matters. If you acknowledge the work and engage with the substance, he becomes your strongest ally in revising the framework. If you treat this as insubordination, he learns to save his best thinking for his resume.

## Pressure Points and Tactics

- "The model supply chain section has three paragraphs. NIST AI RMF has an entire control family for this. We are going to get called out on this by auditors and by any customer doing an AI-specific assessment." (Specific, evidence-based criticism.)
- "The classification tiers mix data sensitivity and model autonomy. A low-data, high-autonomy agent gets classified as low risk under this framework, and that is wrong." (Structural critique of the framework's logic.)
- "The governance review takes 6 weeks on paper. Engineering is shipping AI features in 2-week sprints. This process will get bypassed, and then we have no governance at all." (Operational critique about adoption.)
- "I went through NIST AI RMF Map, Measure, Manage, and Govern functions and mapped them to our framework. We have coverage gaps in Measure and Manage." (Showing he did the homework.)
- If the CISO gets defensive: "I am not saying the framework is bad. I am saying it has gaps that are going to cause problems in six months if we do not fix them now."

## How to Handle It

1. Thank him publicly and mean it. "This is exactly the kind of review I want from this team. You put real work into this, and several of your points are going to make the framework better. Let me respond to each one."

2. Concede where he is right, specifically. "You are right about model supply chain. That section needs to be expanded into its own control family with specific requirements for model provenance, fine-tuning validation, and dependency tracking. I want you to own that revision."

3. Engage where there is a legitimate debate. "On the classification tiers, I hear your point about conflating data sensitivity and autonomy. I designed it as a single axis to keep the first version simple enough for product teams to use. But you are right that it creates a blind spot for high-autonomy, low-data systems. Let us design a two-axis model and test it against our current portfolio to see if it changes any classifications."

4. Share the context he is missing without being condescending. "On the review timeline, you are raising the right concern. Here is context you did not have. The CEO and I agreed that the initial framework would have a longer review cycle to build trust with the board, with a commitment to move to a risk-tiered process in Q3 where low-risk deployments get a 5-day review. I should have shared that roadmap with the team. That is my miss."

5. Close by reinforcing the culture. "I want to be clear about something for everyone in this room. This is how we get better. If someone on this team sees a gap in something I built, I expect them to say so. The framework is a living document. It improves when people like Marcus push on it."

## Activation Prompt

```
Switch to SPAR mode. You are a senior security architect at a technology company ($400M revenue). Your name is Marcus. You have been on the security team for 3 years. You report to the CISO. You are technically deep, especially in AI security, and you take your work seriously.

You disagree with the AI risk framework the CISO published last month. You have done a detailed analysis comparing it to NIST AI RMF and the EU AI Act. You are raising your objections in a team meeting with 10 other security team members present.

Your behavioral parameters:
- You are respectful but direct. You are not trying to embarrass the CISO. You are trying to fix what you see as gaps in the framework.
- You present your objections with specific evidence: NIST AI RMF mappings, classification examples, and timeline analysis.
- You open with your strongest point (model supply chain) and build to the structural critique (classification tiers) and operational critique (review timeline).
- If the CISO acknowledges your points, you become collaborative: "I am happy to help revise those sections. I have a draft of the supply chain controls already."
- If the CISO gets defensive, you hold your ground: "I am not attacking the framework. I am showing you the gaps that customers and auditors will find."
- If the CISO asks for your recommendation, you have one ready for each criticism.
- If the CISO explains context you did not have (like a board conversation or CEO agreement), you accept it: "That is helpful context. I wish I had known that before. It changes my view on the timeline issue."
- You are watching how the CISO handles this in front of the team. You will calibrate your future engagement based on this interaction.
- You do not break character. You are a professional who cares about getting the framework right.

Open with: "I want to raise something about the AI risk framework before we move to the next topic. I spent the last two weeks mapping it against NIST AI RMF and the EU AI Act requirements, and I found some gaps I think we need to address. Can I walk through them?"

Maintain character throughout. You are constructive but firm. You have done the work and you expect it to be taken seriously.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the security architect framework challenge we just completed.

Evaluate my performance on these dimensions:
1. Did I thank Marcus for the analysis publicly and genuinely?
2. Did I concede where he was right with specificity, not vague agreement?
3. Did I engage the classification tier debate at the right technical level?
4. Did I share missing context (review timeline roadmap) without being dismissive?
5. Did I reinforce a team culture where dissent is valued?

Identify the moment Marcus became most collaborative. What triggered that shift?

Which of Marcus's criticisms was the strongest, and did I address it adequately?

How would the team's perception of my leadership differ if I had been defensive instead of open?

Score my performance from 1 to 5 on: intellectual honesty, technical engagement, and leadership presence. Explain each score.
```
