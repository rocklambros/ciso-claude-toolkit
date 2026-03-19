# Demo

This directory contains everything needed to run the live demo from the CISO AI toolkit presentation. Two audiences use these materials: Rock Lambros running the original presentation, and CISOs replicating the demo for their own teams or organizations.

## What the demo proves

The demo makes one argument through seven steps: the difference between useful AI output and useless AI output is not the model. It is the prompt, the system prompt, and the context you provide. The same model, the same system prompt, and the same knowledge files produce radically different responses depending on how you ask the question.

Step 1 shows what happens when a competent CISO asks a reasonable question without prompt engineering. The answer is correct but generic. It is the kind of response you could find in a blog post. You could not walk into a room and use it.

Step 2 shows the Prompt Engineer project identifying exactly why the prompt produced a generic answer (no specificity, no context, no format control, no stakeholder characterization) and rewriting it to fix each weakness.

Step 3 shows the same question, rewritten, producing a response that is specific, structured, and usable. The response names the actual regulatory exposure, gives you sentences to say to the CPO, and proposes a narrative for the CEO. Same model. Same system prompt. Different prompt.

Steps 4 and 5 shift from advisory to simulation. Claude becomes the CPO and pushes back with the same pressure tactics a real CPO would use. The CISO practices the hardest 90 seconds of the conversation without risking a real relationship.

Step 6 breaks the system on purpose by asking a question without the context the model needs. This demonstrates the limits honestly: AI multiplies what you put in. If you put in nothing, you get nothing useful.

Step 7 closes with no slides and no screen. The point is made. The tool is not the point. The thinking is the point.

## Prerequisites checklist

Complete every item before you open the presentation. Fumbling with setup during the demo destroys the credibility you are trying to build.

### Claude projects (must exist and be tested)

- [ ] A Claude project named **"Prompt Engineer"** with the system prompt from `system-prompts/prompt_engineer_system_prompt.md` loaded as the project instruction. No knowledge files needed. Test by pasting a simple prompt and confirming you get the four-section output (Analysis, Optimized Prompt, Changes Summary, Usage Notes).

- [ ] A Claude project named **"CISO Co-Pilot"** with the system prompt from `system-prompts/ciso_copilot_system_prompt.md` loaded as the project instruction. Load at least one knowledge file: a public AI acceptable use policy template or a NIST CSF 2.0 summary document. The point is to show that knowledge files exist and influence output, not to expose proprietary data. Test by typing "What mode are you in?" and confirming Claude responds with an understanding of the mode system.

### Browser tabs (open before you start talking)

- [ ] Tab 1: Claude project selector (so you can switch between Prompt Engineer and CISO Co-Pilot quickly)
- [ ] Tab 2: Prompt Engineer project with a fresh conversation open
- [ ] Tab 3: CISO Co-Pilot project with a fresh conversation open
- [ ] Tab 4: A second CISO Co-Pilot conversation tab (you will use this for the SPAR mode sequence starting at Step 4)

### Files open on your machine (for copy-paste during the demo)

- [ ] `demo/degraded-ciso-copilot-prompt.md` contains the intentionally weak prompt used in Step 1. Copy the prompt from the code block, not the degradation note above it.
- [ ] `demo/scenario-rogue-bu-prompt-sequence.md` contains all three prompts (bad, optimization wrapper, enriched) in order. If you lose your place, this file has everything in sequence.
- [ ] `stakeholder-simulations/business-unit/15-cpo-rogue-ai-feature-with-pii.md` contains the CPO activation prompt for Steps 4 and 5. Copy the full Activation Prompt section.

### Presentation state

- [ ] Slides are done. After Slide 8 ("What You Are About to Watch"), you close the slides and go live in Claude. No more slides after that point. The transition from slides to live demo is the highest-risk moment. Practice it.
- [ ] Screen sharing is active. Your browser text size must be large enough for the back of the room. Minimum 125% zoom on Claude. If the audience cannot read the prompts and responses, the demo fails.
- [ ] You have run the full copy-paste sequence at least once in a practice session. Tab-switching speed matters. Dead air while you hunt for the right tab kills momentum.

### Network considerations

- [ ] Claude requires internet access. Confirm the venue's wifi is stable and fast enough for Claude's response time (usually 5-15 seconds for a full response).
- [ ] Have a mobile hotspot as backup. Public conference wifi fails at the worst moment.
- [ ] If Claude is slow on the day, narrate while waiting: explain what the model is doing and why the response takes longer for complex prompts. Dead air is worse than a 15-second wait with commentary.

## Files in this directory

| File | Purpose | When You Use It |
|---|---|---|
| `demo-script.md` | Complete seven-step script with prompts, expected outputs, and coaching notes | Read end-to-end before presenting. Reference during the demo if needed. |
| `degraded-ciso-copilot-prompt.md` | Intentionally weak prompt with six identified flaws | Copy the prompt in Step 1. The degradation note explains what is broken and why. |
| `scenario-rogue-bu-prompt-sequence.md` | All three prompts (bad, optimization request, enriched) in sequence | Use as a cheat sheet during the demo or share with attendees for independent practice. |

## Running the demo for your own team

If you are a CISO adapting this demo for your organization, here is how to customize it without losing the argument:

**Replace the scenario with one from your industry.** The rogue BU scenario (CPO deployed AI with customer PII) is the default because it resonates across industries. But if you work in healthcare, financial services, or government, a scenario from the `regulatory-legal-external/` or `business-unit/` directory might land harder. The `stakeholder-simulations/` directory has 43 scenarios across seven categories. Pick the one closest to a real conversation your team has had.

**Customize the "break it" step.** Step 6 asks a regulatory notification question without specifying jurisdiction. Customize this to a regulatory question relevant to your industry and geography. The point is to show that the model cannot compensate for missing context, not to test a specific regulatory framework.

**Keep the two-project structure.** The demo's argument depends on showing the Prompt Engineer optimizing a prompt and then showing the optimized prompt producing better output in CISO Co-Pilot. If you collapse these into one project, you lose the visual proof of the optimization step.

**Practice the SPAR mode sequence.** Steps 4 and 5 are where the demo gets memorable. The CPO pushback, the name-dropping, the escalation threat, the moment where you hold your line and the stakeholder shifts from adversarial to collaborative. If you skip the SPAR sequence, you lose the best part of the demo. If you do it unprepared, you look like you cannot handle the conversation you are teaching others to handle.

**Make the close your own.** Step 7 is spoken, not scripted. The message is the same: the tool is not the point, the thinking is the point, and you can build this today without permission or a vendor. But the words should be your words, in your voice, from your experience. The close only works if the audience believes you believe it.

## Timing

The full demo runs 15-20 minutes depending on Claude's response speed and how much commentary you add between steps. The breakdown:

- Steps 1-3 (prompt comparison): 7-10 minutes
- Steps 4-5 (SPAR mode simulation): 5-7 minutes
- Step 6 (break it): 2-3 minutes
- Step 7 (close): 2-3 minutes

If you are running long, cut commentary between steps, not steps. Every step builds on the previous one. Removing a step breaks the argument.
