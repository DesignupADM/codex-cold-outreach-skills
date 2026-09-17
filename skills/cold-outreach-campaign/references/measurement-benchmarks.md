# Measurement and Benchmarks

Use this reference when the user asks what good performance looks like, which KPIs matter, or how many contacts are needed to sustain a sequence.

## Metric hierarchy

Use this order by default:

1. Positive reply rate
2. Total reply rate
3. Meetings booked rate
4. Opportunity or pipeline conversion
5. Bounce rate
6. Inbox placement and domain health
7. Open rate as a secondary signal only

Open rate still helps diagnose subject-line relevance and deliverability, but it is no longer a reliable primary success metric because tracking inflation and privacy protections distort it.

## Practical benchmark ranges

These are directional 2026-style planning ranges, not universal guarantees:

- Around 3% to 4% total reply rate is a common platform-level baseline
- Above 5% total reply rate is generally good
- Above 10% total reply rate is excellent for many cold outbound contexts
- Positive reply rate is often materially lower than total reply rate
- Segment executive and non-executive outreach separately; do not assume seniority has a universal effect on reply rates

When the user asks for forecasts, emphasize that list quality, offer strength, market saturation, and sending health can move results sharply.

## Dated vendor benchmarks

- [Instantly's 2026 benchmark discussion](https://instantly.ai/blog/ai-sales-agent-benchmarks-2026-the-complete-performance-report/) reports a 3.43% average reply rate, 5.5%+ for the top quartile, and 10.7%+ for the top decile from its broader cold-email dataset. These are vendor-platform results, not an AI-agent-specific baseline or a forecast for every industry.
- [Expandi's 2026 report](https://expandi.io/blog/linkedin-outreach-benchmarks-2026/) reports 28.5% connection acceptance across 13.2 million requests sent through its accounts from May 2025 through April 2026. This is a platform sample, not all LinkedIn activity.

Sources checked September 18, 2026. Retain the reporting period and population when quoting these figures. Do not combine acceptance, message replies, and positive replies into one conversion rate.

## Define the denominator

For internal sequence reporting, use unique contacts with a delivered email as the denominator for contact-level reply and meeting rates. Count each contact once per outcome and report the observation window. Separate positive replies from objections, opt-outs, and automatic responses. If a source uses messages sent instead, label that difference before comparing it.

For calls, report human connects per dial, qualified conversations per connect, and meetings per dial separately. Track held meetings as well as booked meetings. A day's share of all connects is not its connect rate unless dial volume is also known.

## Operational health thresholds

- Keep bounce rate under 2%
- If bounce rises above 2%, pause list expansion and fix data quality first
- Watch domain health and placement before scaling volume

## KPI guidance by campaign type

### Single-contact cold email

Track:

- Total reply rate
- Positive reply rate
- Meetings booked rate
- Bounce rate

### Multi-touch account outreach

Track:

- Stakeholders engaged per account
- Positive reply rate by account
- Meeting creation by target account
- Pipeline influence

## List sizing logic

Sequences consume fresh contacts faster than many teams expect.

Planning shortcut:

```text
Net-new contacts needed per month = Monthly send throughput / Sequence steps
```

Example:

```text
9,000 monthly sends / 5-step sequence = 1,800 fresh contacts needed per month
```

Add a buffer for bounces, opt-outs, and contacts that are not worth emailing again.

## How to use benchmarks safely

- Compare results to contextually similar campaigns, not generic internet averages
- Prioritize positive replies over vanity metrics
- If reply rate is low but bounce and placement are healthy, the problem is usually targeting, angle, or offer
- If opens look weak and bounce is rising, diagnose infrastructure and list quality first
