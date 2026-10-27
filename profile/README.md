# Open Energy Methods

<p align="center">
  <a href="https://open-energy-methods.github.io/">
    <img src="https://raw.githubusercontent.com/Open-Energy-Methods/.github/main/assets/brand/oem-logo-full-primary.svg" alt="Open Energy Methods — full-color navy and teal logo" width="500">
  </a>
</p>

### The model ran. But is it right?

Hi, I'm **Abhijith Sivaprasadan**, **Creator & Maintainer** of Open Energy Methods. This is my independent, open-source workspace for energy-engineering projects, experiments, numerical models, research methods and field notes.

A simulation completing successfully is not proof that its results make physical sense. Sometimes a balance check finds an obvious mistake. Sometimes the balances close, but the underlying operating point is still wrong.

I find that second case especially interesting.

**This is an open engineering workbench, not a company or a research institute.** I want to make the source, assumptions, tests, failures and lessons from my projects available for others to inspect, reproduce and build upon.

## First experiment: [EnerLint](https://github.com/Open-Energy-Methods/enerlint)

EnerLint is an experimental Python toolkit for checking *specified* physical properties of exported energy-model results. The first version deals with steady mass and energy balances and one-interval thermal storage accounting.

The deliberately modest starting tests include:

- Four hand-constructed reference cases that pass their declared checks.
- Six developer-selected altered cases that trigger expected failures.
- **One compensating error that escapes**, even though the result looks perfectly balanced.

That last case is a feature of the research record, not a result to hide. These tests are not measurements, industrial validation, independently measured detection rates, or a claim that EnerLint improves on existing tools.

**[Read the worked example: why a passing energy balance isn't proof](https://open-energy-methods.github.io/notes/001-a-pass-isnt-proof.html)**

## What belongs on the workbench

For the next year, the main objective is straightforward: publish engineering work that is technically substantive, inspectable and reusable. That may include numerical experiments, simulation models, benchmark studies, documented methods and small software tools. Not everything needs to become a standalone product.

EnerLint remains the first active OEM project. Its immediate research questions concern independent physical checks, boundaries, numerical tolerances and comparison with native model diagnostics. Other projects will be added when there is real work to publish—not to fill out an organization chart.

## Where the questions came from

Some of my other personal projects explore [thermodynamic simulation](https://github.com/abhijith-sivaprasadan/thermotwin), [steam and power modelling](https://github.com/abhijith-sivaprasadan/opensteamopt), and [regional energy-system evidence](https://github.com/abhijith-sivaprasadan/kerala2040). They have informed my curiosity, but they are **not automatically OEM-owned modules** or external validation for EnerLint.

## Come challenge the work

If you model physical systems, an edge case or a reason a check is redundant is genuinely useful. You can [open an EnerLint issue](https://github.com/Open-Energy-Methods/enerlint/issues), read the [verification contract](https://github.com/Open-Energy-Methods/enerlint/blob/main/docs/VERIFICATION_CONTRACT.md), or follow the [experimental roadmap](https://github.com/Open-Energy-Methods/enerlint/blob/main/docs/ROADMAP.md).

**[Website and field notes](https://open-energy-methods.github.io/)** · **[LinkedIn](https://www.linkedin.com/company/open-energy-methods)** · **[Brand assets](../assets/brand/)**

---

<sub>Open Energy Methods is an independent, creator-maintained research workbench, not a registered company or nonprofit, an accredited verification body, or an official KTH or other institutional initiative.</sub>
