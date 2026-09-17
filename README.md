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
      ai-assisted-execution.md
      preflight-deliverability.md
      research-brief.md
      prospecting-frameworks.md
      personalization-by-tier.md
      show-me-you-know-me.md
      opening-lines.md
      subject-lines.md
      copy-frameworks.md
      sequence-patterns.md
      social-selling.md
      multichannel-outreach.md
      measurement-benchmarks.md
      qa-rubric.md
research/
  cold-outreach-sources.md
```

## Skill highlights

- Research-first workflow so personalization is tied to a real angle
- AI-assisted research with evidence checks, stakeholder coordination, and response handoffs
- Prospecting and prioritization frameworks to focus time on the best-fit buyers
- Personalization-by-tier guidance for balancing manual research with automation
- Executive outreach guidance centered on Show Me You Know Me® research and human-first personalization
- Preflight guidance for authentication, warm-up, list verification, and send readiness
- Subject line guidance focused on curiosity, relevance, and deliverability
- Opener guidance centered on signal-based first lines
- Copy frameworks for short, reply-focused outbound emails
- Sequence guidance for 3-touch and 5-touch campaigns
- Social selling guidance for LinkedIn engagement and trust-building
- Multichannel sequence guidance that combines email, calls, and social touchpoints
- KPI and benchmark guidance that prioritizes replies over vanity metrics
- QA rubric to tighten clarity, proof, tone, and CTA quality before launch

## Install

List the available skills with the [skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add DesignupADM/codex-cold-outreach-skills --list
```

Install this skill and select your agent when prompted:

```bash
npx skills add DesignupADM/codex-cold-outreach-skills --skill cold-outreach-campaign
```

Listing confirms discovery by that installer; it does not certify skill quality or safety.

## Publishing a release

Maintainers need an authenticated [GitHub CLI](https://cli.github.com/) version that includes `gh skill`. Run these commands from the repository root after committing and pushing the intended release content:

```bash
gh auth status
gh skill publish --dry-run
```

After validation succeeds, publish interactively to choose a version and configure the repository topic:

```bash
gh skill publish
```

For a predetermined, unused release tag, use `gh skill publish --tag v1.0.0` instead. See the [official publishing documentation](https://cli.github.com/manual/gh_skill_publish) for validation rules and options. The repository must be public for others to install without private-repository access.

## Using the skill in Codex

Place the skill folder inside your Codex skills directory, then invoke it in a prompt such as:

```text
Use $cold-outreach-campaign to create a 4-email outbound sequence for CFOs at SaaS companies. Our offer is a pricing optimization audit and the CTA is a 15-minute call.
```

## Notes

- The skill is optimized for email outreach, but the campaign logic can also support founder-led outreach, partnerships, and SDR workflows.
- The reference files are intentionally split by job so Codex can load only the detail it needs for a given request.
- The repository also includes a research notes file that maps the external sources used to strengthen this skill.
