# CISO Claude Toolkit

This is a working toolkit for CISOs who want to use Claude as a strategic advisor, training partner, and operational copilot. It is not a concept deck or a product pitch. It is a collection of system prompts, prompt chains, stakeholder simulations, and crisis scenarios designed to make a CISO better at the hardest parts of the job: the conversations, the decisions, and the pressure.

The toolkit exists because the gap between what AI can do for security leaders and what most security leaders are doing with AI is enormous. Most CISOs paste a question into ChatGPT and get a generic answer. This project gives you a governed, context-rich AI environment that speaks your language, knows your frameworks, and pushes back when your thinking has gaps.

## Why this approach works

Most security leaders interact with AI tools the same way they interact with search engines: they type a question and hope the answer is useful. That approach fails for the same reason asking a consultant a question with no context fails. The answer might be correct, but it will not be specific enough to act on.

This toolkit takes a different approach. Instead of treating Claude as a search engine, it treats Claude as an advisory system with three layers of context:

1. **System prompts** define who Claude is in each project. The CISO Co-Pilot system prompt gives Claude doctoral-depth expertise across four pillars (business knowledge, communication, leadership, and AI security), three operating modes (TRAIN for skill building, SUPPORT for real work, SPAR for stress testing), and the ability to simulate specific stakeholders with authentic pressure tactics. The Prompt Engineer system prompt gives Claude the ability to analyze and improve any prompt you write.

2. **Knowledge files** give Claude access to your organizational context. When you load your AI acceptable use policy, your risk register, or your board presentation template into the CISO Co-Pilot project, Claude's responses become grounded in your actual environment rather than generic best practices.

3. **Structured prompts** tell Claude exactly what to produce and how. The prompt chains in this toolkit use XML tags for format control, grounding protocols to prevent speculation, state management for multi-turn conversations, and explicit mode selection so Claude knows whether to advise, act, or push back.

The difference between a bare prompt and a structured prompt in a governed project is the difference between a generic blog post answer and a response you can walk into a room with.

## Directory structure

```
ciso-claude-toolkit/
├── system-prompts/           Two Claude project system prompts that power the toolkit
│   ├── ciso_copilot_system_prompt.md     The CISO advisory system prompt
│   └── prompt_engineer_system_prompt.md  The prompt optimization system prompt
│
├── prompt-chains/            Multi-stage prompt sequences for common CISO workflows
│   ├── incident-response-chain.md        5-stage AI data exposure response
│   ├── board-communication-engine.md     Technical findings to board-ready comms
│   ├── control-gap-analyzer.md           Framework compliance gap analysis
│   ├── fair-lite-risk-quantification.md  FAIR methodology risk quantification
│   ├── red-team-your-ai-governance.md    AI governance doc attack from 3 angles
│   ├── shadow-ai-discovery.md            Shadow AI usage identification
│   ├── vendor-questionnaire-interpreter.md  Skeptical vendor response review
│   ├── what-just-happened-incident-summarizer.md  2am rapid incident summary
│   └── hiring-interview-question-generator.md     JD/resume gap-based questions
│
├── stakeholder-simulations/  43 realistic stakeholder scenarios across 7 categories
│   ├── c-suite/              8 scenarios: CFO, GC, CEO, CTO, COO, CHRO, CMO
│   ├── board/                5 scenarios: audit chair, risk member, new director
│   ├── business-unit/        9 scenarios: dev managers, CPO, VP Sales, finance
│   ├── technical-peers/      6 scenarios: CIO, cloud architects, SOC managers
│   ├── regulatory-legal-external/  7 scenarios: FTC, state AGs, auditors, DPAs
│   ├── investors-ma/         4 scenarios: PE acquirers, activists, target CISOs
│   └── employees-culture/    4 scenarios: engineers, whistleblowers, breach victims
│
├── high-difficulty-scenarios/ 7 crisis scenarios at difficulty 4-5
│   ├── 44 through 50: peer CISO breach disclosure, CEO marketing claims,
│   │   board member conflicts, journalist calls, vendor blame-shifting,
│   │   regulator direct contact, outgoing CEO data exfiltration
│
├── demo/                     Live demo script and supporting materials
│   ├── demo-script.md        Complete 7-step demo with exact prompts
│   ├── degraded-ciso-copilot-prompt.md   Intentionally weak prompt for demo
│   └── scenario-rogue-bu-prompt-sequence.md  3-prompt comparison sequence
│
├── presentation/             Speaker notes for the accompanying talk
│   └── speaker-notes/        Spoken content for slides 3, 4, 5, and 8
│
├── ARCHITECTURE.md           Project architecture and Claude project design guide
├── CONTRIBUTING.md           How to submit new simulations, chains, and scenarios
└── LICENSE                   MIT License, Copyright 2026 Rock Lambros
```

## Quickstart

**Time to first useful output: under 10 minutes.**

### Step 1: Create the CISO Co-Pilot project

Open Claude (claude.ai). Click "Projects" in the left sidebar. Create a new project called "CISO Co-Pilot." In the project settings, paste the full contents of `system-prompts/ciso_copilot_system_prompt.md` into the system prompt field.

