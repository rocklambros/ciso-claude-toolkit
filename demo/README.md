# Demo

This directory contains everything needed to run the live demo from the CISO AI toolkit presentation. Two audiences use these materials: Rock Lambros running the original presentation, and CISOs replicating the demo for their own teams.

## What you are about to do

The demo walks through a seven-step sequence that shows the difference between throwing a question at Claude cold and running the same question through a governed Claude project with a structured system prompt. Along the way, you will show the Prompt Engineer optimizing a weak prompt, the CISO Co-Pilot producing a real advisory response, and the SPAR mode simulating a hostile stakeholder conversation. You will also break the system on purpose to show its limits.

The full walkthrough is in `demo-script.md`. Read it end to end before presenting. The demo depends on setup that takes five minutes but will ruin the presentation if skipped.

## Prerequisites checklist

Complete every item before you open the presentation.

**Claude projects (must exist before demo starts):**

- [ ] A Claude project named "Prompt Engineer" with the system prompt from `system-prompts/prompt_engineer_system_prompt.md` loaded as the project instruction. No knowledge files needed for the demo.
- [ ] A Claude project named "CISO Co-Pilot" with the system prompt from `system-prompts/ciso_copilot_system_prompt.md` loaded as the project instruction.
- [ ] At least one knowledge file loaded in CISO Co-Pilot. For the demo, use a public AI acceptable use policy template or a NIST CSF 2.0 summary document. The point is to show that knowledge files exist and influence output, not to expose proprietary data.

**Browser tabs (open before you start talking):**

- [ ] Tab 1: Claude project selector (so you can switch between Prompt Engineer and CISO Co-Pilot quickly)
- [ ] Tab 2: Prompt Engineer project with a fresh conversation open
- [ ] Tab 3: CISO Co-Pilot project with a fresh conversation open
- [ ] Tab 4: A second CISO Co-Pilot conversation tab (you will use this for the SPAR mode sequence starting at Step 4)

**Files open on your machine (for copy-paste during the demo):**

- [ ] `demo/degraded-ciso-copilot-prompt.md` (the intentionally weak prompt used in Step 1)
- [ ] `demo/scenario-rogue-bu-prompt-sequence.md` (all three prompts in order)
- [ ] `stakeholder-simulations/business-unit/15-cpo-rogue-ai-feature-with-pii.md` (the CPO scenario activation prompt for Step 4)

**Presentation state:**

- [ ] Slides are done. After Slide 8, you close the slides and go live in Claude. No more slides after that point.
- [ ] Screen sharing is active and your browser text size is large enough for the back of the room (minimum 125% zoom on Claude).
- [ ] Do a dry run of the copy-paste sequence at least once. Fumbling with tabs kills momentum.

## Files in this directory

| File | Purpose |
|---|---|
| `demo-script.md` | The complete seven-step demo script with exact prompts, expected outputs, and coaching notes |
| `degraded-ciso-copilot-prompt.md` | The intentionally weak CISO Co-Pilot prompt submitted in Step 1 to show what bad looks like |
| `scenario-rogue-bu-prompt-sequence.md` | The three-prompt sequence (bad, optimized, final) formatted for any CISO to run independently |

## Running the demo for your own team

If you are a CISO adapting this demo for your organization:

1. Set up the two Claude projects using the system prompts in `system-prompts/`.
2. Replace the rogue BU scenario with one that matches your industry. The `stakeholder-simulations/` directory has 43 scenarios across seven categories. Pick the one closest to a real conversation your team has had.
3. Customize the "break it" step (Step 6) with a regulatory question relevant to your jurisdiction.
4. Practice the SPAR mode sequence. The CPO pushback in Steps 4 and 5 is where the demo gets memorable. If you skip it, you lose the best part.
5. The close (Step 7) is spoken, not scripted. Use your own words. The message is the same: the tool is not the point, the thinking is the point.
