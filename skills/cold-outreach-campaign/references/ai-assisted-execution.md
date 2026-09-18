# AI-Assisted Outreach Execution

Use when designing research, stakeholder coverage, or handoffs between automated outreach and sales conversations.

## Help the buyer evaluate independently

Treat early outreach as a way to become useful before a formal evaluation, as well as a way to earn a meeting. Offer a relevant checklist, comparison, diagnostic, or short case study when a meeting would be premature. Make the asset useful without requiring a discovery call to understand it.

For complex deals, map the economic buyer, likely champion, end users, and technical or procurement reviewers as relevant. Give each role a distinct business reason to engage. Coordinate account ownership and contact frequency so multiple sellers do not duplicate outreach.

## Research before generation

1. Capture a relevant signal with its source, date, and account match.
2. Label the evidence with a confidence level before using it.
3. Separate the observed fact from the hypothesized business implication.
4. Match that implication to an approved capability and a supported proof point.
5. Draft concise context, value, and one low-friction ask.
6. Check the source, personalization fields, claims, confidence labels, and next step before execution.

### Evidence confidence levels

Classify every research signal as high, medium, or low confidence:

- **High**: directly observed from a primary source (company careers page, official announcement, verified profile), dated within the last 90 days. Usable in external messaging.
- **Medium**: primary source that is ambiguous or older than 90 days, or a reputable secondary source. Usable cautiously in external messaging with softer framing ("looks like", "seems").
- **Low**: a single third-party mention, inferred from context, or unverifiable. Internal hypothesis only; never presented to the prospect as fact.

Record the level in the internal brief:

```yaml
signal:
  type: hiring
  evidence: "3 enterprise AE positions open"
  source: company careers page
  observed_at: 2026-09-16
  confidence: high
```

When evidence is weak, omit the claim or label the assumption in the internal brief. Do not imply that a funding round, job posting, or executive change proves purchase intent.

Use AI to organize evidence, prioritize accounts, and draft variants. Evaluate tools by evidence traceability, data freshness, CRM integration, review controls, and stop-on-reply behavior. Verify current capabilities and pricing before recommending a vendor.

## Coordinate automation and human ownership

Drafting a campaign does not authorize sending it. Operate within the user's authorized scope and configured review process.

- Pause queued automated touches when a reply arrives on any connected channel; assign an owner to handle the response.
- Distinguish a substantive reply from an out-of-office message, bounce, or opt-out. Reschedule out-of-office contacts appropriately; suppress bounces and opt-outs.
- Log the channel, last touch, response, owner, and next action in the shared account record.
- Review unsupported product claims, unusual promises, and sensitive account context before sending.
- Re-engage only with a relevant new reason and appropriate timing; elapsed time alone is not a reason to restart a sequence.

## Human review gate

Stop before execution when any of these apply, and output a `HUMAN REVIEW REQUIRED` flag with the triggering reasons:

- Personalization is based on an ambiguous, undated, or low-confidence source
- The message makes a non-standard claim, promise, or guarantee not in approved evidence
- The account context is sensitive (mergers, litigation, layoffs, regulated industries)
- The target is a Tier 1 executive or strategic account
- Deliverability preflight is incomplete or unknown

Format:

```text
HUMAN REVIEW REQUIRED
Reasons:
- personalization based on ambiguous source
- high-value account
```

A campaign that clears the gate is still subject to the user's configured approval process. Drafting does not authorize sending, and passing QA does not mean the campaign is approved.

## Measure the contribution

Track research time saved alongside positive replies, qualified conversations, held meetings, and opportunities. Compare similar segments and offers; do not attribute every change in conversion to AI. More drafts or more sends are not sufficient evidence of commercial improvement.
