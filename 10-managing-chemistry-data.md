---
title: "Managing Data from Common Chemistry Techniques"
teaching: 12
exercises: 8
---

::::::::::::::::::::::::::::::::::::::: objectives

- Apply good data management practices to data from common analytical techniques
- Identify the metadata required for NMR, IR, and mass spectrometry records
- Understand the data management challenges posed by high-throughput and large-scale facilities

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What metadata should I record for each analytical technique I use?
- How do I keep my raw data safe and well-organised across a multi-technique project?
- What changes when experiments are run at scale?

::::::::::::::::::::::::::::::::::::::::::::::::::

## A Day in the Lab

The best way to understand chemistry data management in practice is to follow a realistic
workflow from bench to publication. Consider a researcher synthesising a new compound
and characterising it by NMR, IR, and mass spectrometry. At each stage, data management
decisions are either made or missed.

### Step 1: Synthesis and ELN entry

The reaction is set up and recorded in an electronic lab notebook. This is the point at
which several critical pieces of metadata should be captured:

- Batch numbers and purities of all starting materials and reagents
- Exact masses and equivalents used (not just "10 mg" but enough to reconstruct the
  stoichiometry)
- Instrument and conditions: reaction temperature, inert atmosphere method (glovebox,
  Schlenk line, nitrogen balloon), stirring rate, time
- Solvent identity and drying method, where relevant

This information is easiest to record in real time. Reconstructing it from memory a
week later is error-prone; reconstructing it from memory two years later for a
resubmission is nearly impossible.

### Step 2: NMR acquisition

The compound goes on the NMR spectrometer. Good practice at this step means:

- Saving the raw FID alongside the processed spectrum. Never keep only the processed
  spectrum, because the processing choices (phasing, baseline correction, integration)
  become impossible to review or redo
- Recording the full acquisition parameters: nucleus (¹H, ¹³C, etc.), field strength
  (e.g. 400 MHz), solvent, temperature, pulse sequence, reference compound, and
  concentration
- Exporting to JCAMP-DX alongside the vendor format (Bruker `.fid`, Varian, etc.) for
  long-term accessibility
- Naming the file consistently -- the file name should identify the compound, technique,
  and experiment date unambiguously

### Step 3: IR and mass spectrometry

The same principles apply:

- **IR:** Record whether ATR or transmission mode was used, the resolution, the wavenumber
  range, and how the sample was prepared. These parameters affect whether results from
  different instruments can be compared.
- **Mass spectrometry:** Record the ionisation method (ESI, APCI, EI, MALDI, etc.),
  instrument model, mass range, resolution, and calibration standard. High-resolution
  mass spectrometry data files can be very large so plan storage accordingly.

:::::::::::::::::::::::::::::::::::::::  challenge

## What Is Missing From This Record?

A researcher submits the following metadata record to accompany an NMR spectrum in a
repository:

> **File:** compound_14_NMR.jdx
> **Instrument:** Bruker
> **Solvent:** CDCl₃
> **Date:** 2024-11-05

Which essential pieces of metadata are missing from this record? Choose all that apply.

- A. The field strength (e.g. 400 MHz or 600 MHz)
- B. The nucleus measured (¹H, ¹³C, DEPT, etc.)
- C. The colour of the compound
- D. The pulse sequence used
- E. The reference compound (e.g. TMS, residual solvent)
- F. The concentration of the sample
- G. The instrument software version

:::::::::::::::  solution

**A, B, D, E, and F are all missing and are essential metadata for NMR.**

Without the field strength and nucleus, you cannot interpret the spectrum (¹H at 400 MHz
and ¹³C at 100 MHz are very different experiments). Without the pulse sequence, you
cannot know whether any special experiment was run. Without the reference compound and
concentration, quantitative comparisons are unreliable.

**C (compound colour)** is not NMR metadata but it is useful information for an ELN entry
but not for the spectrum record.

**G (software version)** is good practice to record because processing artefacts can be
software-version-dependent, but it is less critical than A, B, D, E, and F for
basic reusability.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## Organising a Multi-Technique Project

Across a project generating NMR, IR, MS, and possibly crystallographic or computational
data, a consistent folder structure and file naming scheme become essential. Without
them, finding the raw FID for compound 47 from three years ago or linking an NMR
spectrum to the correct ELN entry becomes an investigation in itself.

A practical folder structure for a synthetic chemistry project:

```
project-name/
├── 01_raw-data/
│   ├── NMR/
│   │   ├── 2024-11-05_cpd14_1H_400MHz.fid
│   │   └── 2024-11-05_cpd14_1H_400MHz.jdx
│   ├── IR/
│   ├── mass-spec/
│   └── XRD/
├── 02_processed-data/
├── 03_analysis/
├── 04_manuscripts/
└── 05_documentation/
    ├── README.md
    └── data-dictionary.csv
```

The `README.md` file at the project root should explain the naming scheme, describe
the folder structure, and cross-reference the ELN. The `data-dictionary.csv` should
define any abbreviations used in file names. Neither of these takes long to write at
the start of a project, and both are invaluable when you revisit the data later or
when someone else inherits the project.

:::::::::::::::::::::::::::::::::::::::  callout

## Tip: Raw Data Is Sacred

