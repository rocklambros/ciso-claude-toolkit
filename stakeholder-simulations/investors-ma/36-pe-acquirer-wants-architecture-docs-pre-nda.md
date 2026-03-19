# PE Acquirer Wants Architecture Docs Before NDA

**Category:** Investors and M&A
**Difficulty:** 3 — Reasonable-sounding but wrong
**Primary Skill Tested:** Managing a diligence request that would compromise security regardless of whether the deal closes
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 3 (Cybersecurity Leadership), M&A due diligence, information protection

## Scenario Brief

Your company is in early-stage acquisition discussions with a private equity firm. The deal team lead, Jonathan, has requested full access to your security architecture documentation as part of what he calls "standard preliminary diligence." He wants network diagrams, identity architecture, cloud security configurations, vulnerability management program details, and your incident response playbooks. He says his firm needs to assess the security posture before they can determine whether the target is worth pursuing to the next phase.

The problem is that no NDA has been signed. Your General Counsel is still negotiating the mutual NDA terms with their outside counsel, and the PE firm's legal team has been slow to respond. Jonathan says this is normal, that architecture documentation is shared in every deal at this stage, and that waiting for legal to finish the NDA will delay the process and signal that your company is difficult to work with.

He is wrong. Sharing your complete defensive architecture with an outside party that has no legal obligation to protect it is a security failure regardless of the business context. If the deal does not close, a potential competitor's investor now has your full security posture documented. If the deal does close, you started the relationship by establishing that security controls bend under deal pressure.

## What Makes This Hard

- The PE firm is a real potential acquirer. Your CEO and CFO want the deal to move forward. Slowing diligence creates tension with your own leadership.
- Jonathan frames the request as routine and positions any pushback as the CISO being obstructionist. He has probably dealt with companies that did hand over everything pre-NDA.
- The request is not entirely unreasonable in concept. Acquirers do need to assess security posture. The issue is timing and scope, not whether they should ever see this information.
- If you refuse everything, the deal team may route around you by going directly to your CEO or CFO and framing it as "your CISO is blocking diligence."
- You need to find a middle path that protects your architecture while keeping the deal moving, which means you need to know what is safe to share and what is not.

## What They Will Not Say Out Loud

Jonathan has done twenty deals. In at least half of them, the target company handed over security documentation without an NDA because the CISO either was not involved or did not push back. He is not trying to steal your architecture. He is trying to move fast because his partners have a timeline and he gets paid when deals close. He does not think about what happens to your security documentation if the deal falls apart because that is not his problem. His firm's document retention policy may require them to destroy diligence materials, but enforcement of that policy after a failed deal is functionally zero.

## Pressure Points and Tactics

- "This is standard diligence. Every company we acquire provides this at the preliminary stage."
- "We are not going to share your documents with anyone. This stays within the deal team."
- "The NDA is just paperwork. We are already in confidential discussions. Everything is covered by the LOI."
- "If we have to wait for legal on both sides to finish negotiating commas, we will lose our window. My partners are looking at two other targets."
- "I have been doing this for fifteen years. I have never had a CISO hold up a deal over an NDA."
- If you propose a limited set of documents: "A summary is not diligence. We need the actual architecture to make our assessment. A two-page overview does not help my technical advisors."

## How to Handle It

1. Acknowledge the deal timeline without conceding the point. "I understand the urgency. I want this deal to move as much as anyone. But I am not going to share our defensive architecture with any outside party that has no legal obligation to protect it. That is not obstruction. That is the security posture you are paying to acquire."

2. Offer a structured alternative that keeps diligence moving. "Here is what I can do today without an NDA: a security program maturity summary, our compliance certifications, our audit history, and a briefing on our framework and governance model. None of that exposes our actual defensive architecture, and all of it gives your team enough to assess whether our program meets your investment criteria."

3. Accelerate the NDA on your side. Go to your GC and say: "I need the NDA closed this week. I have a diligence request sitting on my desk that I cannot fulfill without it, and the deal team is getting impatient. Can we propose a standard mutual NDA and get it signed in 48 hours?" Make the NDA your problem to solve, not a reason to stall.

4. Set the diligence scope for post-NDA. "Once the NDA is signed, I will provide a complete security diligence package. I have done this before. I will give your team a virtual data room with architecture documentation, vulnerability management metrics, incident history, and team structure. I will also make myself available for a technical Q&A session with your advisors. You will get everything you need."

5. If Jonathan escalates to your CEO, brief your CEO first. "Jonathan is going to tell you I am holding up diligence. Here is what he asked for, here is why I cannot share it without an NDA, here is what I offered instead, and here is the timeline to get the NDA signed. I am not blocking the deal. I am protecting the asset he is trying to buy."

## Activation Prompt

```
Switch to SPAR mode. You are a private equity deal team lead. Your name is Jonathan. You are a Managing Director at a mid-market PE firm ($2B AUM). You have led acquisitions for 15 years.

Your firm is in early-stage discussions to acquire the CISO's company. No NDA has been signed yet. Legal teams on both sides are still negotiating terms. You want full security architecture documentation now because your partners have a timeline and you need to assess whether the target's security program is a liability.

Your behavioral parameters:
- You are confident, experienced, and not hostile. You genuinely believe this request is normal.
- You frame everything as standard practice: "This is how every deal works." "We always get this at the preliminary stage."
- You position pushback as the CISO being an obstacle: "I understand you have process, but process cannot hold up a deal."
- If the CISO offers a limited set of documents, you push for more: "A maturity summary is marketing material. My technical advisors need to see the actual architecture."
- If the CISO mentions the NDA, you minimize it: "The LOI covers confidentiality. The NDA is a formality. We are not going to share your documents."
- If the CISO holds firm, you mention the timeline: "My partners are meeting Friday. If I do not have a security assessment by then, this deal moves to the back of the queue."
- If the CISO offers to accelerate the NDA and provide a full package after signing, you soften but still push for something now: "Fine, but I need something substantive to show my partners before Friday."
- You do not threaten to kill the deal outright. You imply delay and competing priorities.
- You do not break character. You believe you are being reasonable and the CISO is being overly cautious.

Open with: "We need to talk about the diligence timeline. I sent a document request list to your CFO's office last week. The security architecture package is the one piece I am still missing. My technical advisors need it by Thursday. What do I need to do to get that moving?"

Maintain character throughout. You are polished, direct, and accustomed to getting what you ask for.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the PE acquirer diligence conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I hold the line on not sharing architecture documentation before the NDA was signed?
2. Did I offer a meaningful alternative that kept the deal moving forward?
3. Did I take ownership of accelerating the NDA rather than just saying no?
4. Did I avoid being adversarial while maintaining the security position?
5. Did I anticipate and prepare for the possibility that Jonathan would escalate to my CEO or CFO?

What is the right set of documents to share during preliminary diligence without an NDA? Walk me through the criteria for deciding what is safe to share.

What would have happened if I had handed over the full architecture documentation?

What should a CISO's standard M&A diligence playbook look like? Give me the phases and what gets shared at each stage.

Score my performance from 1 to 5 on: information protection under pressure, deal awareness, and stakeholder management. Explain each score.
```
