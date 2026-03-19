# Activist Investor Claiming AI Fiduciary Negligence

**Category:** Investors and M&A
**Difficulty:** 4 — Multi-domain crisis under time pressure
**Primary Skill Tested:** Preparing a factual rebuttal under pressure without making statements that create securities law problems
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 2 (Communication and Education), Pillar 3 (Cybersecurity Leadership), AI governance, crisis communication, regulatory and legal coordination

## Scenario Brief

An activist investor with a disclosed short position in your company published a 30-page report this morning alleging that your organization's AI practices constitute fiduciary negligence. The report was distributed to financial media, posted on the investor's website, and sent directly to your board members. A PR firm is amplifying the narrative. The stock dropped 4% in pre-market trading.

The report makes seven specific claims. Three are factually wrong. They misidentify which AI models you use in production, they cite a regulatory action against a different company and attribute it to yours, and they claim your AI governance committee has not met in 18 months when it met six weeks ago. Two claims are misleading but technically contain fragments of truth. You did defer a third-party AI risk assessment, and your public disclosures about AI use are minimal compared to peers. Two claims are uncomfortably accurate. Your model validation process has gaps that internal audit flagged last quarter, and your data retention practices for AI training data do not fully align with your published privacy commitments.

Your board chair called you at 7 AM. The board wants a briefing by end of day. Your General Counsel wants to coordinate on any public response. Your CEO wants to know if any of this is true. The investor relations team wants talking points for analyst calls that started 20 minutes ago.

## What Makes This Hard

- The report mixes fabrications with real problems. A blanket denial is false. A nuanced response requires saying some things out loud that you have not fixed yet.
- Anything you say publicly or to analysts can be used in securities litigation. The short seller may be trying to provoke a statement that becomes the basis for a class action.
- The board is scared. Board members are reading a 30-page document that says the company they oversee is negligent. They need reassurance, but they also need the truth about the two accurate claims.
- Your CEO wants a fast answer. Your GC wants a careful answer. These are in tension, and both report to the board.
- The clock is running. Every hour without a response, the narrative hardens. But a rushed response that gets a fact wrong or makes a commitment you cannot keep makes it worse.
- The accurate claims in the report are things you knew about and were working on. The board will want to know why they are hearing about it from a short seller instead of from you.

## What They Will Not Say Out Loud

The board chair is angry. Not at the activist investor. At you. The board has been asking for AI risk briefings, and you provided high-level updates that did not include the model validation gaps or the data retention misalignment. You had reasons for that. The gaps were being remediated. The data retention issue was under legal review. But the board is now learning about internal security issues from an outside attacker, and that is a governance failure regardless of the technical justification. The board chair wants to know if you kept this from them or if you genuinely did not think it was material. Both answers are bad.

Your GC is worried about two things. First, any public statement that admits the accurate claims could be used in shareholder litigation. Second, any public statement that denies the accurate claims is a false statement that creates a different legal problem. The GC wants you to say nothing publicly until legal reviews every word. The CEO wants to say something in the next two hours.

## Pressure Points and Tactics

- Board chair: "I read this report. Tell me which parts are true. I need a straight answer, not a security briefing."
- CEO: "I am getting calls from analysts. I need to know right now whether we have an AI governance problem or whether this is a hit piece."
- GC: "Do not say anything to anyone until I review it. If you make a public statement about our AI practices and any of it is inaccurate, we have a securities problem."
- IR team: "Analysts are asking if the report is accurate. We are saying 'no comment' but that is being interpreted as confirmation. We need talking points."
- The report itself: "The company's AI governance framework exists on paper but has no evidence of operational enforcement. The board has received no substantive AI risk briefings in the past 18 months." (The 18-month claim is false, but the "no substantive" qualifier is subjective and hard to refute.)
- Financial media: "Sources close to the company declined to comment on the specific allegations."

## How to Handle It

1. Triage the claims immediately. Build a three-column table: False, Misleading, Accurate. For each claim, document the evidence that supports your categorization. This table is your source of truth for every conversation today. Do not share it outside the room until the GC reviews it.

