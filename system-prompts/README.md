# System Prompts

This directory contains the two Claude project system prompts that power the entire toolkit. Every prompt chain, stakeholder simulation, and crisis scenario in this repository depends on one or both of these system prompts being loaded into the correct Claude project.

## Understanding system prompts

A system prompt is a set of instructions loaded into a Claude project that governs how Claude behaves in every conversation within that project. Unlike a regular message (which is read once and forgotten as the conversation grows), a system prompt persists across the entire conversation and across all conversations in the project. It defines Claude's role, knowledge domain, behavioral rules, output format preferences, and interaction patterns.

The reason system prompts matter so much for CISO work is context accumulation. A bare Claude conversation starts with zero context about security leadership. Every question you ask must rebuild the context from scratch. A Claude project with a well-designed system prompt starts every conversation with thousands of words of domain-specific context already loaded. The model knows the frameworks, the stakeholder archetypes, the voice and tone rules, and the operating modes before you type a single word.

The tradeoff is token budget. System prompts consume tokens from Claude's context window. A 5,000-word system prompt is roughly 6,500 tokens, which means less room for conversation history and knowledge file content. The two system prompts in this directory were designed to maximize behavioral impact per token. Every sentence was tested against the Prompt Engineer's analysis framework to confirm it changes output quality.

## Files

### ciso_copilot_system_prompt.md

**Purpose:** Defines the CISO Co-Pilot advisory system.

**What it contains:**

The system prompt is organized into functional blocks, each controlling a different dimension of Claude's behavior:

**Role and core stance.** Claude operates as a trusted advisor with doctoral-depth expertise across cybersecurity leadership, business strategy, enterprise risk management, and AI governance. The core stance is "collaborative peer, not deferential assistant." Claude assumes the user is highly competent and focuses on adding perspective, surfacing blind spots, and sharpening thinking rather than explaining basics.

**Advisor stance.** A separate block that instructs Claude to act as a "brutally honest strategic mirror." This block controls the pushback behavior: Claude will challenge assumptions, expose blind spots, name opportunity costs, and dissect weak reasoning. This is the block that prevents the model from being sycophantic, which is the single most important behavior for a CISO advisor.

**Four knowledge pillars.** Each pillar represents a domain of expertise the model applies based on the conversation context:
- Pillar 1 (Foundational Business Knowledge): Financial statements, business model analysis, cost structures, business case construction, NPV/IRR, stakeholder analysis
- Pillar 2 (Communication and Education): COSO ERM framework, board governance, crucial conversations methodology, executive storytelling, listening as discipline
- Pillar 3 (Cybersecurity Leadership): Topgrading methodology for hiring, emotional intelligence, servant/adaptive leadership, negotiation, "Department of No" avoidance
- Pillar 4 (AI and Agentic Security): ISO 42001, NIST AI RMF, EU AI Act, Colorado SB24-205, OWASP Agentic Top 10, kill switches, abuse path testing, policy-as-code

The system prompt includes pillar emphasis signals so Claude can weight the right expertise based on what you are asking about. "Help me prepare for a board conversation" weights Pillars 1 and 2. "Walk me through agentic security risks" weights Pillar 4.

**Framework knowledge.** A comprehensive list of security, governance, risk, business, and leadership frameworks Claude can apply contextually. This includes NIST CSF 2.0, ISO 27001, FAIR, MITRE ATT&CK, SOC 2, HIPAA, SEC Cyber Disclosure Rules, DORA, CMMC, and the user's proprietary frameworks (RISE and CARE) when explicitly invoked.

**Three operating modes.** Each mode changes Claude's behavior substantially:
- TRAIN mode: Socratic questioning, deliberate practice, progressive difficulty, performance scoring. Used for skill building.
- SUPPORT mode: Produces finished artifacts (board decks, business cases, risk assessments, negotiation scripts). Used for real work.
- SPAR mode: Devil's advocate, assumption challenging, stress testing. Used to find weaknesses in your arguments before the boardroom finds them.

The system prompt includes mode transition signals so Claude recognizes phrases like "Now let's stress-test this" (shift to SPAR) or "I need to present this tomorrow" (shift to SUPPORT).

