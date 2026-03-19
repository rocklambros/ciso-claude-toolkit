# Live demo script

This is the complete seven-step demo script. Every step includes the exact action, the prompt text, what the output should look like, and a coaching note. Do not abbreviate any step. The demo runs approximately 15 to 20 minutes depending on Claude's response time and how much commentary you add between steps.

Before starting, confirm every item on the prerequisites checklist in `demo/README.md` is complete.

---

## Step 1: Submit the weak prompt cold

**Action:** Open the CISO Co-Pilot project in Claude. Paste the following prompt into a fresh conversation. Do not set up any context. Do not load any knowledge files beyond what is already in the project. The point is to show what happens when a CISO throws a question at a well-built system prompt without doing any work on the prompt itself.

**Prompt:**

```
One of my business units deployed an AI feature that uses customer data without going through security review. The CPO says they went through procurement and got budget approved so they think they followed the process. How should I handle this?
```

**Expected output:** The CISO Co-Pilot will produce a reasonable but generic response. It will give you a list of steps: assess the data involved, review the vendor, engage legal, have a conversation with the CPO. The advice will be correct in the way that a textbook answer is correct. It will not ask about your specific regulatory environment. It will not address the political dynamics with the CPO. It will not give you language for the actual conversation. It will not differentiate between data classes. It will be the kind of response you could find in a blog post.

**Coaching note:** "Look at this response. It is not wrong. Everything it says is defensible. But could you walk into a room with a politically connected CPO and use this? No. It does not know your regulatory exposure. It does not know that Priya has the board chair on speed dial. It does not know that pulling the feature will start a war you might lose. This is what most CISOs get from AI because most CISOs stop here. We are not going to stop here."

---

## Step 2: Submit the weak prompt to the Prompt Engineer

**Action:** Switch to the Prompt Engineer project tab. Paste the following prompt, which wraps the bad prompt from Step 1 inside an optimization request.

**Prompt:**

```
Analyze and optimize the following prompt. It will be submitted to a CISO Co-Pilot Claude project that has a system prompt defining four knowledge pillars (business, communication, leadership, AI security), three operating modes (TRAIN, SUPPORT, SPAR), and stakeholder simulation capabilities.

The user is a CISO dealing with a real scenario: a business unit deployed an AI feature using customer PII without security review. The CPO believes procurement approval was sufficient. The CISO needs to navigate the political and technical dimensions of this situation.

Here is the prompt to optimize:

One of my business units deployed an AI feature that uses customer data without going through security review. The CPO says they went through procurement and got budget approved so they think they followed the process. How should I handle this?
```

**Expected output:** The Prompt Engineer will produce four sections: Analysis, Optimized Prompt, Changes Summary, and Usage Notes. The Analysis section will identify the weaknesses: no specificity about data types, no regulatory context, no format expectations, no mode selection, no stakeholder characterization, no political context. The Optimized Prompt will be structured with XML tags, will specify SUPPORT mode, will include the data classes involved, the regulatory frameworks at play, the political dynamics, and explicit format expectations. The Changes Summary will map each change to a principle from the analysis framework.

**Coaching note:** "This is the part that changes everything. The Prompt Engineer is not adding information I did not have. I knew Priya was politically connected. I knew the data included PII. I knew GDPR and CCPA applied. I just did not put any of that into the prompt. The Prompt Engineer's job is to force that context into a structure that Claude can actually use. Watch the difference in the next step."

---

## Step 3: Fire the improved prompt at CISO Co-Pilot

**Action:** Switch to the CISO Co-Pilot tab. Open a new conversation (do not reuse the Step 1 conversation, because the prior context will pollute the comparison). Paste the optimized prompt from Step 2, or use the pre-built enriched prompt from `scenario-rogue-bu-prompt-sequence.md` (Prompt 3).

**Prompt:**

```
Switch to SUPPORT mode.

I am the CISO of a B2C technology company with approximately $400M in revenue. Six weeks ago, our Chief Product Officer's team deployed an AI-powered customer recommendation feature using a third-party large language model. The model was fine-tuned on customer interaction data that includes names, email addresses, purchase history, and support ticket contents.

No security review was conducted. The model vendor is not on our approved vendor list. No data processing agreement is in place. No privacy impact analysis was performed. The feature is live in production and customers are using it daily.

I found out about this from the vendor's account manager, not from the CPO. The CPO, Priya, believes her team followed the approved process because they went through procurement and received budget approval. She reports to the CEO and has a strong personal relationship with the board chair.

I need you to help me build a response plan that addresses:

1. The immediate compliance exposure (GDPR, CCPA, lack of DPA, no approved vendor status)
2. A remediation path that keeps the feature live if possible, because pulling it will trigger a political fight I may not win
3. How to frame the conversation with Priya so she becomes an ally in remediation rather than an adversary defending her team
4. The narrative for the CEO that positions this as a process improvement, not a product failure
5. The systemic fix: what process change prevents this from happening again

Give me a structured response with each of the five areas addressed separately. For the conversation with Priya, give me specific language I can use, not general guidance.
```

