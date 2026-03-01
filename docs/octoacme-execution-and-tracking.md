# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Dependency Management

Cross-team and external dependencies must be tracked explicitly to avoid surprises late in the sprint or release cycle.

**Tracking dependencies with the Risk Register:**
- Every external dependency (another team, third-party service, or external approval) should be logged as a risk in the [Risk Register](./octoacme-risks-and-communication.md) with Impact, Likelihood, and an Owner.
- Dependencies that block a milestone should be escalated to **Level 2** immediately (see [Escalation Paths](./octoacme-risks-and-communication.md#escalation-paths)).
- Review all open dependency risks at the weekly delivery sync and update their status.

**Cross-team dependency checklist:**
- [ ] Dependency identified and described (what is needed, from whom, by when)
- [ ] Logged in the Risk Register with ID, owner, and mitigation plan
- [ ] Counterpart team or owner notified and date confirmed
- [ ] Dependency linked to the relevant GitHub Issue or milestone
- [ ] Fallback plan documented if dependency is not delivered on time
- [ ] Status reviewed at weekly delivery sync until resolved

**Examples of dependency tracking in practice:**
- *API contract with Platform team:* Logged as R-03 in Risk Register. Owner: Backend Lead. Mitigation: Use mock API for development; confirm final contract by Sprint 3 end. Status updated weekly.
- *Design assets from Design team:* Logged as R-07. Owner: PM. Dependency flagged in sprint planning; assets confirmed received and linked in issue #45.
- *Legal approval for new data fields:* Logged as R-12. Escalated to Level 2 (PM → Product Lead) after 3-day delay. Fallback: ship feature behind a flag pending approval.

**Marking dependencies in GitHub Issues:**
- Use the `dependency` label on issues that are blocked by external work.
- Reference the blocking issue or external ticket in the issue description.
- Add a comment when the dependency is resolved, linking to the deliverable or confirmation.

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

See [octoacme-risks-and-communication.md](./octoacme-risks-and-communication.md) for escalation timelines and response expectations.

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] Cross-team dependencies identified, logged in Risk Register, and owners notified
