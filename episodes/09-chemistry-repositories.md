---
title: "Chemistry Data Repositories and Databases"
teaching: 10
exercises: 8
---

::::::::::::::::::::::::::::::::::::::: objectives

- Identify domain-specific repositories for chemistry data
- Understand when to use a specialist repository rather than a general-purpose one
- Find and evaluate a chemistry repository relevant to your own research area

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- Where should I deposit chemistry data to make it findable and reusable?
- What chemistry-specific repositories exist and what do they accept?
- How do I choose the right repository for my data type?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Why Use a Chemistry-Specific Repository?

You can deposit almost any data in a general-purpose repository like Zenodo or Figshare,
satisfy most funder requirements, and obtain a DOI. So why bother with a domain-specific
repository?

The answer is discoverability and reusability. A general repository stores your files
and mints a DOI, but a chemistry-specific repository understands your data. It can
index compounds by chemical structure, enforce community metadata standards, validate
file formats, and link your deposition directly to established databases. A crystal
structure deposited in the Cambridge Structural Database (CSD) becomes part of a curated
collection of over a million structures, searchable by geometry, connectivity, or space
group. The same file sitting in Zenodo is just a file.

The hierarchy of preference introduced in Episode 5 applies directly here:

1. **Domain-specific repository:** always the first choice if one exists for your data type
2. **Institutional repository:** required by many UK universities for reporting purposes
3. **General-purpose repository:** (Zenodo, Figshare) -- always a valid fallback

## Key Chemistry Repositories

The table below covers some ofthe repositories most relevant to chemistry researchers in the UK.

