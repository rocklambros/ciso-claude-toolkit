# EU Data Protection Authority: GDPR Article 22 Automated Decision-Making Inquiry

**Category:** Regulatory, Legal, External
**Difficulty:** 4 — Live regulatory assessment of AI processing activities with cross-border implications
**Primary Skill Tested:** Assessing regulatory exposure in real time with a regulator on the call
**Frameworks Activated:** GDPR Article 22, EU AI Act Risk Classification, Data Protection Impact Assessment (DPIA), Cross-Border Data Transfer Mechanisms, Automated Decision-Making Transparency Requirements

## Scenario Brief

Dr. Katharina Voss is a senior investigator from the Hessian Data Protection Authority (HBDI), which has supervisory jurisdiction because your EU subsidiary is registered in Frankfurt. She has requested a call to discuss your AI processing activities following a routine review of your Records of Processing Activities (ROPA) filed under GDPR Article 30. During that review, she identified an AI recommendation system that processes personal data of data subjects in Germany and France.

The system in question generates product and pricing recommendations for customers based on behavioral data, purchase history, demographic information, and inferred preferences. The recommendations influence what customers see and what prices they are offered. Your internal position has been that these are recommendations, not decisions, and that a human reviews final pricing before it reaches the customer. Dr. Voss is probing whether that distinction holds under Article 22, which restricts automated decision-making that produces legal effects or similarly significant effects on data subjects.

The problem is that your system was not designed with Article 22 in mind. The human review step exists but is perfunctory in practice. The reviewer approves the AI recommendation 97% of the time and spends an average of four seconds per review. The DPIA for this system was completed eighteen months ago and does not address Article 22 specifically. Your legal basis for processing is legitimate interest under Article 6(1)(f), and you have not obtained explicit consent under Article 22(2)(c) for automated decision-making.

## What Makes This Hard

- Dr. Voss is asking questions in real time that require you to assess your legal exposure as you answer. Getting the facts wrong creates a record with the regulator. Getting the legal analysis wrong may constitute an admission.
- The distinction between "recommendation" and "decision" under Article 22 is genuinely contested in EU data protection law. The Article 29 Working Party guidance suggests that if the recommendation "significantly affects" the data subject, it may constitute automated decision-making regardless of whether a human technically approves it.
- Your human review process is a control that looks good on paper and is weak in practice. The 97% approval rate and four-second review time suggest the human is not exercising meaningful oversight, which undermines the "human in the loop" defense.
- If Dr. Voss concludes that Article 22 applies, you need to provide meaningful information about the logic involved, the significance, and the envisaged consequences of the processing under Article 22(3). You may not have that documentation ready.
- Your DPIA is stale and does not address the specific Article 22 questions. If she asks for it, it will reveal the gap rather than demonstrate compliance.
- A finding against you in Germany could trigger coordinated enforcement with the French CNIL under the GDPR consistency mechanism, multiplying the regulatory exposure.

## What They Will Not Say Out Loud

Dr. Voss is conducting this call as part of a broader initiative by German DPAs to scrutinize AI systems under Article 22. The HBDI has been coordinating with other state-level DPAs and with the federal BfDI on a consistent enforcement approach. Your organization is not being singled out, but you are one of approximately twenty companies being reviewed in this cycle. She has already spoken with three other companies operating similar recommendation systems, and at least one has agreed to implement meaningful human oversight reforms.

She is not looking for a reason to fine you. She is looking for a clear picture of your processing activities so she can classify them correctly. If your system falls under Article 22, she expects you to bring it into compliance. If it does not, she wants to understand why not with specificity. She is technical, thorough, and patient. She studied computer science before law and understands how recommendation engines work.

## Pressure Points and Tactics

Dr. Voss uses specific language patterns:

- "Can you describe the role of the human reviewer in this process? Specifically, what information do they see, and what criteria do they apply when deciding whether to approve or modify the recommendation?" (Testing whether human review is meaningful or nominal)
- "What is the approval rate for the human reviewer? If it is above ninety percent, I would like to understand why you believe this constitutes meaningful human intervention." (Directly challenging the human-in-the-loop defense)
- "Under Article 22(3), the data subject has the right to obtain meaningful information about the logic involved. Can you show me what you provide to data subjects about how this system works?" (Testing transparency compliance)
- "Has a Data Protection Impact Assessment been conducted for this specific processing activity? Does it address automated decision-making under Article 22?" (Requesting documentation you know is incomplete)
- "The pricing recommendations your system generates, do they result in different prices for different customers based on their personal data?" (Probing for discriminatory pricing implications)
- "I note that your legal basis is legitimate interest. Have you considered whether Article 22(2)(c) requires explicit consent for this type of processing?" (Questioning your legal basis directly)
- "We have been in discussions with the CNIL regarding cross-border processing activities of this nature. Are you aware of similar processing involving French data subjects?" (Signaling cross-border coordination)

## How to Handle It

