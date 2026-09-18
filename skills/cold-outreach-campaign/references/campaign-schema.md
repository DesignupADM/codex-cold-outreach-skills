# Campaign Output Schema

Use this reference when the user asks for structured campaign output, or when preparing a handoff to a CRM, spreadsheet, or automation tool (HubSpot, Apollo, n8n, Make, Zapier, another agent).

## When to use it

- The user requests structured output (YAML or JSON)
- The campaign will be handed off to a CRM, database, or automation pipeline
- The user wants repeatable, comparable campaign records across clients

Emit YAML by default; use JSON when the downstream system requires it. Never invent values: leave unknown fields as `null` (or omit them) and mark them in the `qa` block instead of guessing.

## Top-level schema

```yaml
campaign:
  name:
  objective:

audience:
  segment:
  buyer_role:
  geography:

offer:
  core_promise:
  outcomes:
  proof:

prospecting:
  tier:          # Tier 1 | Tier 2 | Tier 3
  fit_reason:

research:
  company:
  person:
  buying_context:

signals:
  - signal:
    type:
    evidence:
    source:
    observed_at:
    confidence:  # high | medium | low

hypothesis:
  problem:
  why_now:

messaging:
  angle:
  subject_lines:
  openers:
  emails:

sequence:
  touches:

qa:
  evidence_check:
  personalization_check:
  deliverability_check:
  claims_check:

execution:
  status:                # draft | preflight_passed | human_review_required | ready_to_send
  human_review_required: true | false
  human_review_reasons:
```

## Field semantics

- **campaign**: internal name and the single objective the campaign is judged on.
- **audience**: segment, buyer role, and geography. Keep one segment per record; split audiences into separate records instead of merging them.
- **offer**: one core promise, up to three supporting outcomes, and the approved proof attached to it.
- **prospecting**: research tier per [prospecting-frameworks.md](prospecting-frameworks.md), plus the explicit fit reason for this account.
- **research**: the three research layers (person, company, buying context) from [research-brief.md](research-brief.md).
- **signals**: one entry per signal. `confidence` is required. Keep `source` and `observed_at` populated so downstream reviewers can re-verify.
- **hypothesis**: the problem the signal implies and why the timing matters now. Labeled as a hypothesis, never as fact.
- **messaging**: chosen angle and the generated assets.
- **sequence**: ordered touches with channel, purpose, and timing.
- **qa**: outcome of each rubric check, including anything that failed or is unknown.
- **execution**: current status and review gate state.

## Confidence enum

```text
high   → primary source, dated within the last 90 days → usable in external messaging
medium → primary but ambiguous or dated, or reputable secondary source → usable with softer framing
low    → unverifiable or inferred → internal hypothesis only
```

## Human review flag

Set `execution.human_review_required: true` and list reasons when:

- Personalization is based on an ambiguous, undated, or low-confidence source
- The message makes a non-standard claim, promise, or guarantee not in approved evidence
- The account context is sensitive (mergers, litigation, layoffs, regulated industries)
- The target is a Tier 1 executive or strategic account
- Deliverability preflight is incomplete or unknown

## Execution status and launch-ready vs legally ready

Use this progression:

```text
draft → preflight_passed → human_review_required → ready_to_send
```

- `launch-ready` means **technical and operational preflight passed**. It is not legal approval.
- GDPR, PECR, CAN-SPAM, CASL and other requirements depend on jurisdiction, recipient type, purpose, and data source. This skill does not provide legal advice.
- Mark `status: human_review_required` rather than `ready_to_send` when any review trigger applies or the preflight is unknown.

## Handoff notes

- Flatten nested fields for spreadsheets: one row per signal, one row per touch, with the campaign id repeated.
- Map fields to the target system's columns explicitly; do not assume vendor field names.
- Preserve `source` and `observed_at` for every signal so downstream reviewers can re-verify before send.
