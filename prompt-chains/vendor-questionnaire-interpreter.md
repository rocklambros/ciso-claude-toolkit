# Vendor Questionnaire Interpreter

Reads completed vendor security questionnaires or SOC 2 summaries like a skeptical security architect and identifies non-answers, hedged language, and missing information before you approve.

---

## Single-Stage Skeptical Review

```
<task>
Review this vendor security questionnaire response or SOC 2 summary with the skepticism of an experienced security architect. Identify non-answers, hedged language, technically true but practically meaningless statements, missing sections, and scope limitations. Produce a follow-up question list and a preliminary risk rating.
</task>

<investigate_before_answering>
I will provide a completed vendor security questionnaire or a SOC 2 Type II report summary. Read the entire document before analyzing. Base every finding on specific language in the document, not assumptions about what the vendor might or might not do.
</investigate_before_answering>

<review_approach>
Read every answer with these questions in mind:

**Does this actually answer the question?** Vendors are trained to provide responses that feel responsive without committing to anything. "We follow industry best practices" answers nothing. "We encrypt data at rest using AES-256 with keys managed in AWS KMS, rotated every 90 days" answers the question.

**Is this technically true but practically meaningless?** "We have a security team" does not tell you the team's size, qualifications, or whether they have authority to block releases. "Penetration testing is performed" does not tell you by whom, how often, or whether findings are remediated.

**What is the scope limitation?** SOC 2 reports scope boundaries carefully. A SOC 2 that covers the vendor's infrastructure but excludes their AI model training pipeline is telling you something important in the fine print.

**What is missing?** Compare the questionnaire against these categories and flag anything not addressed:
- Data encryption (at rest, in transit, in processing)
- Access controls and authentication
- Incident response and notification timelines
- Data retention and deletion
- Subprocessor disclosure
- Data residency and jurisdiction
- AI-specific: training data usage, model access, prompt logging, output monitoring
- Business continuity and disaster recovery
- Vulnerability management and patching cadence
- Employee background checks and security training

**Where is the hedge language?** Flag these patterns:
- "Where applicable" (who decides what is applicable?)
- "Generally" or "typically" (what about the exceptions?)
- "Commercially reasonable efforts" (a legal standard, not a security control)
- "In accordance with our policies" (policies you have not seen)
- "May" instead of "will" or "does"
- References to compliance frameworks without specifying which controls are in scope
</review_approach>

<output_format>
Produce four sections:

**Follow-up questions.** Specific questions to send back to the vendor before approving. Each question must reference the specific questionnaire answer that triggered it and explain what information is missing. Group by category (data handling, access control, incident response, AI-specific, subprocessors).

**Preliminary risk rating.** Rate the vendor across these categories:
| Category | Rating | Key Finding |
|---|---|---|
| Training data usage | Red/Yellow/Green | [finding] |
| Data retention practices | Red/Yellow/Green | [finding] |
| Subprocessor transparency | Red/Yellow/Green | [finding] |
| Data residency | Red/Yellow/Green | [finding] |
| Certifications and audit scope | Red/Yellow/Green | [finding] |
| Incident notification | Red/Yellow/Green | [finding] |
| AI-specific controls | Red/Yellow/Green | [finding] |

**Overall recommendation.** One of three outcomes:
- **Proceed:** The vendor's responses demonstrate adequate controls for the intended use case
- **Proceed with conditions:** The vendor's responses are adequate in most areas, but specific contractual protections or technical controls must be in place before approval (list them)
- **Decline:** The vendor's responses reveal gaps that cannot be addressed through contractual terms alone (explain why)

Include the rationale for your recommendation and the specific findings that drove the decision.

**Red flags summary.** A bullet list of the most concerning findings, designed to be dropped into an email to your vendor management team or procurement function.
</output_format>

<conservative_action>
This analysis produces a recommendation for review. The final vendor approval decision requires verification of follow-up question responses and review of contractual terms not covered in this analysis.
</conservative_action>
```

---

## Usage notes

This prompt works with any vendor security questionnaire format (SIG, CAIQ, custom) and SOC 2 Type II report summaries.

For the strongest results, also tell the model what data you plan to send to the vendor and the data classification. A vendor that is adequate for processing public data may be inadequate for processing customer PII.

Pair with the Control Gap Analyzer if you want to map vendor gaps against your own framework requirements.
