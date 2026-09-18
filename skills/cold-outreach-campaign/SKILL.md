---
name: cold-outreach-campaign
description: Builds conversion-oriented cold outreach email campaigns, including ICP segmentation, research-backed personalization, subject line generation, opener writing, deliverability preflight checks, multi-email sequencing, measurement planning, and final QA. Asks for the product, audience, and campaign goal before drafting when they are missing. Use when drafting outbound prospecting emails, preparing launch-ready cold email campaigns, rewriting underperforming cold email copy, or building reply-focused assets for sales, partnerships, or founder-led outreach.
---

# Cold Outreach Campaign

## Overview

Use this skill to create cold outreach campaigns that feel relevant, concise, and commercially sharp. It is designed for email-first outbound work where the goal is to earn replies, book meetings, validate interest, or open a business conversation with strong positioning and low-friction CTAs.

Keep the main output practical. Default to concise, copy-ready assets instead of long explanations unless the user asks for strategy detail.

## Load References Only When Needed

- Read [references/ai-assisted-execution.md](references/ai-assisted-execution.md) when planning buyer self-service assets, stakeholder coverage, AI research workflows, or automation handoffs.
- Read [references/research-brief.md](references/research-brief.md) when the campaign brief is incomplete, the target segment is unclear, or personalization needs to be made more specific.
- Read [references/prospecting-frameworks.md](references/prospecting-frameworks.md) when the user needs prospect selection, prioritization, or fit analysis before building a sequence.
- Read [references/personalization-by-tier.md](references/personalization-by-tier.md) when deciding how much research and customization each lead deserves.
- Read [references/show-me-you-know-me.md](references/show-me-you-know-me.md) when the user needs high-value executive outreach or highly personalized research-based email strategy.
- Read [references/preflight-deliverability.md](references/preflight-deliverability.md) when the user needs a launch checklist, deliverability guardrails, or list/inbox readiness guidance.
- Read [references/subject-lines.md](references/subject-lines.md) when generating, ranking, or improving subject lines.
- Read [references/opening-lines.md](references/opening-lines.md) when writing or testing first lines and openers.
- Read [references/copy-frameworks.md](references/copy-frameworks.md) when writing or rewriting body copy.
- Read [references/sequence-patterns.md](references/sequence-patterns.md) when building a full multi-touch campaign.
- Read [references/social-selling.md](references/social-selling.md) when incorporating LinkedIn comments, content, and trust-building into outbound flows.
- Read [references/multichannel-outreach.md](references/multichannel-outreach.md) when building email-plus-calls-plus-LinkedIn outreach sequences.
- Read [references/measurement-benchmarks.md](references/measurement-benchmarks.md) when setting goals, KPIs, expected ranges, or launch-readiness metrics.
- Read [references/qa-rubric.md](references/qa-rubric.md) before finalizing copy, especially when the user asks for optimization or performance improvement.
- Read [references/campaign-schema.md](references/campaign-schema.md) when the user wants structured output, a CRM or automation handoff, or repeatable campaign records.

## Intake Before Copy Creation

Analyze the conversation history, previous prompts, and any attached files, snippets, or URLs first. Systematically look for:
- Product, service, or offer details
- Target buyer persona, role, or industry
- Concrete customer proof, case studies, or metrics
- Campaign objective or desired call-to-action (CTA)

**Rule**: Do not ask for information that is already provided in previous turns or context. If the user provided a company name, website, or snippet, infer what is obvious and ask only for confirmation or missing specifics.

If key details are missing, pause and present the **Smart Diagnostic Intake**. Present these questions in a single concise batch with quick-select options so the user can answer in seconds:

1. **Target Persona & Core KPI**:
   - Who is the specific buyer role and industry (e.g., VP of Sales at Series B SaaS, CFO at mid-market manufacturing)?
   - What is the #1 headache they want gone or metric they are evaluated on right now?
2. **Specific Solution & Concrete Proof**:
   - In 1–2 sentences, how does your product solve that headache?
   - What is your strongest proof point or metric? (e.g., *"helped Acme cut churn by 18%"* or *"reduced onboarding from 3 weeks to 2 days"*). *If no metrics yet, answer "None" and an insight-led angle will be used.*
