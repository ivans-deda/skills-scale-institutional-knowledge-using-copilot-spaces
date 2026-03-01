# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

**Example Risk Register entry:**

| ID | Description | Impact | Likelihood | Owner | Mitigation | Status |
|----|-------------|--------|------------|-------|------------|--------|
| R-01 | Third-party API deprecation in Q3 | High | Med | Dev Lead | Evaluate alternatives by end of sprint 4 | Active |
| R-02 | Key team member leave during release week | Med | Low | PM | Cross-train backup; document runbook | Monitoring |

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based)
- Use a single source of truth (project README or release doc) for status

## Communication Templates

### Weekly Status Update
**Subject:** [Project Name] — Weekly Status Update, [Date]

```
**Overall Status:** 🟢 On Track / 🟡 At Risk / 🔴 Blocked

**Progress this week:**
- [Completed item 1]
- [Completed item 2]

**Next steps (upcoming week):**
- [Planned item 1]
- [Planned item 2]

**Risks & blockers:**
- [Risk/blocker description] — Owner: [Name] — Mitigation: [Action]

**Asks / decisions needed:**
- [Decision or action needed from stakeholder, with deadline]
```

**Example:**
> **Overall Status:** 🟡 At Risk
>
> **Progress this week:** Completed authentication module; API integration 70% done.
>
> **Next steps:** Finalize API integration; begin QA testing of auth flow.
>
> **Risks & blockers:** Third-party payment sandbox is intermittently unavailable — Owner: Dev Lead — Mitigation: Opened support ticket #4521; fallback to mock in CI.
>
> **Asks / decisions needed:** Approval needed from Legal on updated ToS copy by Friday to stay on schedule.

---

### Milestone Update
**Subject:** [Project Name] — Milestone [X] Complete / [Milestone Name]

```
**Milestone:** [Name]
**Status:** Completed / Delayed / At Risk
**Original target date:** [Date]
**Actual / revised date:** [Date]

**What was delivered:**
- [Deliverable 1]
- [Deliverable 2]

**What was deferred and why:**
- [Item deferred] — Reason: [explanation]

**Next milestone:** [Name] — Target: [Date]
**Key risks heading into next milestone:**
- [Risk description]
```

---

### Incident Response Communication
**Subject:** [INCIDENT] [Severity: P1/P2/P3] — [Brief description] — [Date/Time]

```
**Incident summary:** [One-sentence description of what is impacted]
**Severity:** P1 (critical) / P2 (major) / P3 (minor)
**Detected at:** [Timestamp]
**Current status:** Investigating / Mitigating / Resolved

**Impact:**
- [Who/what is affected and to what degree]

**Actions being taken:**
- [Immediate action 1] — Owner: [Name]
- [Immediate action 2] — Owner: [Name]

**Expected resolution timeline:** [Best estimate or "TBD — next update in 30 min"]

**Next update at:** [Timestamp]
```

**Post-incident follow-up (after resolution):**
- Root cause identified: [Yes/No — brief description]
- Blameless retrospective scheduled: [Date]
- Action items logged in: [project backlog / Risk Register]

---

## Communication Checklist by Phase

| Phase | Communication Action | Owner | Cadence |
|-------|---------------------|-------|---------|
| Initiation | Share Project One-pager with stakeholders | PM | Once |
| Planning | Send kickoff summary and milestone plan | PM | Once |
| Execution | Weekly status update to stakeholders | PM | Weekly |
| Execution | Risk Register review with team | PM + Team | Weekly |
| Release | Pre-release go/no-go notification | PM | Per release |
| Release | Release announcement with notes | PM | Per release |
| Close | Retrospective summary shared with team | PM | Per retro |
| Ongoing | Escalation notification (if needed) | PM | As needed |

## Escalation Paths

OctoAcme uses a three-level escalation path with defined response time expectations:

- **Level 1 — Team triage:** Raised in daily standup. Team attempts to resolve within the **current sprint (≤ 5 business days)**. Owner: team member who identified the blocker.
- **Level 2 — PM escalation:** If unresolved at Level 1, PM escalates to Product Lead and dependent teams within **1 business day** of identifying the blocker as sprint-blocking.
- **Level 3 — Sponsor escalation:** For business-impacting issues (e.g., missed external deadlines, budget decisions, cross-org dependencies), PM escalates to the project sponsor within **4 hours** of confirming business impact.

**When to escalate immediately (skip Level 1):**
- A blocker directly impacts an external customer commitment or contractual deadline
- A security vulnerability is discovered in production
- A key dependency team is unresponsive for more than 2 business days

For security incidents, follow the security incident runbook and notify Security on-call immediately, regardless of the above timeline.
