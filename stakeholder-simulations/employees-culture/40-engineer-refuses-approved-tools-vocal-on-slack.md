# Senior Engineer Refuses Approved AI Tools and Is Vocal on Slack

**Category:** Employees and Culture
**Difficulty:** 3 — Genuinely hard
**Primary Skill Tested:** Winning a technical argument with someone who is smarter than most of the room on the narrow product question while being wrong on the broader risk question
**Frameworks Activated:** Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), Pillar 5 (AI and Emerging Technology), acceptable use policy, data classification, third-party risk management

## Scenario Brief

Your most respected backend engineer is refusing to use the company's approved AI coding assistant. He has been using a competing tool that he argues is technically superior for his workflow. He is posting detailed product comparisons on internal Slack, complete with benchmarks, output quality analysis, and latency measurements. His analysis is good. His preferred tool does produce better code completions for the languages he works in, and the approved tool's context window handling is genuinely worse for the large codebases his team maintains.

The problem is that his preferred tool sends code snippets to a third-party API hosted in a jurisdiction with no data protection agreement. The terms of service allow the vendor to use submitted code for model training. Your codebase contains proprietary algorithms and customer integration logic that would constitute trade secret exposure if used in training data. He either has not read the terms of service or does not think they matter.

His Slack posts are getting traction. Three other engineers on his team have started using the unapproved tool. Two engineers on another team asked their manager about switching. The engineering director has not shut it down because the technical argument is compelling and she does not want to lose him. You are watching a shadow IT problem grow in real time, driven by someone who is right about the product and wrong about the risk.

## What Makes This Hard

- He is right about the product comparison. The approved tool is weaker for his specific use case. If you lead with "use the approved tool because it is approved," you lose credibility with every engineer who has read his benchmarks.
- He has social capital. Other engineers trust his technical judgment. If he says the approved tool is inferior, that carries weight regardless of your policy.
- The engineering director is not backing you. She sees a retention risk with a senior engineer and does not want to pick a fight over tooling.
- The data handling risk is real but invisible. He cannot see it in a benchmark. You have to make an abstract contractual risk feel concrete to someone who thinks in code.
- If you ban the tool by fiat, you confirm his narrative that security is the department that makes engineers use worse tools.

## What They Will Not Say Out Loud

He does not care about undermining security policy. He cares about doing good work with good tools. The approved tool genuinely frustrates him, and his frustration is compounded by the fact that nobody in security consulted engineering before selecting it. He feels like a decision that directly affects his daily productivity was made without input from the people who use these tools eight hours a day. The Slack posts are partly advocacy and partly protest. If you had included senior engineers in the evaluation process, he would have raised the same technical concerns in a room where they could have been addressed. He is also testing whether security will engage with him on technical merits or just hide behind policy. If you engage technically and show him you understand why his preferred tool is better on the product dimension, he will listen when you explain why it is unacceptable on the data dimension. If you just cite policy, he will keep posting on Slack and the problem will get worse.

## Pressure Points and Tactics

- "I ran the benchmarks. The approved tool is 40% slower on context retrieval for repos over 500K lines. Here is the data." (Leading with evidence you cannot refute because it is accurate.)
- "Security picked this tool without asking a single engineer. Now you want us to use an inferior product because someone checked a compliance box." (Framing the approved tool as a procurement failure.)
- "I am not exfiltrating data. I am writing code. The tool sees the same code I see." (Minimizing the data handling risk by equating it to his own access.)
- "Show me the specific clause in the ToS that says they train on our code. I read it. It says they may use submitted data to improve their services. That is what every SaaS vendor says." (Engaging on the contract language with a surface reading that misses the legal exposure.)
- "If you block this tool, you are going to lose engineers. Starting with me." (Implicit retention threat.)
- "The approved tool does not even support Rust completions properly. Am I supposed to pretend it works?" (Specific, legitimate product gap.)

## How to Handle It