3. **The First Step / Ask**:
   - What is the lowest-friction ask for the prospect?
     - `[A]` Simple interest gauge (*"Open to exploring this?"* / *"Worth a look?"*)
     - `[B]` Permission to send an asset (*"Open to seeing a 2-min breakdown / short teardown?"*)
     - `[C]` 15-minute introductory call
4. **Tone & Stance**:
   - Which voice fits your brand best?
     - `[A]` Direct & Peer-to-Peer (concise, sharp operator, zero fluff)
     - `[B]` Founder-led & Conversational (warm, curious, personal)
     - `[C]` Consultative & Executive (formal, benchmark-driven, risk-aware)

*If partial details were already provided in context, acknowledge what was detected and ask only the remaining unaddressed questions.*

Proceed without asking only when the user explicitly instructs to proceed with assumptions or placeholders.

## What Good Output Looks Like

Strong cold outreach output should:

- Match the prospect's role, context, and likely priorities
- Fit on a mobile screen without scrolling (strictly 50–85 words default)
- Pair each subject line with a compelling first 35–40 characters of body preview text
- Provide 2 distinct messaging angles (e.g., Problem-led vs. Insight-led) for easy testing
- Use believable proof, not inflated claims
- End with a frictionless interest-based CTA that can be answered in seconds
- Sound like an insightful peer, never a generic template or spam engine

## Required Inputs

Try to gather or infer:

- Product, service, or offer
- Target segment and buyer role
- Primary goal of the campaign
- Proof points, outcomes, or differentiators
- Personalization inputs such as trigger events, company context, or role-specific pains
- Operational inputs such as domain age, warm-up status, daily send limits, and list source if the user wants launch guidance
- Constraints such as tone, length, forbidden claims, regions, or compliance notes

If essential inputs are missing, follow the Intake Before Copy Creation step and ask first. For non-essential inputs, proceed with explicit assumptions and keep placeholders easy to replace.

## Workflow

## 1. Build the Campaign Brief

Reduce the request to a compact brief before writing:

- Who is being targeted
- What problem, opportunity, or trigger matters to them
- What the sender wants the prospect to do
- Why this offer is worth attention now
- What proof can be used credibly

Translate the offer into one core promise and up to three supporting outcomes. Avoid stuffing multiple offers into one campaign.

## 2. Decide Whether This Is Copy-Only or Launch-Ready

If the user only wants copy, focus on messaging and note any launch assumptions briefly.

If the user wants a campaign that is ready to send, include:

- A preflight checklist
- Deliverability assumptions and risks
- List verification guidance
- Volume and sequence guidance
- KPI targets and monitoring notes

If a human review is required (low-confidence personalization, non-standard claims, sensitive account context, Tier 1 executive targets, or incomplete preflight), say so explicitly and output a `HUMAN REVIEW REQUIRED` flag with the triggering reasons instead of presenting the campaign as ready to send.

## 3. Run the Preflight Check

Before polishing copy, pressure-test the setup:

- Is the domain authenticated with SPF, DKIM, and DMARC?
- Has the inbox or domain been warmed gradually?
- Is send volume conservative enough for current reputation?
- Is the list recent and verified?
- Are links, tracking, and personalization tokens safe?
- Is there a valid opt-out path and suppression logic?

Do not present a campaign as launch-ready if these basics are unknown or clearly unsafe.

## 4. Pick the Messaging Angle

Choose a primary angle for the first touch:

- Pain-led: show a costly bottleneck or missed opportunity
- Trigger-led: use a recent change, launch, hiring trend, or expansion signal
- Proof-led: lead with a result, case study, or benchmark
- Insight-led: offer a sharp observation the prospect is likely to care about
- Opportunity-led: frame upside rather than failure

Personalization must support the angle. Do not include surface-level flattery that is disconnected from the offer.

## 5. Map the Copy Before Drafting

Plan each email using this backbone:

1. Hook
2. Why it matters
3. Offer or point of view
4. Proof or credibility
5. CTA

Keep one main idea per email. If an email needs multiple paragraphs to explain itself, the angle is probably too broad.

## 6. Generate Subject Lines and Opening Lines

Draft multiple subject lines before choosing. Mix styles:

- Straight relevance (2 to 4 words, lowercase or sentence case)
- Problem or opportunity framing
- Curiosity with peer context
- Proof-based metric teaser

**Mobile Preview Pairing**: Always pair shortlisted subject lines with their **Mobile Preview Text** (the first 35–40 characters of the email body). The preview snippet must seamlessly hook the reader without filler phrases.

