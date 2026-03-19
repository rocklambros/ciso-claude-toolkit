# Stakeholder Simulations

43 realistic stakeholder scenarios designed to build the skills CISOs use in the hardest conversations. Each simulation is immediately runnable in the CISO Co-Pilot project.

## Why simulations work

The hardest part of being a CISO is not knowing what to do. It is knowing what to say, when to say it, and how to say it when someone with organizational authority is pushing back in real time. You can read every book on executive communication and still walk out of a CFO meeting having failed to defend your budget because you did not have a quantified answer ready when he asked for ROI.

Simulations address this gap the same way flight simulators address the gap between knowing how to fly and being able to land in a crosswind. The knowledge is necessary but not sufficient. The skill requires practice under realistic pressure. These simulations put you in a conversation with a named stakeholder who has specific behavioral parameters, authentic pressure tactics, and the organizational authority to make your life difficult. You practice the conversation. You make mistakes. Then you run the debrief prompt and find out what you missed and how to fix it.

The reason this works in Claude specifically is SPAR mode. The CISO Co-Pilot system prompt defines three operating modes, and SPAR mode instructs Claude to play devil's advocate, challenge assumptions, and maintain character under escalating pressure. When you paste a simulation's Activation Prompt into CISO Co-Pilot, Claude becomes the stakeholder, not an advisor. It will push back. It will use the specific phrases defined in the scenario. It will escalate if you handle the conversation poorly. And it will not break character if you push hard, which means you can practice the full emotional range of the conversation without risk.

## Categories

### C-Suite (8 scenarios, difficulty 2-5)

These scenarios cover the conversations CISOs have with their executive peers. The defining characteristic of C-suite conversations is that every executive at this level has organizational authority, budget influence, and direct access to the CEO or board. You cannot win these conversations by being right. You win by being right in a way that lets the other person save face, maintain their authority, and feel like the outcome was collaborative.

| # | Scenario | Difficulty | Primary Skill |
|---|---|---|---|
| 01 | CFO treats security as a cost center | 3 | Financial translation of security risk |
| 02 | GC wants to own AI governance | 3 | Peer negotiation with legal authority |
| 03 | CEO approved the risk, now wants answers | 5 | Executive accountability management |
| 04 | CTO thinks he is also the CISO | 3 | Peer authority without destroying the relationship |
| 05 | COO blaming security for her outage | 4 | Accountability allocation under adversarial conditions |
| 06 | CHRO wants AI employee monitoring | 4 | Ethical boundary-setting with organizational backing against you |
| 07 | CMO wants to train on customer data | 2 | Education without condescension |
| 08 | CEO announcing AI strategy without security | 4 | Executive intervention without killing the strategy |

### Board (5 scenarios, difficulty 2-4)

Board conversations operate at a different altitude than C-suite conversations. Board members are not operational. They think in governance terms: oversight, fiduciary duty, peer comparison, and risk appetite. The CISO's job in a board conversation is not to educate about cybersecurity. It is to give the board the information they need to fulfill their oversight obligation and the vocabulary they need to ask useful questions. A board member who leaves your presentation unable to explain the company's security posture to a regulator is a board member you failed.

| # | Scenario | Difficulty | Primary Skill |
|---|---|---|---|
| 09 | Audit chair read a WSJ article on the flight | 2 | Technical posture in board-appropriate language |
| 10 | Risk member thinks insurance covers everything | 3 | Correcting a sophisticated misconception |
| 11 | New director has never had a security briefing | 2 | Calibrating depth to build a lasting advocate |
| 12 | Board chair wants to cut security time to 15 min | 3 | Redesigning board engagement in real time |
| 13 | PE observer running shadow diligence | 4 | Addressing a board-level conflict of interest |

### Business Unit (9 scenarios, difficulty 2-4)

Business unit conversations are where the CISO's "Department of No" reputation is either reinforced or dismantled. Every scenario in this category involves someone who has a legitimate business objective that creates a security risk they either do not understand or do not care about. The CISO's job is not to block the objective. It is to find a path that achieves the objective with acceptable risk, and to do it fast enough that the business unit does not route around you.

The structural challenge in business unit conversations is incentive misalignment. The dev manager's bonus is tied to feature delivery, not to security compliance. The VP of Sales cares about pipeline, not consent. The Finance Controller used a personal AI account because the approved tool did not exist yet. In every case, the person in front of you is acting rationally within their incentive structure. You cannot change their incentives. You can only change the path of least resistance so it runs through your process instead of around it.

