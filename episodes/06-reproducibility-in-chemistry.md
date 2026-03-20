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

## Building on Episode 1

In Episode 1 we saw that over 70% of researchers had tried and failed to reproduce another scientist's results, and that chemists showed the highest rates of irreproducibility in Baker's 2016 *Nature* survey. Here we look at why chemistry is particularly vulnerable, and what the research community is doing about it.

## Why Chemistry Is Hard to Reproduce

A 2024 review in *Heliyon* examined reproducibility specifically in chemistry research and identified several structural factors that make the field particularly prone to reproducibility failures.

> "Reproducibility in chemistry research." (2024) *Heliyon* 10, e35986.
> [doi:10.1016/j.heliyon.2024.e35986](https://pmc.ncbi.nlm.nih.gov/articles/PMC11305220/)

### Insufficient methods reporting

Chemistry papers routinely omit details that turn out to be critical. A reaction described as "carried out under inert atmosphere in dry solvent at elevated temperature" leaves an enormous amount unspecified: which inert gas? which solvent, and how was it dried? what temperature, exactly? what concentration? what purity of starting materials?

These details are often treated as obvious by the authors, or considered too routine to mention. But small variations -- a few degrees of temperature, trace water in a solvent, a different source of a commercial reagent -- can determine whether a reaction succeeds or fails. A synthetic chemist trying to reproduce the work is left to guess.

### Chemistry-specific experimental pitfalls

Some chemistry sub-fields face reproducibility challenges that are almost entirely hidden in published methods:

- **Trace impurities:** In supramolecular and coordination chemistry, small amounts of impurities in building blocks can template completely different products. The "successful" outcome may have depended on a specific batch of reagent that is never mentioned.
- **Pathway complexity:** Many systems can reach multiple thermodynamic or kinetic outcomes depending on how a reaction is set up, e.g., stirring rate, order of addition, concentration during mixing. Published methods rarely capture this level of procedural detail.
- **Polymorphism:** Crystal form depends sensitively on conditions (solvent, temperature, seeding, rate of cooling). A compound described as having certain properties may exist in a different polymorph than the one actually isolated, with different physical characteristics.
- **Atmospheric sensitivity:** Reactions sensitive to oxygen or moisture depend heavily on technique -- glovebox, Schlenk line, or just a nitrogen balloon -- and the skill with which each is used.

### Publication culture

The *Heliyon* review also found that chemistry papers contain more "hyping" language than those in other disciplines with 2.54 promotional terms per 100 words on average. Phrases like "novel", "superior", "unprecedented", and "highly efficient" appear routinely regardless of the strength of the underlying evidence. This does not cause irreproducibility directly, but it correlates with selective reporting: the pressure to present positive, impactful results discourages the publication of failure modes, contradictory results, and the conditions under which a method does *not* work.

## The Industrial Perspective

The stakes become clearest in pharmaceutical and applied chemistry contexts. Bayer HealthCare reported that only 7 of 67 internal target validation projects (around 10%) were fully reproducible, with published and in-house data agreeing in only 20--25% of cases. Amgen reported that 89% of landmark oncology results they attempted to replicate could not be confirmed.

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

## Challenge 7: Reproducibility Detective

Below is an excerpt from the methods section of a fictional chemistry paper. Read it carefully, then discuss with a neighbour:

1. What information is missing that would be needed to reproduce this experiment?
2. Which missing details do you think are most likely to affect the outcome?
3. What metadata should the authors have recorded and where?

---

> *"The catalyst was prepared according to our previously reported method and was used without further purification. NMR spectra were recorded on a standard spectrometer. The reaction was carried out at elevated temperature under inert atmosphere in dry solvent. The mixture was stirred until complete, as judged by TLC. Yields were determined by standard analytical methods and are reported as averages of three independent runs."*

:::::::::::::::  solution

## Discussion

This excerpt is almost entirely uninformative for reproduction purposes. Some of the missing details:

**Catalyst:** Which previously reported method? From which paper? What batch number and purity? Was it freshly prepared or stored, and how?

**NMR:** Which nucleus? What field strength (MHz)? Which solvent? What reference standard? What concentration? Which instrument model and at what temperature?

**Reaction conditions:** What temperature, exactly? What inert atmosphere -- nitrogen or argon, and how was it maintained? Which solvent, and how was it dried? What concentration of reagents? What scale?

**"Until complete, as judged by TLC":** What TLC system (solvent, plate type, staining)? What Rf values indicated completion? How long did this take?

**Yields:** What analytical method -- weight, NMR, titration? What are the actual values from three runs, not just the average? What was the variance?

The phrase "standard" appears three times in this excerpt and specifies nothing. What seems obvious to the author may be far from obvious to someone in a different lab, institution, or country -- and even within the same group, "standard" conditions may differ between researchers.

**Where should this metadata have been recorded?** In an ELN at the time of the experiment, attached to the raw data files, and included in the supplementary information at publication. Many of these details can be captured automatically by instruments if the metadata is set up correctly.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  keypoints

- Chemistry is fundamentally a reproducible science, but inadequate methods reporting and poor data management undermine this in practice.
- Experimental details that seem obvious to the author -- solvent source, exact temperature, reagent purity -- are often critical for reproduction.
- Publication pressure and selective reporting compound the problem: failure modes rarely appear in the literature.
- Good RDM practices -- recording metadata systematically, keeping raw data, documenting processing steps -- directly address the most preventable causes of irreproducibility.

::::::::::::::::::::::::::::::::::::::::::::::::::