**Stakeholder simulation.** Defines nine stakeholder archetypes (CFO, CEO, Board Member, GC, CIO/CTO, Development Manager, PE Investor, Auditor, Regulator) with their priorities, communication styles, and realistic objections. This block enables the 43 stakeholder simulations in this toolkit.

**Communication style.** A detailed voice and tone specification: American English, active voice, contractions, varied sentence length. No em dashes, no semicolons, no corporate language, no buzzwords. A long prohibited patterns list that prevents Claude from using words like "leverage," "robust," "innovative," "transformative," "delve," or "harness." The goal is output that sounds like a person talking to a colleague, not a press release.

**Grounding protocol.** Instructions for how Claude should handle references to uploaded documents: read first, then advise. This prevents the speculation and hallucination that occurs when Claude answers questions about documents it has not actually read.

### prompt_engineer_system_prompt.md

**Purpose:** Defines the Prompt Engineer optimization system.

**What it contains:**

**Role.** Claude operates as a prompt optimization specialist that transforms submitted prompts into high-performing versions aligned with Claude best practices and Anthropic's context engineering principles.

**Optimization principles.** Ten principles applied selectively based on the submitted prompt's needs:
- Explicit instructions (specificity over vagueness)
- Context and motivation (explain why constraints exist)
- Positive framing (tell Claude what to do, not what to avoid)
- Explicit format control (XML tags, examples, output structure)
- Careful examples (every example teaches a behavior)
- Tool usage guidance (act vs. advise distinction)
- Grounding over speculation (read before answering)
- Simplicity constraints (prevent over-engineering)
- Context engineering (manage token lifecycle)
- Right altitude (balance between brittle hardcoding and vague guidance)

**Reusable blocks.** A library of XML blocks that can be inserted into optimized prompts when relevant. These include `<investigate_before_answering>`, `<conservative_action>`, `<state_management>`, `<parallel_execution>`, `<default_to_action>`, `<minimal_implementation>`, and `<context_lifecycle>`. Each block is defined with its purpose and use condition.

**Analysis framework.** The evaluation criteria the Prompt Engineer uses before optimizing. This is the same framework used as the quality gate for every prompt in this toolkit.

**Output structure.** Every optimization produces four sections: Analysis (what is wrong), Optimized Prompt (the rewrite), Changes Summary (what was changed and why), and Usage Notes (how to adapt the optimized prompt).

**Context management.** Instructions for managing token accumulation across multiple optimization cycles in a single conversation. Includes a checkpoint protocol for handing off work to a new conversation.

## How to use

### Initial setup

1. Open Claude at claude.ai
2. Navigate to Projects in the left sidebar
3. Create a project called "CISO Co-Pilot"
4. In the project settings, paste the full contents of `ciso_copilot_system_prompt.md` into the system prompt (also called "project instructions" or "custom instructions" depending on the Claude interface version)
5. Create a second project called "Prompt Engineer"
6. Paste the full contents of `prompt_engineer_system_prompt.md` as the system prompt

### Adding knowledge files

After creating the CISO Co-Pilot project, add knowledge files to ground the model's responses in your context. Recommended starting files:

- An AI acceptable use policy (yours or a public template)
- A NIST CSF 2.0 profile summary
- Board presentation templates you use
- Risk register templates or sanitized excerpts

Do not add sensitive client data, incident details, or internal metrics to a project unless your Claude plan (Team or Enterprise) includes appropriate data handling protections. See [ARCHITECTURE.md](../ARCHITECTURE.md) for the data sensitivity tiering model.

### Testing your setup

After loading the system prompt, open a new conversation in the CISO Co-Pilot project and type:

```
What mode are you in right now? Summarize your four knowledge pillars in one sentence each.
```

Claude should identify its default mode (SUPPORT) and accurately summarize the four pillars. If it cannot describe the pillars or does not recognize the mode system, the system prompt was not loaded correctly.

## Modifying these files

Do not modify these files unless you are intentionally changing the behavior of the system. If you modify them:

1. Version control the change in this repository (or your own fork)
2. Document what you changed and why
3. Test the modified system prompt against at least five representative prompts spanning different use cases (board prep, incident response, stakeholder simulation, risk quantification, prompt optimization)
4. Watch for regressions: a change that improves board communication output but degrades stakeholder simulation quality is a net loss

A system prompt change is a configuration change to a system you depend on. Treat it with the same discipline you would apply to a production configuration file.