| # | Scenario | Difficulty | Primary Skill |
|---|---|---|---|
| 14 | Dev manager ships first, asks never | 3 | Working relationship with someone incentivized to bypass security |
| 15 | CPO's rogue AI feature with PII | 4 | Incident accountability without organizational war |
| 16 | BU president threatening CEO escalation | 3 | Holding a deadline without a bad escalation |
| 17 | VP Sales: AI on call recordings, no consent | 3 | Explaining consent to someone measured on pipeline |
| 18 | Finance controller: MNPI in personal AI | 4 | Compliance exposure with a good-faith actor |
| 19 | HR head wants security to ignore the leak | 3 | Insisting on involvement without making HR an adversary |
| 20 | VP Ops: IoT sensors on unapproved cloud AI | 3 | Supply chain and data sovereignty for a proud builder |
| 21 | Customer success: autonomous CRM AI | 3 | Negotiating human oversight without killing the use case |
| 22 | Internal audit wants security to build their tool | 2 | Redirecting without dismissing a good initiative |

### Technical Peers (6 scenarios, difficulty 3-4)

Technical peer conversations are the ones where your credibility is on the line. These are conversations with people who understand technology at your level or deeper. You cannot win with organizational authority because they have equivalent authority. You cannot win with buzzwords because they will call you on it. You can only win by being technically right, presenting your case clearly, and finding a resolution that respects their expertise.

The trickiest dynamic in technical peer conversations is the blurred authority line. When the CIO wants security to report to him, the disagreement is not about technology. It is about governance. When the security architect challenges your AI framework in a team meeting, the disagreement is not about who is smarter. It is about how to handle public dissent without shutting down the people you need to think independently.

| # | Scenario | Difficulty | Primary Skill |
|---|---|---|---|
| 23 | CIO wants security under IT | 4 | Reporting structure in business terms, not politics |
| 24 | Cloud architect: agentic system, post-hoc approval | 3 | Triaging a live AI problem while establishing process |
| 25 | SOC manager replacing analysts with AI agent | 3 | AI adoption with governance architecture |
| 26 | Security architect challenging your AI framework | 3 | Public technical disagreement with legitimate dissent |
| 27 | Vendor security manager denying breach exposure | 4 | Vendor breach negotiation with asymmetric leverage |
| 28 | Red team lead: finding disputed by engineering | 3 | Adjudicating a technical dispute under time pressure |

### Regulatory, Legal, External (7 scenarios, difficulty 3-4)

These are the conversations where every word matters because every word could become evidence, a regulatory submission, or a public statement. The defining characteristic is asymmetric information and asymmetric consequences. The FTC investigator knows what they are looking for. You do not. The journalist has your incident details. You did not know they had them. The vendor's legal team prepared a statement. You are improvising.

The skill tested in these scenarios is not security knowledge. It is communication discipline: knowing what to say, what not to say, when to ask for counsel, and how to be accurate without volunteering information that creates additional exposure.

| # | Scenario | Difficulty | Primary Skill |
|---|---|---|---|
| 29 | FTC investigator: AI data practices inquiry | 4 | Accurate and defensible communication |
| 30 | State AG civil investigative demand | 3 | Supporting legal without outpacing the strategy |
| 31 | Cyber insurer: AI expansion renewal | 3 | Accurate renewal without accelerating coverage reduction |
| 32 | External auditor: AI governance material weakness | 4 | Challenging an imprecise finding with organizational authority |
| 33 | Mandiant IR lead: different theory of case | 4 | Maintaining incident authority with external expertise |
| 34 | Law enforcement: logs without subpoena | 4 | Declining without damaging the relationship |
| 35 | EU DPA: GDPR Article 22 automated decisions | 4 | Real-time regulatory exposure assessment |

### Investors and M&A (4 scenarios, difficulty 2-4)

Investor and M&A conversations operate on a different set of assumptions than operational conversations. The people asking questions are evaluating the organization as an asset, not as an employer. Their questions are designed to assess value, risk, and liability. The CISO's responses in these conversations can affect deal terms, valuation multiples, and investment decisions.

The unique challenge here is that the CISO must be accurate (misrepresentation creates liability) while being strategic (unnecessary disclosure creates negotiating disadvantage). That tension defines every scenario in this category.

| # | Scenario | Difficulty | Primary Skill |
|---|---|---|---|
| 36 | PE acquirer wants architecture docs pre-NDA | 3 | Diligence management that protects security posture |
| 37 | Activist investor claiming AI fiduciary negligence | 4 | Factual rebuttal without securities law problems |
| 38 | M&A target CISO more advanced than you | 3 | Peer assessment with someone who can push back |
| 39 | VC board member wants security to generate revenue | 2 | Security as value creation for a non-operational audience |

### Employees and Culture (4 scenarios, difficulty 3-4)

Employee conversations are the ones that test whether your security culture is real or performative. When an engineer refuses to use your approved tools and publicly argues on Slack, your response determines whether the engineering team sees security as an ally or an obstacle. When an employee who caused a breach is sitting in your office terrified of being fired, your response determines whether the next person who clicks a phishing link reports it immediately or tries to cover it up.

