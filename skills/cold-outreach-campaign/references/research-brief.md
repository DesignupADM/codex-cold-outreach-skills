# Research Brief & Intake Extraction

Use this reference when analyzing user inputs, extracting details from conversation history or pasted URLs, or guiding the intake questioning.

## The 4 Essential Intake Anchors

When evaluating the prompt and conversation history, extract or confirm these 4 anchors:

1. **Target Persona & Core KPI**:
   - Exact decision-maker title (e.g., VP of Sales, Head of Engineering, CFO).
   - The primary friction point or business metric they are judged on (e.g., sprint velocity, customer churn, CAC, onboarding time).
2. **Specific Solution & Concrete Proof**:
   - The direct operational mechanism: how the product relieves that friction.
   - At least one verifiable metric, case study, or data point (e.g., *"cut ramp time by 30%"*, *"saved 12 hrs/week for Acme"*).
   - *If no metrics exist, classify as "Insight-led" and frame an industry observation rather than a generic claim.*
3. **The First Step / CTA**:
   - The low-friction ask: simple interest check, permission to send a 2-min breakdown/diagnostic, or a brief conversation.
4. **Tone Posture**:
   - Direct/Peer-to-Peer, Founder-led/Conversational, or Consultative/Executive.

## Rapid Extraction Heuristics (Unstructured Inputs)

When a user provides rough notes, a company URL, or a product snippet, extract the anchors using these heuristics:

| Input Source | What to Mine First | What to Discard |
| :--- | :--- | :--- |
| **Website URL / Landing Page** | • Hero headline (core promise)<br>• Customer logos or case study stats<br>• Target role indicated in navigation or testimonials | • Generic marketing buzzwords ("all-in-one platform")<br>• Technical documentation / feature checklists |
| **Pasted Pitch Deck / Raw Notes** | • Problem slide (the prospect's pain)<br>• Concrete ROI metrics or traction numbers | • Internal company goals, funding details, or valuation |
| **Previous Chat Turns** | • Prior audience definitions<br>• Tone preferences previously stated | • Unrelated previous coding or prompt tasks |

## Rule of Inferred Context

1. **Never interrogate for known data**: If the user's prompt or past context clearly implies the audience (e.g. *"Our tool automates SOC 2 compliance"* $ightarrow$ Target: Head of Security / Compliance / CTO), adopt that role and ask only the remaining gaps (proof point and CTA).
2. **Offer quick-select defaults**: Whenever a question must be asked, provide multiple-choice options (`[A]`, `[B]`, `[C]`) to reduce typing effort.

## Angle Selection Heuristic

Pick the dominant angle based on available assets:
- If a hard customer metric exists $ightarrow$ **Proof-Led / Case Study**
- If an urgent industry shift, funding, or hiring trend is visible $ightarrow$ **Trigger / Insight-Led**
- If a universal operational bottleneck is undisputed $ightarrow$ **Problem-Led / Cost of Inaction**

## Assumption & Placeholder Handling

When non-critical specifics are unavailable:
- State assumptions in one sentence before the copy.
- Use clean, obvious bracketed placeholders: `[Company]`, `[Specific Metric]`, `[Industry]`.
- Keep the surrounding sentence coherent so the copy is immediately readable even before filling brackets.

## Evidence Confidence

Label each extracted signal high, medium, or low confidence before it enters copy:

- **High**: primary source, dated within the last 90 days. Usable in external messaging.
- **Medium**: primary but dated, or a reputable secondary source. Usable with softer framing.
- **Low**: unverifiable or inferred. Internal hypothesis only.

Full definitions and the signal record format: see [ai-assisted-execution.md](ai-assisted-execution.md).
