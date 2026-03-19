# Architecture

This document explains why the project is structured the way it is, how to build your own Claude project architecture for security work, and how the two Claude projects in this toolkit relate to each other. If you are setting up CISO Co-Pilot for the first time, start here.

## Why project architecture matters more than prompt quality

A well-written prompt in a poorly structured Claude project will underperform a mediocre prompt in a well-structured project. The reason is context. Claude's effectiveness depends on what it knows when it processes your request. A standalone prompt has only the words in that prompt. A Claude project has a system prompt defining behavior, knowledge files providing domain expertise, and conversation history building shared context over time.

Most CISOs who try AI start with a single prompt pasted into a blank conversation. That is the equivalent of calling a consultant, giving them 30 seconds of background, and expecting a board-ready deliverable. The architecture of your Claude projects determines how much of your organizational context, risk framework, and decision history the model can use.

## How to tier Claude projects by data sensitivity

Not everything belongs in one project. Create separate Claude projects based on what data flows through them.

**Tier 1: General advisory (no sensitive data).** Strategic thinking, framework analysis, interview prep, training scenarios. This is where CISO Co-Pilot lives. No client names, no incident details, no internal metrics.

**Tier 2: Sanitized operational (anonymized data).** Risk assessments with company names removed, sanitized incident summaries, anonymized vendor questionnaires. Create a separate project for this work with a system prompt that reinforces data handling expectations.

**Tier 3: Sensitive operational (requires organizational controls).** If your organization has Claude Team or Enterprise with appropriate data handling agreements, you can create projects for work involving internal data. The system prompt for these projects must include explicit data handling instructions, retention expectations, and scope limitations.

Never put Tier 3 data into a Tier 1 project. The system prompt does not prevent data from being processed. It governs the model's behavior, not the platform's data handling.

## What knowledge files belong in which project

Claude projects accept knowledge files that persist across conversations. Choose what to load based on the project's purpose.

**CISO Co-Pilot knowledge files:**
- The CISO Evolution book content or key excerpts (provides the advisory foundation)
- Your organization's AI acceptable use policy (for policy review and gap analysis)
- Relevant framework documents (NIST CSF 2.0 profile, ISO 27001 statement of applicability)
- Board presentation templates (for consistent output formatting)
- Risk register templates (for structured risk assessment output)

