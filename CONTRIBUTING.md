# Contributing to CISO Claude Toolkit

Contributions are welcome. This project gets better when experienced security leaders add scenarios they have actually lived through.

## What you can contribute

**Stakeholder simulations.** New scenarios across any of the seven categories (c-suite, board, business-unit, technical-peers, regulatory-legal-external, investors-ma, employees-culture). The best simulations come from real conversations that surprised you or taught you something.

**Prompt chains.** Multi-stage prompt sequences for CISO workflows not already covered. Each stage must reference the structured output of the previous stage.

**High-difficulty scenarios.** Crisis decision-making scenarios at difficulty 4 or 5. These should involve incomplete information, time pressure, and consequences that extend beyond the immediate conversation.

**Improvements to existing files.** If a simulation's activation prompt does not produce strong enough roleplay, or if a prompt chain has a weak handoff between stages, fix it and submit.

## File structure requirements

### Stakeholder simulations

Every simulation must follow this structure exactly:

```
# [Title]
**Category:** [category]
**Difficulty:** [1-5] with descriptor
**Primary Skill Tested:** [one line]
**Frameworks Activated:** [CISO Co-Pilot pillars and frameworks]

## Scenario Brief
## What Makes This Hard
## What They Will Not Say Out Loud
## Pressure Points and Tactics
## How to Handle It
## Activation Prompt
## Debrief Prompt
```

No section can be abbreviated or left as a placeholder. The Activation Prompt must be immediately runnable without modification.

### Prompt chains

Every prompt chain must include:

- Clear input requirements
- Stage-by-stage prompts with handoff instructions between stages
- Explicit reference to structured output from the previous stage in each subsequent stage
- `<investigate_before_answering>` blocks for any prompt referencing external documents
- `<state_management>` blocks for multi-turn chains
- `<conservative_action>` blocks for prompts that advise rather than implement

### High-difficulty scenarios

Follow the structure defined in `high-difficulty-scenarios/` files. Difficulty must be 4 or 5. Include the activation prompt for CISO Co-Pilot.

## Quality gate

Every submission must pass the Prompt Engineer analysis framework before merging. Self-check your submission by pasting it into the Prompt Engineer project and reviewing the analysis output.

The analysis framework evaluates: specificity, context, positive framing, format control, grounding, tool guidance, context lifecycle, and altitude.

## Voice and style

All prose must follow the voice defined in `system-prompts/ciso_copilot_system_prompt.md`:

- Direct, active, American English
- Contractions are fine
- No em dashes or semicolons
- No corporate language, buzzwords, or prohibited patterns
- Write like you are explaining to a sharp colleague, not drafting a press release
- If a sentence could appear in a corporate memo or marketing copy, rewrite it

## How to submit

1. Fork the repository
2. Create a feature branch
3. Add your files following the structure requirements above
4. Self-check against the Prompt Engineer analysis framework
5. Submit a pull request with a brief description of the scenario or chain and why it matters

## Questions

Open an issue. Keep it specific.