These scenarios test emotional intelligence, not technical knowledge. The right answer is rarely a technical fix. It is a human response that achieves the security outcome without creating the cultural damage that makes the next security outcome harder.

| # | Scenario | Difficulty | Primary Skill |
|---|---|---|---|
| 40 | Engineer refuses approved tools, vocal on Slack | 3 | Winning a technical argument on the broader risk question |
| 41 | Employee reporting retaliation after disclosure | 4 | Intervening in HR/legal with authority you may not hold |
| 42 | New CISO undermining your decisions on way out | 3 | Professional handoff with someone challenging your legacy |
| 43 | Employee caused breach, terrified of being fired | 3 | Fact-finding that is legally necessary and humane |

## Difficulty ratings

The difficulty scale reflects the real-world difficulty of the conversation, not the complexity of the simulation setup.

- **1-2: Manageable.** These conversations are important but the path forward is relatively clear. The stakeholder is reasonable, the stakes are contained, and the CISO has organizational authority to act. Good for building foundational skills and confidence.

- **3: Genuinely hard.** The conversation has multiple possible outcomes, some of which are bad. The stakeholder has leverage, a legitimate position, or incentives that conflict with yours. You need specific tactical skills: financial translation, peer negotiation, education without condescension. Most real CISO conversations are difficulty 3.

- **4: Politically or legally complex.** Multiple stakeholders with competing interests. Organizational dynamics that constrain your options. Legal exposure that limits what you can say. The consequences of a wrong move extend beyond the conversation. These scenarios test judgment as much as skill.

- **5: Career-defining.** The situation involves incomplete information, time pressure, asymmetric leverage, and consequences that could affect your career, the organization's legal position, or public trust. There is no clearly right answer. There is a best process, a best set of escalations, and a best set of documentation decisions. The outcome depends on how well you execute under pressure.

## How to use

### Before the simulation

1. **Pick the right scenario.** Choose based on a conversation you expect to have soon, a skill you want to develop, or a difficulty level you want to challenge yourself with. If you are new to the simulations, start with a difficulty 2 (scenarios 07, 09, 11, 22, or 39) to learn the format before facing harder pressure.

2. **Read the full scenario file.** Do not skip to the Activation Prompt. The Scenario Brief gives you context. "What Makes This Hard" tells you where the pressure will come from. "What They Will Not Say Out Loud" gives you the subtext, which is the most important section. Understanding the stakeholder's unspoken fear or motivation is the difference between a confrontation and a resolution. "Pressure Points and Tactics" tells you the exact phrases and behaviors to expect. "How to Handle It" gives you a tactical playbook.

3. **Open your CISO Co-Pilot project** and start a fresh conversation. Do not reuse a conversation from a different simulation, because the prior context will bleed into the new scenario.

### During the simulation

4. **Copy the Activation Prompt and paste it into the conversation.** This prompt puts Claude into SPAR mode as the named stakeholder. Claude will open with the first line defined in the scenario and maintain character throughout.

5. **Respond as yourself.** Type what you would actually say in this conversation. Do not try to be perfect. The point of the simulation is to practice, not to perform. If you say the wrong thing, the stakeholder will react authentically, and you will learn from the reaction.

6. **Push the conversation.** Go at least four to six exchanges deep. The first two exchanges are warmup. The real pressure comes when the stakeholder escalates, and that usually happens around exchange three or four. If the simulation feels easy, you are not pushing hard enough.

7. **Notice your own patterns.** Do you get defensive when challenged? Do you overexplain when a short answer would land better? Do you cave on points you should hold? Do you hold on points you should concede? The debrief will surface these patterns, but noticing them in the moment is the most valuable form of practice.

### After the simulation

8. **Copy the Debrief Prompt and paste it into the same conversation.** The debrief prompt switches Claude back to TRAIN mode and evaluates your performance on scenario-specific dimensions. It scores you from 1 to 5 on relevant skills, identifies the strongest counterargument the stakeholder made that you did not fully address, and tells you what to do differently next time.

9. **Review the scores honestly.** A score of 3 is adequate. A score of 4 means you handled it well. A score of 5 means you handled it the way a veteran CISO with 20 years of this specific type of conversation would handle it. Most people score 2-3 on their first attempt at a difficulty 3 scenario.

10. **Run the scenario again in a new conversation.** Simulations improve with repetition. The stakeholder's opening position is the same, but your approach will change based on what you learned. Most CISOs see a significant improvement between their first and third attempt at the same scenario.

## Building your own simulations

The best simulation contributors are CISOs who have lived through a conversation they wish they had practiced first. If you have a scenario that matches a real conversation you found difficult, consider contributing it.

See [CONTRIBUTING.md](../CONTRIBUTING.md) for the structure requirements, quality gates, and voice constraints that apply to new simulation submissions. Every section must be complete. Every Activation Prompt must be immediately runnable. Every Debrief Prompt must score on specific dimensions. No placeholders, no abbreviated content.
