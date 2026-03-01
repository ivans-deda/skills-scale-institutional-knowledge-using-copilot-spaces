# OctoAcme Project Management — Documentation Hub

Welcome to OctoAcme's project management documentation. This README provides a quick-reference overview of how OctoAcme plans, executes, and ships projects. Whether you're a new team member getting up to speed or a seasoned contributor looking for a refresher, this guide is your starting point. For deeper detail on any topic, follow the links to the dedicated documents in this folder.

---

## Table of Contents

- [Framework & Principles](#framework--principles)
- [Project Lifecycle](#project-lifecycle)
- [Core Roles & Responsibilities](#core-roles--responsibilities)
- [Communication Cadence](#communication-cadence)
- [Quality Assurance Practices](#quality-assurance-practices)
- [Risk Management & Escalation](#risk-management--escalation)
- [Document Index](#document-index)

---

## Framework & Principles

OctoAcme uses a lightweight, iterative project management framework designed for cross-functional product and engineering teams. The framework is grounded in five core principles that guide every decision from initiation through retrospective:

- **Customer-first** — Always prioritize customer value and usability. Every feature, change, and trade-off is evaluated against its impact on the people who use our products.
- **Iterative delivery** — Ship small, testable increments rather than large monolithic releases. Shorter feedback loops reduce risk and allow us to course-correct quickly.
- **Clear ownership** — Every project has a named Project Manager and Product Lead. Ambiguity in ownership is one of the most common causes of missed deadlines and dropped work.
- **Data-informed decisions** — Measure impact, monitor key signals, and use evidence to prioritize next steps. Intuition is valuable; evidence makes it actionable.
- **Psychological safety** — Encourage candid feedback, celebrate learning from mistakes, and create an environment where team members feel safe raising concerns early.

→ See [octoacme-project-management-overview.md](./octoacme-project-management-overview.md) for the complete framework overview.

---

## Project Lifecycle

All OctoAcme projects follow a five-phase lifecycle. Each phase has defined goals, minimum deliverables, and a decision gate before moving forward.

1. **Initiation** — Validate the business need, align stakeholders, and decide go/no-go. Key deliverables include a Project One-pager, a stakeholder list, a high-level timeline, and an initial risk list.

2. **Planning** — Convert the approved initiative into an actionable backlog. Activities include a kickoff meeting, backlog prioritization with acceptance criteria, dependency mapping, and creation of a release plan and milestone map.

3. **Execution** — Build, test, review, and iterate. The team follows a daily standup rhythm, uses a project board to track work in progress, and applies PR and CI conventions to maintain quality throughout development.

4. **Release** — Deploy the increment, verify it in production, and communicate to stakeholders. Releases are categorized as patch, minor, or major, and every release requires passing CI/security scans, smoke tests, and documented rollback plans.

5. **Close & Retrospective** — Capture learnings, celebrate wins, and convert improvement ideas into backlog items with clear owners and due dates. Retrospectives run after each sprint, release, or major milestone.

→ Detailed guidance for each phase:
- [octoacme-project-initiation.md](./octoacme-project-initiation.md)
- [octoacme-project-planning.md](./octoacme-project-planning.md)
- [octoacme-execution-and-tracking.md](./octoacme-execution-and-tracking.md)
- [octoacme-release-and-deployment.md](./octoacme-release-and-deployment.md)
- [octoacme-retrospective-and-continuous-improvement.md](./octoacme-retrospective-and-continuous-improvement.md)

---

## Core Roles & Responsibilities

OctoAcme projects are staffed with four primary roles. Each role has distinct responsibilities, and healthy collaboration between them is critical to delivery.

- **Project Manager (PM)** — Coordinates delivery activities, maintains project plans and timelines, manages risks and dependencies, facilitates key meetings (kickoff, planning, retrospectives), and ensures consistent status reporting across stakeholders.

- **Product Manager (PdM)** — Defines what should be built and why. Owns the product vision, prioritizes the roadmap and backlog, collaborates with engineering on trade-offs, and validates outcomes through user research and metrics.

- **Developers** — Design, implement, and maintain software components. Write and maintain tests and documentation, participate in design and code reviews, assist with estimation, and help identify technical risks early.

- **QA/Testing** — Validate quality and acceptance criteria at every stage of the lifecycle. Define test plans, execute manual and automated tests, and serve as a quality gate before features are released to production.

→ See [octoacme-roles-and-personas.md](./octoacme-roles-and-personas.md) for full role definitions including goals and typical communication patterns.

---

## Communication Cadence

Consistent, predictable communication keeps teams aligned and surfaces blockers before they become critical. OctoAcme uses the following default cadence, which teams adapt to their size and context:

- **Daily standups (15 min)** — Focus on progress since yesterday, plans for today, and any blockers or dependencies. Standups are time-boxed and action-oriented; in-depth discussions are taken offline.
- **Weekly PM + PdM sync** — Align on roadmap status, resurface risks, review the Risk Register, and plan stakeholder communications for the week.
- **Weekly delivery sync** — Broader team check-in covering sprint progress, demo previews, and flagged risks. Risk Register is reviewed and updated.
- **Monthly stakeholder updates** — Written or presented summary of project health, milestone progress, upcoming decisions, and any asks from leadership.
- **Ad-hoc escalations** — For blockers that cannot wait for the regular cadence, follow the escalation path described in the Risk Management section below.

→ See [octoacme-risks-and-communication.md](./octoacme-risks-and-communication.md) for communication templates and escalation paths.

---

## Quality Assurance Practices

Quality is embedded throughout the lifecycle rather than bolted on at the end. The following practices apply across all project phases:

- **Unit tests** — Required for all new logic. Developers own unit test coverage and maintain it as part of their Definition of Done.
- **Integration tests** — Applied where components interact with external systems, APIs, or databases, to catch contract and behavioral regressions.
- **End-to-end smoke tests** — Run against critical user flows before every release to verify that the most important paths through the product are working correctly.
- **Security scanning** — Automated security scans run in CI on every pull request. Findings must be triaged before a release ships.
- **PR workflow** — Pull requests are kept small (≤ 400 lines when possible), linked to their issue and acceptance criteria, and require at least one approval plus passing CI before merging.
- **Manual QA** — Feature acceptance testing is performed by QA/Testing for significant or user-facing changes before they advance to release.

→ See [octoacme-execution-and-tracking.md](./octoacme-execution-and-tracking.md) for the full PR workflow and QA checklist.

---

## Risk Management & Escalation

Risks are identified early, tracked centrally, and reviewed regularly. OctoAcme uses a Risk Register as the single source of truth for project risk.

**Risk Register columns:** ID · Description · Impact (High/Med/Low) · Likelihood (High/Med/Low) · Owner · Mitigation plan · Status

The risk lifecycle follows four steps: **Identify** (during planning and ongoing execution) → **Assess** (estimate impact and likelihood) → **Mitigate** (define actions and contingency plans) → **Monitor** (review at weekly syncs and update status).

When a risk materializes into a blocker, OctoAcme uses a three-level escalation path:

- **Level 1 — Team triage:** Raised and discussed in the daily standup. The team attempts to resolve within the sprint.
- **Level 2 — PM escalation:** PM escalates to Product Lead and any dependent teams if the blocker cannot be resolved at the team level.
- **Level 3 — Sponsor escalation:** For business-impacting issues, the PM escalates to the project sponsor for executive decision-making or resource intervention.

Security incidents follow a separate runbook and require immediate notification of the Security on-call team.

→ See [octoacme-risks-and-communication.md](./octoacme-risks-and-communication.md) for the full Risk Register template and communication templates.

---

## Document Index

| Document | Description |
|---|---|
| [octoacme-project-management-overview.md](./octoacme-project-management-overview.md) | Framework overview: principles, roles, lifecycle, key artifacts |
| [octoacme-project-initiation.md](./octoacme-project-initiation.md) | Initiation phase: one-pager template, stakeholder alignment, decision gate |
| [octoacme-project-planning.md](./octoacme-project-planning.md) | Planning phase: backlog, estimation, release plan, Definition of Done |
| [octoacme-execution-and-tracking.md](./octoacme-execution-and-tracking.md) | Execution phase: team rhythm, PR workflow, QA, metrics, escalation |
| [octoacme-release-and-deployment.md](./octoacme-release-and-deployment.md) | Release phase: deployment checklist, rollback playbook, release notes template |
| [octoacme-retrospective-and-continuous-improvement.md](./octoacme-retrospective-and-continuous-improvement.md) | Close phase: retrospective structure, action item tracking, continuous improvement |
| [octoacme-roles-and-personas.md](./octoacme-roles-and-personas.md) | Role definitions: PM, PdM, Developers, QA — goals and communication patterns |
| [octoacme-risks-and-communication.md](./octoacme-risks-and-communication.md) | Risk Register, escalation paths, stakeholder communication templates |
