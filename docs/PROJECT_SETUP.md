# EnerLint GitHub Project — live board operating guide

**Updated:** 27 October 2026 · **Project:** [EnerLint | Development & Research Roadmap](https://github.com/orgs/Open-Energy-Methods/projects/1) · **Project v2 number:** 1

This is an *existing* organization GitHub Project—not a request to create another one. It currently holds the EnerLint scientific tickets. For at least October 2026–October 2027, Open Energy Methods is Abhijith's independent open engineering research workbench, not a commercial venture or staffed institute.

## Important access boundary

Connected GitHub repository tools can edit issue content, issue labels, assignees, milestones and state. They **cannot currently mutate GitHub Projects v2 item Status, Priority, Estimate, Start date or Target date fields; nor can they rename/edit Project views**, because those fields and layouts require organization Projects GraphQL permissions that are not exposed by the connected tool.

An issue label like `workflow:in-progress` is useful metadata but **does not itself move the Project item to the In Progress column**. An issue's planning date in its body is likewise **not** the Project's native Target date.

The instructions below are an exact owner-facing finishing checklist. Avoid saying the Project view was updated unless its native field has actually been changed and verified.

## Live views and desired configuration

### [1 · Backlog](https://github.com/orgs/Open-Energy-Methods/projects/1/views/1)

**Use:** all uncommitted research problems, future experiments and optional explorations.

- **Layout:** Table.
- **Filter:** `status:Backlog`, optionally `is:open` if supported by the Projects filter.
- **Fields:** Title, Status, Priority, Estimate, Assignees, Labels, Milestone.
- **Sort:** Priority then estimate/size where supported.
- **Rule:** don't push G2/G3 external-review or commercial ideas into the active sprint just to make the board look busy.

### [2 · Priority board](https://github.com/orgs/Open-Energy-Methods/projects/1/views/2)

**Use:** the day-to-day Kanban, with real WIP limits.

- **Layout:** Board grouped by **Status** (not by cosmetic priority labels).
- **Columns:** Backlog · To Do · In Progress · In Review · Blocked · Done. Map any existing status choices to these names; create missing choices only if necessary.
- **Filter:** current two-week research tasks where practical (e.g. `label:sprint:S0`), or retain all items but visually prioritize the current sprint. GitHub Projects filters can use issue labels when they're on the synced item.
- **Card fields:** Priority, Estimate, Assignees, Target date.
- **WIP limit:** at most **two** In Progress issues for a solo maintainer. Prefer one. Never count To Do as begun.
- **Definition of Done:** acceptance evidence linked, applicable CI green, rights/claims respected, issue closed **completed**, Project Status Done. Close `not_planned` issues as Won't Do—not Done.

### [3 · Team items → recommended rename: Maintainer workload](https://github.com/orgs/Open-Energy-Methods/projects/1/views/3)

**Use:** clarify what Abhijith owns and what remains unclaimed rather than imply a research staff/team.

- **Layout:** Table grouped by Assignees (currently this tab already groups assigned and unassigned issues).
- **Filter:** open items; show active To Do / In Progress / In Review / Blocked first; hide future Backlog if it obscures current workload.
- **Fields:** Status, Priority, Estimate, Start date, Target date, Labels, Milestone.
- **Owner:** assign current sprint work to `abhijith-sivaprasadan`. Do not assign future reviewers or collaborators without consent.
- **Interpretation:** 30 unassigned backlog items are future possibilities, not overdue tasks or a team staffing gap.

### [4 · Roadmap](https://github.com/orgs/Open-Energy-Methods/projects/1/views/4)

**Use:** a credible sequence of research questions, not a fake product/company launch calendar.

- **Layout:** Roadmap/time scale using Project **Start date** and **Target date**.
- **Fields:** Title, Status, Priority, Milestone, Estimate.
- **Time horizon:** 27 October–9 November for the current execution slice, with next-stage work later only as tentative planning.
- **Only date issues with real near-term intent**. Treat independent reviewer feedback, external data rights and third-party solver comparisons as *dependencies*, not date promises.
- **Roadmap sequence:** boundary/contracts → evidence claim policy → property/datum constraints → CI audit → alpha release decision. External validation remains subsequent work.

### [5 · My items](https://github.com/orgs/Open-Energy-Methods/projects/1/views/5)

**Use:** the personal research queue.

- **Layout:** Table or Board, filtered `assignee:@me` and open work.
- **Group/sort:** Status first, then Priority and nearest Target date.
- **Fields:** Status, Priority, Target date, Estimate; hide the unnecessary Team/Size duplication.
- **Expected current workload:** five explicitly assigned research/maintenance issues. Closed-completed issues may be shown in a separate delivered/retrospective view, but not mixed with open work.

## Two-week S0 owner queue (27 October–9 November 2026)

The **issue records** below have been updated with assignee, labels, estimates, exact planning dates and acceptance conditions. Project fields still require owner-side entry until an authorized Projects integration is available.

| Issue | Planned Project Status | Priority | Estimate | Start | Target |
|---|---|---|---:|---|---|
| [EnerLint #8 — Physical control-volume contracts](https://github.com/Open-Energy-Methods/enerlint/issues/8) | **In Progress** | P0 | 5 | 27 Oct | **31 Oct** |
| [EnerLint #6 — Scientific evidence/claim policy](https://github.com/Open-Energy-Methods/enerlint/issues/6) | To Do | P0 | 2 | 1 Nov | **2 Nov** |
| [EnerLint #15 — Property/datum acceptance policy](https://github.com/Open-Energy-Methods/enerlint/issues/15) | To Do | P0 | 3 | 2 Nov | **5 Nov** |
| [EnerLint #16 — CI, security and reproducibility](https://github.com/Open-Energy-Methods/enerlint/issues/16) | To Do | P0 | 3 | 5 Nov | **7 Nov** |
| [EnerLint #5 — Alpha release-readiness metadata](https://github.com/Open-Energy-Methods/enerlint/issues/5) | To Do | P0 | 2 | 7 Nov | **9 Nov** |

**Total outstanding committed effort: 15 estimated points, not a promise of 15 hours.** Estimates may be revised after S0. This roster supersedes any startup-first sprint template that presumes KTH Innovation outreach or venture preparation must be delivered this month.

Already completed and suitable for Done **only if their items are present in the Project**: [#13 distribution installation](https://github.com/Open-Energy-Methods/enerlint/issues/13), [#17 benchmark case-card specification](https://github.com/Open-Energy-Methods/enerlint/issues/17), and [#7 report schema](https://github.com/Open-Energy-Methods/enerlint/issues/7). Each issue is closed as completed and has a `workflow:done` label.

**Keep in Backlog:** [#3 external tolerance critique](https://github.com/Open-Energy-Methods/enerlint/issues/3), [#9 ten reviewed analytical reference cases](https://github.com/Open-Energy-Methods/enerlint/issues/9), [#18 native-tool comparative experiment](https://github.com/Open-Energy-Methods/enerlint/issues/18), [#25 independent review](https://github.com/Open-Energy-Methods/enerlint/issues/25), and conditional new research domains. These require separate bounded tasks, real external evidence or reviewers.

## Exact finishing operations in the GitHub UI

1. In the [Project](https://github.com/orgs/Open-Energy-Methods/projects/1), use **Backlog** table and search by `#8`, `#6`, `#15`, `#16`, `#5` (or find each issue by its title). For those existing items, enter Project **Status** values from the table. Do not make duplicate project items.
2. Populate the existing Project **Priority** field as `P0` for those five, **Estimate** as 5/2/3/3/2 and **Start date/Target date** as above. If the board offers `Size` instead of Estimate, select one canonical effort field rather than both.
3. For **Priority board**, group by Status; keep one In Progress item. For **Team items**, optionally rename to `Maintainer workload`. For **My items**, set the assignee filter to `@me`.
4. For **Roadmap**, select the new populated date fields and verify five entries are visible in the intended window.
5. In **Workflows**, confirm the native rules `Item closed → Done` and `Item reopened → Backlog` are configured. This is independent of the issue-label workflow. Ensure `Closed as not planned` does not enter Done for delivery metrics.
6. Preserve/snapshot [Backlog](https://github.com/orgs/Open-Energy-Methods/projects/1/views/1), [Priority board](https://github.com/orgs/Open-Energy-Methods/projects/1/views/2), [Maintainer workload](https://github.com/orgs/Open-Energy-Methods/projects/1/views/3), [Roadmap](https://github.com/orgs/Open-Energy-Methods/projects/1/views/4), and [My items](https://github.com/orgs/Open-Energy-Methods/projects/1/views/5), and verify the same five issues appear consistently. A connected repo tool cannot confirm Project-field writes.

## Ongoing lifecycle for our future work

- When a real task starts: update the issue `workflow:todo → workflow:in-progress`, add a concise implementation note, and **also** move its Project Status to `In Progress` through an authorized Project interface.
- When a result is ready for review: change label to `workflow:in-review` and Project Status to `In Review`, include exact commits, tests and CI evidence.
- When accepted: close issue as **completed** (the repository workflow applies `workflow:done`); verify Project Status **Done**, either via an enabled Project automation or a manual field edit.
- When blocked: put a short public-safe blocker explanation in the issue, then set both issue `workflow:blocked` and Project Status `Blocked`. Do not pretend a third-party review has happened.
- Avoid turning the board into a company hiring plan. Only the engineering workbench's actual tasks belong in active lanes.

## Permissions and security

Do not share PATs or paste credentials into chats, issues or repository files. An authorized GitHub Projects integration or Work-mode browser interaction is needed for view/field mutations; repository-scoped Actions tokens are not automatically allowed to modify organization Project fields.

See [Agile playbook](AGILE_PLAYBOOK.md), [scientific programme](https://github.com/Open-Energy-Methods/enerlint/issues/36), and the [one-year workbench plan](WORKBENCH_PLAN_2026_2027.md).