**Prompt Engineer knowledge files:**
- Claude documentation on prompt engineering (Anthropic's official guidance)
- Examples of strong and weak prompts from your own usage
- This toolkit's system prompts (so the Prompt Engineer can reference them when optimizing)

Keep knowledge files current. Outdated policy documents in your project context will produce outdated advice.

## How to structure CISO Co-Pilot

The system prompt in `system-prompts/ciso_copilot_system_prompt.md` defines four pillars (business knowledge, communication, leadership, AI security), three operating modes (TRAIN, SUPPORT, SPAR), and stakeholder simulation capabilities.

When you create the CISO Co-Pilot project in Claude:

1. Set the system prompt to the full contents of `ciso_copilot_system_prompt.md`
2. Add knowledge files relevant to your current priorities
3. Start a new conversation for each distinct topic or engagement
4. Use SPAR mode to stress-test any deliverable before it leaves your desk

The system prompt is designed to be loaded once and used across many conversations. You should not need to modify it frequently. When you do modify it, version control the change (see below).

## How to use the Prompt Engineer to improve all other projects

The Prompt Engineer project exists to make every other prompt you write better. The workflow:

1. Write a prompt for any purpose (a new simulation, a prompt chain stage, a custom system prompt)
2. Paste it into the Prompt Engineer project
3. Review the analysis output: it will identify weaknesses in specificity, context, framing, format control, grounding, and altitude
4. Take the optimized prompt and use it in the target project

This is the quality gate for the entire toolkit. Every prompt chain and simulation in this repository was evaluated against the Prompt Engineer's analysis framework before inclusion.

## Context handoff between projects

Claude projects do not share context with each other. When you optimize a prompt in the Prompt Engineer project and want to use it in CISO Co-Pilot, you copy the output manually. This is intentional. It creates a review step.

For multi-session work within a single project, Claude maintains conversation history within each conversation. Start a new conversation when you change topics. Use the same conversation when you are iterating on a single deliverable.

## Token budget management

Every Claude conversation has a context window. System prompts, knowledge files, conversation history, and your current message all consume tokens from that window. When the window fills up, Claude starts losing access to earlier context.

Manage this actively:

- Keep system prompts focused. The CISO Co-Pilot system prompt is long because it needs to be. Do not add content that does not directly improve output quality.
- Rotate knowledge files. Load the files relevant to your current work, not everything you have.
- Start new conversations when topics change. Do not run a board prep conversation and an incident response conversation in the same thread.
- For long prompt chains, summarize completed stages before starting the next one if you are running all stages in a single conversation.

## Kill switches and fallback modes

The CISO Co-Pilot system prompt includes three operating modes. If the model produces output that does not match your expectations:

- Switch to SPAR mode explicitly: "Switch to SPAR mode and challenge the recommendation you gave me."
- Reset the conversation: start a new conversation in the same project to clear accumulated context
- Simplify the request: if the model is overcomplicating, state "Give me the three most important points only"
- Check your knowledge files: outdated or contradictory knowledge files cause inconsistent output

If the model consistently misses the mark, the system prompt may need adjustment. Use the Prompt Engineer project to evaluate and improve it.

## Version controlling system prompts like code

Treat system prompts as configuration files. They define the behavior of a system you depend on. Version control them.

This repository is your version control system for the toolkit's prompts. For your own custom system prompts:

- Store them in a Git repository (this one or a private one)
- Date each version
- Document what changed and why
- Test changes by running a representative set of prompts against the new version before adopting it

A system prompt change that improves board communication output but degrades incident response output is a regression. Test across use cases.

## Reference architecture

```
┌─────────────────────────────────────────────────────┐
│                    CISO Workflow                     │
│                                                     │
│  Write prompt ──► Prompt Engineer ──► Optimized     │
│                   (analysis +         prompt         │
│                    rewrite)                          │
│                        │                             │
│                        ▼                             │
│              ┌─────────────────┐                     │
│              │  CISO Co-Pilot  │                     │
│              │                 │                     │
│              │  System Prompt  │◄── Version          │
│              │  Knowledge Files│    controlled       │
│              │  Conversation   │                     │
│              │  History        │                     │
│              └────────┬────────┘                     │
│                       │                              │
│            ┌──────────┼──────────┐                   │
│            ▼          ▼          ▼                    │
│         TRAIN      SUPPORT     SPAR                  │
│         mode       mode        mode                  │
│            │          │          │                    │
│            ▼          ▼          ▼                    │
│       Scenarios   Deliverables  Stress               │
│       Practice    Artifacts     Testing              │
│       Feedback    Board decks   Challenges           │
│                   Risk assess.  Assumptions          │
│                   Comms drafts  exposed              │
└─────────────────────────────────────────────────────┘

Data Sensitivity Tiers:
┌──────────┐  ┌──────────┐  ┌──────────┐
│  Tier 1  │  │  Tier 2  │  │  Tier 3  │
│ General  │  │Sanitized │  │Sensitive │
│ Advisory │  │Operational│  │Operational│
│          │  │          │  │          │
│No client │  │Anonymized│  │Internal  │
│data      │  │data only │  │data with │
│          │  │          │  │controls  │
└──────────┘  └──────────┘  └──────────┘

Prompt Quality Pipeline:
  Raw prompt ──► Prompt Engineer ──► Analysis ──► Optimized prompt
                                        │
                                        ▼
                                  Quality gates:
                                  - Specificity
                                  - Context
                                  - Positive framing
                                  - Format control
                                  - Grounding
                                  - Tool guidance
                                  - Context lifecycle
                                  - Altitude
```

## What this architecture does not cover

This toolkit does not address Claude API integration, automated workflows, or programmatic access. It is designed for interactive use through Claude's project interface. If you need API-level integration for security operations, that is a different architecture with different security considerations.
