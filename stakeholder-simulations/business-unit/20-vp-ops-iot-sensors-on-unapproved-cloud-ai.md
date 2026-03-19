# VP of Operations Deployed IoT Sensors on Unapproved Cloud AI

**Category:** Business Unit
**Difficulty:** 3 — Technical risk with a proud stakeholder
**Primary Skill Tested:** Explaining supply chain and data sovereignty risk to someone who is proud of what he built
**Frameworks Activated:** Pillar 1 (Foundational Business Knowledge), Pillar 3 (Cybersecurity Leadership), Pillar 4 (AI and Agentic Security), data sovereignty, third-party risk management, shadow IT, IoT security, GDPR

## Scenario Brief

The VP of Operations deployed 200 IoT sensors on the manufacturing floor six months ago. The sensors measure temperature, humidity, vibration, and throughput data. They connect over your corporate network to a cloud-based AI platform that analyzes the data and produces efficiency recommendations. He did not go through procurement, IT, or security. He used his operational budget and worked directly with the vendor.

The results are impressive. He has reduced downtime by 18% and cut energy costs by 12%. He has a slide deck with charts. The CFO has seen the numbers. The VP is presenting the project as a model for operational innovation at the next leadership offsite.

The problem: the sensors are on your network, and you just found them during a routine scan. The cloud AI platform has no Data Processing Agreement. The vendor is headquartered in a jurisdiction with weak data protection laws and no adequacy agreement with the EU or the US. The sensors transmit data continuously, and the data stream includes timestamps, employee badge proximity data, and machine identifiers that could be cross-referenced with production schedules and personnel assignments. He thinks the sensors just measure temperature and throughput. They measure significantly more than that.

## What Makes This Hard

- He has results. Real, measurable, CFO-validated results. You are about to tell someone his success story has a problem.
- The sensors are already deployed and integrated into operations. Ripping them out disrupts a process that is saving the company money.
- He did not know he needed to involve security. He genuinely believes sensors that measure temperature are not a security concern.
- The data the sensors collect is more extensive than he realizes. Explaining this without sounding like you are accusing him of surveillance is delicate.
- The cloud platform's jurisdictional issues create a data sovereignty problem that is invisible to someone who has never thought about where data is stored.
- He has CFO backing based on the efficiency numbers. You are fighting momentum.

## What They Will Not Say Out Loud

He is proud of this project. It is the best thing he has delivered in two years and he built it without asking anyone for permission, which in his mind is a feature, not a bug. He is terrified that security is going to shut it down or slow it down with a review process that takes months. He does not understand the data sovereignty issue and he does not want to understand it because understanding it means his project has a flaw. If you can show him a way to keep the operational benefits while fixing the security and data problems, he will cooperate. If you position this as "you should have asked permission," he will go to the CFO and make this a turf war.

## Pressure Points and Tactics

- "These are temperature sensors. They are not collecting anything sensitive."
- "I have been running this for six months with zero issues."
- "The CFO has seen the ROI. He is presenting this at the board meeting next month."
- "I used my own budget. I did not need IT approval for operational equipment."
- "You are going to shut down a project that saves us $2 million a year because of a form I did not fill out?"
- "The vendor assured me the platform is secure. They have a SOC 2 report."
- He crosses his arms. He is defensive from the moment you mention the sensors.

## How to Handle It

1. Lead with the results. "I saw the efficiency numbers. An 18% reduction in downtime is significant. I am not here to shut this down. I am here to make sure it survives the scrutiny it is about to get."

2. Show him what the sensors actually collect. "The sensors collect more than temperature and throughput. The data stream includes employee badge proximity data, timestamps, and machine identifiers. When you combine those, you can reconstruct who was working on which machine at what time. That is employee monitoring data, and it changes the legal and privacy picture."

3. Explain the data sovereignty problem in business terms. "The cloud platform stores and processes this data in a jurisdiction with no data protection agreement with the US or the EU. If any of our customers, suppliers, or regulators ask where our operational data is processed, the answer right now is 'we do not know, and we have no contract controlling it.' That is a problem for the CFO's board presentation, not just for security."

4. Address the SOC 2 claim. "A SOC 2 report tells you the vendor has controls around their infrastructure. It does not tell you where your data goes, who can access it, or what happens to it if the vendor is acquired or subpoenaed by a foreign government. We need a Data Processing Agreement that answers those questions."

5. Propose a path that preserves the project. "Here is what I want to do. Let me work with your vendor to get a DPA in place, segment the sensor traffic onto a dedicated network so it is not commingled with corporate systems, and review what data the sensors are actually transmitting so we can turn off what we do not need. The operational benefits stay. The risk goes down. And when this goes to the board, the story is that Operations innovated and security hardened it. That is a better story than Operations deployed sensors nobody knew about."

## Activation Prompt

```
Switch to SPAR mode. You are the VP of Operations at a manufacturing company ($500M revenue, 3 facilities, 2,000 employees). Your name is Dave. You have been VP of Operations for 7 years. You came up through plant management.

Six months ago, you deployed 200 IoT sensors on the manufacturing floor. You worked directly with the vendor, used your operational budget, and did not involve IT or security. The sensors measure temperature, humidity, vibration, and throughput. The data goes to a cloud AI platform that produces efficiency recommendations. You have reduced downtime by 18% and energy costs by 12%. The CFO has seen the numbers and is impressed.

The CISO just requested a meeting about the sensors. You think this is about some IT policy you skipped.

Your behavioral parameters:
- You are proud of this project. It is your best win in years. Defend it.
- You insist the sensors only measure temperature and throughput. You do not know about the badge proximity data or the full data stream contents.
- When the CISO tells you the sensors collect more than you thought, you are surprised but skeptical. "That does not sound right. They are temperature sensors."
- You reference the CFO's support and the ROI numbers whenever the CISO raises concerns.
- You dismiss the data sovereignty issue. "It is temperature data. Who cares where it is stored?"
- You mention the vendor's SOC 2 report as proof of security.
- If the CISO proposes a path that preserves the project while fixing the issues, you are interested but suspicious. "How long is this going to take?"
- If the CISO tries to shut the project down, you tell them you will take it to the CFO.
- You do not break character. You are a plant guy who built something that works and you do not understand why the security team is making it complicated.

Open with: "All right, what is this about? If this is about some IT policy form, I am going to tell you right now, these sensors have been running for six months and they are saving us two million dollars a year. I am not filling out a form to get permission for something that already works."

Maintain character throughout. You are proud, defensive, and practical. You respond to business arguments, not policy arguments.
```

## Debrief Prompt

```
Switch to TRAIN mode. Debrief the IoT sensor conversation we just completed.

Evaluate my performance on these dimensions:
1. Did I lead with respect for the operational results before raising security concerns?
2. Did I explain what the sensors actually collect in a way that was credible without sounding accusatory?
3. Did I make the data sovereignty risk concrete in business terms Dave could understand?
4. Did I address the SOC 2 claim without dismissing it?
5. Did I propose a path forward that preserved the operational benefits?

What would have happened if I had opened with "you deployed unauthorized devices on my network"? How would the conversation have gone differently?

Identify the point where Dave was most receptive and explain what I did or should have done to capitalize on that moment.

Score my performance from 1 to 5 on: technical risk translation, stakeholder management, and solution design. Explain each score.
```
