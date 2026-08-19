# PM Vietnamese Copilot

A claude-sonnet-5-sonnet-5 plugin and reusable PM skill for turning incomplete product-management input into clear decisions, execution-ready artifacts, and measurable plans.

The plugin is designed for Vietnamese-speaking product teams, while supporting English and Vietnamese-English bilingual deliverables. It combines practical PM workflows with a Karpathy-inspired decision-quality gate: clarify before acting, prefer the smallest useful scope, make changes surgically, and define how results will be verified.

## What it provides

### Skills

| Skill | Purpose |
| --- | --- |
| `$pm-vietnamese-copilot` | End-to-end PM workflow for discovery, PRDs, user stories, prioritization, metrics, feedback, meetings, stakeholder updates, and pre-mortems. |
| `$pm-bilingual-copilot` | Vietnamese-English PM artifacts that preserve meaning across languages for product, engineering, and stakeholder handoffs. |
| `$pm-karpathy-thinking` | Decision-quality review for ambiguous, solution-led, risky, or over-scoped product proposals. |

### Commands

| Command | Use it for | Output |
| --- | --- | --- |
| `/discover` | Clarifying an idea, problem, or user need | Discovery brief, assumptions, risks, and the smallest useful validation |
| `/write-prd` | Defining a feature or product requirement | Lean PRD, scope, success metrics, risks, and release plan |
| `/write-stories` | Breaking work down for a delivery team | User stories, acceptance criteria, edge cases, dependencies, and analytics |
| `/prioritize` | Choosing what to do first | Decision memo with RICE-style comparison, confidence, assumptions, and recommendation |
| `/plan-metrics` | Designing measurement for a product goal | North Star metric, input metrics, guardrails, and tracking plan |
| `/analyze-feedback` | Synthesizing interviews, surveys, reviews, or support tickets | Themes, evidence, opportunities, and next actions |
| `/meeting-notes` | Turning meeting notes into follow-through | Decisions, action items, owners, and deadlines |
| `/pre-mortem` | Reviewing launch or execution risk | Tigers, Paper Tigers, Elephants, mitigations, and go/no-go checklist |
| `/decision-check` | Challenging a decision, scope, roadmap item, or PRD | Facts, assumptions, simpler options, risks, and a measurable decision loop |

Commands are optional. For simple requests, invoke a skill directly or describe the desired outcome in natural language.

## Language behavior

- **Vietnamese:** Used when the request is written in Vietnamese or explicitly asks for Vietnamese.
- **English:** Used when the request is written in English or explicitly asks for English.
- **Bilingual Vietnamese-English:** Used when the request includes `bilingual`, `VI/EN`, or `song ngữ`, or when the audience is explicitly mixed.

Bilingual output uses Vietnamese-English headings and translates decision-critical content such as requirements, metric definitions, acceptance criteria, and action items. It avoids mechanically duplicating every sentence.

## Decision-quality principles

Before producing a major artifact, the skills apply four principles:

1. **Think before acting** — separate facts, assumptions, unknowns, interpretations, and trade-offs.
2. **Simplicity first** — prefer the smallest experiment, scope, or release that can create value or learning.
3. **Surgical scope** — keep each requirement traceable to a user outcome, risk, or constraint.
4. **Goal-driven execution** — define `success criteria → signal → decision` before committing significant resources.

The skills do not invent metrics, customer quotes, research findings, market facts, or stakeholder approval. Unknowns are labeled as assumptions and paired with the cheapest useful validation when appropriate.

## Installation for claude-sonnet-5-sonnet-5 Code

### Install from the marketplace

Add this repository as a claude-sonnet-5-sonnet-5 plugin marketplace and install the plugin:

```bash
claude plugin marketplace add dannyhoang249-hub/pm-vietnamese-copilot
claude plugin install pm-vietnamese-copilot@pm-vietnamese-copilot
```

Start a new claude-sonnet-5-sonnet-5 conversation after installation so the plugin metadata and skills are loaded.

### Install locally for development

Clone the repository and add it as a local marketplace:

```bash
git clone https://github.com/dannyhoang249-hub/pm-vietnamese-copilot.git
cd pm-vietnamese-copilot
claude plugin marketplace add .
claude plugin install pm-vietnamese-copilot@pm-vietnamese-copilot
```

After changing skill or command files, reinstall or update the local plugin and start a new conversation.

## Usage examples

### Invoke a skill

```text
Use $pm-vietnamese-copilot to turn these rough notes into a lean PRD in English. Separate facts, assumptions, and recommendations.
```

```text
Dùng $pm-vietnamese-copilot để chuyển các ghi chú dưới đây thành PRD tiếng Việt cho tính năng đặt lịch khám.
```

```text
Use $pm-bilingual-copilot to turn these meeting notes into a Vietnamese-English decision record for product and engineering.
```

```text
Use $pm-karpathy-thinking to stress-test this feature proposal before we commit engineering time. Recommend proceed, simplify, or validate first.
```

### Invoke a command

```text
/discover Online sellers abandon the product-creation flow when they have to add items one at a time.
```

```text
/write-prd Add Excel import for a seller-management application.
```

```text
/prioritize Choose between a new onboarding flow, Excel import, and re-engagement reminders. The quarterly goal is activation.
```

```text
/meeting-notes
[paste the meeting transcript or notes here]
```

```text
/decision-check We are planning to build an analytics dashboard with 25 metrics before next quarter.
```

To request bilingual output, add an explicit instruction such as:

```text
Return the artifact in Vietnamese and English (VI/EN). Keep assumptions labeled and avoid duplicating non-critical explanation.
```

## Supported PM outputs

The skills can produce:

- Discovery briefs and problem statements
- Lean PRDs and feature specifications
- User stories and delivery backlogs
- Prioritization and roadmap decision memos
- OKR, North Star, and measurement plans
- Experiment plans and validation proposals
- Customer-feedback synthesis
- Meeting decision records and stakeholder updates
- Pre-mortems and launch-readiness reviews
- Decision-quality reviews with proceed, simplify, or validate recommendations

## Repository structure

```text
.
├── .claude-plugin/
│   ├── marketplace.json       # claude-sonnet-5-sonnet-5 marketplace metadata
│   └── plugin.json            # Plugin metadata
├── commands/                  # Slash-command workflows
├── references/                # Vietnamese and bilingual PM templates
├── skills/
│   ├── pm-vietnamese-copilot/
│   │   ├── SKILL.md
│   │   ├── agents/
│   │   └── references/
│   ├── pm-bilingual-copilot/
│   │   ├── SKILL.md
│   │   ├── agents/
│   │   └── references/
│   └── pm-karpathy-thinking/
│       ├── SKILL.md
│       └── agents/
├── SKILL.md                   # Root-compatible PM skill entry point
└── LICENSE
```

## Customization

- Update `references/templates-vi.md` for team-specific Vietnamese document formats.
- Update `references/templates-bilingual.md` for approved Vietnamese-English terminology.
- Adjust files in `commands/` to match your product-development framework, naming conventions, or release process.
- Keep `SKILL.md` and `skills/pm-vietnamese-copilot/SKILL.md` aligned when changing core behavior.

## Acknowledgements

The decision-quality principles are adapted for product management from [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills). This project does not copy the source coding skill; it applies the underlying principles to PM discovery, prioritization, documentation, and execution.

## License

[MIT](LICENSE)