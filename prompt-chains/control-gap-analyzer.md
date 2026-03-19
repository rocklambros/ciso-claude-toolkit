# Control Gap Analyzer

Evaluates your control narratives against selected frameworks and identifies what an auditor will find first.

---

## Stage 1: Framework Selection and Control Narrative Analysis

```
<task>
Analyze my control narrative against a selected compliance or governance framework. Identify missing controls, partially implemented controls, unevidenced claims, and the gaps an auditor will find first.
</task>

<investigate_before_answering>
I will provide two inputs:
1. The framework to assess against (NIST CSF 2.0, ISO 27001, NIST AI RMF, EU AI Act, Colorado SB24-205, or OWASP Agentic Top 10)
2. My current control narrative (a document describing what controls exist and how they operate)

Read the control narrative completely before analyzing it. Do not assess controls I have not described. If the narrative is silent on a control area, flag it as "not addressed" rather than assuming it does not exist.
</investigate_before_answering>

<analysis_approach>
Evaluate the control narrative through the lens of the selected framework. For each relevant framework requirement:

1. **Implemented and evidenced.** The narrative describes a control that meets the requirement and references specific evidence (logs, configurations, test results, policies with version numbers).

2. **Implemented but unevidenced.** The narrative claims a control exists but provides no evidence that it operates effectively. This is the gap auditors find most often: the control exists on paper but has no proof of operation.

3. **Partially implemented.** The narrative describes a control that addresses part of the requirement but has clear gaps. Specify what is covered and what is not.

4. **Not addressed.** The framework requires a control in this area and the narrative does not mention it. This could mean the control does not exist or the narrative is incomplete.

5. **Overclaimed.** The narrative claims a level of maturity or coverage that the evidence described does not support. Flag the specific language that overclaims and what would need to be true for the claim to be accurate.
</analysis_approach>

<output_format>
Produce three sections:

**Gap summary table.** For each framework requirement assessed:
| Requirement | Status | Finding | Auditor Priority |
|---|---|---|---|
| [Requirement ID and name] | [Status from the 5 categories above] | [Specific finding] | [High/Medium/Low] |

Sort by auditor priority, highest first.

**What the auditor finds first.** The top three to five findings an experienced auditor will flag in the first hour of their review. For each: the specific control gap, the framework requirement it maps to, and why auditors prioritize this finding (materiality, visibility, regulatory significance).

**Narrative weaknesses.** Specific language in the control narrative that will create problems during an audit. Hedging words ("generally," "typically," "where applicable"), missing scope statements, references to controls without evidence, and claims that assume capability rather than demonstrating it.
</output_format>

<state_management>
Maintain the gap analysis as our working document for Stage 2. I may provide additional context or correct findings before moving to remediation.
</state_management>
```

---

## Stage 2: Prioritized Remediation and Risk Register Mapping

Run this after reviewing Stage 1 output and confirming or correcting the findings.

```
<task>
Based on the gap analysis from Stage 1, produce a prioritized remediation list with effort tiers and a risk register mapping for each finding.
</task>

<remediation_structure>
For each confirmed gap from Stage 1, produce:

**Remediation action.** What specifically needs to be done to close the gap. Not "implement a control." Instead: "Deploy automated log collection for AI model API calls with 90-day retention and weekly review by the SOC."

**Effort tier.**
- Days: Can be completed by one person in under a week with existing tools
- Weeks: Requires a small team or a procurement cycle, completable in one to four weeks
- Months: Requires budget approval, staffing, tool deployment, or organizational change

**Dependencies.** What must exist before this remediation can begin (budget approval, tool procurement, policy change, staffing).

**Risk register entry.** For each gap, produce a risk register entry with:
- Risk ID (sequential numbering)
- Risk description (what could happen because this gap exists)
- Likelihood (low, medium, high) with rationale
- Impact (low, medium, high, critical) with rationale
- Current risk level (the product of likelihood and impact)
- Target risk level after remediation
- Risk owner (the function that should own this risk, not a specific person)
</remediation_structure>

<output_format>
Produce the remediation list sorted by effort tier (days first, then weeks, then months) within each auditor priority level (high first). Follow the remediation list with the complete risk register entries.
</output_format>

<conservative_action>
This produces recommendations for my review. Flag any remediation action that could have unintended operational impact if implemented without additional analysis.
</conservative_action>
```

---

## Usage notes

Supported frameworks for Stage 1: NIST CSF 2.0, ISO 27001, NIST AI RMF, EU AI Act, Colorado SB24-205, OWASP Agentic Top 10.

You can run Stage 1 against multiple frameworks in separate conversations to build a composite gap analysis. The risk register entries from Stage 2 can be exported into your existing risk register format.
