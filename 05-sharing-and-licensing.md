---
title: "Sharing, Preserving, and Licensing Your Data"
teaching: 10
exercises: 10
---

::::::::::::::::::::::::::::::::::::::: objectives

- Explain the key reasons to share research data openly
- Choose an appropriate repository for a given dataset
- Select a licence that allows appropriate reuse of your data
- Write a data access statement that meets funder requirements

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- Why should I share my research data, and what are my options?
- How do I choose a repository and a licence?
- What is a data access statement and when do I need one?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Why Share Your Data?

Data sharing is increasingly expected -- by funders, publishers, and the research community -- but the underlying reasons go beyond compliance. Shared data:

- **Enables reproducibility.** Others can verify your results and build on your work without starting from scratch.
- **Generates credit.** A dataset with a DOI can be cited independently of the paper, giving you a citable output for work that would otherwise be invisible.
- **Increases efficiency.** Experiments do not have to be repeated, and computational researchers can validate methods against real datasets.
- **Is increasingly required.** UKRI, EPSRC, and most major journals now mandate data sharing or, at minimum, a statement explaining why data cannot be shared.

The question is not really whether to share, but how.

## The Spectrum of Data Sharing

Data sharing is not all-or-nothing. In rough order from most to least desirable:

1. **Deposit in a data repository** -- data gets a DOI, is discoverable, and is preserved long-term. This is best practice.
2. **Restricted/controlled access** -- some repositories (e.g. the UK Data Service) provide tiered access for sensitive data, where users must register or agree to terms before downloading. The data is still findable and citable.
3. **Supplementary information** -- some journals host small datasets alongside papers. Discoverability is limited, there is usually no DOI, and long-term preservation is not guaranteed. Use this only for small illustrative datasets, not as a substitute for repository deposit.
4. **"Available upon request"** -- should be a last resort. Evidence consistently shows that requests frequently go unanswered, contact details become stale, and data may no longer exist. The practical availability of "on request" data drops sharply within just a few years of publication.

## Choosing a Repository

When selecting where to deposit data, a simple hierarchy applies:

1. **Domain-specific repository** -- best for discoverability within your field and most likely to apply community standards and metadata schemas. Examples: Chemotion Repository (synthetic chemistry), NOMAD (computational materials), Cambridge Structural Database (crystal structures). We will cover these in more detail in Part 2.
2. **Institutional repository** -- most UK universities have one, and depositing here formally links your dataset to your institution's research outputs and reporting systems. Some funders require deposit in an institutional repository as well as (or instead of) a domain-specific one. Check your institution's guidance.
3. **General-purpose repository** -- [Zenodo](https://zenodo.org/) (hosted by CERN, with an explicit 20-year preservation commitment) and [Figshare](https://figshare.com/) are widely used fallbacks. Both are free, mint DOIs automatically, and are trusted by funders. If no domain-specific repository exists for your data type, Zenodo is a safe default.

:::::::::::::::::::::::::::::::::::::::::  callout

## ML and Community Platforms Are Not a Substitute

For computational or AI-adjacent research, community platforms such as Kaggle and Hugging Face Hub offer useful tools and visibility for models and datasets. However, they do not provide DOIs or the same long-term preservation guarantees as a research archive. Use them in addition to a proper repository (such as Zenodo) rather than as your primary deposit.

:::::::::::::::::::::::::::::::::::::::::::::::::

The key thing a repository gives you that supplementary information cannot is a **Digital Object Identifier (DOI)** -- a persistent link that remains stable even if the underlying URL changes, making your data citable and findable for the long term.

## Licensing Your Data

Depositing data without a licence does not make it freely reusable. Without a licence, the default legal position is "all rights reserved." While individual facts are not protected by copyright, the structure, selection, documentation, and any associated database rights usually are, meaning that cautious researchers will avoid reusing unlicensed data rather than risk infringement. A licence tells others exactly what they are permitted to do, turning your data from "visible but unusable" into a reusable research output.

### Data licences

For most deposited datasets -- a CSV of experimental results, a collection of spectra, a table of computed properties -- a **Creative Commons** licence is appropriate:

- **CC-BY** (Attribution) is the recommended default for research data. Free to use, adapt, and redistribute for any purpose, including commercially, as long as the original source is credited.
- **CC-BY-SA** (Attribution-ShareAlike) is the same permissions as CC-BY, but with the condition that any derivatives must be released under the same licence. Use this if you want the "share-alike" condition to propagate downstream.
- **CC0** (Public Domain Dedication) has no restrictions whatsoever: no attribution required. An option where maximum reuse with minimum friction is the priority, and attribution credit is not important to the researcher.
- **CC-BY-NC** (Attribution-NonCommercial) restricts commercial use. This sounds appealing but in practice limits reuse significantly: many universities count as commercial entities under some interpretations, and the restriction can prevent reuse in ways you did not intend. Avoid unless a specific contractual obligation requires it.

### Database licences

If you are releasing a structured, searchable data collection -- a relational database, a curated online resource, or an API-driven platform -- a **Creative Commons** licence may not cover the underlying database rights. In these cases, consider an **Open Data Commons** licence instead:

- **ODC-By** (Attribution) is the recommended default for databases. Freely share, modify, and use the database, providing attribution.
- **ODbL** (Open Database Licence) makes attribution required, and any derivative databases must be released under the same terms.

In practice, if you are depositing a fixed collection of files in a repository, treat it as a dataset and use Creative Commons. If you are releasing a maintained, queryable platform, treat it as a database and consider Open Data Commons.

If your data involves contractual restrictions (e.g. data under NDA or from an industrial collaboration), discuss the appropriate approach with your institution's legal or technology transfer team before depositing anything.

:::::::::::::::::::::::::::::::::::::::  challenge

## Check Your Understanding: Which Licence?

For each of the following situations, which licence would be most appropriate? Discuss with a neighbour.

**Situation A.** A crystallographic dataset from a purely academic project, with no commercial partners and no contractual restrictions. The researcher wants maximum reuse with attribution.

**Situation B.** A set of reaction yield data produced in collaboration with an industrial partner. The agreement with the company prohibits commercial use of the data by third parties.

**Situation C.** A researcher wants her data to be freely reusable, but wants to ensure that anyone who builds on it and publishes a derivative dataset also makes that derivative freely available.

:::::::::::::::  solution

## Discussion

**Situation A:** **CC-BY** is the recommended default -- permits any use including commercial, requires attribution, and is widely understood by researchers and institutions. If attribution credit is not important to the researcher, **CC0** is also a valid choice for maximum reuse with minimum friction.

**Situation B:** **CC-BY-NC** reflects the contractual constraint. However, it is worth flagging that this will limit reuse more broadly than intended -- many academic institutions can be interpreted as commercial under NC clauses. The better long-term solution is to negotiate more permissive terms with the industrial partner at the outset, or to apply a time-limited embargo before releasing under CC-BY.

**Situation C:** **CC-BY-SA** is the licence designed for this: anyone who adapts the data must release their adaptation under the same terms. This is a legitimate choice, but it is worth thinking through whether "share-alike" is really what the researcher wants -- it can create compatibility problems with other licences downstream.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## Data Access Statements

All UKRI-funded publications must include a **data access statement** -- a short paragraph explaining where associated data can be found and under what terms. This is required even when there are no data (in which case a statement to that effect is needed). The requirement also applies increasingly to non-UKRI funders and many journals regardless of funding source.

A good data access statement includes:

- Where the data can be accessed (with a DOI or persistent link)
- The licence under which data can be used
- An explanation if data cannot be shared -- and the reason why

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge: Evaluate These Data Access Statements

Below are three fictional data access statements from chemistry papers. For each one, discuss with a neighbour:

1. Does it meet UKRI requirements?
2. Could you actually find and access the data based on this statement?
3. How would you improve it?

---

**Statement A**

> "Data are available from the corresponding author upon reasonable request."

---

**Statement B**

> "Raw NMR, IR, and mass spectrometry data supporting this study are deposited in the Chemotion Repository at <https://doi.org/10.14272/xxxxx> under a CC-BY 4.0 licence. DFT input and output files are available on Zenodo at <https://doi.org/10.5281/zenodo.xxxxx> under CC0."

---

**Statement C**

> "All data supporting the conclusions of this paper are included in the supplementary information."

:::::::::::::::  solution

## Discussion

**Statement A** does not meet UKRI requirements. "Available on request" is explicitly discouraged: there is no persistent link, no licence, no guarantee of long-term access, and the author may not be reachable in five years. It also makes verification of results nearly impossible.

**Statement B** is a strong example. It names the repositories, gives DOIs (persistent and citable), specifies a licence for each dataset type, and separates experimental and computational outputs. A reader can access the data immediately without contacting anyone.

**Statement C** is borderline. Supplementary information does not have a DOI, is not independently discoverable, and long-term preservation depends on the journal's policies. For small illustrative datasets it may be acceptable, but it should not be used for primary data that others might want to reuse. It also gives no licence, which makes the legal status of reuse unclear.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## Data Preservation

Sharing data at publication is important, but so is ensuring it remains usable over time. EPSRC requires funded research data to be preserved for a minimum of ten years from the point of last access. A few things affect long-term usability:

- **File formats.** Proprietary formats can become unreadable as software changes. Prefer open, non-proprietary formats where possible: CSV over XLSX, JCAMP-DX over vendor-specific spectral formats, CIF for crystal structures. We will return to chemistry-specific formats in Part 2.
- **Documentation.** A dataset without a README or data dictionary is difficult to interpret even a few years later -- and nearly impossible for someone who was not involved in the research. Write documentation as you go, not as an afterthought before submission.
- **Repository choice.** General-purpose repositories like Zenodo have explicit long-term preservation commitments. Not all institutional repositories do -- check your institution's retention policy before depositing data you need to preserve for ten years.

:::::::::::::::::::::::::::::::::::::::  callout

## End of Part 1

This concludes Part 1 on general research data management principles. After a
break, Part 2 applies everything covered so far to the specific challenges of
chemistry research.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  keypoints

- Share your data via a repository: it makes your work citable, discoverable, and preserved long-term.
- Choose domain-specific repositories first; Zenodo is a good general-purpose fallback.
- Always apply a licence. Without one, the default is "all rights reserved" and others cannot safely reuse your data. CC-BY is the recommended default for research datasets; use Open Data Commons licences (ODC-By) for structured databases.
- All UKRI-funded publications require a data access statement, even when there is no associated data.
- Prefer open file formats and include documentation to ensure data remains usable for the required ten-year preservation period.

::::::::::::::::::::::::::::::::::::::::::::::::::