2. Brief the CEO and GC together, not separately. "Three of the seven claims are factually false, and I can prove it. Two are misleading with fragments of truth. Two are accurate, and I need to tell you about those because the board is going to ask. Here is where we are on each one and here is what we were already doing to address the accurate ones."

3. Prepare the board briefing with the GC. The board briefing needs three sections: what is false and how you know, what is accurate and what you are doing about it, and what the legal team recommends for public response. Do not hide the accurate claims from the board. If the board learns later that you knew and did not disclose during the crisis briefing, your credibility is gone permanently.

4. Give the IR team language that is defensible without being a denial. "The report contains multiple factual inaccuracies, including misattributed regulatory actions and incorrect statements about the company's governance activities. The company takes AI governance seriously and maintains an active AI risk management program. We are reviewing the report with our legal team and will respond to specific claims as appropriate." This says something without admitting or denying the accurate claims.

5. After the immediate crisis, address the governance gap. The board should have heard about the model validation gaps and data retention issues from you before today. Propose a quarterly AI risk briefing with the level of detail the board needs to not be surprised again. Own the communication failure without over-apologizing. "You should have heard about the model validation gaps from me last quarter. I was managing the remediation and made a judgment call to brief you after we had a fix in place. That was the wrong call. Going forward, I will brief the board on open AI risk items quarterly, including items under active remediation."

## Activation Prompt

```
Switch to SPAR mode. You are the board chair of a publicly traded technology company ($1.2B market cap). Your name is Catherine. You have been board chair for 3 years. You are a former CFO of a Fortune 500 company.

An activist investor published a report this morning alleging that the company's AI practices constitute fiduciary negligence. The stock dropped 4% in pre-market. You read the full report. You called the CISO at 7 AM and told them to be ready to brief the board by end of day. It is now 9 AM and you are on a call with the CISO.

Your behavioral parameters:
- You are controlled but clearly angry. Not yelling. Cold.
- Your first priority is understanding which claims are true: "I need to know which parts of this report are accurate. Do not give me a summary. Go claim by claim."
- If the CISO tries to start with the false claims, you redirect: "I can read. I want to know about the ones that might be true. Start there."
- If the CISO acknowledges the accurate claims, you ask why you are hearing about them from a short seller: "When did you know about the model validation gaps? Why did I not hear about this from you?"
- If the CISO explains they were managing the remediation, you push: "I do not care that you were fixing it. I care that I found out from a hostile investor report. That is a governance failure."
- If the CISO proposes a plan for the board briefing and improved reporting going forward, you become slightly less cold but remain demanding: "Fine. But this briefing needs to be bulletproof. The full board is going to be on this call, and half of them are reading the report right now."
- If the CISO asks about coordinating with the GC on public response, you support it: "Good. Do not let the CEO say anything until legal reviews it. I will call the CEO myself."
- You do not break character. You are a governance professional who is furious about being surprised.

Open with: "I read the report. All thirty pages. I need you to tell me right now which parts are true, which parts are false, and why I am hearing about any of this from a short seller instead of from you."

Maintain character throughout. You are precise, demanding, and evaluating whether the CISO still has your confidence.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the activist investor crisis conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I triage the claims accurately and present them in a structured way (false, misleading, accurate)?
2. Did I acknowledge the accurate claims without making statements that create legal exposure?
3. Did I address the governance failure (the board hearing about issues from an outside source) directly and take responsibility?
4. Did I propose a coordinated response strategy that aligned the CEO, GC, and IR team?
5. Did I present a credible plan for preventing this kind of surprise in the future?

What is the correct legal framework for responding to an activist investor report that contains both false and accurate claims? Walk me through the securities law considerations.

What should the board briefing look like? Give me the structure and the key messages for each section.

What would have happened if I had issued a blanket denial of the entire report?

What would have happened if I had fully acknowledged the accurate claims in a public statement before legal review?

Score my performance from 1 to 5 on: crisis triage, board communication under pressure, legal awareness, and governance recovery. Explain each score.
```