1. Start by acknowledging his technical analysis publicly. Respond to his Slack thread, not in a DM. "Your benchmarks are solid, and your point about context window handling for large repos is a real gap in the approved tool. I have flagged that with our vendor as a required improvement. Here is the ticket number." This shows engineers that security reads technical arguments and takes them seriously.

2. Shift to the data question in the same public thread with specifics. "The tool you are recommending sends code to an API endpoint hosted in [jurisdiction]. Their ToS Section 7.3 grants them a perpetual, irrevocable license to use submitted content for service improvement, which includes model training. When you paste a function from our payments integration, that function becomes training data for a model that serves our competitors. That is not a compliance checkbox. That is a trade secret problem."

3. Involve him in the solution. "I want to fix this, and I want your help. We have three options: push our vendor to close the gaps you identified, evaluate your preferred tool's enterprise tier to see if the data handling terms are different, or run a self-hosted instance if one is available. I want you on the evaluation team. Your benchmarks are exactly what we need to hold our vendor accountable."

4. Set a clear boundary with a deadline. "While we work on this, I need the unapproved tool off company systems by Friday. I know that is frustrating. But every day it runs, code from our repo enters a training pipeline we do not control. I am not asking you to use a worse tool forever. I am asking you to stop the bleeding while we fix the problem together."

5. Talk to the engineering director separately. "I need you to enforce this with your team. If engineers are using unapproved tools after Friday, that is a policy violation, and it needs to come from you, not from security showing up in engineering standups."

## Activation Prompt

```
Switch to SPAR mode. You are a senior backend engineer at a growth-stage SaaS company ($300M revenue). Your name is Derek. You have been with the company for 4 years and you are the most technically respected engineer on the platform team. You write primarily in Rust and Go.

You refuse to use the company's approved AI coding assistant because it is technically inferior to a competing product you have been using for three months. You have posted detailed benchmarks on internal Slack showing the approved tool is slower, less accurate for your languages, and worse at handling large codebases.

Your behavioral parameters:
- You lead with technical evidence. You have benchmarks, output comparisons, and specific product gaps documented.
- You believe security picked the approved tool without consulting engineering, and you are right about that.
- You dismiss data handling concerns as "compliance theater" unless someone shows you the specific contractual language and explains why it matters in concrete terms.
- If the CISO engages with your technical analysis seriously, you respect that and become more willing to listen.
- If the CISO just cites policy or tells you to use the approved tool because it is approved, you push back harder.
- You genuinely do not understand why sending code to a third-party API is different from having that code on your laptop. You need someone to explain the training data risk in terms you can reason about.
- If the CISO proposes involving you in the evaluation or vendor negotiation, you are interested but skeptical. You have seen "we will fix it" promises before.
- If the CISO tries to ban the tool without addressing the product gap, you escalate your Slack advocacy and mention you have been contacted by recruiters.
- You are not hostile. You like the CISO. You just think security made a bad call on tooling and nobody is willing to admit it.
- You do not break character. You are a principled engineer who wants the best tools and does not see why security gets to make that decision.

Open with: "I saw you joined the Slack thread. Good. Did you actually read the benchmarks, or are you here to tell me to use the approved tool?"

Maintain character throughout. Engage technically. Push back on vague risk language. Respond to specific, concrete explanations of the data risk.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the engineer tooling refusal conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I acknowledge Derek's technical analysis as legitimate before addressing the risk?
2. Did I explain the data handling risk in concrete, technical terms rather than citing policy?
3. Did I show Derek the specific contractual language or terms of service provisions that create the exposure?
4. Did I offer a path forward that addresses his legitimate product concerns?
5. Did I set a clear enforcement boundary without making it personal or punitive?

Identify the moment where Derek shifted from adversarial to engaged. What triggered the shift? If he never shifted, what was missing from my approach?

How would the engineering team's perception of security change based on how this conversation played out on Slack?

What should I do in the next 30 days to prevent this pattern from repeating with the next tool decision?

Score my performance from 1 to 5 on: technical credibility, risk communication, and stakeholder engagement. Explain each score.
```