| Repository | What it holds | Notes |
|------------|---------------|-------|
| **[Chemotion Repository](https://www.chemotion-repository.net/)** | Reaction data, NMR, MS, IR, UV-Vis | Free, open; integrates with Chemotion ELN; DOI minting |
| **[Cambridge Structural Database (CSD)](https://www.ccdc.cam.ac.uk/)** | Small-molecule crystal structures | Free to search; academic licence for full access; mandatory deposition for many journals |
| **[NOMAD](https://nomad-lab.eu/)** | Computational materials science data | Strong metadata standards for DFT, molecular dynamics |
| **[ioChem-BD](https://www.iochem-bd.org/)** | Computational chemistry (DFT, MD, etc.) | Accepts Gaussian, ORCA, CP2K, VASP outputs |
| **[RADAR4Chem](https://radar4chem.radar-service.eu/)** | General chemistry research data | Part of NFDI4Chem; accessible internationally |
| **[Protein Data Bank (PDB)](https://www.rcsb.org/)** | Protein and macromolecular structures | Essential for biochemistry and structural biology |
| **[Zenodo](https://zenodo.org/)** | Anything | Best fallback for data types without a specialist home |

:::::::::::::::::::::::::::::::::::::::  challenge

## Which Repository Would You Choose?

A researcher produces the following datasets during a project. For each one, select the
most appropriate repository from the options given and explain your reasoning.

**1.** A set of single-crystal X-ray diffraction data for a new organic small molecule.

- A. Zenodo
- B. Cambridge Structural Database (CSD)
- C. NOMAD
- D. Protein Data Bank

**2.** DFT input and output files from geometry optimisations of a series of
transition metal complexes.

- A. Chemotion Repository
- B. Cambridge Structural Database (CSD)
- C. ioChem-BD or NOMAD
- D. Figshare

**3.** Reaction yield data, ¹H NMR spectra, and mass spectra from a synthetic chemistry
project -- no crystal structures or computational data.

- A. NOMAD
- B. Protein Data Bank
- C. Chemotion Repository
- D. Zenodo is the only valid option for spectroscopic data

:::::::::::::::  solution

**1. B: Cambridge Structural Database (CSD).**
Crystal structure data for small organic molecules belongs in the CSD. Deposition is
mandatory for most crystallography journals, and the CSD is the world's curated
reference collection for this data type. Zenodo is a valid fallback but provides none
of the structural search, curation, or community visibility that the CSD offers.

**2. C: ioChem-BD or NOMAD.**
Both are designed for computational chemistry output files and understand DFT codes.
ioChem-BD is particularly well-suited for molecular systems; NOMAD has broader coverage
of solid-state and materials codes. Chemotion is oriented towards experimental synthetic
chemistry and does not handle DFT input/output files.

**3. C: Chemotion Repository.**
Chemotion is built for exactly this type of data: it understands reactions and spectra,
accepts JCAMP-DX and other open formats, links records to chemical structures, and
integrates with the Chemotion ELN. Answer D is wrong: Zenodo is a valid alternative,
but it is not the *only* option and is not the best choice when a domain-specific
repository exists.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## NFDI4Chem and the German Chemistry Data Infrastructure

**NFDI4Chem** is Germany's national initiative for chemistry research data infrastructure,
part of the broader National Research Data Infrastructure (NFDI). Despite being
German-led, its resources are freely available internationally and represent current
best practice for chemistry data management. NFDI4Chem maintains the Chemotion
ecosystem, working groups developing community standards for NMR and mass spectrometry,
and a detailed knowledge base at
[knowledgebase.nfdi4chem.de](https://knowledgebase.nfdi4chem.de/) covering repositories,
file formats, metadata standards, and practical guidance. Whether or not you are based
in Germany, the NFDI4Chem Knowledge Base is one of the best free resources for practical
chemistry RDM.

## Journal Policies and Mandatory Deposition

Many chemistry journals now require data deposition as a condition of publication.
Requirements vary by journal and are tightening across the field:

- **Crystal structures:** Deposition in the CSD is mandatory for most crystallography
  journals (RSC, Wiley, ACS). The CCDC reference number must be cited in the paper.
- **Spectroscopic data:** RSC journals expect supporting data to be deposited in a
  repository rather than attached as supplementary information.
- **Computational data:** Journals such as *Journal of Chemical Theory and Computation*
  encourage deposition of input and output files in a specialist repository.

Always check the specific journal's data policy before submission.

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge 9: Find and Evaluate a Repository

Go to [re3data.org](https://www.re3data.org/), a global registry of research data
repositories, and search for repositories relevant to your own area of chemistry.

Find one repository you were not previously aware of, then note down:

1. What is it called, and what type of data does it accept?
2. Does it mint DOIs?
3. Is it free to deposit?
4. What metadata standards or controlled vocabularies does it use?
5. What file formats does it require or recommend?

Share your findings with your neighbour.

:::::::::::::::  solution

## Discussion

Common finds  when navigating re3data.org for chemistry include:

- **Chemotion Repository** (synthetic chemistry, spectroscopy)
- **CSD/CCDC** (crystal structures)
- **NOMAD or ioChem-BD** (computational data)
- **MassBank** (mass spectrometry reference spectra)
- **nmrXiv** (NMR spectra, developed by NFDI4Chem)
- **Zenodo** (general fallback for any data type)

Key things to check: persistent identifiers (DOIs), long-term preservation commitments,
metadata standards enforced at upload, and whether the repository is indexed in re3data,
FAIRsharing, or DataCite. A repository that appears in multiple registries with an active
community is a safer long-term choice than one that is only recently established.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  keypoints

- Domain-specific repositories provide better discoverability and community-standard
  validation than general-purpose alternatives -- use them as your first choice.
- Key repositories for chemistry include Chemotion (synthetic/spectroscopic), CSD
  (crystal structures), NOMAD and ioChem-BD (computational), and Zenodo (general fallback).
- Crystal structure deposition in the CSD is mandatory for most crystallography journals.
- re3data.org and FAIRsharing.org are the best starting points for finding a repository
  appropriate for your data type.
- NFDI4Chem provides freely accessible guidance and tools for chemistry data management
  regardless of where you are based.

::::::::::::::::::::::::::::::::::::::::::::::::::
