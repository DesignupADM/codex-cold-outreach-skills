# Preflight and Deliverability

Use this reference when the user wants a launch-ready campaign, a pre-send checklist, or help avoiding deliverability problems.

## Default preflight sequence

Run this checklist in order:

1. Sending setup
2. Warm-up status
3. Tracking and links
4. List verification
5. Content safety
6. Seed tests and rendering
7. Send-volume plan
8. Suppression and opt-out logic

## 1. Sending setup

Confirm or recommend:

- SPF, DKIM, and DMARC are configured
- DMARC starts permissive during warm-up, then tightens over time
- A separate sending domain or adjacent domain is considered when protecting the main brand domain matters
- Shared public tracking links are avoided when a custom tracking domain is available

If the setup is unknown, say the campaign is not fully launch-ready yet.

## 2. Warm-up status

Conservative default guidance:

- Warm new inboxes for at least 14 days
- For stricter enterprise or executive outreach, 30 days is safer
- Start around 5 to 10 sends per inbox per day
- Increase gradually rather than jumping to high volume
- Keep warm-up behavior running after launch when possible

If the user is sending from a fresh inbox with no warm-up, flag that as a meaningful risk.

## 3. Tracking and links

- Keep links minimal
- Prefer relevant links only
- Avoid public shorteners when possible
- Use branded or custom tracking domains if tracking is required

If the campaign does not need links, leaving them out is often safer.

## 4. List verification

List quality is a launch gate, not a cleanup task.

- Verify addresses close to send date
- A 72-hour freshness window is a strong default
- Remove duplicates, risky domains, and unclear catch-alls when reputation is weak
- Do not use scraped or stale data if the user is aiming for safe scale

Bounce guidance:

- Under 2% is the safe default threshold
- If projected or observed bounce rate is above 2%, pause and clean the list before scaling

## 5. Content safety

Check for:

- Spam-trigger phrasing
- Overuse of links or HTML styling
- Personalization tokens that may fail
- More than one CTA
- Misleading urgency or false familiarity

Avoid filler language and hard-sell language that reads like promo email.

## 6. Seed tests and rendering

Before launch:

- Send seed tests across Gmail, Outlook, and Yahoo where possible
- Check mobile and desktop rendering
- Confirm variables render correctly
- Confirm reply handling, stop-on-reply, and bounce suppression are enabled

If seed tests fail or placements look poor, treat it as no-go until corrected.

## 7. Send-volume posture

Use conservative phrasing unless the user already has healthy infrastructure:

- Start lower than your theoretical max
- Default to caution for new domains or new lists
- Per-inbox daily caps around 30 are a safe planning baseline for many campaigns
- Only scale when bounce, reply quality, and placement look stable

## 8. Suppression, compliance, and opt-out

- Include a functioning opt-out path for commercial outreach
- Honor opt-outs across all future campaigns, not just one sequence
- Maintain a global suppression list
- If EU or EEA contacts are involved, note that local legal requirements may be stricter

## How to report preflight status

When summarizing, use one of these labels:

- `Ready`: no obvious blockers stated
- `Ready with caveats`: copy is usable, but setup assumptions need confirmation
- `Not ready`: infrastructure, verification, or compliance risk is too high
