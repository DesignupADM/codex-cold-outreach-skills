# Cold Outreach Agent Skill

A provider-agnostic [Agent Skill](https://agentskills.io) for building cold outreach campaigns: ICP segmentation, research-backed personalization, subject lines, openers, deliverability preflight checks, multi-email sequencing, measurement, and final QA. It works in Claude Code, Google Antigravity, Codex, Cursor, GitHub Copilot, Gemini CLI, OpenCode, and any other agent that supports `SKILL.md` skills.

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

Before drafting, the skill analyzes the prompt and conversation context first. If the product, its description, target audience, or sequence goal (booked meetings, replies, demos, signups, and so on) are missing, it asks a short batch of intake questions instead of inventing assumptions.

## Repository structure

```text
skills/
  cold-outreach-campaign/
    SKILL.md
    agents/
      antigravity.yaml
      claude-code.yaml
      cursor.yaml
      gemini-cli.yaml
      github-copilot.yaml
      openai.yaml
      opencode.yaml
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
      campaign-schema.md
research/
  cold-outreach-sources.md
```

## Skill highlights

- Research-first workflow so personalization is tied to a real angle
- Intake step that confirms offer, audience, and campaign goal before copy creation
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

### Universal installer (recommended)

Install with the [skills CLI](https://github.com/vercel-labs/skills), which detects your agents and installs to the correct paths for each one:

```bash
npx skills add DesignupADM/codex-cold-outreach-skills --list
```

```bash
npx skills add DesignupADM/codex-cold-outreach-skills --skill cold-outreach-campaign
```

Target specific agents non-interactively:

```bash
npx skills add DesignupADM/codex-cold-outreach-skills --skill cold-outreach-campaign -a claude-code -a antigravity -a codex -y
```

Listing confirms discovery by that installer; it does not certify skill quality or safety.

### Manual install

Copy or symlink the `skills/cold-outreach-campaign/` folder into the skills directory for your agent.

| Agent | Project path | Global path |
| --- | --- | --- |
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |
| Google Antigravity (2.0 / IDE) | `.agents/skills/` | `~/.gemini/config/skills/` |
| Antigravity CLI | `.agents/skills/` | `~/.gemini/antigravity-cli/skills/` |
| Codex | `.agents/skills/` | `~/.agents/skills/` |
| Cursor | `.agents/skills/` | `~/.cursor/skills/` |
| GitHub Copilot | `.agents/skills/` | `~/.copilot/skills/` |
| Gemini CLI | `.agents/skills/` | `~/.gemini/skills/` |
| OpenCode | `.agents/skills/` | `~/.config/opencode/skills/` |
| Amp, Replit | `.agents/skills/` | `~/.config/agents/skills/` |

Path details come from the [supported agents table](https://github.com/vercel-labs/skills#supported-agents). Prefer the installer when possible so paths stay correct as agents evolve.

## Invoking the skill

- Claude Code: run `/cold-outreach-campaign`, or let Claude load it automatically when the description matches your request.
- Google Antigravity: run `/cold-outreach-campaign`, or let the agent pick it autonomously based on the skill description.
- Codex (CLI, IDE, desktop): mention `$cold-outreach-campaign`, browse with `/skills`, or rely on implicit matching.
- Cursor, GitHub Copilot, Gemini CLI, OpenCode, and similar agents: the skill is selected automatically when your prompt matches. You can also point the agent at `SKILL.md` directly.

Example prompt:

```text
Use cold-outreach-campaign to create a 4-email outbound sequence for CFOs at SaaS companies. Our offer is a pricing optimization audit, the goal is booked meetings, and the CTA is a 15-minute call.
```

## Compatibility

This skill follows the open Agent Skills standard so the same files work across providers:

- Frontmatter uses only the standard `name` and `description` fields. No provider-specific fields, so nothing is silently ignored or rejected.
- Reference files use progressive disclosure: agents read `SKILL.md` first and load individual references only when relevant.
- No shell injection, hooks, subagent config, or tool permission grants are required, so behavior is consistent in every host.
- `agents/openai.yaml` is optional metadata consumed by Codex and ChatGPT (`interface.display_name`, `interface.short_description`, `interface.default_prompt`). The other files in `agents/` mirror the same interface schema with provider-specific invocation syntax (`/cold-outreach-campaign` for Claude Code and Antigravity, natural language elsewhere). They are advisory metadata for installers and tooling; agents that do not recognize them ignore the folder entirely.

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

## Notes

- The skill is optimized for email outreach, but the campaign logic can also support founder-led outreach, partnerships, and SDR workflows.
- The reference files are intentionally split by job so agents can load only the detail they need for a given request.
- The repository also includes a research notes file that maps the external sources used to strengthen this skill.
