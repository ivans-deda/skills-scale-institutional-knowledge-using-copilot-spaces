# OctoAcme — Retrospective & Continuous Improvement

## Purpose
Capture learnings and convert them into actionable improvements.

## When
After each sprint, release, or important milestone. Also after incidents.

## Structure
- What went well
- What could be improved
- Action items (owner, due date)
- Follow-up on previous action items

## Running a Retrospective
- Timebox: 45–75 minutes depending on team size
- Use an anonymous idea board if needed to encourage candor
- Prioritize 2–3 top action items to avoid overload

## Action Item Tracking Workflow

Retrospective action items must be traceable from identification through completion:

1. **Capture** — During the retrospective, record each action item using the template below.
2. **Log** — After the meeting, the PM or facilitator creates a GitHub Issue (or equivalent backlog item) for each action item. Tag issues with `retro-action` for easy filtering.
3. **Prioritize** — Action items are added to the project backlog and prioritized against other work in the next sprint planning session. Items with high impact or low effort are fast-tracked.
4. **Assign** — Each action item must have a named owner and a due date before the retro session closes.
5. **Review** — Outstanding action items are reviewed at every **weekly PM sync**. The PM checks status, unblocks owners, and escalates if items are stale (no progress for 2+ weeks).
6. **Close** — When the owner completes the action, they update the linked issue with evidence of completion (e.g., merged PR, updated doc, process change confirmed by team) and mark it Done.

**Action item lifecycle states:** Open → In Progress → Blocked → Done

## Example Action Item Template
- Title:
- Description:
- Owner:
- Due date:
- Success criteria:
- Linked issue/backlog item: [To be added after issue is created — see Action Item Tracking Workflow step 2]

## Impact Measurement Framework

Not all improvements are equal. Use this framework to evaluate the impact of completed action items:

| Dimension | How to Measure | Example |
|-----------|---------------|---------|
| **Process efficiency** | Reduction in time spent on a recurring task | PR review cycle time dropped from 3 days to 1 day |
| **Quality** | Change in defect rate, escaped bugs, or test coverage | Regression count per release reduced by 40% |
| **Team health** | Survey scores, reduced meeting overload, fewer blockers | Team satisfaction score improved in next retro |
| **Delivery predictability** | Sprint completion rate, milestone hit rate | Milestone hit rate improved from 70% to 90% |

**Measurement cadence:** Evaluate impact of completed action items during the following retrospective. Include a brief "Did it work?" summary for each closed item.

## Tracking Improvements
- Add action items to the project backlog or issues with clear owners and timelines
- Review outstanding actions in the weekly PM sync
- Use the `retro-action` label in GitHub Issues to filter and report on all open improvements

## Continuous Improvement Culture
- Measure impact of action items
- Celebrate improvements and make small, iterative changes
- Share wins at team demos or in the weekly update to reinforce the habit of acting on retro feedback
