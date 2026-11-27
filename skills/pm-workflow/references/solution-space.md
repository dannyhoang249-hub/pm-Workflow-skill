# Solution space: Shape and Specify

## Contents
1. Solution direction
2. Which artifact for what
3. Workflow
4. CDM and ORD
5. User stories
6. Activity diagram
7. Wireframe
8. Delivery

Order: direction, then Workflow and CDM/ORD, then user stories, preconditions, activity diagrams, wireframes. Each one tests the previous one. When a later artifact exposes a hole, go back and fix the source.

## 1. Solution direction

Diverge before converging: consider several mechanisms, including process change, expectation-setting, and doing nothing.

A direction names the **mechanism** that closes the gap. It should be able to reject ideas. "Make it easier" rejects nothing. "A popup with a save button" has already skipped to form. "Capture the evidence at the moment of purchase" is a direction.

For each candidate: alternatives and trade-offs, other use cases it could extend to, behaviour at larger scale, conflicts with existing or planned features, risks. Review with leadership, design and engineering.

Think through all three layers of a solution: **presentation, business logic, data**. A screen description that says nothing about validation or storage is half a spec.

## 2. Which artifact for what

| Artifact | Aligns on | Owner | With |
| --- | --- | --- | --- |
| Workflow | What each role must do | PM | Design, engineering, business |
| CDM | Concepts and relationships | PM | Same, including non-technical people |
| ORD | CDM plus attributes and keys; real complexity | PM or engineer | Engineering |
| User story | A unit of user value | PM | Design, engineering |
| Activity diagram | User and system, step by step, for one story | PM, engineer or designer | Design, engineering |
| Wireframe | What is on screen and in what hierarchy | PM or designer | Design, engineering |

Skip artifacts that align nobody. A small scope may need no workflow.

## 3. Workflow

Describes **what must happen**, not how.

- Actors are people or roles. The system is not an actor.
- No mechanisms: "Verify identity", not "Click Google sign-in and call the API". Splitting a "how" into smaller steps keeps it a "how".
- Exception: a legacy constraint that cannot change within the planning horizon behaves like a requirement. Include it and mark it as a constraint.
- State preconditions and every ending, happy and unhappy.
- Start and end nodes; every action connected in and out; decision nodes phrased as questions; one consistent notation.

## 4. CDM and ORD

Do this before estimating. Three simple screens can sit on many concepts and relationships.

- Include concepts (things with data). Actions belong in the workflow. An actor may also be a concept when you store data about it.
- Label every relationship and set cardinality by asking both directions: how many B per A, how many A per B?
- Many-to-many hides a joining concept that holds data about the pair (quantity, price at time of order).
- ORD adds attributes, types, primary and foreign keys, and constraints. Do not store values derivable from others.
- Show CDM or a plain-language picture to non-technical stakeholders, ORD to engineers.
- Check the ORD against the workflow: every step's data has a home, and every object is used somewhere.
- Separate **authentication** (who you are) from **authorization** (which records you may act on). A login screen only covers the first.

## 5. User stories

`As a [role], I want to [action on the product], so that [value].`

A job story lives in problem space. A user story lives in solution space. The middle turns a wish into something doable on the product, and "so that" still points back to the job story's outcome. If the team wants a different outcome, revisit the problem openly.

**Find stories with two cuts**

- Vertical: follow the workflow, one actor action at a time.
- Horizontal: for each actor and each ORD object, walk create, read, update, delete. This exposes missing stories.

Map them: workflow steps across, stories beneath by priority, then draw the release line.

**Actors** are roles the system treats differently (permissions, screens, data). Personas, named individuals and data scopes ("teacher of course A") are not roles. Avoid a generic "user" when roles differ.

**Preconditions** (true before the story starts):
1. Who, authenticated and authorized
2. Where in the product
3. What triggers it
4. Any required state of the object

**Acceptance criteria** are observable, at least one per story, Given/When/Then where behaviour is conditional. Cover empty, loading, error and permission states where relevant. One story per independently estimable and testable action unless engineering agrees to bundle.

## 6. Activity diagram

One per user story, including the system.

- Report success only after the data change actually succeeded.
- Every branch goes somewhere. A blank branch means each developer decides differently.
- A failure branch returns to the step where the user can fix the cause, not to the start or to the same submit button. If the user cannot fix it (lost session, network), design that path separately.
- "Nothing visible happens" is a product decision; write it down.
- Do not impose input order that the product does not require.

## 7. Wireframe

Settle the backbone first: (1) navigation across screens, (2) layout of each screen, (3) information hierarchy. Visual detail comes after.

- Tier information by what the user must decide, usually found in the job story's "so I can". PM sets the priority; the designer sets how it looks.
- Every data object needs somewhere to be created, read, updated and deleted, or a stated reason why not.
- Keep first versions deliberately plain so discussion stays on need and structure.
- The first draft belongs to whoever has the most user context and the skill to draw it. Split them? Draw together.
- A clickable or AI-built prototype fits when the backbone is already settled, or the question can only be answered by clicking (can people discover a gesture, which states did nobody think of). Handing one over earlier pushes the structural thinking onto the reviewer. A design system settles appearance, not structure.

## 8. Delivery

Review stories with the team, estimate relatively (for example planning poker against agreed baselines), and plan against real capacity. Kanban suits early, fluid phases; Scrum or a hybrid suits phases with delivery commitments. The PM follows design, engineering and QA through, and keeps sales, support, marketing and customers informed.

If engineers resist, find the cause first. Bring enough technical understanding to discuss, ask rather than assert, and argue with true data. Inflating business value to win costs credibility later.
