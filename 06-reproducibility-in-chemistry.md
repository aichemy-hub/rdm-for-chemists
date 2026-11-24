---
title: "The Reproducibility Crisis in Chemistry"
teaching: 10
exercises: 5
---

::::::::::::::::::::::::::::::::::::::: objectives

- Describe chemistry-specific factors that undermine reproducibility
- Identify the kinds of information missing from typical chemistry methods sections
- Explain how good data management practices directly address reproducibility failures

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- Why is reproducibility a particular challenge in chemistry?
- What kinds of detail are routinely missing from chemistry publications?
- What can I do to make my own work more reproducible?

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  callout

## Part 2: Chemistry-Specific Data Management

Welcome to Part 2. Episodes 6--11 apply the principles from Part 1 to the
specific challenges, tools, and opportunities in chemistry research: the
reproducibility crisis, electronic lab notebooks, metadata standards,
chemistry repositories, managing analytical data, and the UK data
infrastructure landscape.

::::::::::::::::::::::::::::::::::::::::::::::::::

## Building on Episode 1

In Episode 1 we saw that over 70% of researchers had tried and failed to reproduce another scientist's results, and that chemists showed the highest rates of irreproducibility in Baker's 2016 *Nature* survey. Here we look at why chemistry is particularly vulnerable, and what the research community is doing about it.

## Why Chemistry Is Hard to Reproduce

A 2024 review in *Heliyon* examined reproducibility specifically in chemistry research and identified several structural factors that make the field particularly prone to reproducibility failures.

