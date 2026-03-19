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
4. **"Available upon request"** -- should be a last resort. Evidence shows that requests frequently go unanswered, contact details become stale, and data may no longer exist. A 2022 study found that data sharing rates dropped dramatically even a few years after publication when data was held "by the authors".

## Choosing a Repository

When selecting where to deposit data, a simple hierarchy applies:

1. **Domain-specific repository** -- best for discoverability within your field and most likely to apply community standards and metadata schemas. Examples: Chemotion Repository (synthetic chemistry), NOMAD (computational materials), Cambridge Structural Database (crystal structures). We will cover these in more detail in Part 2.
2. **Institutional repository** -- most UK universities have one, and some funders require deposit there as well as (or instead of) a domain-specific repository. Check your institution's guidance.
3. **General-purpose repository** -- [Zenodo](https://zenodo.org/) (hosted by CERN) and [Figshare](https://figshare.com/) are widely used fallbacks. Both are free, mint DOIs automatically, and are trusted by funders. If no domain-specific repository exists for your data type, Zenodo is a safe default.

The key thing a repository gives you that supplementary information cannot is a **Digital Object Identifier (DOI)** -- a persistent link that remains stable even if the underlying URL changes, making your data citable and findable for the long term.

## Licensing Your Data

Depositing data without a licence does not make it freely reusable -- it makes its legal status ambiguous, and cautious researchers will avoid it. Applying a licence is one of the most important steps you can take.

The Creative Commons licences are the standard for research data:

- **CC0** (public domain dedication) -- no restrictions whatsoever. The preferred choice for most research data: maximum reuse, minimum friction.
- **CC-BY** -- free to use, adapt, and redistribute, with attribution required. Widely used and still very permissive.
- **CC-BY-SA** -- attribution required, and any derivatives must be shared under the same terms. Less common for data.
- **CC-BY-NC** -- restricts commercial use. This sounds appealing but in practice limits reuse significantly: many universities count as commercial entities under some interpretations, and commercial-restriction licences can prevent reuse in ways you did not intend.

The general principle is to use the most permissive licence your situation allows. For most research data, **CC0 or CC-BY** are the right choices, and funders and repositories increasingly prefer them. If your data involves contractual restrictions (e.g. data under NDA, or proprietary compounds), you will need to discuss the appropriate approach with your institution's legal or technology transfer team.

:::::::::::::::::::::::::::::::::::::::  challenge

## Check Your Understanding: Which Licence?

For each of the following situations, which Creative Commons licence (CC0, CC-BY, CC-BY-SA, or CC-BY-NC) would be most appropriate? Discuss with a neighbour.

**Situation A.** A crystallographic dataset from a purely academic project, with no commercial partners and no contractual restrictions. The researcher wants maximum reuse.

**Situation B.** A set of reaction yield data produced in collaboration with an industrial partner. The agreement with the company prohibits commercial use of the data by third parties.

**Situation C.** A researcher wants her data to be freely reusable, but wants to ensure that anyone who builds on it and publishes a derivative dataset also makes that derivative freely available.

:::::::::::::::  solution

## Discussion

**Situation A:** **CC0** is ideal -- no restrictions, maximum discoverability and reuse. CC-BY would also be acceptable if attribution is important to the researcher, but for data (as opposed to software or creative works), CC0 is generally preferred.

**Situation B:** **CC-BY-NC** reflects the contractual constraint, though it is worth noting this will limit reuse more broadly. The better long-term solution may be to negotiate more permissive terms with the industrial partner from the outset, or to apply a time-limited embargo before releasing under CC-BY.

**Situation C:** **CC-BY-SA** is the licence designed for this: anyone who adapts the data must share their adaptation under the same terms. This is a legitimate choice but less common in research data practice -- worth thinking through whether the "share-alike" requirement matches the researcher's actual goals.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## Data Access Statements

All UKRI-funded publications must include a **data access statement** -- a short paragraph explaining where associated data can be found and under what terms. This is required even when there are no data (in which case a statement to that effect is needed). The requirement also applies increasingly to non-UKRI funders and many journals regardless of funding source.

A good data access statement includes:

- Where the data can be accessed (with a DOI or persistent link)
- The licence under which data can be used
- An explanation if data cannot be shared -- and the reason why

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge 6: Evaluate These Data Access Statements

Below are three fictional data access statements from chemistry papers. For each one, discuss with a neighbour:

1. Does it meet UKRI requirements?
2. Could you actually find and access the data based on this statement?
3. How would you improve it?

---

**Statement A**

> "Data are available from the corresponding author upon reasonable request."

---

**Statement B**

> "Raw NMR, IR, and mass spectrometry data supporting this study are deposited in the Chemotion Repository at https://doi.org/10.14272/xxxxx under a CC-BY 4.0 licence. DFT input and output files are available on Zenodo at https://doi.org/10.5281/zenodo.xxxxx under CC0."

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

:::::::::::::::::::::::::::::::::::::::  keypoints

- Share your data via a repository: it makes your work citable, discoverable, and preserved long-term.
- Choose domain-specific repositories first; Zenodo is a good general-purpose fallback.
- Always apply a licence -- without one, others cannot legally reuse your data. CC0 or CC-BY are preferred for most research data.
- All UKRI-funded publications require a data access statement, even when there is no associated data.
- Prefer open file formats and include documentation to ensure data remains usable for the required ten-year preservation period.

::::::::::::::::::::::::::::::::::::::::::::::::::