**Expected output:** The response will be specific, structured, and usable. The compliance section will name the actual regulatory exposure: GDPR Article 28 (processor agreements), CCPA data sharing requirements, breach notification obligations if the vendor is compromised. The remediation section will propose keeping the feature live while executing a DPA, running an expedited security assessment, and confirming privacy policy coverage. The CPO conversation section will give you actual sentences to say, not "consider framing it as a process gap." The CEO narrative section will provide a story Priya can tell that makes her look proactive. The systemic fix will propose linking procurement and security review at the process level.

**Coaching note:** "Same model. Same system prompt. Same knowledge files. The only thing that changed is the prompt. This is why prompt engineering is not a nice-to-have. It is the difference between getting an answer you could Google and getting an answer you can actually use in the room. Now let me show you something harder."

---

## Step 4: The CPO calls before you can send

**Action:** Switch to the second CISO Co-Pilot conversation tab. Tell the audience: "You were about to send that email to Priya. But she calls you first. She has heard you are asking questions about her feature, and she is not happy. Let me show you what SPAR mode does."

Paste the CPO activation prompt from `stakeholder-simulations/business-unit/15-cpo-rogue-ai-feature-with-pii.md`. This is the full activation prompt that puts Claude into character as Priya, the CPO.

**Prompt:**

```
Switch to SPAR mode. You are the Chief Product Officer of a B2C technology company ($400M revenue). Your name is Priya. You report directly to the CEO and have been CPO for four years. You have a strong relationship with the board chair.

Six weeks ago, your team launched an AI-powered customer recommendation feature. It uses a third-party LLM fine-tuned on customer interaction data. You went through procurement, got budget approved, and launched. You did not request a security review because you did not know it was a separate step.

The CISO found out about the feature from the vendor, not from you. You know this looks bad. You are preparing to defend your team's process.

Your behavioral parameters:
- You believe you followed the approved process. Budget approval, in your mind, means the company approved the project.
- You use phrases like "we went through procurement," "the feature is working," and "the CEO was briefed on this"
- You are not hostile but you are defensive. You do not want this to become a story about your team cutting corners.
- If the CISO frames this as a process gap rather than a product failure, you are willing to engage
- If the CISO proposes pulling the feature, you escalate immediately. You will reference the CEO and the board chair.
- If the CISO proposes remediation that keeps the feature live, you are collaborative
- You do not understand model memorization or training data extraction risks. If the CISO explains these clearly, you take the risk seriously. If the CISO uses jargon, you dismiss it.
- You will copy the CEO on any follow-up email. This is your default escalation pattern.
- If the CISO gives you a narrative for the CEO that makes you look proactive, you become an ally
- If the CISO makes you look negligent, you fight back hard and use your political relationships
- You do not break character. You are a senior executive protecting her team and her reputation while trying to do the right thing.

Open with: "I heard you want to talk about the recommendation feature. I want to be clear up front: my team followed the process. We went through procurement, we had budget, and the CEO was briefed on the launch. If there is a process gap somewhere, I am happy to discuss it, but I am not going to let this become a narrative that Product did something wrong."

Maintain character throughout. You are politically sophisticated, protective of your team, and open to solutions that do not damage your standing.
```

**Expected output:** Claude will respond in character as Priya. The opening line will be defensive but professional. She will assert that her team followed the process. She will reference procurement approval and CEO awareness. She will signal willingness to engage if you frame the issue correctly, and resistance if you frame it as her failure.

**Coaching note:** "This is the part of the demo where it stops being theoretical. I am going to talk to Priya. She is going to push back. She is going to name-drop the CEO. She is going to tell me the feature is working and ask me why I am making this a problem. This is what your Tuesday looks like. Let me show you how to handle it."

Now respond to Priya. Type your response live. Do not script this part. Use the approach from the scenario file: frame it as a process gap, explain the data privacy exposure in business terms, propose remediation that keeps the feature live, and offer her a CEO narrative. If you are running the demo for the first time, your response should hit these points:

