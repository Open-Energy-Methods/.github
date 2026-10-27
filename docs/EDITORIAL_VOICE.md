# Open Energy Methods — editorial voice and evidence rules

**Status:** living creator-facing editing guide · updated 27 October 2026

This exists because an open-source research workbench started sounding like a fully staffed scientific company. That is not the reality or the voice we want to communicate.

The approved navy/teal visual identity stays. The problem was not a lack of polish. It was a surplus of generic language and an absence of the specific questions, imperfect experiments, and actual person behind the work.

## The short version

> Show what question led to the work. Show a real example. Say what it catches. Say what it misses. Make it possible to reproduce. Then invite someone to challenge it.

Scientific discipline is the backbone. Personal curiosity is the voice. Neither replaces the other.

## Creator and maintainer

Open Energy Methods was created and is maintained by **Abhijith Sivaprasadan**, an energy engineer working with thermodynamics, energy-system modelling and numerical methods. It is an independent open-source engineering research workbench, not a university lab, registered company, certification body or formal multi-person research group. When a role title is needed, use **Creator & Maintainer**, not Founder/CEO or Lead Maintainer.

The author can write **“I”** on the website, public notes and project updates. Avoid institutional **“we”** when the work was done by one person. Future contributions should receive specific attribution and may appropriately change the pronouns.

Do **not** invent autobiographical incidents or imply that a specific past simulation was defective unless the founder verifies that event and its evidence. Curiosity about a possible failure is not testimony that it occurred.

## What people should encounter, in order

1. **A specific question.** Example: “The model ran. But is it right?”
2. **The experiment.** What model, case or physical balance are we checking?
3. **The evidence.** Exact inputs, expected output, failed mutation, reproducible source.
4. **The limitation.** What could look right for the wrong reason?
5. **The person.** Who is doing the work, and how can a reader challenge it?

Do not lead a homepage with a hierarchy of corporate values, unearned “industry” language, advisory boards, a large roadmap, or research aspirations presented as completed capabilities.

## Voice

- Curious, precise, personally accountable; never synthetic enthusiasm.
- Prefer short concrete sentences to dense strings of academic or startup nouns.
- Technical terms are welcome when they do actual work; explain them with an example.
- An unexpected pass or failure may be the most interesting result.
- Write as someone doing careful engineering in public, not as a marketing department selling trust.
- Let some uncertainty stand. “I don't know yet” is a legitimate research statement.

## Before → after examples

| Avoid | Prefer |
|---|---|
| “We deliver trustworthy computational energy verification solutions.” | “I want to know what a model's results actually prove.” |
| “Our flagship platform empowers stakeholders to ensure numerical credibility.” | “EnerLint currently checks declared mass and energy balances from model exports.” |
| “A robust framework with comprehensive fault-detection capabilities.” | “It flagged six deliberate faults. A compensated error still passed.” |
| “A dynamic research ecosystem advancing interoperable scientific infrastructure.” | “A workbench for small energy-modelling tools, experiments and notes.” |
| “Validated, reliable and industry-ready.” | Do not claim this; specify the actual test and independent review status. |

The before examples are anti-patterns, not descriptions of verified past claims.

## Things that must remain explicit

- EnerLint alpha tests are **synthetic hand-constructed self-tests**. They do not establish real-world fault prevalence, sensitivity, specificity, external adoption or industrial suitability.
- “Independent” means a separately implemented *specified check*, not an independent laboratory, reference dataset or accreditation.
- A conservation pass does **not** prove the model's parameters, operating point, assumptions or measurements are correct.
- A published repository, GitHub Actions success, LinkedIn page or software DOI does not create scientific validation, a legal company, or a funded research role.
- The creator's other repositories can be linked as influences, but are not automatically OEM assets. Permission/IP/provenance review precedes copying code or data.
- No unfounded KTH, Siemens Energy, reviewer, collaborator, customer, or institutional endorsement.

These restrictions apply equally to energetic social posts and to formal scientific documents.

## Different surfaces have different jobs

- **OEM website:** approachable technical workbench, actual engineering projects, first-person notes, examples, negative cases and reasons to care.
- **Organization GitHub profile:** concise origin, what exists, how to examine the work, who maintains it.
- **EnerLint README:** developer-facing installation and physical contracts; a short truthful origin note, not marketing copy.
- **LinkedIn:** individual projects or Featured links are appropriate; if a branded page is maintained, use a small authentic description and actual project updates, never investor-deck language. OEM is not automatically an employment entry.
- **Technical docs and research bible:** explicit hypotheses, source registers, definitions, numerical contracts, evidence hierarchy, legal boundaries. Do not make formal research imprecise merely to sound personal.

## Every new public claim gets a five-question check

1. **Who did this?** Author/maintainer attribution is real.
2. **What is observable now?** Link to code, a benchmark result or a source.
3. **What is only planned?** Mark it unambiguously.
4. **What would falsify the claim?** Record native-tool alternatives and missed errors.
5. **Would the creator naturally say this?** If not, rewrite or remove it.

Any AI-assisted copy should be reviewed and adjusted by the creator before being treated as his own first-person account. AI may organize and edit material; it may not invent motivations, memories, technical accomplishments or collaborators.

## Preferred public starting point

> The model ran. But is it right?
>
> I started Open Energy Methods to investigate the space between a simulation finishing and an engineering result making sense. EnerLint is my first attempt at checking a small part of that problem. The source, the assumptions and the failures are open.

This is a working editorial direction, not a required script. It can—and should—evolve in the founder's own words.

## Direction for 2026–27

OEM is a **personal research and engineering workspace with a distinct open identity**. The primary outputs are open-source engineering projects, simulation and numerical models, experimental case studies, documented research methods and field notes. They should stand on their own with accessible evidence and appropriately scoped claims.

EnerLint's verification focus does **not** obligate every future OEM project to be a verification tool. Publishing a useful negative result or imperfect experiment counts; claiming a release, external review or commercial readiness without evidence does not.

Avoid website sections or issue milestones designed chiefly to imply company growth, customer acquisition, a services business, staff or revenue. Revisit possible collaboration or legal incorporation only if later warranted. This is a direction for public communication and research priorities, not a claim about permanent organizational form.

## How this is maintained

Revisit this guide after outside readers try the software, when collaborators join, or if OEM changes legal/organizational status. Change the copy to reflect actual work, not to preempt an imagined future company.
