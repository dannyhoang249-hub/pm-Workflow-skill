# Decision check

A quality gate before committing to a large feature, roadmap item, launch, experiment or cross-team plan.

1. **Think before acting.** Separate facts, assumptions and unknowns. If the request has several reasonable readings, show them and how each changes the decision. Say so if the proposed solution does not address the stated problem.
2. **Simplicity first.** Find the smallest scope, experiment or analysis that can test the outcome now: an existing workflow, a prototype, a manual concierge test, or an instrumented release. Cut anything added only for the future.
3. **Surgical scope.** Trace each requirement, task and metric to a user outcome, risk or constraint. Flag adjacent opportunities without absorbing them. Keep existing commitments unless this decision explicitly replaces them.
4. **Verifiable goal.** Set a success criterion, a guardrail, a stop condition, and the loop `step -> signal -> decision`. Prefer reversible steps.

Close with one verdict: **proceed**, **simplify then proceed**, or **validate before committing**.

```markdown
# Decision check: [name]
Decision and intended outcome:
Facts / assumptions / unknowns:
Simpler viable path:
Scope and trade-offs:
| Step | Signal to check | Owner | Decision it triggers |
| --- | --- | --- | --- |
Verdict:
```

These four principles are adapted for product work from [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills).
