# PM Workflow Skill

An agent skill that works alongside a Product Manager, from **problem space** to **solution space**, and challenges weak reasoning at each step.

It is built for one failure in particular: a polished document resting on a problem nobody verified.

## How it works

```text
PROBLEM SPACE                                  SOLUTION SPACE
Frame -> Discover -> Define -> Prioritize -[gate]-> Shape -> Specify -> Ship and learn
  ^                                                                        |
  +------------------------------ new evidence ----------------------------+
```

| Stage | Question | Output |
| --- | --- | --- |
| Frame | Whose problem, why now? | Hypothesis, research direction |
| Discover | What actually happens? | Past behaviour, Job Map |
| Define | Which gap is worth closing? | Job stories, problem statement |
| Prioritize | Why this, at what cost? | Decision and trade-off |
| Shape | What mechanism, how complex? | Solution direction, Workflow, CDM/ORD |
| Specify | What gets built, in what slices? | User stories, activity diagrams, wireframes |
| Ship and learn | Did the gap close? | Metrics, pre-mortem, learnings |

**The gate.** Before solution work, the problem is rated **Solid**, **Thin** or **Assumed**, with the missing evidence and the cheapest way to get it. The gate informs; you decide. If you proceed anyway, the assumptions are written at the top of the artifact.

## Principles

1. A problem is a gap between one specific subject's reality and what they want.
2. Problem space comes first and gets the most thought.
3. Requests are inputs, not validated problems.
4. Past behaviour beats opinion.
5. Make data concrete before abstracting it.
6. Discovery reduces uncertainty enough to place a bet.
7. Trade-offs are made in the open.
8. Context decides.

The skill does not invent interviews, quotes, numbers or approvals, and keeps facts, assumptions and recommendations separate.

## Installation

```bash
git clone https://github.com/dannyhoang249-hub/pm-vietnamese-skill.git
cp -r pm-vietnamese-skill/skills/pm-workflow <your-agent-skills-directory>/
```

Copy the whole folder, since `SKILL.md` loads the files in `references/`.

## Usage

```text
Use pm-workflow. My manager wants in-app chat because a competitor launched it.
```

```text
Use pm-workflow to turn these interview notes into job stories. Tell me what is still missing.
```

```text
Use pm-workflow. Sprint planning is in 3 hours, users say the app is slow, and engineering wants to add caching.
```

```text
Use pm-workflow to run a decision check on this roadmap item.
```

Output is in English by default. Ask for another language or a bilingual version when you need one.

## Structure

```text
skills/pm-workflow/
├── SKILL.md                  # Principles, stages, gate, how a session runs
├── agents/openai.yaml
└── references/
    ├── problem-space.md      # Interviews, JTBD, job stories, Job Map, synthesis
    ├── prioritization.md     # Strategy, Kano, trade-offs, pushing back
    ├── solution-space.md     # Workflow, CDM/ORD, user stories, diagrams, wireframes
    ├── communication.md      # Ladder of abstraction, meeting notes
    ├── decision-check.md     # Stress-test before committing
    ├── launch-and-learn.md   # Metrics, pre-mortem, launch
    └── templates.md          # Artifact templates
```

## Upgrading from the earlier version

`pm-vietnamese`, `pm-bilingual`, `pm-karpathy-thinking` and the slash commands have been replaced by `pm-workflow`. Their feedback synthesis, meeting notes, metrics, pre-mortem, decision check and bilingual rules now live inside it. The old files remain in git history at commit `14fa030`.

## Acknowledgements

- The discovery-to-delivery method draws on the author's study in the *Breaking into Product Management* course. This is an independent, paraphrased adaptation, not affiliated with or endorsed by the course.
- Decision-check principles are adapted from [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills).

## License

[MIT](LICENSE)
