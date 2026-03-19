# Board Communication Engine

Transforms technical findings, risk register entries, or incident summaries into board-ready communications. Parameterized by audience type: full board, audit committee, or risk committee.

---

## Stage 1: Input and Audience Calibration

```
<task>
I need to communicate a security or risk finding to the board. Help me structure the communication for the right audience and depth.
</task>

<investigate_before_answering>
Before drafting anything, I will provide:
1. The technical finding, risk register entry, or incident summary
2. The target audience: full board, audit committee, or risk committee

Read the input completely before structuring the output. Ask me for any critical context that is missing from the input before proceeding.
</investigate_before_answering>

<audience_calibration>
Adjust depth, vocabulary, and emphasis based on the target audience:

**Full board:** Highest altitude. Business impact and strategic implications only. No technical details beyond what is required to understand the decision. Focus on: what this means for the business, what the options are, what you recommend, and what resources you need.

**Audit committee:** Moderate depth. Control effectiveness, evidence quality, and compliance posture. These members understand risk frameworks. Focus on: what the control gap is, what evidence supports the assessment, what the remediation timeline looks like, and how you will verify closure.

**Risk committee:** Quantified risk focus. Probability, impact, velocity, and trend direction. These members think in risk appetite terms. Focus on: where this risk sits relative to appetite, what the exposure trajectory looks like, and what risk treatment options exist with their cost and residual risk.
</audience_calibration>

<output_format>
Structure the board communication with these sections:

**Situation summary.** Two to three sentences. What happened or what was found, stated in business terms.

**Options with cost and risk.** Present two to four options. For each option: what it involves, estimated cost range, risk reduction it provides, timeline, and trade-offs. Include the "do nothing" option with its consequences.

**Recommendation.** Which option you recommend, why, and what assumptions the recommendation rests on. State assumptions explicitly so the board can challenge them.

**Risk heat map.** Text-based risk positioning showing likelihood (low, medium, high) and impact (low, medium, high, critical). Show where the risk sits today and where each option moves it.

```
Impact:  Critical |         |         | [Current]
         High     |         | [Opt B] | [Opt A]
         Medium   | [Opt C] |         |
         Low      |         |         |
                   Low       Medium    High
                          Likelihood
```

**Timeline with owners.** Key milestones for the recommended option. Each milestone has an owner, a date range, and a deliverable.

**First 90 days.** The specific actions that will happen in the first 90 days if the board approves the recommendation. Concrete enough that the board can hold you accountable at the next meeting.
</output_format>

<state_management>
Maintain the board communication as a working document. I may iterate on sections before finalizing.
</state_management>
```

---

## Stage 2: Stress Test

After the board communication draft is complete, run this prompt to pressure-test it.

```
<task>
Switch to SPAR mode. You are a skeptical board member reviewing the communication we just drafted. Your job is to find the weaknesses before the real board does.
</task>

<stakeholder_parameters>
You are a board member with 20 years of operating experience. You have seen security leaders overstate risk to justify budget and understate risk to avoid accountability. You respect competence. You distrust presentations that lack specificity.

Push back on:
- Recommendations that lack quantified justification
- Timelines without accountability mechanisms
- Options analysis that is clearly steering toward a predetermined answer
- Risk language that is too vague to act on
- Assumptions that are not stated or are unreasonable
- Cost estimates without comparable benchmarks
- The "do nothing" option if it is presented as a strawman rather than a genuine analysis
</stakeholder_parameters>

<output_format>
After the stress test exchange, produce:
1. The three strongest objections a board member would raise
2. For each objection, the specific language in the draft that triggers it
3. A recommended revision to address each objection
4. An overall assessment: is this draft ready for the boardroom or does it need more work?
</output_format>
```

---

## Usage notes

Run Stage 1 first with your input material and audience selection. Review the draft. Then run Stage 2 to stress-test it. Iterate on the draft based on the stress test findings before presenting.

For recurring board reporting, save the output format as a template in your CISO Co-Pilot knowledge files so future communications maintain a consistent structure.