> "Reproducibility in chemistry research." (2024) *Heliyon* 10, e35986.
> [doi:10.1016/j.heliyon.2024.e35986](https://pmc.ncbi.nlm.nih.gov/articles/PMC11305220/)

### Insufficient methods reporting

Chemistry papers routinely omit details that turn out to be critical. A reaction described as "carried out under inert atmosphere in dry solvent at elevated temperature" leaves an enormous amount unspecified: which inert gas? which solvent, and how was it dried? what temperature, exactly? what concentration? what purity of starting materials? These details are often treated as obvious, or too routine to mention -- but small variations can determine whether a reaction succeeds or fails entirely.

The same problem is acute in computational chemistry. A DFT study reported as "performed using a GGA functional and plane-wave basis set" says almost nothing: which exact basis set? which dispersion correction, if any? what convergence criteria? which software package, and which version? Computational results can be sensitive to all of these choices. Trajectories, input files, and pseudopotentials are routinely discarded after publication making independent validation impossible even in principle.

### Chemistry-specific experimental pitfalls

Beyond missing parameters, some chemistry sub-fields face pitfalls that are almost impossible to convey in a conventional methods section. Trace impurities in building blocks can template entirely different products in supramolecular chemistry. Polymorphic outcomes depend on subtle conditions -- stirring rate, seeding, rate of cooling -- that rarely appear in published procedures. Reactions sensitive to oxygen or moisture are highly dependent on technique: a glovebox, a Schlenk line, and a nitrogen balloon are not equivalent, even if the paper says only "under inert atmosphere."

### Publication culture

The *Heliyon* review also found that chemistry papers contain more "hyping" language than those in other disciplines with 2.54 promotional terms per 100 words on average. Phrases like "novel", "superior", "unprecedented", and "highly efficient" appear routinely regardless of the strength of the underlying evidence. This does not cause irreproducibility directly, but it correlates with selective reporting: the pressure to present positive, impactful results discourages the publication of failure modes, contradictory results, and the conditions under which a method does *not* work.

## The Industrial Perspective

The stakes become clearest in pharmaceutical and applied chemistry contexts. Bayer HealthCare reported that only 7 of 67 internal target validation projects (around 10%) were fully reproducible, with published and in-house data agreeing in only 20--25% of cases. Amgen found that 89% of landmark oncology results they attempted to replicate could not be confirmed.

> Prinz, F., Schlange, T. & Asadullah, K. (2011) "Believe it or not: how much can we rely on published data on potential drug targets?" *Nature Reviews Drug Discovery* 10, 712–713. [doi:10.1038/nrd3439](https://doi.org/10.1038/nrd3439)
>
> Begley, C.G. & Ellis, L.M. (2012) "Drug development: Raise the bar of cancer research." *Nature* 483, 531–533. [doi:10.1038/483531a](https://doi.org/10.1038/483531a)

These are not academic curiosities. Failed reproduction wastes enormous resources and, in drug discovery, can mean years of downstream work built on a shaky foundation.

:::::::::::::::::::::::::::::::::::::::::  callout

## This Is Also a Data Management Problem

Many reproducibility failures stem directly from poor data management:

- Raw data was lost, so the processing pipeline cannot be checked
- Instrument settings were not recorded, so conditions cannot be replicated
- Ambiguous file names mean no one is sure which version of the data was used in the paper
- Processing steps were applied but not documented

Good RDM does not solve everything. You still need good experimental practice and honest reporting, but it removes a large class of reproducibility failures that are entirely preventable.

::::::::::::::::::::::::::::::::::::::::::::::::::

## What Good Looks Like

The chemistry community has started to develop practical responses:

- **Mandatory "Failure Analysis" sections:** Some journals and groups are experimenting with requiring authors to include a discussion of conditions under which the method failed or gave poor results. This information is often known to the authors but never published.
- **Independent replication:** A small number of high-profile journals now require independent replication of key results before publication.
- **Structured supplementary information:** Rather than a narrative methods section, it is now sometimes possible to provide machine-readable records of experimental conditions, including ELN exports and instrument metadata files.

The last point connects directly to what we cover in the rest of Part 2: electronic lab notebooks, metadata standards, and structured data repositories are the practical tools for making chemistry reproducible at scale.

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge: Reproducibility Detective

Below is an excerpt from the experimental section of a fictional chemistry paper that would routinely pass peer review. Read it carefully, then discuss with a neighbour:

1. What does this procedure report well?
2. What information is missing that would prevent you from reproducing it?
3. What should the authors have recorded in their ELN that did not make it into the paper?

---

> *"4-Bromoanisole (1.87 g, 10.0 mmol) and phenylboronic acid (1.46 g, 12.0 mmol) were combined with Pd(PPh₃)₄ and Cs₂CO₃ in DMF/water and heated to 80 °C under nitrogen. After stirring overnight, the mixture was cooled to room temperature and extracted with EtOAc (3 × 30 mL). The combined organic layers were dried over MgSO₄, filtered, and concentrated under reduced pressure. Purification by column chromatography (hexane/EtOAc) gave the product as a white solid (87%). ¹H NMR (400 MHz, CDCl₃): δ 7.52 (d, J = 8.6 Hz, 2H), 7.41–7.30 (m, 5H), 6.97 (d, J = 8.6 Hz, 2H), 3.84 (s, 3H)."*

:::::::::::::::  solution

## Discussion

**What is reported well:**

The starting material masses and molar quantities are given. Temperature (80 °C) and atmosphere (nitrogen) are stated. The workup is described in detail. NMR data include field strength (400 MHz), solvent (CDCl₃), and coupling constants; enough for someone to compare their product to the reported spectrum.

**What is missing:**

- **Catalyst loading:** Pd(PPh₃)₄ is listed but no amount or mol% is given. Palladium catalyst loading is one of the most important variables in cross-coupling reactions.
- **Base equivalents:** Cs₂CO₃ appears with no quantity. The amount of base affects both rate and selectivity.
- **Solvent ratio:** "DMF/water" -- what ratio? This is well known to affect Suzuki coupling outcomes significantly.
- **Reaction time:** "Overnight" is anywhere from 12 to 18 hours. For an optimised procedure, the actual time matters.
- **Column conditions:** "hexane/EtOAc" with no ratio. Anyone reproducing this needs to develop their own conditions from scratch.
- **Characterisation:** No HRMS (high-resolution mass spectrometry) data, no melting point, no purity assessment. The NMR alone is not sufficient for unambiguous identification of a new compound.

**What should have been in the ELN:**

Exact masses and volumes of all reagents including catalyst and base, lot numbers for commercial reagents, the actual reaction time, TLC conditions used to monitor the reaction, column gradient used in purification, and the mass of product actually isolated from each run (not just the percentage yield). Much of this is captured automatically if a structured ELN with a stoichiometry calculator is used.

The lesson here is not that the paper is fraudulent or careless; this level of reporting is commonplace and accepted. The problem is that what passes peer review is often not enough to reproduce the work.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  keypoints

- Chemistry is fundamentally a reproducible science, but inadequate methods reporting and poor data management undermine this in practice.
- Experimental details that seem obvious to the author -- catalyst loading, solvent ratio, reagent purity -- are often critical for reproduction and routinely absent from publications.
- The same problem applies in computational chemistry: functional, basis set, software version, and input files must be archived and shared, not discarded after publication.
- Publication pressure and selective reporting compound the problem: failure modes rarely appear in the literature.
- Good RDM practices -- recording metadata systematically in an ELN, keeping raw data, documenting processing steps -- directly address the most preventable causes of irreproducibility.

::::::::::::::::::::::::::::::::::::::::::::::::::
