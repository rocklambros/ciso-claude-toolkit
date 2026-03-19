# High-Difficulty Scenarios

7 crisis decision-making scenarios at difficulty 4 and 5. These are not stakeholder simulations. The pressure is situational, not conversational. The CISO must make real-time decisions with incomplete information, time constraints, and consequences that extend beyond the immediate moment.

## How these differ from stakeholder simulations

Stakeholder simulations test communication skills: how you handle a person with specific motivations, pressure tactics, and organizational authority. The stakeholder is the challenge.

High-difficulty scenarios test decision-making skills: how you make choices when the facts are incomplete, the clock is running, the consequences are severe, and there is no clearly right answer. The situation is the challenge. There may be stakeholders involved (a journalist on the phone, a regulator asking questions, an outgoing CEO moving data), but the core difficulty is not the conversation. It is the decision.

The distinction matters because different skills are required. Stakeholder simulations require emotional intelligence, communication discipline, and political awareness. High-difficulty scenarios require risk assessment under uncertainty, escalation judgment, evidence preservation instincts, and the ability to make a defensible decision with 60% of the information you need while knowing that waiting for the other 40% will make the situation worse.

## When to use these

**For practice.** Run these in CISO Co-Pilot in TRAIN mode before you face the real thing. The model will walk you through each decision point, present options with risks, and push back on choices that have second-order consequences you might miss.

**For real-time support.** If you are in the middle of a crisis that resembles one of these scenarios, run it in SUPPORT mode. Paste the scenario context plus your actual facts, and the model will help you think through the decision points structured for your specific situation.

**For team training.** Run a scenario in a team meeting. Present the "What Just Happened" section and the "What You Know" section. Ask your team to work through the decision points as a group. Compare their approach to "What Good Looks Like" at the end. This is particularly effective for developing decision-making instincts in your deputies and senior analysts.

## Scenarios

| # | Scenario | Difficulty | Decision Type | Time Pressure | Core Tension |
|---|---|---|---|---|---|
| 44 | Peer CISO lateral movement disclosure | 5 | Crisis / Legal | Real-time | You have insider knowledge from a peer. Acting on it reveals the source. Not acting on it exposes the company. |
| 45 | CEO wants to market program before it is ready | 4 | Political / Ethical | Days | The program has open critical findings. The claims are aspirational. The CEO does not see the distinction. |
| 46 | Board member wants briefing for portfolio company | 4 | Ethical / Political | Hours | A reasonable-sounding request that is actually a conflict of interest and IP disclosure issue. |
| 47 | Journalist has accurate undisclosed incident info | 5 | Crisis / Legal | 45 minutes | The journalist knows what happened. Legal is not available. Everything you say could become a quote. |
| 48 | AI vendor blaming your prompts for discriminatory output | 4 | Technical / Legal | Hours | The vendor has lawyers and a technical argument. You have logs. The feature is still live and causing harm. |
| 49 | Regulator calls directly bypassing legal | 5 | Legal / Political | Real-time | An informal call that could become formal evidence. Legal does not know it is happening. |
| 50 | Outgoing CEO exfiltrating data on last day | 5 | Crisis / Legal / Ethical | Real-time | The most senior person in the organization is moving data. His assistant says it is authorized. The board chair is unreachable. |

## File structure

Every scenario follows an identical structure designed to present the situation the way it actually arrives: incomplete, ambiguous, and without tidy framing.

**What Just Happened.** The situation as the CISO experiences it. Not a clean briefing. A messy, partial picture that mirrors how crises actually begin. You learn about the journalist's call from your admin. You see the data exfiltration alert in a Slack message from your SOC analyst. You get a call from a peer CISO who says "I need to tell you something, and I do not have much time."

**What You Know.** Confirmed facts only, in bullet format. These are the things you can act on with confidence. The list is always shorter than you want it to be.

**What You Do Not Know.** The critical unknowns that make the decision hard. This section is the core of every scenario. If you knew everything in this section, the decision would be straightforward. You do not know it, and you have to decide anyway.

**Why This Is Harder Than It Looks.** The hidden complexity, the second-order effects, the political landmines, and the things most CISOs miss the first time they face this type of situation. This section is the educational content. It explains why experienced CISOs handle these situations differently from first-timers, and what the first-timers typically get wrong.

**The Decision Points.** Two to four specific decisions that must be made, in the order they must be made. The decisions are concrete: "Do you throttle the data transfer, block it completely, or allow it to continue while you investigate?" Not abstract: "Consider the implications."

**How to Run This in CISO Co-Pilot.** The exact prompt to paste into your CISO Co-Pilot project. The prompt provides the scenario context and instructs Claude to help you think through each decision point with options, risks, and a recommendation. The model will present the trade-offs, ask what you want to do, and then surface the consequences you might not have considered.

**What Good Looks Like.** The outcome a strong CISO produces. Not a perfect answer, because there is no perfect answer in a difficulty 5 scenario. Instead, this section describes the right process, the right escalations, the right documentation, and the right organizational outcome. It is the benchmark you evaluate yourself against after running the scenario.

## How to get the most out of these scenarios

**First pass: react.** Read the "What Just Happened" and "What You Know" sections. Stop. Write down what you would do in the next 30 minutes. Do not read ahead. Your instinctive reaction is the baseline you are training from.

**Second pass: analyze.** Read "What You Do Not Know" and "Why This Is Harder Than It Looks." Compare your instinctive reaction to the complexity you just learned about. Most CISOs find that their first reaction missed at least one critical dimension.

**Third pass: practice.** Paste the prompt into CISO Co-Pilot and work through the decision points with the model. The model will push back on choices that have problematic consequences and surface options you did not consider.

**Fourth pass: evaluate.** Compare your approach to "What Good Looks Like." Identify the gaps. The gaps are your development areas.

**For recurring practice,** run the same scenario again in two weeks. The situation is the same, but your decision-making will be faster and more complete. Track your improvement across attempts.

## A note on difficulty 5

The four difficulty 5 scenarios in this directory (44, 47, 49, and 50) represent situations where there is no good outcome, only less-bad outcomes. The journalist will publish the story regardless of what you say. The outgoing CEO may have authorization you cannot verify. The regulator's informal call may already be part of an investigation.

In these scenarios, the CISO's job is not to solve the problem. It is to make the best decision available with the information available in the time available, and to document that decision so it is defensible later. "What Good Looks Like" in a difficulty 5 scenario is not a win. It is a situation where the organization's exposure is minimized, the right people were notified, the evidence was preserved, and the CISO can explain their reasoning to the board, to regulators, or to outside counsel after the fact.