This system prompt is approximately 5,000 words. That is intentional. It defines the four knowledge pillars, three operating modes, nine stakeholder archetypes, voice and tone rules, and interaction principles that make the model useful. A shorter system prompt would produce a less capable advisor.

Optionally, add knowledge files. Good starting choices: a public AI acceptable use policy template, a NIST CSF 2.0 summary, or your organization's sanitized risk register. Knowledge files persist across conversations and ground the model's responses in your actual environment.

### Step 2: Create the Prompt Engineer project

Create a second Claude project called "Prompt Engineer." Paste the full contents of `system-prompts/prompt_engineer_system_prompt.md` as the system prompt.

This project serves a different purpose. Instead of answering security questions, it analyzes and optimizes the prompts you write for any Claude project. Think of it as a quality gate: any prompt you plan to use repeatedly should pass through the Prompt Engineer first. It will identify weaknesses in specificity, context, framing, format control, grounding, and altitude, then rewrite the prompt to fix them.

### Step 3: Run something

**For a quick win,** open `prompt-chains/what-just-happened-incident-summarizer.md`. Copy the prompt into a CISO Co-Pilot conversation and paste in some raw incident notes. The model will produce a structured summary, a severity-calibrated stakeholder communication draft, and an evidence preservation list. This chain was designed for 2am when you have a CEO brief in 20 minutes.

**For skill building,** open any file in `stakeholder-simulations/`. Start with `c-suite/01-cfo-security-cost-center.md` if you want a difficulty 3 conversation about defending your security budget with financial translation. Read the scenario brief to understand the context, then copy the Activation Prompt into CISO Co-Pilot. Have the conversation. When you are done, copy the Debrief Prompt into the same conversation to get scored on your performance.

**For crisis practice,** open any file in `high-difficulty-scenarios/`. Start with `47-journalist-has-accurate-undisclosed-incident-info.md` if you want to feel 45 minutes of real pressure. Copy the prompt into CISO Co-Pilot and work through the decision points.

## The two-project architecture

The toolkit uses two separate Claude projects because they serve fundamentally different purposes:

**CISO Co-Pilot** is the advisor. It answers questions, produces deliverables, simulates stakeholders, and stress-tests your thinking. Its system prompt defines the security leadership domain, the voice and tone, and the operating modes.

**Prompt Engineer** is the optimizer. It makes the prompts you submit to CISO Co-Pilot (and to any other Claude project) more effective. Its system prompt defines an analysis framework with ten evaluation criteria and a library of reusable blocks that can be inserted into optimized prompts.

These projects do not share context. That is by design. When you optimize a prompt in the Prompt Engineer project and then paste the optimized version into CISO Co-Pilot, the manual copy step creates a review moment. You can read the optimized prompt, understand why each change was made, and modify it before using it. This separation also prevents context pollution: the analytical conversation about prompt structure does not contaminate the advisory conversation about security strategy.

For a deeper explanation of the architecture, data sensitivity tiering, knowledge file management, token budgets, and kill switches, see [ARCHITECTURE.md](ARCHITECTURE.md).

## How to improve your prompts

Every prompt in this toolkit was written to pass the analysis framework defined in the Prompt Engineer system prompt. That framework evaluates prompts on ten dimensions:

1. **Specificity:** Does each instruction tell Claude exactly what to produce?
2. **Context:** Does the prompt explain why constraints or preferences exist?
3. **Positive framing:** Are instructions phrased as desired behaviors rather than prohibitions?
4. **Format control:** Is the expected output format explicitly defined?
5. **Examples:** Do examples demonstrate only desired behaviors?
6. **Tool guidance:** Is it clear whether Claude should act or advise?
7. **Grounding:** Will Claude need to inspect documents before responding?
8. **Complexity risk:** Could Claude over-engineer the solution?
9. **Context lifecycle:** Does the prompt manage tokens across long interactions?
10. **Altitude:** Is the prompt at the right level of specificity?

If you write your own prompts, chains, or simulations, submit them to the Prompt Engineer project first. Paste the prompt, ask the Prompt Engineer to analyze and optimize it, and review the four-section output (Analysis, Optimized Prompt, Changes Summary, Usage Notes). Then use the optimized version.

The single biggest improvement most CISOs can make is adding context. The difference between "How should I handle a rogue AI deployment?" and a prompt that specifies the data classification, the regulatory environment, the stakeholder's political position, and the desired output format is the difference between a generic answer and an actionable one.

## What this toolkit does not do

This toolkit does not connect to your security tools, ingest your logs, run your playbooks, or automate your operations. It is an advisory and training system that runs entirely through Claude's project interface. You paste prompts in and get responses back. The value comes from the quality of those responses, which is determined by the system prompt, the knowledge files, and the prompt quality.

It also does not replace your judgment. Claude produces strong analysis and well-structured recommendations, but it does not know your organizational politics, your budget reality, or the relationship dynamics in your executive team unless you tell it. The prompts in this toolkit are designed to pull that context out of you and feed it to the model. The model multiplies what you put in. If you put in nothing, you get a textbook answer. If you put in the full picture, you get something you can use.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for submission guidelines. The best contributions come from CISOs who have lived through a conversation they wish they had practiced first.

## License

MIT License. Copyright (c) 2026 Rock Lambros.
