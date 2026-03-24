---
title: "PSDI and the Chemistry Data Landscape"
teaching: 10
exercises: 0
---

::::::::::::::::::::::::::::::::::::::: objectives

- Describe what the Physical Sciences Data Infrastructure (PSDI) is and what it provides
- Identify PSDI tools and resources relevant to your own work
- Place PSDI in the context of the wider chemistry data ecosystem

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What is PSDI and how can it help me manage chemistry data?
- How does the UK chemistry data infrastructure connect to international initiatives?
- Where can I go for further training and support in chemistry data management?

::::::::::::::::::::::::::::::::::::::::::::::::::

## What Is PSDI?

The **Physical Sciences Data Infrastructure** ([PSDI](https://www.psdi.ac.uk/)) is a
UK initiative funded by UKRI that supports researchers in chemistry, materials
science, and related physical sciences to work with research data more effectively.
Rather than building a single monolithic platform, PSDI focuses on connecting and
strengthening the data ecosystem that already exists: repositories, standards,
conversion tools, and training.

PSDI works alongside and complements other UK infrastructure, including institutional
RDM services, the Carpentries training network, and the Diamond and ISIS large-scale
facilities. Its tools and resources are freely available to all researchers regardless
of their funder or institution.

## PSDI Resources and Tools

### Data Conversion Service

One of the most practical barriers to open, FAIR chemistry data is format conversion.
Vendor instrument files (Bruker `.fid`, Agilent `.d`, Thermo `.raw`) need to become
open formats (JCAMP-DX, mzML, CIF) for deposition, and this conversion is often
technically difficult or lossy.

PSDI provides a [Data Conversion Service](https://data-conversion.psdi.ac.uk/) that handles
common chemistry format conversions and, importantly, assesses the quality of the
conversion. It is available as a web application, a command-line tool, and a Python
library, making it accessible at every level of technical confidence.

### Data Revival

Legacy data -- spectra recorded on instruments no longer in service, data stored in
obsolete formats, or results captured only on paper -- represents a large body of
scientific knowledge that is increasingly inaccessible. PSDI's **Data Revival** service
uses AI-assisted tools to transform handwritten lab notes and legacy records into
machine-readable data, making it possible to integrate historical datasets into modern
workflows.

### Resource Catalogue

PSDI maintains a curated catalogue of high-quality data sources relevant to physical
scientists, both open and commercial. Rather than searching the web for relevant
databases and repositories, the catalogue provides a vetted starting point.

### Guidance and Training

PSDI publishes practical guidance for physical scientists on working with research data:
tool documentation, worked examples, and best-practice recommendations. Much of this
material is chemistry-specific and complements more generic RDM training resources
like the ones covered in Part 1 of this workshop.

### CaMML School

The **Chemistry and Materials Machine Learning (CaMML) School** is a PSDI-supported
training programme for PhD students and early-career researchers, covering data-driven
approaches to chemistry and materials research. If you are interested in machine
learning applied to chemical data, this is a good next step.

> PSDI Resources: [resources.psdi.ac.uk](https://resources.psdi.ac.uk/)
> PSDI on GitHub: [github.com/PSDI-UK](https://github.com/PSDI-UK)

## The Wider Chemistry Data Landscape

PSDI does not operate in isolation. The chemistry data ecosystem is increasingly
international and interconnected, with several major initiatives working towards
compatible standards and infrastructure.

**NFDI4Chem** (Germany) maintains the Chemotion ecosystem and a detailed knowledge
base for chemistry RDM. Its community standards for NMR, mass spectrometry, and
synthetic chemistry are internationally recognised best practice regardless of where
you work.

**IUPAC** coordinates digital chemistry standards through its Committee on Publications
and Cheminformatics Data Standards (CPCDS), including InChI, SMILES, and the FAIRSpec
standard for spectroscopic data. These standards form the language that connects
instruments, notebooks, repositories, and publications.

**Horizon Europe**, the EU's research funding framework, requires open data by
default under the principle "as open as possible, as closed as necessary." As
collaborative projects with European partners become more common, understanding this
framework is increasingly relevant for UK researchers.

The long-term vision is a connected ecosystem: data flows from an instrument into an
ELN, is annotated with standard identifiers and metadata, exported in an open format,
deposited in a domain-specific repository, assigned a DOI, and cited in a publication
-- with each step automated or assisted as far as possible. We are not fully there yet,
but the infrastructure described in this workshop is moving steadily in that direction.

:::::::::::::::::::::::::::::::::::::::  keypoints

- PSDI provides practical tools and guidance for chemistry and physical sciences data
  management in the UK, including format conversion, legacy data digitisation, and
  training resources.
- The chemistry data ecosystem is becoming more connected: PSDI, NFDI4Chem, and IUPAC
  are working towards compatible standards that connect instruments, notebooks,
  repositories, and publications.
- You do not need to adopt everything at once -- picking one or two concrete
  improvements and building from there is more sustainable than an overhaul.
- re3data.org, the NFDI4Chem Knowledge Base, and PSDI Resources are all free starting
  points for further learning.

::::::::::::::::::::::::::::::::::::::::::::::::::