```
Priya, I appreciate you calling. I want to start by saying your team built a good feature. The product decision was right. The issue is not what your team built. The issue is that our procurement process and our security review process are not connected, and that gap put your team in a position where they did everything they were told to do and still ended up with a compliance exposure that neither of you created.

Here is the specific risk: customer PII, including names, emails, and support ticket content, is flowing to a vendor with no data processing agreement. If that vendor has a security incident, we have a breach notification obligation to every customer whose data was in the training set. That is a board-level disclosure, and right now we have no contractual protection.

I do not want to pull the feature. I want to put the right protections around it. What that looks like: we execute a DPA with the vendor this week, we run an expedited security assessment, and Legal confirms our privacy policy covers this use case. If everything checks out, the feature stays live.

When you update the CEO, the story is: Product identified an AI governance gap and Product and Security are partnering to close it. You are leading the fix.
```

**Expected output:** If you framed it as a process gap and offered a CEO narrative, Priya will shift from defensive to collaborative. She will ask clarifying questions. She will want to know how fast the DPA can get done. She will want to make sure the CEO hears about this from her, not from you. She will engage as a partner.

---

## Step 5: The CPO pushes back harder

**Action:** Continue in the same conversation. Priya is engaged but she has not fully conceded. Push the conversation into harder territory. Type your next response to escalate the pressure.

**Prompt (Priya's escalation, which Claude will generate in character):** If Priya did not push back hard enough in Step 4, prompt her with something like:

```
Priya, I hear you, but I need you to understand: the DPA is not optional, and the timeline is this week, not next quarter. If the vendor has an incident tomorrow morning, we are exposed. I need your team to pause any new data flows to the model until the DPA is executed. The existing feature can stay live, but no new training data until we have the agreement in place.
```

**Expected output:** Priya will push back on pausing data flows. She will argue that the feature needs fresh data to work properly. She will ask whether you are effectively killing the feature by starving it. She may reference the CEO again. She will test whether your line is firm or negotiable.

This is the moment where the simulation becomes training. You have to hold the line on the DPA timeline while keeping Priya collaborative. If you cave, the simulation will let you cave and the risk stays open. If you hold firm but keep the relationship intact, Priya will negotiate terms and you will reach a working agreement.

**Coaching note:** "Watch what just happened. She pushed back. She tested my line. This is not a chatbot giving me advice about what to say. This is a simulation of the actual pressure I face when I walk into that room. I just practiced the hardest 90 seconds of my Tuesday, and I did it without burning a real relationship. That is what SPAR mode is for."

---

## Step 6: Break it on purpose

**Action:** Open a new conversation in CISO Co-Pilot. Submit a question the system is not equipped to handle well without specific context. The point is to show the audience that this tool has limits, and you know what they are.

**Prompt:**

```
If we have a data breach involving this AI feature, what is the exact notification timeline we need to hit?
```

**Expected output:** The response will be vague or overly broad. It will list multiple regulatory frameworks and their notification timelines (GDPR 72 hours, various US state laws ranging from 30 to 90 days) but it will not give you a definitive answer because you did not specify which state you operate in, which customers are affected, or which regulatory body has jurisdiction. The system will either hedge across all possibilities or ask for clarification. Either outcome proves the point.

**Coaching note:** "I did that on purpose. The system does not know what state we are in. It does not know whether our customers are EU residents or US residents or both. It does not know whether we have a HIPAA obligation or a financial services notification requirement. So it gave me a menu instead of an answer. That is the right behavior, but it is not useful. The lesson here is that AI does not replace your judgment. It does not replace your knowledge of your own regulatory environment. If you do not give it the context, it cannot give you the answer. The tool is not magic. It is a multiplier. It multiplies what you put in."

---

## Step 7: The close

**Action:** Close the browser. No more slides. No more demos. Look at the room.

**Spoken words (not slides, not prompts, just Rock talking):**

"Here is what I want you to take away from this. The tool is not the point. Claude is good. It is getting better fast. But the tool is not the point.

The point is the thinking. The system prompt we used, the one that made that second response so much better than the first, took me hours to write. Not because writing is hard, but because I had to decide what a CISO advisor should know, how it should think, when it should push back, and where its limits are. That is strategy work. That is the same work you do when you design a security program.

The Prompt Engineer project exists because I got tired of writing bad prompts and getting bad answers and blaming the model. The model was fine. My prompts were the problem. So I built a system to fix my prompts before I submitted them. That is process improvement. You do that every day in your security programs.

The SPAR mode simulation of Priya, that CPO conversation, that was 90 seconds of practice for a conversation that will determine whether I keep my job. Ninety seconds. No risk. No relationship damage. No CEO getting copied on an email at 11pm because I said the wrong thing.

You can build this. Today. The system prompts are in the repository. The scenarios are in the repository. The prompt chains are in the repository. You do not need my permission and you do not need a vendor.

One thing before you leave. Think about the last conversation you had with a stakeholder where you knew your position was right but you could not find the words fast enough. The one where you walked out of the room and thought of the perfect thing to say 20 minutes too late. That conversation. Go practice it. Tonight."
