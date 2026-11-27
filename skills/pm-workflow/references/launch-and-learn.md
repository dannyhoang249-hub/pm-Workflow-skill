# Ship and learn

## Measure whether the gap closed

Define this before release, starting from the problem statement and the decision the data must support.

- One primary outcome metric tied to the desired reality, a few input metrics, and guardrails against local optimization.
- A North Star metric helps when several teams share one goal. Skip it for a single feature.
- Tracking plan: event, when it fires, required properties, purpose. Start from the decision, not from a list of events.
- Name data risks: missing events, identity stitching, sample bias, vague definitions.
- For each: formula, event or source, segment, baseline, target, owner, review cadence. Unknown baseline is stated as unknown.
- A decision rule written in advance: what leads to ship, iterate, stop, or investigate the data.
- Pair numbers with qualitative follow-up. Usage shows what happened, not why.
- Do not claim causes the data cannot support. Do not stretch a few cases into prevalence.

## Pre-mortem

Run it before committing, on a PRD, roadmap or launch plan. Assume the release failed. List concrete mechanisms across user, business, technical, operational, dependency and compliance.

- **Tiger:** a real threat. Give likelihood, impact, trigger, mitigation, owner, and whether it blocks launch.
- **Paper tiger:** manageable. Note what would make it real.
- **Elephant:** the thing people avoid saying. Raise it constructively.

End with go, no-go, or go with conditions.

## Launch

Public documentation, sales and support enablement, customer announcement, phased rollout where risk justifies it, a way to roll back.

## After launch

Check whether people use it. If not, find out why. Compare the result with the original hypothesis and record what was learned. A new or unmet gap returns to the Frame stage.