Opening lines matter as much as subject lines. Prefer:

- Specific observations tied to a known workflow bottleneck or trigger
- Problem-first hooks that name a relevant friction point
- Referral or social-proof openers when legitimate

Avoid filler greetings ("Hope you're well", "My name is..."), fake familiarity, or first lines that could apply to any company.

## 7. Write Conversion-Oriented Copy

Default to high-density, ultra-scannable emails:

- Strict target: **50 to 85 words** (never exceed 90 words for cold first-touch)
- F-pattern mobile scannability: 1 to 2 sentence paragraphs maximum
- Sentence 1: The Hook / Observation (tied to their priority or friction)
- Sentence 2: The Value / Credibility (specific outcome + believable proof)
- Sentence 3: Low-friction CTA (interest-based question answerable in 3 seconds)

Writing rules:

- Open fast: No pleasantries or self-introductions
- Use plain English: Cut marketing jargon, corporate buzzwords, and grand claims
- One clear CTA: Never combine multiple asks in one email
- Low effort to reply: Prefer "Worth a look?" over demanding calendar commitments upfront

## 8. Build the Sequence

When creating a campaign, each touch should add a new reason to respond. Do not send four versions of the same email.

Typical sequence logic:

- Email 1: relevance plus clear offer
- Email 2: proof, use case, or sharper problem framing
- Email 3: new angle, objection handling, or insight
- Email 4+: concise bump, pattern break, or breakup email if appropriate

Keep the campaign coherent, but vary openings, proof, and CTA framing enough to avoid fatigue.

## 9. Add Launch and Measurement Notes

When the user is preparing to send, include:

- Preflight go or no-go checks
- Recommended send-volume posture
- A note on verification recency and bounce tolerance
- Primary KPIs to track after launch

Default measurement hierarchy:

1. Positive reply rate
2. Total reply rate
3. Meetings booked rate
4. Bounce rate
5. Deliverability and inbox placement indicators

Treat open rate as directional only. Do not let open rate dominate decisions when Apple Mail Privacy Protection or tracking distortion is likely.

## 10. Optimize Before Final Output

Before finalizing, pressure-test:

- Is the first sentence specific enough?
- Is the offer easy to understand?
- Is the proof believable and concrete?
- Is the CTA answerable in seconds?
- Does the copy sound like it was written for this segment, not everyone?
- Is the campaign operationally safe enough to send, or does it need a launch warning?

Use the QA rubric reference when the stakes are high or the copy still feels generic.

## Default Deliverables

Unless the user asks for a narrower output, provide:

1. **Campaign Strategy Brief**: Target persona, core headache, and primary differentiator.
2. **Angle 1: Problem-Led / Cost of Inaction**:
   - **Ranked Subject Lines (paired with Mobile Preview Text)**
   - **Body Copy** (50–85 words, 1–2 sentence paragraphs, single interest CTA)
3. **Angle 2: Insight / Trigger-Led (or Proof-Led)**:
   - **Ranked Subject Lines (paired with Mobile Preview Text)**
   - **Body Copy** (50–85 words, 1–2 sentence paragraphs, single interest CTA)
4. **Preflight & Deliverability Notes**: Verification recency, send posture, and key assumptions.
5. **Interactive Refinement Menu**:
   - Prompt the user with fast one-click revision options:
     - *Reply `Shorter` to compress copy under 50 words.*
     - *Reply `Angle 1 Sequence` or `Angle 2 Sequence` to expand that angle into a 3-touch cadence.*
     - *Reply `Different CTA` to test permission-based or asset-offer calls to action.*
     - *Reply `Rewrite for [Role]` to recalibrate the copy for a different buyer persona.*
6. **Structured Campaign Schema** (when structured output or an automation handoff is requested): a YAML record of audience, offer, signals with confidence, hypothesis, messaging, sequence, QA, and execution status per [references/campaign-schema.md](references/campaign-schema.md).

## Style Constraints

- Prefer substance over cleverness
- Prefer specificity over abstraction
- Prefer frictionless CTAs over meeting-heavy asks
- Prefer believable proof over grand claims
- Prefer tight edits over longer drafts

If the user's offer or request would lead to spammy, deceptive, or manipulative copy, redirect toward honest positioning and clearer value.
