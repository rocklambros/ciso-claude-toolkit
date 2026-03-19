# Prompt Chains

Multi-stage prompt sequences for common CISO workflows. Each chain builds structured output across stages, with explicit handoff instructions between stages.

## Files

| File | Purpose | Stages |
|---|---|---|
| incident-response-chain.md | AI-related data exposure incident response | 5 stages: triage, ownership, communications, regulatory, post-incident |
| board-communication-engine.md | Transform technical findings into board-ready communications | 2 stages: draft + stress test |
| control-gap-analyzer.md | Evaluate controls against compliance frameworks | 2 stages: gap analysis + remediation planning |
| fair-lite-risk-quantification.md | Quantified risk assessment using FAIR methodology | Interactive guided assessment |
| red-team-your-ai-governance.md | Attack AI governance docs from three angles | Single-stage comprehensive assessment |
| shadow-ai-discovery.md | Identify shadow AI usage from organizational data | Single-stage triage and response |
| vendor-questionnaire-interpreter.md | Skeptical review of vendor security responses | Single-stage review with follow-up generation |
| what-just-happened-incident-summarizer.md | Rapid incident summary for 2am CEO briefs | Single-stage rapid summary |
| hiring-interview-question-generator.md | Targeted interview questions from JD/resume gap analysis | Single-stage question generation |

## How to use

1. Open the prompt chain file for your use case
2. Copy the Stage 1 prompt into your CISO Co-Pilot project
3. Follow the handoff instructions between stages
4. For multi-turn chains, keep the conversation going in the same thread so the model maintains context from prior stages

## Design principles

Every chain in this directory follows these rules:

- Each stage references the structured output of the previous stage
- `<investigate_before_answering>` blocks are present wherever the prompt references a document the user will paste in
- `<state_management>` blocks are present in multi-turn chains
- `<conservative_action>` blocks are present in prompts that advise rather than implement
- Every prompt was evaluated against the Prompt Engineer analysis framework before inclusion
