# Codex Outreach Skills

This repository contains reusable Codex skills for cold outreach content and campaign creation.

## Included skill

### `cold-outreach-campaign`

Use this skill when you need to:

- Build a cold email campaign from scratch
- Rewrite underperforming outbound copy
- Create subject lines that are clear, relevant, and testable
- Create stronger first-line openers and preview-text hooks
- Write conversion-oriented email copy with stronger positioning and lower-friction CTAs
- Add launch-readiness and deliverability preflight checks
- Produce a multi-touch campaign with distinct angles instead of repetitive follow-ups
- Define practical outbound KPIs and benchmark expectations

## Repository structure

```text
skills/
  cold-outreach-campaign/
    SKILL.md
    agents/openai.yaml
    references/
      preflight-deliverability.md
      research-brief.md
      opening-lines.md
      subject-lines.md
      copy-frameworks.md
      sequence-patterns.md
      measurement-benchmarks.md
      qa-rubric.md
research/
  cold-outreach-sources.md
```

## Skill highlights

- Research-first workflow so personalization is tied to a real angle
- Preflight guidance for authentication, warm-up, list verification, and send readiness
- Subject line guidance focused on curiosity, relevance, and deliverability
- Opener guidance centered on signal-based first lines
- Copy frameworks for short, reply-focused outbound emails
- Sequence guidance for 3-touch and 5-touch campaigns
- KPI and benchmark guidance that prioritizes replies over vanity metrics
- QA rubric to tighten clarity, proof, tone, and CTA quality before launch

## Using the skill in Codex

Place the skill folder inside your Codex skills directory, then invoke it in a prompt such as:

```text
Use $cold-outreach-campaign to create a 4-email outbound sequence for CFOs at SaaS companies. Our offer is a pricing optimization audit and the CTA is a 15-minute call.
```

## Notes

- The skill is optimized for email outreach, but the campaign logic can also support founder-led outreach, partnerships, and SDR workflows.
- The reference files are intentionally split by job so Codex can load only the detail it needs for a given request.
- The repository also includes a research notes file that maps the external sources used to strengthen this skill.
