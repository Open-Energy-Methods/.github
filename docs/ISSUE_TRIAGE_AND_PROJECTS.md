# Open Energy Methods — issue triage and project structure

**Status:** operational proposal applied to current public GitHub issues. The organization remains an independent research-software initiative, not an incorporated company or accredited verification body.

## Fields and meaning

| Field | Suggested values | Definition |
| --- | --- | --- |
| Priority | `priority:P0`, `priority:P1`, `priority:P2` | Scheduling: P0 foundation, P1 independently evaluated/adoption work, P2 conditional/scoping. Not a severity scale. |
| Severity | `severity:critical`, `severity:high`, `severity:medium`, `severity:low` | Consequence **if the underlying risk is mishandled or requirement omitted**. These labels are a *planning impact assessment*, not confirmation that a defect or incident has occurred. |
| Work type | `type:task`, `type:research`, `type:experiment`, `type:feature`, `type:documentation`, `type:governance` | Planning classification for the issue; not necessarily the native GitHub Issue Type field. |
| Area | `area:physics`, `area:benchmarks`, `area:reporting`, `area:adapters`, `area:ci`, `area:research`, `area:commercial`, `area:legal`, `area:community`, `area:branding`, `area:governance` | Primary responsible topic. |
| Stage | `stage:G0` through `stage:G4` | Current target research stage; separate from native GitHub Milestones. |
| Assignee | Actual GitHub user | Accountable maintainer of next action. Unassigned means prospective contributor/review needed or work not committed. |
| Author | Automatically set by GitHub | The account that originally opened the issue. Not a task ownership designation. |

### Severity definitions

- **Critical:** An unresolved issue can expose restricted information, create a serious legal/IP problem, or materially misrepresent safety/certification/validation. Escalate before public release or commercial use.
- **High:** Material risk of numerically incorrect reports, misleading scientific assertions, loss of research reproducibility, or inappropriate conclusions; needs review before the affected capability is released.
- **Medium:** Functionality, research usability, adoption, or maintenance might be impaired without immediate severe exposure.
- **Low:** Optional enhancement, future domain expansion, contingent outreach, or cosmetic improvement.

Severity labels on planning tasks represent hypothetical **failure impact**. Do not claim there is an active security incident or observed defect solely because a task has severity high/critical. Reassess when evidence appears.

## Suggested GitHub-native setup (requires repository/organization UI access)

1. Create a single **organization-level GitHub Project**: `OEM | Scientific & Venture Roadmap` (table + board + roadmap views).
2. Add both repositories' issues; project fields: `Status` (Backlog, Ready, In Progress, In Review, Blocked, Done), `Priority` (P0–P2), `Severity` (Critical/High/Medium/Low), `Stream` (EnerLint/OEM), `Stage` (G0–G4), and optional `Effort` (XS/S/M/L).
3. Create GitHub **milestones** separately in each repository (they are repo-local): `G0 | Foundation (2026-11)`, `G1 | Thermal core (2026-12)`, `G2 | External evidence (2027-03)`, `G3 | Pilot (2027-06)`, `G4 | Conditional growth (2027+)`. Dates are targets, not commitments.
4. Define native **organization Issue Types**, if supported and available: Task, Feature, Bug; use GitHub issue type only when appropriately supported. Our `type:...` labels provide the more granular research taxonomy meanwhile.
5. Color label families in GitHub's label settings: P0/P1/P2, severity, type, area and stage. This connector can apply labels but cannot set their colors.
6. Only assign items to people who actually accept maintenance responsibility. A planned external scientific reviewer is not an assignee or adviser without consent.

## Review policy

- Triage P0 and high/critical issues first. High **severity** is not a promise that all P2 speculative ideas are urgent.
- Link PRs to issues via `Fixes #N` only when completion criteria are satisfied.
- Preserve negative benchmark results and `NOT_CHECKED` states.
- Keep private legal, immigration, research contacts, and client discovery details outside public issues.
- Review scope, sequencing and the stop/upstream-pivot decision quarterly.
