---
title: "FAIR Data Principles"
teaching: 10
exercises: 10
---

::::::::::::::::::::::::::::::::::::::: objectives

- Explain the four FAIR principles and what each means in practice
- Distinguish between FAIR data and open data
- Assess how FAIR a dataset is using a simple checklist

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What does FAIR data mean?
- Is FAIR the same as open?
- How do I know if my data is FAIR?

::::::::::::::::::::::::::::::::::::::::::::::::::

## What Is FAIR?

FAIR is a set of guiding principles for research data, first published in
*Scientific Data* in 2016. The acronym stands for:

- **Findable**
- **Accessible**
- **Interoperable**
- **Reusable**

These principles were developed to address a straightforward problem: vast
amount of research data exist but cannot easily be found, understood, or
reused, **even by the researchers who generated them**. FAIR is not a standard
or a certification. It is a framework for thinking about what good data
management looks like from the perspective of someone who wants to use
your data in the future (including your future self).

> Wilkinson, M.D. et al. (2016) "The FAIR Guiding Principles for scientific
> data management and stewardship." *Scientific Data* 3, 160018.
> [doi:10.1038/sdata.2016.18](https://doi.org/10.1038/sdata.2016.18)

## The Four Principles

### Findable

Data should be easy to find, both for humans and machines. This means:

- Assigning a **persistent identifier** (such as a DOI) to your dataset so
  it can be reliably linked to and cited
- Describing the data with **rich metadata**: information about what the
  data contains, how it was generated, and how to access it
- Registering the data in a **searchable resource** such as a data repository

A dataset buried in a supplementary file attached to a journal article with
no identifier and no metadata is not findable. A dataset deposited in a
repository with a DOI, a descriptive title, and keywords is.

### Accessible

Once someone has found your data, they should be able to retrieve it. This
means:

- The data (or at minimum its metadata) can be accessed using a **standard protocol**
  such as HTTP or FTP, not a proprietary system requiring
  special software
- **Authentication and authorisation** may be applied where necessary (for
  example, restricted access to sensitive data), but the process for
  requesting access should be clear
- **Metadata should remain accessible** even if the data itself is no longer
  available so that others can at least discover what once existed

### Interoperable

Data should be able to be combined with other data and used with different
tools and workflows. This means:

- Using **formal, widely used, and openly available formats** (JCAMP-DX for
  spectra, CIF for crystal structures) rather than proprietary vendor formats
- Using **shared vocabularies and ontologies**, for example, identifying
  molecules using InChI or SMILES rather than informal names that may mean
  different things in different contexts
- Including **references to other relevant datasets** where appropriate

Interoperability is where chemistry has historically struggled most. Data
from different instruments, groups, and fields often cannot be combined
without significant manual effort, simply because no common formats or
identifiers were used.

### Reusable

Data should be sufficiently well described that it can be understood and
reused by others (and by you, years later). This means:

- Providing **rich provenance information**: Where did the data come from,
  how was it processed, what instrument was used and under what conditions?
- Applying a **clear licence** so others know what they are permitted to do
  with the data (more on this in a later episode)
- Meeting **community standards** for the relevant domain. In chemistry,
  this might mean following IUPAC recommendations for spectral data or
  depositing crystal structures with the CSD

:::::::::::::::::::::::::::::::::::::::::  callout

## FAIR Is a Spectrum, Not a Switch

No dataset is perfectly FAIR, and improving FAIRness is an ongoing process
rather than a one-time task. A dataset with a DOI and a clear licence is
more FAIR than one without, even if it is not yet using a standard file
format. The goal is to make incremental improvements, starting with the
changes that have the biggest impact for the least effort.

The two highest-impact things most researchers can do immediately are:
deposit data in a repository (gains F and A), and apply a licence (gains R).

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## Check Your Understanding: FAIR or Not FAIR?

For each scenario below, identify which FAIR principle(s) are being
violated, and what could be done to fix it.

A. A researcher deposits their NMR spectra as proprietary Bruker `.fid`
files in Zenodo with a DOI, but includes no information about the
instrument, solvent, or compounds measured.

B. A paper includes the line: "Data are available from the corresponding
author upon reasonable request."

C. A dataset is deposited in a repository under a CC-BY licence with
rich metadata and a DOI, but the files are in a format that requires
a £500/year commercial software licence to open.

:::::::::::::::  solution

## Discussion

**A** violates **Reusable** (and arguably **Interoperable**). The dataset
has a DOI (Findable) and can be downloaded (Accessible), but without
metadata about the instrument, solvent, nucleus, or compounds, no one can
interpret the spectra. The fix: add a README or metadata record describing
the experimental conditions for each file.

**B** violates **Findable** and **Accessible**. There is no identifier, no
repository, and no guarantee the author will respond or that the data will
still exist in five years. Evidence suggests that "available on request"
frequently means "not actually available". The fix: deposit the data in a
repository and replace the statement with a DOI.

**C** violates **Interoperable** (and arguably **Accessible** in practice).
The legal access conditions are fine (open licence, accessible repository),
but the data cannot actually be used without expensive proprietary software.
The fix: export to an open format such as csv, json, mzML (for mass spec) etc.,
alongside the proprietary files.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## FAIR Is Not the Same as Open

This is one of the most common misconceptions about FAIR. The two concepts
are related but distinct:

- **Open** data means anyone can access and use it freely, with no
  restrictions.
- **FAIR** data means it is well described, findable, and usable -- but it
  may still have access restrictions.

A dataset can be FAIR but not open: for example, sensitive patient data or
commercially confidential compounds might be deposited in a repository with
full metadata and a clear licence, but with access controlled so that only
approved users can download the actual files. The metadata is still
findable and the access process is clear. That is FAIR, even though the
data is not open.

Conversely, data can be open but not FAIR: a file uploaded to a personal
website with no metadata, no licence, and no persistent identifier is
technically accessible to anyone, but it is not FAIR.

The principle to remember: **metadata should always be as open as possible, even when the data itself cannot be.**

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge 3: How FAIR Is Your Data?

Think of a dataset you have generated as part of a recent publication, even something simple
like a set of analysis files from an experiment or a table of results.
Or, if you can't think of a specific dataset of your own, think of a dataset from a paper you have read recently.

Using the checklist below, score it against each FAIR principle. Be honest.

**Findable**

- [ ] Does it have a persistent identifier (DOI or similar)?
- [ ] Is it described with a title, keywords, and a summary?
- [ ] Is it registered in a searchable repository?

**Accessible**

- [ ] Can someone download it without needing specialist software or
      institutional access?
- [ ] Is there a clear process for accessing it if it is restricted?

**Interoperable**

- [ ] Is it in an open, non-proprietary file format?
- [ ] Does it use standard identifiers (e.g. InChI for molecules)?

**Reusable**

- [ ] Does it have a licence?
- [ ] Is there enough metadata to understand how it was generated?
- [ ] Does it meet any relevant community standards for your field?

Discuss with your neighbour: which principle did you score lowest on?
What is the single easiest thing you could do to improve your score?

:::::::::::::::  solution

## Discussion

For most researchers, the honest answer is that datasets can score very poorly or very well against FAIR principles.
The point of the exercise is not to feel bad if your dataset scores low,
but to identify the gaps.

The most common weak spots are:

- **No persistent identifier** -- data is on a shared drive or a personal
  laptop, nowhere findable by anyone else
- **No licence** -- data exists but legally cannot be reused
- **Proprietary formats** -- spectra saved only as vendor files that
  require specific software
- **No metadata** -- files named `data_final.xlsx` with no accompanying
  documentation

The single highest-impact improvement for most people is to **deposit data in a repository when publishing**.
This gains F, A, and often R in one step. We will cover how to do this well in Episode 5.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: keypoints

- FAIR stands for Findable, Accessible, Interoperable, and Reusable: It is a framework for making data useful beyond its original context.
- FAIR is not the same as open: data can be FAIR with access restrictions, and open without being FAIR.
- Metadata should always be as open as possible, even when the data itself cannot be shared freely.
- Most researchers' current data scores poorly against FAIR principles -- the goal is incremental improvement, not perfection.
- The highest-impact steps are depositing data in a repository and applying a licence.

::::::::::::::::::::::::::::::::::::::::::::::::::
