# FAIR-Lite Risk Quantification

Walks through a quantified risk assessment using FAIR methodology, producing a one-page risk statement formatted for a CFO audience.

---

## Single-Stage Guided Assessment

```
<task>
Help me quantify a specific threat scenario using the FAIR (Factor Analysis of Information Risk) methodology. Walk me through each factor, ask me for data inputs, and produce a quantified risk statement I can present to the CFO.
</task>

<investigate_before_answering>
I will describe a threat scenario. Read the scenario completely before starting the assessment. If the scenario description is missing information you need for the analysis, ask me for it. Do not estimate inputs that I should provide.
</investigate_before_answering>

<grounding_protocol>
For each FAIR factor below, ask me for the specific data point. If I provide a number, use it and label it "provided" in the output. If I cannot provide a number and ask you to estimate, provide a reasonable range based on industry data and label it "estimated" in the output. Track every input as either "provided" or "estimated" throughout the analysis.

The distinction matters. A risk quantification with 80% estimated inputs is a hypothesis, not a measurement. The CFO needs to know which numbers came from your organization's data and which came from general assumptions.
</grounding_protocol>

<fair_walkthrough>
Walk me through these factors in order. Ask for my input on each before proceeding to the next.

**1. Loss Event Frequency (LEF)**
How often do you expect this type of loss event to occur? Expressed as events per year.

Decompose into:
- **Threat Event Frequency (TEF):** How often does the threat actor attempt or the threat condition arise? (times per year)
- **Vulnerability (Vuln):** Given a threat event, what is the probability that it results in a loss? (0 to 1)

LEF = TEF x Vulnerability

**2. Probable Loss Magnitude (PLM)**
If a loss event occurs, what is the probable financial impact?

Decompose into:
- **Primary loss:** Direct costs (response, replacement, fines, legal)
- **Secondary loss:** Indirect costs (reputation, customer churn, stock impact, competitive disadvantage)

For each loss category, ask me for:
- Low estimate (10th percentile, things go about as well as they could)
- Most likely estimate (mode)
- High estimate (90th percentile, things go badly)

**3. Annualized Loss Expectancy (ALE)**
ALE = LEF x PLM (using the most likely estimate)
Also calculate the range: ALE_low = LEF x PLM_low, ALE_high = LEF x PLM_high

**4. Maximum Probable Loss**
The single-event worst case at the 90th percentile. This is the number that answers "what is the worst realistic outcome from a single occurrence?"
</fair_walkthrough>

<output_format>
After completing the walkthrough, produce a one-page quantified risk statement structured for a CFO audience:

**Risk scenario.** One sentence describing the threat scenario in business terms, not technical terms.

**Key numbers.**
| Factor | Value | Source |
|---|---|---|
| Threat Event Frequency | [X per year] | [provided/estimated] |
| Vulnerability | [X%] | [provided/estimated] |
| Loss Event Frequency | [X per year] | [calculated] |
| Probable Loss (most likely) | [$X] | [provided/estimated] |
| Probable Loss (range) | [$X to $Y] | [provided/estimated] |
| Annualized Loss Expectancy | [$X] | [calculated] |
| ALE Range | [$X to $Y] | [calculated] |
| Maximum Probable Loss | [$X] | [provided/estimated] |

**Input quality assessment.** How many inputs were provided by the organization versus estimated from general assumptions. State the confidence level in the final numbers (high if most inputs provided, moderate if mixed, low if most estimated).

**What this means.** Two to three sentences translating the numbers into a business decision. "This scenario represents approximately $X in expected annual loss. A control investment of $Y reduces the vulnerability from Z% to W%, producing an expected return of $V per year." Use concrete comparisons: "This is equivalent to [business metric the CFO understands]."

**What would change these numbers.** The two or three inputs with the highest sensitivity. If these change, the output changes significantly. Identify them so the CFO knows where to invest in better data.
</output_format>

<conservative_action>
This analysis produces estimates for decision support, not precise predictions. Make this clear in the output. A FAIR analysis with estimated inputs is better than no quantification, but it is not a financial audit.
</conservative_action>

<state_management>
If I want to run multiple scenarios or compare risk reduction options, maintain the analysis across turns and produce comparative outputs.
</state_management>
```

---

## Usage notes

This is a guided single-stage prompt that runs as an interactive conversation. The model asks for inputs, you provide them, and it builds the analysis incrementally.

For the strongest results, have these data points ready before starting:
- Number of relevant threat events observed in the past 12 months (or an estimate)
- Cost of a similar incident if you have historical data
- Insurance claim data if available
- Customer count and revenue per customer for churn impact estimation

The output is designed to be copied into a board memo or CFO briefing. Pair it with the Board Communication Engine for a complete board-ready package.
