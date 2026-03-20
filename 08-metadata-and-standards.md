---
title: "Metadata and Chemical Data Standards"
teaching: 12
exercises: 8
---

::::::::::::::::::::::::::::::::::::::: objectives

- Explain why metadata is essential for making chemistry data reusable
- Identify standard chemical identifiers and explain when to use each
- List the essential metadata for at least two common analytical techniques
- Describe the role of open file formats in chemical data interoperability

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What is metadata and why does it matter in chemistry?
- What are the standard identifiers for chemical compounds?
- What information should I record alongside my analytical data?

::::::::::::::::::::::::::::::::::::::::::::::::::

## What Is Metadata?

Metadata is data about data. It is the contextual information that transforms a raw file into a scientific record that someone else -- or your future self -- can find, understand, and use.

Consider this: if you open an NMR FID file from your hard drive and the filename is `compound3_run2.fid`, what do you know about the compound? The nucleus? The field strength? The solvent? The instrument? The date it was acquired? Almost certainly nothing. Now imagine someone trying to use that file five years later, without access to your memory, your notebook, or your group. This is the metadata problem in chemistry: it is not exotic or abstract, it happens every time an instrument produces a file with an auto-generated name and no accompanying record.

FAIR data, as discussed in Episode 3, is almost entirely a metadata problem. A dataset can be deposited in a repository with a DOI and a licence and still be almost useless if it lacks the metadata needed to interpret it.

**Metadata is what makes the difference between F-A-I-R data and merely F-A data.**

## Standard Chemical Identifiers

One of the most important metadata decisions in chemistry is how to identify the compounds in your data. There are several options, and they are not equally good for FAIR purposes.

### InChI and InChIKey

The **IUPAC International Chemical Identifier (InChI)** is a machine-readable, non-proprietary text representation of a chemical structure, maintained by IUPAC. It encodes the molecular formula, connectivity, stereochemistry, and other structural features into a layered string.

For example, the InChI for aspirin is:

```
InChI=1S/C9H8O4/c1-6(10)13-8-5-3-2-4-7(8)9(11)12/h2-5H,1H3,(H,11,12)
```

The **InChIKey** is a fixed-length 27-character hash of the InChI, designed for web search and database lookup:

```
BSYNRYMUTXBXSQ-UHFFFAOYSA-N
```

InChI and InChIKey are the preferred identifiers for FAIR chemistry data because they are:

- Non-proprietary and freely available
- Unambiguous for a given structure (unlike names, which vary by convention and language)
- Machine-readable and searchable
- Generated automatically by most modern chemistry software

