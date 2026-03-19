# Presentation

This directory contains the speaker notes for the CISO AI toolkit talk. The slide deck itself lives in Gamma and is not stored in this repository. These speaker notes are what Rock says aloud during each slide.

Any CISO can use these materials to deliver their own version of the talk. The speaker notes are written in Rock's voice but contain the substance, not the personality. Adapt the tone to match your own speaking style. Keep the structure and the argument.

## The argument the talk makes

The talk has one argument with three supporting points:

**Main argument:** CISOs are underusing AI because they are using it wrong, not because it is not useful.

**Point 1 (Slides 3-5): The risk is quantifiable and smaller than you think.** Most CISOs avoid AI because they believe the data exposure risk is unacceptable. The math says otherwise. A modeled comparison shows that the per-interaction risk of an LLM tool (0.1% to 1% error rate) at 50 users produces an annualized probability of approximately 5%. The same error rate applied to email (200 external shares) produces an annualized probability of approximately 18%. The LLM is 3-4x safer because the external distribution path is removed. The math does not editorialize. It just shows the structural difference.

This is a modeled estimate, not a measured statistic. The talk says that explicitly. The point is not that the number is precise. The point is that anyone claiming AI risk is uniquely dangerous should show their model, because the available analogs suggest it is comparable to or lower than existing SaaS tools most organizations already accept.

**Point 2 (Slides 6-7): The missing layer is governance, not avoidance.** The right response to AI risk is not to block AI tools. It is to govern them the same way you govern every other tool that touches sensitive data: with policy, controls, monitoring, and response capabilities. The CISO Co-Pilot system prompt and the prompt chains in this toolkit demonstrate what governed AI usage looks like.

**Point 3 (Slide 8 + live demo): See it work.** The live demo shows the difference between an unstructured prompt producing a generic answer and a structured prompt in a governed project producing an actionable answer. Then it shows SPAR mode simulating a hostile stakeholder conversation. Then it breaks the system on purpose to show the limits. The audience sees the full range: what it does well, what it does badly, and what it takes to move from one to the other.

## Directory structure

```
presentation/
└── speaker-notes/
    ├── slide-03-the-actual-number.md
    ├── slide-04-where-the-number-comes-from.md
    ├── slide-05-the-math-you-avoided.md
    └── slide-08-what-youre-about-to-watch.md
```

Speaker notes exist only for the four slides with substantive spoken content. Other slides in the Gamma deck are visual (title slide, section breaks, diagrams) and do not require speaker notes.

## How to use these notes

Each file contains the full spoken content for one slide. Read them as scripts you would say to a room, not as bullet points you would put on a screen. The slides themselves should be minimal: a number, a formula, a diagram, a key phrase. The substance comes from what you say.

Speaker notes are written in first person, present tense, as if Rock is talking to the audience right now. They include the specific numbers, the formulas, the challenge statements ("if your numbers are different, show me the model"), and the transition phrases that connect one slide to the next.

### What each file covers

**slide-03-the-actual-number.md** covers the modeling assumptions. Rock explains the scope constraints (what is included and excluded from the model), the data classes modeled, the baseline comparator (existing SaaS tools, not a theoretical zero-risk state), and the 0.1% to 1% range. He frames it as a modeled estimate, not a measured statistic, and challenges the audience: if you think the methodology is flawed, build a better model and publish it.

**slide-04-where-the-number-comes-from.md** explains the fault tree analysis methodology. The core formula, how paths aggregate using the complement method, the user-driven risk formula, and what happens to the probability as you scale from 50 users to 100 users. Rock acknowledges that no empirical dataset exists for AI-specific data exposure and explains the analogs used (SaaS benchmarks and DBIR data). He challenges the audience again: if your numbers are different, show me the model.

**slide-05-the-math-you-avoided.md** runs two concrete calculations side by side. The email scenario: 200 external shares at 0.1% error rate produces an 18% annualized probability. The LLM scenario: 50 users at 0.1% error rate produces a 5% annualized probability. The 3-4x difference is structural because the external distribution path is removed. Rock states that the math is talking, not editorializing. The numbers say what they say.

**slide-08-what-youre-about-to-watch.md** transitions from slides to the live demo. Rock tells the audience what they are about to see (two Claude projects, a prompt optimization, a stakeholder simulation), asks them to keep one thing in mind (the tool is not the point, the thinking is the point), and bridges to the demo with the ask: one action before you leave, and the uncomfortable question about the last conversation you wish you had practiced.

## Building your own Gamma deck

If you are creating your own version of the talk:

1. Create slides with minimal visual content. One number per slide. One formula per slide. One key phrase per slide. The slides are not the content. You are the content.

2. Paste these speaker notes into the Gamma presenter notes field for each corresponding slide. This gives you a teleprompter if you need it.

3. Practice the transition from Slide 8 into the live demo at least three times. This is the highest-risk moment in the talk. The format shifts from presentation to performance. You close the slides, open Claude, and start typing live in front of the room. If you have not practiced this transition, the dead air and tab-switching will undermine the confidence you just built in the first eight slides.

4. Time yourself. The full talk (slides + demo) should run 30-40 minutes. The slides run 10-15 minutes. The demo runs 15-20 minutes. If your slides are running longer than 15 minutes, you are adding content that belongs in the demo.

## Adapting for your audience

**If your audience already accepts that AI risk is manageable:** Shorten slides 3-5 to one slide with the key comparison numbers (18% email vs. 5% LLM). Spend more time on the demo. The demo is where skeptics become believers.

**If your audience is deeply skeptical about AI risk:** Spend more time on slides 3-5. Walk through the math slowly. Challenge them to produce a model that shows a different result. Skeptics respond to math, not to enthusiasm.

**If your audience is non-technical board members:** Skip the formula slides. Show the comparison numbers on one slide. Focus the demo on SPAR mode (Steps 4-5), which demonstrates the practical value of AI for preparation. Board members care about preparation and judgment, not technical methodology.

**If you are running the talk internally for your security team:** Replace the risk quantification slides with the actual numbers from your environment (user count, data volume, tool inventory). Run a simulation from `stakeholder-simulations/` that matches a conversation your team recently had. The closer the scenario is to their lived experience, the more engaged they will be.
