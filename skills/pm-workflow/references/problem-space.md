# Problem space: Frame, Discover, Define

## Contents
1. Frame the question
2. Choose a research direction
3. Choose and screen participants
4. Write questions
5. JTBD, job stories and Job Map
6. Synthesize
7. Know when to stop
8. Write the problem statement
9. When you cannot talk to users

## 1. Frame the question

Real work usually starts with a high-level business problem or a request. Establish:

- **Trigger:** boss, intuition, customer feedback, sales or support, data, competitor.
- **Whose problem:** the user, the buyer, the business, and why each would care. A real pain for one party may not matter to the one who pays to fix it.
- **Value exchange:** what the company gets back for solving it. A free product still needs this answer.
- **Hidden presumptions:** a goal such as "we need to become a platform" already assumes a solution. List what must be true for it.

With strategy given from above, let it bound the research. Purely bottom-up research can surface patterns the company has no intention of acting on.

For a complaint ("it's slow"), separate three gaps before accepting any fix: reality (measured), perception (how it feels), expectation (what they now compare it to). Each calls for a different solution.

## 2. Choose a research direction

| Situation | Approach | Main risk |
| --- | --- | --- |
| Broad topic, team has not lived it | **Explore first:** 2-3 open interviews, find candidate jobs, pick one, build a Job Map, interview a narrower group | Lots of data nobody can synthesize |
| Narrower topic or real domain knowledge | **Hypothesize and adjust:** assumed JTBD and Job Map as scaffold, interview, correct where reality differs | Interviews turn into a hunt for confirmation |

Avoid locking a cause into the topic ("X happens because Y"). It leaves no fallback and filters out people who would disprove Y.

## 3. Choose and screen participants

- Define people by **situation and behaviour**. Job title and age do not reveal the job they are trying to get done. The same symptom (missed deadlines) can come from unrelated causes.
- Exploring: wide on context, strict on behaviour. Each person must have actually experienced the thing.
- Screeners ask for **countable facts** ("How many times in the past month...?"). Avoid yes/no questions that reveal the wanted answer, and avoid asking people to diagnose their own cause.
- Screen for the phenomenon, not the suspected cause. Deliberately include people who could disprove the hypothesis.
- Check the sample for sameness. People from one network often look alike.

## 4. Write questions

Keep two lists. **Research questions** are what the team needs to know (few, and each affects a decision). **Interview questions** are what you ask so you can infer those answers. If the two lists look the same, rewrite.

Fix a weak question by keeping what you want to learn and anchoring it to something that happened.

| Weak | Why | Better |
| --- | --- | --- |
| Why do you struggle with expense reports? | Invites a theory | Tell me about the last report you filed. |
| How often do you usually...? | Invites an average | What did you do the last three times? |
| What features would you want? | Asks them to design | What did you do when it didn't work? |
| Tell me about your week. | No anchor to the topic | Walk me through the last time you paid for something for work. |

Useful probes: What happened just before? What did you do next? What did it cost you? What triggered you to start? When did you last skip it, and what took priority? Ask "why" only about a specific event they just described.

Test each question by imagining the answer. "I think..." means you asked for opinion. "Usually..." means abstraction. "Last Tuesday..." means behaviour.

In the session, let the user do most of the talking, treat compliments and hypotheticals with suspicion, and notice emotion because it marks impact. Shallow answers are usually fixed by better questions and follow-ups, not by blaming the participant or adding more interviews.

## 5. JTBD, job stories and Job Map

**Jobs-to-be-done:** people "hire" something to make progress in a situation. The job belongs to the user. The company only uncovers it.

**Job story:** `When [situation], I want to [motivation], so I can [desired outcome].`

- The situation carries tension, constraints and a consequence if nothing changes. If there is none, dig deeper or drop it.
- Keep context out of the motivation slot.
- Keep solutions out. "I want to set a reminder" is already a mechanism; "I want to not miss the submission date" is a motivation.

**Hires:** list everything currently used for the job: products, manual workarounds, other people, communities, failed attempts, doing nothing.

**Job Map:** the steps of the job, independent of any solution: Define, Locate, Prepare, Confirm, Execute, Monitor, Modify, Conclude. Under each, write concrete job steps, then insights.

- Before interviews it is a question scaffold, so coverage is not limited to Execute.
- Afterwards it organizes evidence. Crowded steps suggest opportunity. An empty step may mean you never asked.
- Rename, split or merge steps when evidence says so.
- A Job Map is not a Workflow. The first lives in problem space, the second in solution space.

## 6. Synthesize

1. **Climb down.** For each raw excerpt, fill the gaps: trigger, context, motivation, desired outcome, consequence. Follow up if they are missing.
2. **Code.** Label excerpts, compare within and across people, group codes into themes. Go back to the field as questions sharpen. Collection and analysis alternate.
3. **Climb up.** Group by shared job, not shared surface behaviour. Three people may all double-check an output for three different reasons; those are separate jobs until more evidence merges them.

## 7. Know when to stop

Stop when the team can place a defensible bet and the market or a small release can answer the rest. Interview counts and "saturation" are only reference points: a narrow sample saturates early and falsely. If a problem showed up in one person, expand within people like them before committing serious resources.

## 8. Write the problem statement

Include: subject, situation, current reality, desired reality, the gap and its consequence, evidence, current hires, open assumptions.

Check the altitude. It should leave several ways to solve it, be narrow enough to test, and claim only what the data says.

| Failure | Looks like |
| --- | --- |
| Solution inside | "Users lack an auto-fill button" |
| Too high | "Finance workflows are inefficient" |
| Echoed suggestion | "Users need a mobile app" |
| Invented cause | "Users forget because they are undisciplined" |

Better: "Sales reps who pay client costs out of pocket file claims weeks later, lose receipts in between, and absorb the unreimbursed amount."

## 9. When you cannot talk to users

Shadow sales demos, review support tickets with original quotes, run a weekly problem review with customer-facing teams, watch session recordings and usage data, read the communities where users ask for help. Find out why access is blocked and whether it can be changed. Mark findings from proxies as lower confidence.
