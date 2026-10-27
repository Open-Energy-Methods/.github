# Open Energy Methods — native GitHub Issue Types

## Verified organization state — 27 October 2026

Seven native issue types currently exist: **Experiment**, **Bug**, **Research**, **Initiative**, **Epic**, **Story**, and **Spike**. These have been created successfully in the organization's issue type settings.

Two essential types are **not** in the organization's currently available type list:

| Additional native type | Suggested color | Description |
| --- | --- | --- |
| **Task** | yellow or gray | A bounded operational, documentation, governance, or implementation activity with testable completion criteria. |
| **Feature** | blue | A new or modified software capability, with engineering acceptance tests and documentation. |

In the organization **Settings → Planning → Issue types → New type**, create **Task** and **Feature**. A total of nine types remains below GitHub's maximum of 25 types.

The two repository workflows already recognize `Task` and `Feature`, and will backfill them after they are available.

## Live verification

The existing custom types and their native assignments were inspected on GitHub. The issue type synchronization workflows completed successfully in both repositories, but reported the following *deferred* type assignments:

- **OEM `.github`**: 14 Task and 1 Feature
- **EnerLint `enerlint`**: 7 Task and 2 Feature

Some of the affected issues presently retain a **stale native type** left over from the old organization type configuration. For example, a release-metadata documentation task can currently display **Experiment** until the missing **Task** type is created and the sync reruns. Labels and milestones are accurate; the native type field still needs reconciliation for these deferred issues.

## After creating the missing types

1. Open [OEM native type workflow](https://github.com/Open-Energy-Methods/.github/actions/workflows/sync-native-issue-types.yml) and use **Run workflow** on `main`.
2. Open [EnerLint native type workflow](https://github.com/Open-Energy-Methods/enerlint/actions/workflows/sync-native-issue-types.yml) and run it likewise.
3. Confirm both job logs report **zero deferred types**.
4. Spot-check the issues below.

| Issue | Expected native type |
| --- | --- |
| [OEM foundation tracker](https://github.com/Open-Energy-Methods/.github/issues/25) | Initiative |
| [EnerLint scientific tracker](https://github.com/Open-Energy-Methods/enerlint/issues/36) | Initiative |
| [OEM scientific governance epic](https://github.com/Open-Energy-Methods/.github/issues/26) | Epic |
| [OEM organization settings](https://github.com/Open-Energy-Methods/.github/issues/2) | Story |
| [EnerLint release metadata](https://github.com/Open-Energy-Methods/enerlint/issues/5) | Task |
| [EnerLint report schema](https://github.com/Open-Energy-Methods/enerlint/issues/7) | Feature |
| [EnerLint thermal comparison](https://github.com/Open-Energy-Methods/enerlint/issues/18) | Experiment |

## Classification precedence

The GitHub Actions workflow is authoritative and uses:

1. `agile:initiative` → Initiative
2. `agile:epic` → Epic
3. `agile:spike` → Spike
4. `agile:story` → Story
5. `type:bug` → Bug
6. `type:experiment` → Experiment
7. `type:research` → Research
8. `type:feature` → Feature
9. Everything else → Task

GitHub **Issue Types** are native organization settings, not the colored `type:*` labels, Project v2 status fields, or milestone labels. An issue should have one native issue type and may have multiple planning labels.

Creating or changing the organization's native types still requires an organization-owner action, whereas the repository GitHub Actions may set a type that already exists.