Make raw instrument files read-only as soon as you copy them off the instrument. On
most systems this is a single right-click or `chmod -w` command. This prevents
accidental overwriting or deletion, and makes it immediately obvious to anyone who
opens the folder that these files should not be modified. All processing should
happen on copies in the `02_processed-data/` folder.

::::::::::::::::::::::::::::::::::::::::::::::::::

## High-Throughput Facilities

High-throughput experimentation (HTE) changes the data management challenge dramatically.
Automated platforms such as the
[Rapid Online Analysis of Reactions (ROAR)](https://www.imperial.ac.uk/rapid-online-analysis-of-reactions/)
at Imperial College can run hundreds of reactions per day with inline analytics,
producing thousands of data points in a single experiment. Each reaction generates a
reaction record, metadata, and one or more raw files.

At this scale, manual data recording is not feasible. The key requirements are:

- **Automated metadata capture:** Instrument control software must log parameters
  directly into the data files or a companion metadata file. Relying on a researcher
  to transcribe conditions from a notebook is too slow and too error-prone.
- **Consistent naming and structure:** With hundreds of files per run, ad hoc naming
  breaks down immediately. File names and folder structures must follow a defined
  schema from the outset.
- **Cataloguing:** A machine-readable manifest (for example, a CSV file linking each
  reaction to its raw data files, conditions, and outcomes) is essential for downstream
  analysis. This is the kind of structured metadata record we explored in Episode 8.
- **Storage planning:** A single HTE run can generate tens of gigabytes of raw data.
  Plan storage capacity and backup strategy before data collection begins, not after.

## Large-Scale Facilities

Synchrotron and neutron sources including
[Diamond Light Source](https://www.diamond.ac.uk/) and
[ISIS Neutron and Muon Source](https://www.isis.stfc.ac.uk/) in the UK produce very
large datasets from single experiments. These facilities have their own data management
infrastructure, but researchers still need to plan for:

- **Data transfer:** How will you get terabytes of data from the facility to your
  institution? Facilities often provide temporary storage and data transfer services,
  but you need to know what they offer before your beam time starts.
- **Institutional storage:** Check in advance that your institution's storage allocation
  is sufficient. A single synchrotron experiment can exceed default allocations.
- **Facility-specific metadata standards:** Diamond and ISIS use specific metadata
  schemas and file formats (NeXus format for neutron data, for example). Familiarise
  yourself with these before your visit.
- **Embargo and access policies:** Some facility data is subject to an embargo period
  before public release. Understand the policy for your beamline.

In both HTE and large-scale facility contexts, the underlying RDM principles are
identical to a small-scale experiment: record metadata systematically, use consistent
names, keep raw data safe, and plan for deposition. The scale just means that failures
are more expensive and harder to recover from.

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge 10: Mini Data Management Plan

Your group has been awarded funding for a project that involves:

- Synthesising 50 new compounds
- Characterising each by ¹H NMR, ¹³C NMR, IR, and high-resolution mass spectrometry
- Running 10 of them through a high-throughput screening facility
- Publishing results in an RSC journal

In groups of 3--4, spend 8 minutes sketching a mini data management plan:

1. What file naming convention will you use? Write an example file name for a ¹H NMR
   spectrum of compound 23.
2. What metadata will you record for each NMR spectrum? List at least five items.
3. Where will you store raw data during the project?
4. Which repository will you deposit the data in at publication, and why?
5. Roughly how much storage do you think you will need? (Make a back-of-envelope estimate.)

:::::::::::::::  solution

## Discussion

**1. File naming.** A good example:
`2025-03-15_cpd023_1H-NMR_400MHz.fid` (raw) and `2025-03-15_cpd023_1H-NMR_400MHz.jdx`
(exported open format). Key elements: date, compound identifier, technique,
field strength. Avoid spaces and special characters.

**2. NMR metadata.** Essential items: field strength, nucleus, solvent, pulse sequence,
reference compound, temperature, instrument model, acquisition date. Also useful:
concentration, number of scans, processing parameters.

**3. Storage.** Institutional managed storage is the right choice for active project data.
Avoid relying on local hard drives or USB devices.

**4. Repository.** The Chemotion Repository is the best choice for this type of project
(reaction data, NMR, MS, IR). Institutional repository deposit may also be required.
Zenodo is a valid fallback if Chemotion does not suit your data. For journals requiring
it, CSD deposition would be needed for any crystal structures.

**5. Storage estimate.** Rough numbers: a Bruker ¹H FID is typically 1--10 MB;
¹³C and 2D spectra are larger. For 50 compounds × 2 nuclei × ~5 MB average = ~500 MB
for NMR alone. IR and MS data are smaller. HTE data could easily add gigabytes.
A rough estimate of 5--20 GB for the full project is reasonable to plan around.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  keypoints

- Record metadata for every analytical measurement at the time of acquisition -- it
  cannot be reliably reconstructed later.
- For NMR, always save the raw FID alongside the processed spectrum, and record
  field strength, nucleus, solvent, pulse sequence, and reference compound as a minimum.
- A `README.md` and `data-dictionary.csv` at the root of every project folder cost
  little time to write and save a great deal of confusion later.
- High-throughput and large-scale facilities require automated metadata capture and
  advance storage planning -- the same principles apply, but the consequences of
  skipping them are much larger.
- Open format exports (JCAMP-DX for spectra, CIF for crystal structures) should
  accompany vendor format raw files for all deposited data.

::::::::::::::::::::::::::::::::::::::::::::::::::
