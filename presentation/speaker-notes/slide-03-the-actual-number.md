# Slide 3: The actual number

Before I show you the number, I need to tell you how I got it, because a number without methodology is just an opinion with a decimal point.

I built a risk model. The model compares the probability of a data breach or data exposure event when your people use a governed LLM tool versus when they use existing SaaS applications like email, cloud storage, and collaboration platforms. The claim I am making is not that LLMs are safe. The claim is that the risk is comparable to tools you already approved, and in some configurations it is lower.

Here are the scope constraints. This model covers a specific deployment pattern: an enterprise LLM instance with a system prompt, access controls, and no fine-tuning on sensitive data. It does not cover autonomous agents, retrieval-augmented generation with live database connections, or fine-tuned models trained on production customer data. Those are different risk profiles and they need different models. If you are deploying agentic systems, this number does not apply to you. Build a different model.

The data classes I modeled are the ones that show up in most CISO risk registers: PII, financial data, intellectual property, and regulated health information. I did not model classified data or national security data because the deployment patterns and controls for those environments are fundamentally different.

The baseline comparator is existing SaaS. Not paper files. Not locked-down on-premises systems. I compared LLM risk to the tools your people are already using every day: email with external sharing enabled, Google Drive or SharePoint with link sharing, Slack with guest channels, Salesforce with report exports. Those tools have known exposure paths. Most organizations have accepted that risk implicitly by deploying them. I wanted to know whether an LLM changes the risk profile in a meaningful way.

The modeled range is 0.1% to 1% annualized probability of a data exposure event per user, per application. That is not a measured statistic. No empirical dataset exists for enterprise LLM breach rates because the deployment history is too short. It is a modeled estimate built on fault tree analysis using failure mode probabilities drawn from SaaS analogs and the Verizon DBIR.

If you think the methodology is flawed, I want to hear about it. Build a better model and publish it. The field needs more quantified risk analysis for AI deployments, not less. But if your counterargument is "it feels more dangerous," that is not a risk assessment. That is a gut reaction, and you would not let your board make decisions based on gut reactions about any other technology category.

The number on the screen is the starting point for a real conversation about where AI sits in your risk register. Not at the top because it is new and scary. Not at the bottom because a vendor told you it was safe. In the right place, based on the math.
