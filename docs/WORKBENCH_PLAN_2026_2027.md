# Open Energy Methods — one-year engineering workbench plan

**Working period:** October 2026–October 2027  
**Maintainer:** Abhijith Sivaprasadan  
**Status:** a revisable personal research plan, not a business plan or grant/work contract.

## What OEM is this year

OEM is a home for open engineering research and computational experiments. It can host independent numerical methods, models, documentation, case studies and technical notes **when they are worth publishing**.

The name and logo supply continuity; they do not imply a company, a staffed laboratory, a consortium, an academic appointment, a product catalogue, or a customer operation. The maintainer's public role is **Creator & Maintainer**. Individual projects retain their own authorship, provenance, licence and maturity.

There is no requirement to become a company by October 2027. No paid consulting, funding, company registration, co-founder recruitment, advisor announcements, or other venture-related activity is an OEM milestone in this plan.

## Principles worth defending

1. **Show the question before the pitch.** A method should start from an engineering uncertainty or failure mode.
2. **Make an experiment runnable.** Inputs, equations, software versions, parameters, commands, and expected outputs belong alongside the result.
3. **Keep the ugly cases.** Invalid inputs, undetected faults, cancelled experiments and null comparisons are part of the record.
4. **Ask what existing tools already do.** Scientific contribution is not measured by the number of independent repositories.
5. **Name exactly what is known.** Synthetic test ≠ independent validation. A hash ≠ authenticated provenance. A release/DOI ≠ peer review.
6. **Do not collect projects.** Link older personal work first. Migrate only with rights/provenance review and a maintenance reason.
7. **The owner is a person.** Use first-person notes where natural; credit external contributors only for their specific, approved work.

## Active work: EnerLint

EnerLint remains the primary scientific implementation effort until it has passed basic independent-reproducibility gates. Its initial narrow question is whether exported control-volume and one-interval storage data satisfy stated physical balances with explicit numerical thresholds.

### October–December 2026: make a small, readable scientific artifact

- [ ] Demonstrate clean editable, wheel and sdist installation on Python 3.10/3.13 and Linux/macOS/Windows CI; record passes and failures.
- [ ] Specify every benchmark with physical boundaries, SI quantities, independent hand arithmetic, assumptions and reviewer status.
- [ ] Extend the analytical reference catalogue only after cases can be individually checked.
- [ ] Publish deliberately missed or ambiguous cases and explain why they escape.
- [ ] Stabilize report fields, error/abstention semantics and their documented schema.
- [ ] Publish an honest release decision, not a release date promise.

**Gate:** a technically competent person unfamiliar with the source can install EnerLint, verify the arithmetic without its implementation, and see where a `PASS_IN_SCOPE` does *not* imply physical correctness.

### January–March 2027: compare rather than advertise

- [ ] Run one prespecified native-tool-versus-EnerLint thermal test under equivalent information.
- [ ] Attempt one rights-cleared real-model export, prioritizing a genuinely separate implementation.
- [ ] Record false alarms, missed errors, integration hours and information required by each checker.
- [ ] Ask at least two unfamiliar technical users to reproduce and critique the experiment, subject to their willingness.

**Gate:** publish a fair conclusion, including if native diagnostics make EnerLint redundant. No claimed novelty before that comparison.

### April–June 2027: deepen one useful line of research

Choose **one** direction based on results, not on a brand diagram:
- improve thermal physical-contract checking;
- investigate irregular-time energy accounting;
- contribute useful checks to an existing upstream package;
- or publish a clear negative comparative result and close the experiment.

**Gate:** one reusable method, credible limitation study or independently repeatable benchmark; no obligation to invent a new package.

### July–October 2027: review and prune

- [ ] Identify which experiments were actually reused.
- [ ] Link or document selected older work, without automatically transferring its IP.
- [ ] Archive abandoned branches and explain stop decisions.
- [ ] Decide whether this remains a personal workbench, becomes a collaborative open-source initiative, or needs a different structure. **None** is the default requirement.

## Publishing format for experiments

Every public experiment should be readable without a sales deck:

```text
Question
Why I tried it / what prompted the question (only real, founder-confirmed details)
Physical or mathematical boundary
Reference equation and source
Input data and permissions
Reproduce this (environment, command, expected artifact)
Result (including failures or null comparisons)
What this does NOT establish
What I would test next
Author, date, revision, licence
```

Recommended low-overhead surfaces: repository docs, runnable notebooks/examples, and short [site field notes](https://open-energy-methods.github.io/#notes). The [editorial guide](EDITORIAL_VOICE.md) is about clarity and evidence, not corporate style compliance.

## Work discipline without corporate theatre

Use GitHub issues for actual technical tasks. Do not turn every interesting idea into an epic. Keep at most **one primary implementation track** active at a time; documentation and outreach may support that work. Review the plan every quarter and record what changed.

Success measures this year: reproducibility by other people, documented limitations, specific technical critique, meaningful reuse, and publishable negative or positive comparisons. Website traffic, stars, staffing, prospective revenues and the number of organizational repos are not scientific milestones.

## Relationship to the 27 October 2026 research bible

A confidential founder's research bible previously assembled scientific verification definitions, prior art, release gates, scenario market analysis, business/legal risks, and a proposed commercialization schedule. **It remains an internal evidence and historical planning document**, not a public source file.

This one-year workbench decision **supersedes its startup-first execution assumptions** for current OEM operations. The useful scientific safeguards still apply: separate verification and validation; independently reproduce analytical cases; compare fairly with native diagnostics; preserve negative cases; review permissions and code provenance; and never infer institutional endorsement.

If any commercial work is contemplated in future, re-open the legal, IP, data and individual work-authorization checks *before* accepting obligations. Do not treat them as a current reason to form a company.

## First live references

- [EnerLint scientific tracker](https://github.com/Open-Energy-Methods/enerlint/issues/36)
- [EnerLint analytical case cards](https://github.com/Open-Energy-Methods/enerlint/blob/main/docs/BENCHMARK_CASE_CARDS.md)
- [Website and field notes](https://open-energy-methods.github.io/)
- [OEM workbench direction issue](https://github.com/Open-Energy-Methods/.github/issues/25)
