# CISO Claude Toolkit

This is a working toolkit for CISOs who want to use Claude as a strategic advisor, training partner, and operational copilot. It is not a concept deck or a product pitch. It is a collection of system prompts, prompt chains, stakeholder simulations, and crisis scenarios designed to make a CISO better at the hardest parts of the job: the conversations, the decisions, and the pressure.

The toolkit exists because the gap between what AI can do for security leaders and what most security leaders are doing with AI is enormous. Most CISOs paste a question into ChatGPT and get a generic answer. This project gives you a governed, context-rich AI environment that speaks your language, knows your frameworks, and pushes back when your thinking has gaps.

## Directory structure

```
ciso-claude-toolkit/
├── system-prompts/          Two Claude project system prompts: CISO Co-Pilot and Prompt Engineer
├── prompt-chains/           Multi-stage prompt sequences for common CISO workflows
├── stakeholder-simulations/ 43 realistic stakeholder scenarios across 7 categories
├── high-difficulty-scenarios/ 7 crisis decision-making scenarios (difficulty 4-5)
├── demo/                    Live demo script and supporting materials
└── presentation/            Speaker notes for the accompanying talk
```

## Quickstart

1. **Create two Claude projects.** In Claude, create a project called "CISO Co-Pilot" and load `system-prompts/ciso_copilot_system_prompt.md` as the system prompt. Create a second project called "Prompt Engineer" and load `system-prompts/prompt_engineer_system_prompt.md` as the system prompt.

2. **Run a prompt chain.** Open any file in `prompt-chains/` and follow the staged prompts. Start with `what-just-happened-incident-summarizer.md` if you want fast results at 2am with a CEO brief due in 20 minutes.

3. **Run a stakeholder simulation.** Open any file in `stakeholder-simulations/`, copy the Activation Prompt into your CISO Co-Pilot project, and practice the conversation. Run the Debrief Prompt afterward to extract lessons.

## How to improve your prompts

Every prompt in this toolkit was written to pass the analysis framework in the Prompt Engineer system prompt. If you write your own prompts, chains, or simulations, submit them to the Prompt Engineer project first. It will identify weaknesses and rewrite them for you.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for submission guidelines.

## License

MIT License. Copyright (c) 2026 Rock Lambros.