> IUPAC InChI resources: [iupac.org/who-we-are/divisions/division-details/inchi/](https://www.iupac.org/who-we-are/divisions/division-details/inchi/)

### SMILES

**SMILES (Simplified Molecular Input Line Entry System)** is a line notation for chemical structures that is widely used and human-readable. It is less standardised than InChI -- multiple valid SMILES strings can represent the same molecule, unless canonical SMILES is used -- but it is well-supported in cheminformatics tools and databases. SMILES is a practical choice for encoding structures in data files and ELN records.

The SMILES for aspirin is:

```
CC(=O)Oc1ccccc1C(=O)O
```

### CAS Registry Numbers

CAS numbers are a familiar and widely used identifier system. However, they are proprietary, maintained by the American Chemical Society's Chemical Abstracts Service, and not freely assignable. For FAIR data, relying on CAS numbers as the sole identifier is problematic: they cannot be generated programmatically from a structure, and access to the CAS database requires a subscription.

:::::::::::::::::::::::::::::::::::::::::  callout

## Getting Identifiers in Practice

Most structure drawing tools (ChemDraw, Marvin, Ketcher) can generate InChI and SMILES automatically from a drawn structure. Many ELNs do this as well. The NIST Chemistry WebBook and PubChem both provide InChI and InChIKey for known compounds and are freely accessible.

For a quick lookup or conversion, the [NCI/CADD Chemical Identifier Resolver](https://cactus.nci.nih.gov/chemical/structure) can convert between names, SMILES, InChI, and structures directly in the browser.

::::::::::::::::::::::::::::::::::::::::::::::::::

## Metadata for Analytical Techniques

For each common technique, there is a set of metadata that should be recorded alongside the raw data. The table below summarises the essential items. "Essential" means that without this information, the data cannot be reliably interpreted or reproduced.

| Technique | Essential metadata |
|-----------|--------------------|
| **NMR** | Nucleus (¹H, ¹³C, etc.), field strength (MHz), solvent (including deuterated form), temperature, pulse sequence, number of scans, reference standard (TMS, DSS, etc.), concentration (where relevant), instrument model and manufacturer |
| **IR** | Mode (ATR or transmission), resolution (cm⁻¹), scan range, number of scans, sample preparation (neat, KBr disc, solution, specify solvent), instrument model |
| **Mass spectrometry** | Ionisation method (ESI, APCI, EI, etc.), mass range, resolution (nominal or high), instrument model, calibration standard, sample preparation |
| **XRD (powder)** | Radiation source (Cu Kα, Mo Kα, etc.), wavelength, temperature, scan range and step size, sample preparation |
| **XRD (single crystal)** | Radiation source, temperature, crystal dimensions, space group determination software, refinement software and R-factors |
| **UV-Vis** | Solvent, path length, concentration, scan range, instrument model |

These lists are not exhaustive, and community standards for some techniques are more mature than others. The key question to ask for any measurement is: **if someone tried to reproduce this experiment using only what I have recorded, what would they need to know that I have not written down?**

:::::::::::::::::::::::::::::::::::::::  challenge

## Check Your Understanding: What Is Missing?

A research group has run a high-throughput screen of imine condensation reactions to discover new porous organic cages, testing combinations of amine and aldehyde precursors using an automated liquid-handling platform. They recorded their results in the following CSV table (showing four rows from a much larger dataset):

```
reaction_id, amine, aldehyde, amine_aldehyde_ratio, solvent, result, mass_spectrum_file
1, compound_A, compound_X, 2:3, DMSO, cage, raw_data/mass_spec/rxn_001_ms.mzML
2, compound_A, compound_Y, 2:3, DMSO, no cage, raw_data/mass_spec/rxn_002_ms.mzML
3, compound_B, compound_X, 2:3, DMSO, cage, raw_data/mass_spec/rxn_003_ms.mzML
4, compound_B, compound_Y, 2:3, DMSO, unclear, raw_data/mass_spec/rxn_004_ms.mzML
```

Discuss with a neighbour:

1. What does this table record well?
2. What information is still missing that would be needed to reproduce any of these reactions, or to fully interpret the results?
3. If this screen involved 300 reactions run over several weeks by two different researchers, what additional metadata would you want to capture?

:::::::::::::::  solution

## Discussion

**What is recorded well:**

- The stoichiometric ratio and solvent are present: two of the most important experimental variables.
- Each reaction links directly to its raw mass spectrum file. Including file paths in a summary CSV is excellent practice: it creates a machine-readable map between the summary data and the underlying evidence. This works well as long as the CSV is distributed alongside the raw files (e.g. in a zipped archive) and a README or data dictionary explains the directory structure and file format.

**What is still missing:**

- **Compound identifiers:** "compound_A" is meaningless without a SMILES string or InChIKey. Anyone wanting to re-run reaction 1, search a database, or cross-reference with other work has nothing to go on. Each precursor should map to a proper chemical identifier, either as additional columns or in an accompanying lookup table.
- **Concentration and volume:** What was the total reagent concentration? What scale was each reaction run at?
- **Temperature and reaction time:** Were all reactions run under the same conditions? If so, that belongs in the README; if not, it belongs in the table.
- **What "cage" means analytically:** The file link helps, but the table still carries a categorical label with no record of what m/z values were observed, what charge states, or what confidence threshold was used. Row 4's "unclear" is especially hard to interpret without this.
- **Operator and date:** For a multi-week, multi-researcher screen, knowing who ran which reactions and when is important for identifying batch effects or instrument drift. A `date` and `operator` column costs nothing and can save significant time later.

The key insight from HTE data is that because the same type of experiment is repeated many times, getting the metadata schema right once and applying it consistently pays off enormously: the whole dataset becomes machine-readable and analysable as a unit, rather than a collection of entries that have to be interpreted case by case.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## The IUPAC FAIRSpec Standard

IUPAC has developed the **FAIRSpec** specification, a formal standard for FAIR management of spectroscopic data in chemistry. It defines a consistent set of metadata elements for spectroscopic datasets, covering both general experimental context (compound identity, sample preparation, laboratory) and technique-specific elements (for NMR, IR, MS, and others).

FAIRSpec is not yet a universal requirement, but it represents the direction the community is moving in. ELNs and repositories that adopt FAIRSpec will be able to exchange and interpret spectroscopic metadata automatically, without manual mapping or translation.

> "IUPAC specification for the FAIR management of spectroscopic data in chemistry." *Pure and Applied Chemistry* (2022).
> [doi:10.1515/pac-2021-2009](https://www.degruyterbrill.com/document/doi/10.1515/pac-2021-2009/html)

## Standard File Formats

Just as important as the metadata *content* is the format in which data and metadata are stored. Proprietary formats -- Bruker `.fid`, Agilent `.d` directories, Thermo `.raw` -- are not necessarily readable by other software and may become inaccessible as instrument software versions change. Open formats allow any tool to read the data without a proprietary licence.

For tabulated data like reaction yields, calibration curves, summary statistics, computed energies etc., **CSV (comma-separated values)** is perfectly adequate and  preferred over XLSX. CSV is plain text, readable by any software without a licence, and will not become inaccessible as spreadsheet software versions change. Reserve proprietary spreadsheet formats for cases where formatting, formulas, or macros are genuinely necessary, and always export a CSV alongside them for deposition.

For instrument and technique-specific data, some open formats are:

- **JCAMP-DX:** the standard for spectroscopic data (NMR, IR, MS, UV-Vis, Raman). A plain-text format that embeds metadata in a structured header alongside the data. Most instrument software can export to JCAMP-DX.
- **CIF (Crystallographic Information File):** the standard for crystal structure data, required by the Cambridge Structural Database and most crystallography journals.
- **mzML:** the standard open format for mass spectrometry data.
- **nmrML:** an emerging open format for NMR data with richer metadata support than JCAMP-DX.
- **CML (Chemical Markup Language):** an XML-based format for general chemical information, including structures, spectra, and reactions.

The practical workflow for most chemists is to keep vendor files as the primary archival format for raw data (they preserve everything) and export to open formats for deposition and sharing. Many repositories now accept vendor formats but recommend or require an open-format companion file.

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge 8: Identifiers in Practice

Using the [NCI/CADD Chemical Identifier Resolver](https://cactus.nci.nih.gov/chemical/structure) (accessible at `https://cactus.nci.nih.gov/chemical/structure`):

1. Type `aspirin` into the resolver and retrieve the InChI, InChIKey, and SMILES for aspirin.
2. Now enter the SMILES `CC(=O)OC1=CC=CC=C1C(=O)O` -- does it resolve to the same compound?
3. Copy the InChIKey (`BSYNRYMUTXBXSQ-UHFFFAOYSA-N`) and paste it into a Google search. What databases return results?

Discuss with a neighbour:

- What does this tell you about the value of InChIKey as an identifier?
- Why would a researcher include the InChIKey in a data record rather than just the compound name?

:::::::::::::::  solution

## Discussion

**Steps 1 and 2** should both resolve to aspirin (acetylsalicylic acid), confirming that InChI and SMILES are structure-based rather than name-based identifiers. The same compound has one InChI regardless of what it is called in different languages, traditions, or databases.

**Step 3** should return results from PubChem, ChemSpider, Wikidata, and potentially commercial databases -- all linking directly to aspirin without any ambiguity. This is the power of a structure-based identifier: it connects data across databases automatically.

**Why InChIKey rather than a name?** "Aspirin" is unambiguous in English but the compound is known as "Aspirin" (Germany), "Acidum acetylsalicylicum" (pharmacopoeias), "acetylsalicylic acid" (systematic), and "AAS" (abbreviation). All of these map to the same InChIKey. In a data record or database, the InChIKey provides an unambiguous, cross-searchable identifier that works regardless of naming convention -- and can be auto-generated from any structure drawing tool.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  keypoints

- Metadata transforms raw data files into interpretable, reusable scientific records -- it is the practical foundation of FAIR data in chemistry.
- Use InChI or InChIKey as the primary identifier for compounds in data records; SMILES is also widely supported. Avoid relying on CAS numbers alone.
- Record technique-specific metadata systematically: field strength and solvent for NMR, ionisation method for MS, radiation source for XRD.
- Export data to open formats (JCAMP-DX, CIF, mzML) for deposition and sharing alongside proprietary raw files.
- The IUPAC FAIRSpec standard defines a community-agreed metadata schema for spectroscopic data in chemistry.

::::::::::::::::::::::::::::::::::::::::::::::::::
