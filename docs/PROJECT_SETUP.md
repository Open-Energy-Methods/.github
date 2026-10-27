# Create the OEM organization GitHub Project

## Current state and access limitation

Repositories, issues, colored labels, stage milestones, epics and sprint planning tickets are already created. However, **the organization-level GitHub Project v2 must be created in the GitHub interface**: the connected repository automation token does not have organization Projects GraphQL access. A repo-level `GITHUB_TOKEN` cannot create or administer an organization Project. Do not put personal access tokens in source or issues.

**One board for two repositories:** `Open-Energy-Methods/enerlint` and `Open-Energy-Methods/.github`.

## Create once (organization owner)

1. Open https://github.com/orgs/Open-Energy-Methods/projects and click **New project**.
2. Start from **Board**, or an available Team planning template. Name it **OEM | Science & Venture Delivery**. Set visibility to public only if all included items are safe to disclose.
3. Configure built-in **Status** single-select to: `Backlog`, `To Do`, `In Progress`, `In Review`, `Blocked`, `Done` (and optionally `Won't Do`). Board layout: group by Status.
4. Add **Iteration** named `Sprint`, duration **2 weeks**, initial anchor **27 October 2026**. Alternatively select an available 2-week iteration spanning S0.
5. Add project fields: `Stream` (EnerLint / OEM), `Epic` (E1–E8), `Story points` (number), `Severity` (Critical/High/Medium/Low), `Priority` (P0/P1/P2), `Stage` (G0–G4), optionally `Target date`. Use existing organization **Issue Fields** for Priority/Effort where they are already available instead of duplicating them.
6. **Backfill existing work manually:** in Project Table view, click **+ → Add item from repository**, select `enerlint`, bulk-select its open issues and click **Add selected items**; repeat for `.github`. GitHub's auto-add does **not** retroactively import existing issues.
7. **Future issues:** in Project **Workflows → Auto-add to project**, select `enerlint` with filter `is:issue`. **GitHub Free allows only one auto-add workflow**, so `.github` issues require manual additions unless your plan allows more workflows or you configure a properly authorized GitHub App. Built-in **Item added to project** should set Status to **Backlog** (not To Do for everything). Built-in **Item closed** can set Done; check closed-not-planned treatment before relying on completion charts.
8. Reconcile Sprint, Severity, Priority and Story points from existing labels; Project fields are canonical once configured.

## Views

| View | Layout | Scope |
| --- | --- | --- |
| **Scrum board** | Board | Group by Status; all work streams; filter `-status:Done` for working view. |
| **Current sprint** | Board | Sprint/current iteration, group by Status. |
| **Product backlog** | Table | All open issues, sorted Priority → Severity, show assignee, Stage, Epic, points, milestone. |
| **Epics** | Table | `label:agile:epic`; inspect cross-repo linked checklists. |
| **Release gates** | Roadmap | Milestones G0–G4; review timing, dependencies, risks. |
| **Severity & risks** | Table | Critical/High severity, open only. |
| **Team workload** | Table | Group by Assignees, show points/iteration. |
| **Delivered** | Table/chart | Closed completed issues, grouped by sprint/stream. |

## Native GitHub Issue Types and fields

On the organization **Settings**, set up issue types **Epic**, **Feature**, **Task**, **Bug** and optionally **Research spike** where supported. Native issue types are distinct from the `type:*` and `agile:*` labels. The GitHub May 2026 rollout also made structured Issue Fields available to organizations; prefer an org **Severity** field for typed cross-repository management, while keeping severity labels for filtering and visible color.

To set this up: navigate to organization Settings and search **Issue types** / **Issue fields** (availability and labels vary). Configure types/fields and backfill them through the Projects UI. Do not assume these native values were filled automatically from issue labels.

## Initial sprint plan

- [S0](https://github.com/Open-Energy-Methods/.github/issues/34): five stories / **16 tentative points**, starting 27 Oct.
- [S1](https://github.com/Open-Energy-Methods/.github/issues/35): four stories / 16 tentative points.
- [S2](https://github.com/Open-Energy-Methods/.github/issues/36): three stories / 16 tentative points.
- [S3](https://github.com/Open-Energy-Methods/.github/issues/37): three stories / 16 tentative points.

## Security

No need to provide a PAT to any chat or commit. GitHub's native Auto-add and Status workflows can perform the first board automation without any stored token.

## Verification after setup

- Board includes **both** repositories and eight epics.
- At least five S0 stories appear in the current iteration under To Do.
- Native Priority/Severity/Iteration columns are populated rather than merely color labels.
- Closing a completed story moves it to Done; marking one not planned does not falsely count as delivered.
- Filtering by repo, severity, sprint, assignee and issue type works.

Official docs: https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/quickstart-for-projects

GitHub sources: [Auto-add limitations](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project/adding-items-automatically) and [Bulk add from repository](https://docs.github.com/en/issues/planning-and-tracking-with-projects/managing-items-in-your-project/adding-items-to-your-project). The number of auto-add workflows allowed depends on the GitHub plan.
