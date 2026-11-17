---
title: "Electronic Lab Notebooks for Chemists"
teaching: 12
exercises: 3
---

::::::::::::::::::::::::::::::::::::::: objectives

- Explain the advantages of electronic lab notebooks over paper for research data management
- Identify features that are important when choosing an ELN for chemistry
- Evaluate practical considerations before adopting an ELN

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What does an electronic lab notebook do that a paper one cannot?
- What should I look for in an ELN for chemistry research?
- How do I choose between the options available?

::::::::::::::::::::::::::::::::::::::::::::::::::

## The Case for Going Electronic

The paper lab notebook has served chemistry well for centuries, but paper notebooks have serious limitations from an RDM perspective:

- **Not searchable.** Finding a specific experiment from two years ago requires physically flipping through notebooks, if they have not been mislaid, damaged, or left with a former group member.
- **Not backed up.** A notebook left on a lab bench can be lost to fire, flood, or theft. There is no offsite copy.
- **Not easily shared.** Collaboration across sites means scanning pages or physically posting notebooks, with no version control and no way to link entries to associated data files.
- **Not timestamped in any verifiable way.** While a handwritten date can establish priority in principle, it provides no cryptographic proof in the way that an ELN with automatic timestamping can.
- **Hard to link to data.** A notebook entry describing a reaction does not connect directly to the NMR FID or mass spectrum acquired the following day.

Electronic lab notebooks address all of these, and they increasingly integrate with the data repositories and metadata standards that make chemistry data FAIR.

:::::::::::::::::::::::::::::::::::::::::  callout

## Paper and Electronic Can Coexist

Moving to an ELN does not have to mean abandoning paper immediately. Many groups use ELNs for structured records (reaction schemes, experimental parameters, results) while keeping paper for quick sketches and planning. The key is that the primary scientific record -- the one linked to raw data and shared with the group -- is electronic.

::::::::::::::::::::::::::::::::::::::::::::::::::

## What a Good ELN Should Do

At a minimum, an ELN should:

- Allow structured recording of experiments with fields for conditions, observations, and results
- Provide automatic, tamper-evident timestamps
- Store records securely with backup
- Be searchable across all entries
- Allow files (spectra, images, data files) to be attached to experiments
- Support export of data in standard formats so you are not locked in

Chemistry-specific ELNs go further.

## Chemistry-Specific Features

General-purpose ELNs will handle structured notes and file attachments, but they are not chemistry-aware. For synthetic and analytical chemists in particular, several additional features matter:

**Chemical structure drawing.** The ability to draw and search structures directly in the ELN, using tools like Ketcher or ChemDraw integration, rather than attaching image files.

**Reaction scheme capture.** Recording a full synthetic step including reactants, reagents, solvents, conditions, stoichiometry and yield in a structured, machine-readable way rather than as free text.

**Stoichiometry and yield calculators.** Built-in tools that calculate equivalents, masses, and theoretical yields from entered molecular weights and quantities, reducing transcription errors.

**Analytical data integration.** Linking NMR, IR, and mass spectrometry data directly to the experiment that generated it, rather than keeping them in separate folders with no connection.

**Standard identifiers.** Auto-populating InChI and SMILES for compounds drawn in the notebook, making entries interoperable with external databases and repositories.

**Repository export.** Some ELNs can export directly to chemistry data repositories (most notably, Chemotion ELN exports directly to the Chemotion Repository), creating a seamless path from experiment to deposition.

## Some of the Main Options

The ELN landscape is large and changes quickly. New tools appear, and institutional licences change. This table reflects the situation at the time of writing; always check the current state before choosing.

| ELN | Chemistry features | Cost | Open source? | Notes |
|-----|-------------------|------|--------------|-------|
| **Chemotion ELN** | Excellent -- structure drawing, reaction schemes, analytical data integration | Free | Yes | Built specifically for chemistry; direct export to Chemotion repository |
| **eLabFTW** | Basic (general-purpose) | Free | Yes | Flexible, self-hosted, widely used across disciplines |
| **RSpace** | Good via plugins | Free tier for academics | No | UK-based, good institutional support |
| **LabArchives** | Basic | Institutional licence | No | Common at UK and US universities |
| **Signals Notebook** (Revvity) | Excellent -- ChemDraw integration | Commercial | No | Enterprise-grade; may be available via institutional licence |

:::::::::::::::::::::::::::::::::::::::::  callout

## Check What Your Institution Already Has

Before evaluating any ELN independently, find out whether your university already has a site licence. Many UK universities have licences for LabArchives, RSpace, or similar tools that make them free at the point of use. Starting with what is already supported also means institutional IT can help with setup, backup, and migration.

::::::::::::::::::::::::::::::::::::::::::::::::::

## Before You Commit: Questions to Ask

Choosing an ELN is a long-term decision. Switching systems mid-project is disruptive and can result in data loss or fragmentation. Before committing to any tool, consider:

**Data portability.** Can you export all your records, including attached files and metadata, in a usable format? What happens to your data if the company folds, the institutional licence expires, or you move to a different institution? Proprietary formats with no export route create long-term risks.

**Institutional support.** Is the ELN supported by your institution's IT or research data team? Is there a community of users in your group or department who can help?

**Longevity.** Is the tool actively maintained? An ELN that is no longer developed is a liability: security vulnerabilities accumulate and eventually the product may be discontinued.

**Integration.** Does it connect with the instruments, repositories, and workflows you already use? An ELN that sits in isolation from everything else in your workflow adds friction rather than removing it.

**Cost over time.** Free-at-point-of-use tools can introduce costs later, either direct pricing changes or the cost of migration when the product changes strategy. Open-source tools with self-hosting options give more long-term control.

:::::::::::::::::::::::::::::::::::::::  challenge

## Check Your Understanding: ELN Exit Strategy

Your group has been using a commercial ELN for three years. The company announces that the product will be discontinued in 12 months. What would you need to check immediately, and what is the biggest risk?

:::::::::::::::  solution

## Discussion

The most urgent question is **data portability**: can you export all records, including attached files and metadata, in a format that another system can read? If the ELN stores data in a proprietary format with no export route, you have a data rescue problem on your hands.

Other questions to ask quickly: how complete is the export (does it include attachments, timestamps, and audit trails)? Is there institutional IT support for migration? Do you have any records backed up outside the ELN, for example in a data repository?

This is not a hypothetical scenario. It has happened to research groups, and the cost of migration rises sharply the longer you wait. This is why data portability should be assessed *before* committing to a tool, not after receiving bad news.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

For most chemistry groups in UK academia at the time of writing, **Chemotion ELN** (if your work involves synthesis or spectroscopy) or **eLabFTW** (if you need a flexible general solution) are strong starting points. Both are free and open source, and neither locks your data into a proprietary format.

:::::::::::::::::::::::::::::::::::::::  keypoints

- Electronic lab notebooks improve searchability, backup, data linking, and collaboration compared to paper notebooks.
- For chemistry, look for ELNs with structure drawing, reaction scheme capture, stoichiometry tools, and analytical data integration.
- Data portability is critical -- ensure you can export all records in a usable format before committing.
- Check what your institution already provides before evaluating tools independently.
- Chemotion ELN and eLabFTW are widely used open-source options with good chemistry support.

::::::::::::::::::::::::::::::::::::::::::::::::::
