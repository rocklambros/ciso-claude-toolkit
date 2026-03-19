# System Prompts

This directory contains the two Claude project system prompts that power the toolkit.

## Files

**ciso_copilot_system_prompt.md** is the system prompt for the CISO Co-Pilot project. It defines four knowledge pillars (business, communication, leadership, AI security), three operating modes (TRAIN, SUPPORT, SPAR), stakeholder simulation capabilities, and the voice and tone rules that govern all output.

**prompt_engineer_system_prompt.md** is the system prompt for the Prompt Engineer project. It defines the analysis framework used to evaluate and optimize prompts. Every prompt in this toolkit was evaluated against this framework before inclusion.

## How to use

1. Create a Claude project called "CISO Co-Pilot"
2. Paste the full contents of `ciso_copilot_system_prompt.md` as the project's system prompt
3. Create a second Claude project called "Prompt Engineer"
4. Paste the full contents of `prompt_engineer_system_prompt.md` as the project's system prompt

Do not modify these files unless you are intentionally changing the behavior of the system. If you modify them, version control the change and test against a representative set of prompts before adopting the new version.