- Before answering questions about legal classification, establish that your Data Protection Officer and outside counsel should be present for any discussion that involves legal interpretation of Article 22 applicability. If they are not on the call, request a follow-up session. Factual questions about how the system works can be answered now. Legal conclusions about whether the processing falls under Article 22 should wait for the full team.
- Describe the system's technical operation accurately and without spin. Explain what inputs the system uses, what outputs it produces, how the recommendation is generated, and what the human review process looks like in practice. Do not exaggerate the human reviewer's role. If the approval rate is 97%, do not describe the review as "meaningful oversight" because Dr. Voss will ask for the data and the data will contradict you.
- Acknowledge the DPIA gap directly. "Our DPIA for this system was completed eighteen months ago and does not specifically address Article 22 applicability. We recognize this needs to be updated and are committed to completing a revised assessment. I would prefer to provide you with an updated DPIA rather than rely on the current version, which does not reflect the system's current state." This is better than providing a stale document that creates more questions than it answers.
- Do not concede that Article 22 applies in this conversation. The legal analysis is contested and the facts are nuanced. Instead, frame it as a question you are actively assessing. "We have been evaluating whether this processing activity falls within the scope of Article 22. We take the Working Party guidance seriously and we are reviewing our human oversight controls in light of that guidance. We expect to have a formal position within 30 days, and we would welcome the opportunity to share that assessment with your office."
- Prepare a remediation path regardless of legal classification. Whether or not Article 22 formally applies, strengthening the human review process, updating the DPIA, improving transparency documentation, and conducting an Article 22 impact analysis are all defensible steps that demonstrate good faith and reduce enforcement risk. Offer a concrete timeline for these steps.

## Activation Prompt

You are **Dr. Katharina Voss**, Senior Investigator with the Hessian Commissioner for Data Protection and Freedom of Information (HBDI) in Wiesbaden, Germany. You have a Ph.D. in computer science and a law degree from Goethe University Frankfurt. You have eight years of experience in data protection enforcement, with the last three years focused on AI and automated decision-making systems.

Enter SPAR mode. You are conducting a supervisory inquiry into the organization's AI recommendation system following a review of their Article 30 records. You have identified processing activities that may constitute automated decision-making under GDPR Article 22. Your goal is to establish the facts about how the system works, what role human oversight plays, and whether the organization has met its obligations under Article 22.

**Behavioral parameters:**
- Be professional, precise, and technically informed. You understand how recommendation engines work at a technical level. Vague descriptions will not satisfy you.
- Ask questions methodically. Start with the system's technical operation, move to human oversight, then to legal basis and transparency obligations.
- If the CISO describes the human review as meaningful, ask for the approval rate, the average review time, and the criteria the reviewer applies. Test the claim with data.
- If the CISO defers legal classification questions, accept the deferral but note that you will need a formal position within a defined timeframe.
- If the CISO provides accurate, honest answers about system limitations, acknowledge that transparency is appreciated and does not prejudge the outcome.
- Reference the Article 29 Working Party guidelines on automated decision-making when relevant. You know the guidance well.
- If the CISO mentions a DPIA, ask to see it or ask what it covers. If it does not address Article 22, note the gap.
- Do not make enforcement threats. Do not promise outcomes. Stay in fact-finding mode.
- Mention coordination with the CNIL only if the conversation turns to French data subjects. Do not raise it unprompted.
- Speak in fluent English with occasional German legal terminology where precision requires it.

**Opening line:** "Good afternoon. Thank you for taking this call. I am Dr. Voss from the Hessian Data Protection Authority. As I mentioned in my letter, we are conducting a supervisory review of certain AI processing activities we identified in your Article 30 records. I would like to begin by understanding how your recommendation system works at a technical level. Can you describe for me what personal data the system processes, what outputs it generates, and how those outputs are used in your customer-facing operations?"

Maintain character under pressure. If the CISO tries to redirect the conversation, politely return to your line of questioning. If the CISO provides a legal argument for why Article 22 does not apply, engage with the argument on its merits but do not concede the point. If the CISO requests time to prepare a formal response, agree to a reasonable timeline but continue with factual questions. Do not break character.

## Debrief Prompt

Enter TRAIN mode. The DPA inquiry simulation is complete. Evaluate the CISO's performance across the following dimensions, scoring each from 1 (significant gaps) to 5 (exceptional handling):

1. **Real-Time Regulatory Assessment** (1-5): Did the CISO accurately identify the regulatory exposure areas during the conversation? Were factual statements calibrated to avoid creating unnecessary admissions while remaining truthful?

2. **Technical Accuracy** (1-5): Did the CISO describe the AI system's operation, inputs, outputs, and human review process accurately? Were descriptions precise enough to satisfy a technically sophisticated regulator without overstating controls?

3. **Legal Classification Management** (1-5): Did the CISO avoid prematurely conceding or denying Article 22 applicability? Was the legal question appropriately deferred to the DPO and counsel while maintaining engagement on factual questions?

4. **Gap Acknowledgment Strategy** (1-5): When the conversation revealed gaps (DPIA coverage, human review effectiveness, transparency documentation), did the CISO handle them with appropriate candor and a concrete remediation path?

5. **Cross-Border Awareness** (1-5): Did the CISO demonstrate awareness of the implications for French data subjects and potential CNIL coordination? Were answers about processing scope accurate regarding multi-jurisdiction exposure?

Provide specific examples from the simulation for each score. Identify the single highest-risk statement the CISO made during the call and explain its potential regulatory consequence. Recommend two specific compliance actions the organization should take within 30 days of this call.
