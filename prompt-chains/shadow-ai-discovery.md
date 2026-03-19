# Shadow AI Discovery

Triages access logs, expense data, SaaS usage data, or browser proxy logs to identify shadow AI usage patterns and produce a prioritized risk assessment with response strategy.

---

## Single-Stage Triage and Response

```
<task>
Help me identify shadow AI usage patterns from organizational data and produce a prioritized finding list with a response strategy that moves employees toward governed tools.
</task>

<investigate_before_answering>
I will provide one or more of these data sources:
- Access logs (web proxy, firewall, or DNS logs showing outbound connections)
- Expense report summaries (credit card charges or reimbursement requests)
- SaaS usage data (SSO logs, CASB reports, or shadow IT discovery tool output)
- Browser proxy log summaries

Read the data completely before analyzing. If the data contains PII (employee names, email addresses, personal identifiers), flag this immediately and recommend I scrub PII before continuing the analysis. I should be working with role-based or department-level data, not individual identifiers, unless this is an active investigation with HR and legal involvement.
</investigate_before_answering>

<pii_warning>
If the submitted data contains personally identifiable information about employees, stop the analysis and tell me. Shadow AI discovery should use aggregated or anonymized data unless legal and HR have approved an individual-level investigation. Processing employee PII through an external AI tool to detect shadow AI use would be ironic and potentially create its own compliance problem.
</pii_warning>

<triage_logic>
Analyze the data for these pattern categories:

**AI service connections.** Domains and services associated with AI tools: OpenAI, Anthropic, Google AI, Midjourney, Stability AI, Hugging Face, Replicate, and other known AI service endpoints. Distinguish between browser-based access (chat interfaces) and API access (programmatic usage, higher risk).

**Expense indicators.** Charges to AI services, credit card transactions matching AI vendor names, reimbursement requests for AI subscriptions. Individual subscriptions suggest the approved tools are insufficient or inaccessible.

**Usage volume and pattern.** Frequency, time of day, data volume transferred. High-volume API access during business hours with significant upload sizes suggests operational data processing, not casual exploration.

**Department concentration.** Which teams or functions show the highest shadow AI activity. Concentration in specific departments suggests unmet needs rather than random individual behavior.

**Data risk tiering.** Based on the department and usage pattern, assess the likely data classification involved:
- Low risk: Marketing teams using AI for content drafting with public information
- Medium risk: Engineering teams using AI for code assistance with proprietary code
- High risk: Finance, HR, or legal teams processing confidential or regulated data
- Critical risk: Any team processing customer PII, MNPI, health data, or trade secrets through unapproved tools
</triage_logic>

<output_format>
Produce three sections:

**Prioritized finding list.** Sorted by data risk tier (critical first). For each finding:
- What was observed (service, pattern, volume)
- Which department or function
- Likely data classification involved
- Risk assessment (what could go wrong)
- Urgency (address immediately, address this week, address this quarter)

**Root cause assessment.** Why are employees using shadow AI tools? Evaluate whether:
- Approved tools are missing capabilities employees need
- Approved tool access is too slow or bureaucratic
- Employees do not know approved tools exist
- Approved tools have usage restrictions that do not match workflow needs
- No AI acceptable use policy exists or the existing policy is unclear

**Response strategy.** A phased approach that moves employees toward governed tools without creating a punitive culture that drives shadow AI further underground:

Phase 1 (this week): Address critical-risk findings with direct outreach
Phase 2 (this month): Close the gap between what employees need and what approved tools provide
Phase 3 (this quarter): Implement monitoring and a reporting mechanism for new AI tool requests
Phase 4 (ongoing): Quarterly shadow AI reviews using the same data sources

For each phase, specify the actions, the owner (security, IT, business unit, HR), and the success metric.
</output_format>

<conservative_action>
This analysis produces recommendations. Do not implement blocking, monitoring changes, or employee communications without HR and legal review. Shadow AI discovery that becomes perceived as surveillance will damage the security function's relationship with the business.
</conservative_action>
```

---

## Usage notes

Scrub PII from submitted data before running this analysis unless you have explicit HR and legal approval for individual-level investigation.

Run this quarterly. Shadow AI adoption accelerates faster than most security teams expect. A clean finding in Q1 does not mean Q2 will be clean.

Pair the findings with the Board Communication Engine if shadow AI activity is significant enough to warrant board-level discussion.
