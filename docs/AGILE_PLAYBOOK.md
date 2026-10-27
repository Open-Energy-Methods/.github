# OEM Agile Delivery Playbook — v1 (27 October 2026)

This is the public operational companion to [issue triage and project conventions](ISSUE_TRIAGE_AND_PROJECTS.md). It tracks engineering research work without pretending the Open Energy Methods initiative is an incorporated company or that EnerLint is scientifically validated for industrial use.

## Hierarchy — avoid duplicating tickets

1. **Initiative:** Open Energy Methods and EnerLint, represented by the two existing master trackers.
2. **Epic:** Outcome-oriented GitHub issue, eight cross-repository epics in [OEM issues](https://github.com/Open-Energy-Methods/.github/issues), labeled `agile:epic`.
3. **Story:** A testable increment from a researcher's, engineer's, maintainer's or reviewer’s perspective. Linked to an epic and accompanied by clear acceptance conditions, labeled `agile:story`.
4. **Task:** Implementation, operations or documentation piece, labeled `agile:task`; use `agile:spike` for a bounded unknown.
5. **Sprint:** A two-week planning period; the Project **Iteration** field is the canonical tracker after the GitHub Project is created. The temporary `sprint:S0` etc. labels allow issue filtering before board setup.

## Definition of Ready (DoR)

- Scientific/user problem or decision described.
- Scope, deliverable, acceptance criterion and evidence boundary stated.
- Dependencies, required data and sharing rights identified.
- Owner confirms that next action is feasible within the planned sprint.
- Relative estimate (1, 2, 3, 5, or 8 points) agreed, or explicitly `unestimated`.

## Definition of Done (DoD)

- The specific acceptance criteria have evidence links.
- Tests or reproducible documents are present when applicable.
- Independent numerical oracle/counterexample exists for new scientific behavior.
- Review completed by an appropriate maintainer; scientific external review only when specifically committed.
- No private/proprietary material included and accurate claims/limitations preserved.
- CI passes on affected supported targets (where required).
- Issue is closed as **completed** and Project Status is **Done**; a cancelled issue is `not planned`, not a completed story.

## Status workflow

**Backlog → To Do → In Progress → In Review → Done**. **Blocked** can be entered from any active state and requires a blocker link or explanation. Cancelled work is `Won't Do`.

Before the actual GitHub Project exists, colored `workflow:*` labels are the fallback. A GitHub Action ensures at most one workflow label on an issue and applies `workflow:done` when closed as completed; closed as not planned goes to `workflow:wont-do`.

After the Project exists, its **Status** field is the main source of truth. Status labels remain lightweight searchable metadata but are **not automatically synced** with Project fields; do not use contradictory values or treat a label as a project field.

## Severity vs. priority

- **Priority P0/P1/P2**: when the work should be attempted.
- **Severity critical/high/medium/low**: hypothetical consequence if the issue is mishandled, including scientific/contract/legal risks.
- **Story points**: relative effort and uncertainty, not hours or performance. 1=trivial, 2=small, 3=moderate, 5=complex, 8=large/uncertain; split most stories larger than 8.
- A P2 future idea can be low severity even if technically exciting; a P0 legal/IP gate may be critical.

## Sprint rhythm

- **S0: 27 Oct–8 Nov 2026** — scoped first iteration. [Sprint issue](https://github.com/Open-Energy-Methods/.github/issues/34).
- **S1: 9–22 Nov 2026** — provisional. [Sprint issue](https://github.com/Open-Energy-Methods/.github/issues/35).
- **S2: 23 Nov–6 Dec 2026** — provisional. [Sprint issue](https://github.com/Open-Energy-Methods/.github/issues/36).
- **S3: 7–20 Dec 2026** — provisional. [Sprint issue](https://github.com/Open-Energy-Methods/.github/issues/37).

Sprint 0 estimates 16 relative story points across five issues. These estimates are planning assumptions, **not measured capacity or commitments**. Revise after the first sprint retrospective.

### Lightweight ceremonies

- **Planning (30–45 minutes at sprint start):** capacity, sprint goal, blockers, 3–6 high-value stories, assign ownership, estimate.
- **Async standup (brief, as-needed):** update each issue's Status, recent progress, evidence and blockers; avoid process theater.
- **Weekly triage (15 minutes):** review critical/high severity, new issues, scope changes, reproductions and external dependencies.
- **Sprint review (30 minutes):** demo actual artifacts and passing/failing checks to a reviewer; distinguish CI green from scientific validity.
- **Retrospective (15 minutes):** compare planned vs delivered work, observed integration time, false alarms, and improve one process.

## Sprint progress

Closed-completed stories count toward delivered points. Open stories in `workflow:in-progress` count as in progress but not delivered; `workflow:blocked` is separately highlighted. An issue with a `sprint:*` label but no `points:*` label is not part of point totals.

A lightweight live-ish report can be generated at `docs/SPRINT_STATUS.md`. GitHub Projects' built-in charts should become the primary board/report once configured.

## GitHub Project setup

See [Project v2 configuration and limitation](PROJECT_SETUP.md) for the organization-level board, built-in filters, issue types, severity fields and automatic addition. **All native Issue Types are already created and synchronized.** The connected GitHub integration still cannot create the organization-wide GitHub Projects v2 board; that remains an organization-owner UI step.

## Scientific safeguards

No confidential founder/participant histories on public tickets. No presumed KTH, OET or industrial partnerships. No industrial verification claim from synthetic self-tests. Keep compensating-error escapes and null/inconclusive results visible.

