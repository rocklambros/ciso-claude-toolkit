# Red Team Your AI Governance

Attacks your AI acceptable use policy, governance framework, or risk register from three angles simultaneously: regulatory, adversarial, and organizational exploitability.

---

## Single-Stage Comprehensive Assessment

```
<task>
Red team my AI governance documentation. Attack it from three perspectives simultaneously and produce a prioritized gap list with specific remediation language.
</task>

<investigate_before_answering>
I will provide one of the following:
- An AI acceptable use policy
- An AI governance framework document
- An AI risk register

Read the entire document before starting the assessment. Base your analysis on what the document actually says, not what you assume it says. If a topic is not addressed, that is a finding. If a topic is addressed vaguely, that is a different finding. Distinguish between the two.
</investigate_before_answering>

<attack_perspectives>

**Perspective 1: What a regulator finds**
Review through the lens of EU AI Act, NIST AI RMF, and Colorado SB24-205. For each framework, identify:
- Requirements the document does not address at all
- Requirements the document addresses with language too vague to satisfy a regulator
- Requirements where the document's stated controls would not produce the evidence a regulator expects
- Definitions that are missing or insufficiently precise (what counts as "AI," what counts as "high-risk," what counts as "automated decision-making")

**Perspective 2: What an attacker finds**
Review through the OWASP Top 10 for Agentic Applications lens. For each applicable risk category, identify:
- Attack surfaces the document does not acknowledge
- Controls that address traditional software risks but miss AI-specific attack vectors
- Assumptions about AI system behavior that an attacker would exploit (trust assumptions, data boundary assumptions, output validation gaps)
- Missing controls for: prompt injection, tool impersonation, data poisoning, model manipulation, excessive agency, and supply chain compromise

**Perspective 3: What employees will exploit**
Review through the lens of organizational behavior and enforceability. For each policy requirement, assess:
- Is this enforceable with existing tools and processes?
- Is the consequence for violation stated and proportional?
- Does this requirement conflict with employee incentives or productivity expectations?
- Where will employees route around this policy because compliance is harder than circumvention?
- What shadow AI behaviors does this policy unintentionally encourage by making governed paths too restrictive?
</attack_perspectives>

<output_format>
Produce three outputs:

**Prioritized gap list.** Every finding sorted by severity (critical, high, medium, low). For each finding:
| # | Severity | Perspective | Gap Description | Policy Language Creating the Gap | Recommended Fix |
|---|---|---|---|---|---|

**Top 5 exposures.** The five findings that create the most risk for the organization, with a paragraph explaining why each one matters and what the worst realistic outcome is if it remains unaddressed.

**Recommended remediation language.** For each critical and high finding, provide the specific policy language that should replace or supplement the current text. Write the language so it can be dropped into the document with minimal editing.
</output_format>

<conservative_action>
This analysis produces recommendations for review. Policy language changes should go through your legal and governance review process before adoption.
</conservative_action>
```

---

## Usage notes

This prompt works best with a complete policy or framework document. Fragments or outlines will produce surface-level findings.

Run this assessment quarterly or whenever you make significant changes to your AI governance documentation. The regulatory landscape is changing fast enough that a policy current six months ago may have gaps today.

For the strongest results, also provide: a list of AI tools currently approved in your organization, the number of employees using AI tools, and any known shadow AI findings from access log reviews.
