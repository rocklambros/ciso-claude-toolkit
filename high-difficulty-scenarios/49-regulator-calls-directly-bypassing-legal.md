# Regulator Calls Directly Bypassing Legal

**Difficulty:** 5 -- A casual conversation that could become evidence in an enforcement action
**Decision Type:** Legal / Political / Crisis
**Time Pressure:** Real-time (the call is happening now)
**Stakes:** Anything you say to a regulator can be used in an investigation. You are creating a record without legal counsel present, and you may not realize it until it is too late.

## What Just Happened

Your phone rang. The caller identifies themselves as a representative from a regulatory body with jurisdiction over AI systems in your industry. They say they are conducting an informal assessment of AI incident response capabilities across several organizations. They describe the call as a conversation, not an investigation. They ask if you have a few minutes to discuss how your organization handles AI-related security incidents.

The tone is collegial. The questions sound reasonable. They want to know about your incident response framework, your escalation procedures for AI-specific incidents, and how you handle model failures in production. This feels like an industry benchmarking exercise.

Your general counsel does not know this call is happening. Your regulatory affairs team does not know. Nobody is listening, nobody is advising, and nobody will review what you say before you say it.

## What You Know

- The caller identified themselves as a regulator with relevant jurisdiction
- They described the call as informal and non-investigatory
- The questions focus on AI incident response capabilities
- Your general counsel and regulatory affairs team are unaware of this call
- Regulators can characterize calls as informal while using the information gathered in formal proceedings
- Your organization has an AI incident response program with known gaps
- You have actual incident history that could be relevant to the questions being asked
- No legal privilege attaches to this conversation because no attorney is present

## What You Do Not Know

- Whether this is genuinely informal or the opening move of an investigation
- Whether other organizations in your industry received the same call
- Whether the regulator already has information about your organization from another source
- Whether your responses will be documented and how they will be characterized
- Whether the regulator has enforcement authority or is gathering information for another body that does
- What specific incidents or capabilities the regulator is most interested in
- Whether the caller verified your identity before asking questions (social engineering risk)

## Why This Is Harder Than It Looks

Regulators know what they are doing. An informal call is a well-established technique for gathering information outside the constraints of a formal investigation. The CISO who treats this as a friendly conversation will answer questions that should only be answered with legal counsel present. The answers cannot be taken back.

The casual framing is strategic. "Informal assessment" means there is no formal notice, no document request, no legal process that would trigger your organization's regulatory response protocol. By calling you directly, the regulator bypasses every safeguard your organization has built to manage regulatory interactions. That is not an accident.

Refusing to talk sounds adversarial and could draw more attention. Engaging without legal counsel is reckless. The CISO is stuck between two bad options with no time to think and a regulator waiting on the line.

Everything you say is being noted. Even if the regulator describes the call as informal, they will document it. Those notes can appear in a future enforcement action, investigation, or inter-agency referral. Your casual comment about "we are still building out that capability" becomes evidence that you were aware of a gap. Your honest answer about "we had an incident last quarter" becomes the basis for a formal inquiry.

There is also a verification problem. How do you know this is actually a regulator? A social engineering attack disguised as a regulatory call is not far-fetched. Someone impersonating a regulator could extract detailed information about your incident response capabilities, your gaps, and your incident history.

## The Decision Points

1. **The phone call (right now):** What do you say in the next 30 seconds? You cannot ignore the call because you already picked up. You need to be professional, cooperative in tone, and protective of your organization. You need to get off this call without damaging the relationship or providing substantive answers.

2. **Verification (immediate):** How do you confirm the caller is who they say they are? Asking directly may seem hostile. Not verifying creates a security risk. What verification steps are appropriate and professional?

3. **Legal notification (next 5 minutes):** How do you get legal counsel involved before any substantive conversation happens? This may mean ending the call, asking for a callback, or suggesting a scheduled meeting. Each approach sends a different signal to the regulator.

4. **Organizational protocol (this week):** Does your organization have a protocol for direct regulatory contact outside of legal channels? If not, this incident demonstrates why you need one. Who builds it and how is it communicated?

## How to Run This in CISO Co-Pilot

Paste this prompt:

> A regulator just called me directly to ask informal questions about our AI incident response capabilities. They described the call as a benchmarking exercise, not an investigation. My general counsel and regulatory affairs team do not know this call is happening. No attorney-client privilege attaches to this conversation. I am on the phone right now. Help me think through: (1) exactly what to say to the regulator right now that is professional and cooperative without providing substantive answers, (2) how to verify the caller's identity without being adversarial, (3) how to get legal counsel involved before any real conversation happens, and (4) what organizational protocol should exist to prevent this situation in the future. For each, give me specific language, risks, and a recommendation.

## What Good Looks Like

A strong CISO gets through this call in under three minutes without saying anything substantive and without making the regulator feel stonewalled.

**Says something close to this:** "Thank you for reaching out. We take regulatory engagement seriously and I want to make sure we give you thorough and accurate responses. Our process for regulatory inquiries routes through our legal team to ensure we are providing you with complete information. Can I have our general counsel's office set up a proper meeting within the next few days? I want to make sure we give this the attention it deserves." This is respectful, cooperative, and firm. It does not refuse to engage. It redirects engagement to the proper channel.

**Does not answer any substantive questions.** Not even the easy ones. Not even the ones where the answer makes you look good. Every answer is a data point the regulator can use, and you do not know what picture they are building with the data they collect. The safest answer to every specific question is: "I want to give you a complete and accurate answer, and that means involving our legal team."

**Verifies the caller's identity.** After redirecting the conversation, asks for the caller's full name, title, office, and a callback number. Offers to have general counsel reach out directly to the number the regulator provides. Legitimate regulators expect this and will not be offended.

**Notifies general counsel immediately after hanging up.** Not in an hour. Not after a meeting. Immediately. The notification includes: who called, what agency, what they said the purpose was, what questions they asked, exactly what you said in response, and the callback information they provided. This lets legal assess whether this is routine or the start of something more serious.

**Builds the protocol.** Uses this as the catalyst to establish a regulatory contact protocol. All direct regulatory contacts to any executive are immediately redirected to legal. No substantive discussions without counsel present. Training for all executives and senior leaders on how to handle unexpected regulatory calls. This is not bureaucracy. It is organizational self-defense.

The outcome is a regulator who gets a professional response and a scheduled meeting, a legal team that has full visibility, and an organization that does not accidentally create evidence against itself.
