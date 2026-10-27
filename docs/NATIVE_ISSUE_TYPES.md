# OEM native GitHub Issue Types

Open Energy Methods uses GitHub's **native Issue Types**, not only labels. Issue Types are controlled at the organization level, and the issue's native `Type` field is distinct from `type:*`, `agile:*`, priority and severity labels.

## Set up custom types in the organization settings

Go to **Organizations → Open-Energy-Methods → Settings → Planning → Issue types → Create new type**.

These types supplement GitHub's existing default types **Task**, **Bug**, and **Feature**:

| Native type | Color | Description | Current purpose |
| --- | --- | --- | --- |
| **Initiative** | gray | Long-running product or organizational programme with multiple epics. | Two master roadmap trackers |
| **Epic** | purple | A measurable outcome spanning related issues or repositories. | Eight cross-repository epics |
| **Story** | green | A small research or engineering increment with user-visible acceptance criteria. | Sprint stories and independently reviewable deliverables |
| **Research** | blue | Literature, method design, technical evidence or a reproducible reference study. | Research and scientific analysis tickets |
| **Experiment** | orange | Prespecified comparison, fault-injection or adoption test with measurable outcomes. | Scientific and customer-discovery experiments |
| **Spike** | yellow | Time-boxed investigation that resolves a consequential unknown. | Narrow feasibility studies and method investigations |

Keep GitHub's built-in **Feature** (blue), **Bug** (red) and **Task** (yellow) unless the organization has intentionally reconfigured them. Colors above are native **type palette names**, not HEX colors for labels.

## What is already configured

- Repository actions now apply native built-in **Task** and **Feature** to issue records.
- Native **Epic** and **Initiative** cannot be invented by individual repository workflows because these are organization-scoped settings.
- The two programme trackers have `agile:initiative` labels, eight epics have `agile:epic` labels, and individual sprint stories have `agile:story` labels.
- The sync workflow at `.github/workflows/sync-native-issue-types.yml` maps label taxonomy to available native types.

## Complete the backfill after creating types

In **each repository**:

1. Open **Actions → Synchronize native GitHub issue types**.
2. Select **Run workflow** on `main`.
3. Verify the job succeeds; it applies the best available native Type based on the issue's labels.
4. Check [OEM initiative #25](https://github.com/Open-Energy-Methods/.github/issues/25), [EnerLint initiative #36](https://github.com/Open-Energy-Methods/enerlint/issues/36), and [OEM Epic #26](https://github.com/Open-Energy-Methods/.github/issues/26). Their native Type must read Initiative, Initiative, and Epic respectively.
5. Check a sprint story and research/experiment ticket to ensure its native Type matches the intended kind of work.

**Limitations:** The connected GitHub App can assign an already-created type but cannot create organization-wide native Issue Types. Organization owner access or an organization-authorized token with **Issue Types: write** is required to create them. Never put such a token in a public issue, repository, or chat.

Issue type creation and issue fields are distinct from the GitHub Project v2 Kanban board; see [Project setup](PROJECT_SETUP.md).

**Reference:** https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/managing-issue-types-in-an-organization
