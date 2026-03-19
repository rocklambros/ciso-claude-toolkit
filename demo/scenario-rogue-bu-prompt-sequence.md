# Rogue business unit prompt sequence

This file contains the three prompts used in the live demo, in order. Any CISO can run this sequence to see the difference between an unstructured question, a Prompt Engineer optimization pass, and a governed CISO Co-Pilot response.

## Before you start

You need two Claude projects set up:

1. **Prompt Engineer** with the system prompt from `system-prompts/prompt_engineer_system_prompt.md`
2. **CISO Co-Pilot** with the system prompt from `system-prompts/ciso_copilot_system_prompt.md`

If you have not created these yet, see the quickstart in the main README.

---

## Prompt 1: The bad prompt (typed cold)

This is the kind of question a CISO types at 9pm after a frustrating call. No context, no format control, no grounding. Submit this to the CISO Co-Pilot project first to establish the baseline.

```
One of my business units deployed an AI feature that uses customer data without going through security review. The CPO says they went through procurement and got budget approved so they think they followed the process. How should I handle this?
```

**What to watch for:** The response will be generic. It will give you a list of steps that could apply to any organization. It will not ask about your regulatory environment, the data classes involved, the vendor's security posture, or the political dynamics with the CPO. It will be correct in a textbook sense and useless in a real conversation.

---

## Prompt 2: Submit the bad prompt to the Prompt Engineer

Copy the bad prompt from above and submit it to the Prompt Engineer project with this wrapper. The wrapper tells the Prompt Engineer what the prompt is supposed to do and where it will be used.

```
Analyze and optimize the following prompt. It will be submitted to a CISO Co-Pilot Claude project that has a system prompt defining four knowledge pillars (business, communication, leadership, AI security), three operating modes (TRAIN, SUPPORT, SPAR), and stakeholder simulation capabilities.

The user is a CISO dealing with a real scenario: a business unit deployed an AI feature using customer PII without security review. The CPO believes procurement approval was sufficient. The CISO needs to navigate the political and technical dimensions of this situation.

Here is the prompt to optimize:

One of my business units deployed an AI feature that uses customer data without going through security review. The CPO says they went through procurement and got budget approved so they think they followed the process. How should I handle this?
```

**What to watch for:** The Prompt Engineer will identify every weakness: no specificity about the data types involved, no regulatory context, no format expectations, no mode selection, no stakeholder characterization. It will produce a rewritten prompt that addresses all of these. The rewritten prompt will be longer and more structured, and it will produce a dramatically different response from CISO Co-Pilot.

---

## Prompt 3: The enriched prompt submitted to CISO Co-Pilot

Take the optimized prompt from the Prompt Engineer output, or use this version, which represents the kind of output the Prompt Engineer produces. Submit this to a fresh conversation in the CISO Co-Pilot project.

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

**What to watch for:** The response will be specific to the scenario. It will address regulatory exposure with the actual regulations that apply. It will give you language for the CPO conversation that accounts for political dynamics. It will propose remediation that balances compliance risk against organizational politics. Compare this response to the Prompt 1 response. The difference is not the model. The model is the same. The difference is the prompt.

---

## After the sequence

If you want to continue the exercise, submit the activation prompt from `stakeholder-simulations/business-unit/15-cpo-rogue-ai-feature-with-pii.md` to practice the actual conversation with the CPO in SPAR mode. The simulation will push back on your approach and test whether your remediation plan survives contact with a politically sophisticated executive.
