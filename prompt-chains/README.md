# Prompt Chains

Multi-stage prompt sequences for common CISO workflows. Each chain builds structured output across stages, with explicit handoff instructions between stages.

## What prompt chains are and why they matter

A prompt chain is a sequence of prompts where each stage produces structured output that the next stage references. This is different from asking a single question and getting a single answer. The chain approach works better for complex CISO workflows because it mirrors how you actually work: gather facts, then assign ownership, then draft communications, then assess regulatory exposure. Each step depends on what you learned in the previous step.

The alternative, putting everything into one massive prompt, fails for two reasons. First, you overwhelm the model with competing objectives and get a response that touches everything but goes deep on nothing. Second, you cannot course-correct between stages. If the triage stage of an incident response misidentifies the data classification, every subsequent recommendation is wrong. With a chain, you review and correct each stage before moving to the next.

Every chain in this directory was designed with three engineering principles from the Prompt Engineer analysis framework:

**Grounding.** Any chain stage that references a document you will paste in includes an `<investigate_before_answering>` block. This block tells Claude to read the document completely before analyzing it. Without this block, Claude will speculate about what the document contains based on your description rather than reading the actual text. Speculation causes hallucination.

**State management.** Multi-turn chains include `<state_management>` blocks that tell Claude to maintain structured output as a working document across stages. When you produce a triage summary in Stage 1 of the incident response chain, Claude holds that summary as context for all subsequent stages. If you provide new information, it updates the summary rather than starting over.

**Conservative action.** Every chain that produces recommendations (which is most of them) includes `<conservative_action>` blocks. These tell Claude to produce recommendations for your review rather than stating them as definitive answers. The distinction matters: a regulatory notification assessment should say "the following factors suggest notification may be required" rather than "you must notify." The CISO makes the decision, not the model.

## Files

| File | Purpose | Format | When to Use |
|---|---|---|---|
| incident-response-chain.md | AI-related data exposure response | 5 sequential stages | An AI tool exposed or processed data it should not have |
| board-communication-engine.md | Technical findings to board-ready communications | 2 stages (draft + stress test) | Any board update, risk briefing, or budget request |
| control-gap-analyzer.md | Framework compliance gap analysis | 2 stages (analysis + remediation) | Audit prep, framework assessment, compliance review |
| fair-lite-risk-quantification.md | Quantified risk assessment using FAIR | Interactive guided session | CFO conversations, budget justification, risk register entries |
| red-team-your-ai-governance.md | AI governance documentation attack | Single comprehensive stage | Quarterly policy review, pre-audit preparation |
| shadow-ai-discovery.md | Shadow AI usage identification | Single stage with triage | Quarterly shadow IT review, incident investigation |
| vendor-questionnaire-interpreter.md | Skeptical vendor security response review | Single stage with follow-ups | Before approving any vendor, especially AI vendors |
| what-just-happened-incident-summarizer.md | Rapid incident summary for leadership briefs | Single rapid stage | Active incident, CEO brief due in minutes |
| hiring-interview-question-generator.md | JD/resume gap analysis with interview questions | Single stage with rubric | Before any security team interview |

## How to use

### Running a multi-stage chain

1. Open the chain file and read the full structure. Understand how many stages exist and what each produces.
2. Open your CISO Co-Pilot project and start a fresh conversation.
3. Copy the Stage 1 prompt and paste it into the conversation. Follow the instructions in the prompt (some will ask you to provide inputs like a document, a data source, or a scenario description).
4. Review the Stage 1 output. If any facts are wrong or missing, correct them before moving on. The chain only works if each stage starts with accurate inputs.
5. Copy the Stage 2 prompt and paste it into the same conversation. The `<state_management>` block ensures Claude references the Stage 1 output automatically.
6. Continue through all stages.

### Running a single-stage chain

Some chains (shadow-ai-discovery, vendor-questionnaire-interpreter, red-team-your-ai-governance) are single-stage. These still involve interaction: the model asks you questions, you provide inputs, and it builds the analysis incrementally. Copy the prompt, paste it in, and follow the model's lead.

### When to start a new conversation

Start a new conversation in these situations:
- You are running a different chain on a different topic
- The conversation has grown long (more than 15 exchanges) and you notice the model losing track of earlier context
- You want to compare outputs between two different approaches to the same problem

Keep the same conversation when:
- You are iterating on a single chain's output
- You want the model to reference its prior analysis

### Customizing chains for your organization

Every chain accepts inputs that customize it for your context. The incident response chain asks for your regulatory environment, your data classification, and your stakeholder map. The board communication engine asks for the target audience (full board, audit committee, or risk committee) and adjusts depth and vocabulary accordingly.

For repeated use, consider creating a "context block" that you paste at the top of every conversation. This block would include your organization's industry, revenue range, regulatory frameworks, data classification scheme, and key stakeholder roles. You do not need to put this in the system prompt. Pasting it at the start of each conversation is sufficient and more flexible.

## Design principles

Every chain in this directory was evaluated against the Prompt Engineer analysis framework before inclusion. The specific principles applied:

**Specificity.** Every stage tells Claude exactly what to produce, in what format, with what sections. "Assess regulatory exposure" is too vague. "For each applicable framework, produce: triggering factor, notification timeline, notification recipient, recommended action, and confidence level" is specific enough to produce consistent, usable output.

**Context propagation.** Each stage explicitly references the structured output of the previous stage. Stage 2 says "Based on the triage summary from Stage 1" rather than assuming Claude remembers. This reference is not just for clarity. It is an engineering decision. Claude's attention mechanism works better when you explicitly point it at the relevant context rather than hoping it retrieves it from the conversation history.

**Format control.** Every stage defines its output format with either a description ("produce a table with these columns") or XML tags for complex structures. Format control prevents Claude from choosing its own format, which tends toward generic lists and bullet points. Specific formats produce specific, usable output.

**Handoff instructions.** Multi-stage chains include explicit handoff instructions between stages and at the end of the chain. If you need to continue in a new conversation, across sessions, or with a different team member, the handoff instructions tell you exactly what to copy and how to frame the continuation.

## Combining chains

The chains are designed to work independently, but several produce outputs that feed naturally into others:

- **Incident Summarizer** output feeds into the **Incident Response Chain** for a full five-stage response
- **FAIR-Lite Risk Quantification** output feeds into the **Board Communication Engine** for a quantified board-ready brief
- **Control Gap Analyzer** output feeds into the **Board Communication Engine** for a remediation budget request
- **Shadow AI Discovery** findings feed into the **Board Communication Engine** if findings are significant enough for board reporting
- **Vendor Questionnaire Interpreter** findings feed into the **Control Gap Analyzer** to map vendor gaps against your framework requirements

When combining chains, carry the structured output from the first chain into the second chain by pasting it at the start of the new conversation with a note like: "I completed a FAIR risk quantification for a threat scenario. The output is below. I now want to build this into a board communication using the Board Communication Engine format. Target audience: risk committee."
