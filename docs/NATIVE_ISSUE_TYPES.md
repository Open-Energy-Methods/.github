# Open Energy Methods — native GitHub Issue Types

**Verified on 27 October 2026.**

All **nine organization-wide native types** are enabled and available in both public repositories. The successful GitHub Actions backfill classified **71 of 71 existing issues** with no missing Type fields.

| Native type | Purpose |
| --- | --- |
| Initiative | Long-running product or organizational programme |
| Epic | Outcome spanning multiple stories or tickets |
| Story | Reviewer- or user-facing, testable increment |
| Research | Analytical references, science methods and literature |
| Experiment | Prespecified scientific benchmark or customer discovery comparison |
| Spike | Time-boxed investigation of an unknown |
| Task | Bounded scientific maintenance, documentation or operational activity |
| Feature | Added or modified software capability |
| Bug | Reproducible fault or unexpected behavior |

The two master trackers are **Initiative**, the eight OEM workstream issues are **Epic**, and the sprint-committed increments are **Story**. Other tickets use Task, Feature, Research or Experiment as dictated by their pre-existing labels.

## Live synchronization

- [OEM native Issue Type action](https://github.com/Open-Energy-Methods/.github/actions/workflows/sync-native-issue-types.yml)
- [EnerLint native Issue Type action](https://github.com/Open-Energy-Methods/enerlint/actions/workflows/sync-native-issue-types.yml)

The actions query the organization's available types, then assign native Type using the following label precedence:

1. `agile:initiative` → Initiative
2. `agile:epic` → Epic
3. `agile:spike` → Spike
4. `agile:story` → Story
5. `type:bug` → Bug
6. `type:experiment` → Experiment
7. `type:research` → Research
8. `type:feature` → Feature
9. Otherwise → Task

**Safeguard:** If a required native type is temporarily unavailable, the sync leaves that issue untyped rather than preserving an incorrect classification. No other issue fields, labels, milestones, or status are modified.

## What issue types are not

Native Type is not a project board. It is independent from:

- **Priority** — P0/P1/P2, expressed through issue labels
- **Severity** — risk/consequence categorization, expressed through issue labels
- **Status** — Backlog/To Do/In Progress/In Review/Blocked/Done
- **Stage** — milestones G0–G4
- **Sprint** — two-week iterations, tracked with labels until Project v2 is established

All existing issues have native Type set. The **organization-wide GitHub Project v2 board** remains a distinct, pending configuration task: [setup guide](PROJECT_SETUP.md).

## Future maintenance

New tickets are initialized from the issue templates and receive type assignments through the workflows on issue creation and labeling. If an issue's taxonomy is intentionally changed, re-run the type synchronization action after adjusting the labels.

Do not edit the native Type arbitrarily while retaining a conflicting `type:*` or `agile:*` label; the next synchronization can legitimately restore the mapping.

For native type API semantics and permission requirements, see the [official GitHub documentation](https://docs.github.com/en/rest/orgs/issue-types).
