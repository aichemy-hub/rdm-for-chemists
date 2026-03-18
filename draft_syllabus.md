# Research Data Management for Chemists — Draft Syllabus

> **Format:** Carpentries-style workshop (episodes with objectives, challenges, key points)
> **Duration:** 2.5–3 hours total
> **Audience:** PhD students and postdocs working in chemistry (UK-based institutions)
> **Prerequisites:** None assumed — designed for a mixed audience with quick refreshers on basics
> **Delivery:** In person or online. All participants should have a laptop. No physical handouts — all challenge materials are provided via a shared data directory (`challenge-data/`) distributed ahead of the workshop.

---

## Learning Outcomes

By the end of the workshop, participants will be able to:

1. Make informed research data management decisions before, during, and at the end of a project
2. Understand the importance of managing research data well
3. Appreciate research data management challenges specific to chemistry and how they can be mitigated

---

## Workshop Structure Overview

| Part | Duration | Focus |
|------|----------|-------|
| **Part 1** | 60–75 min | Generic research data management principles |
| *Break* | 10–15 min | |
| **Part 2** | 75–90 min | Chemistry-specific data management |

---

## Shared Data Directory Structure

All challenge materials are provided in a shared directory with the following structure:

```
challenge-data/
├── 03_data-access-statements/
│   └── data_access_statements.md
├── 04_fair-self-assessment/
│   └── fair_checklist.md
├── 05_fix-this-folder/
│   └── messy-project/
│       ├── (badly named files, duplicates, no documentation)
│       └── ...
├── 06_sharing-licensing-repositories/
│   ├── 06a_licensing/
│   │   └── scenario.md
│   ├── 06b_data-access-statement/
│   │   └── scenario.md
│   └── 06c_repository-selection/
│       └── scenario.md
├── 07_reproducibility-detective/
│   └── fictional_methods_excerpt.md
├── 09_metadata/
│   ├── 09a_sample_nmr.jdx
│   └── 09b_inchi_smiles_exercise.md
├── 10_find-a-repository/
│   └── instructions.md
├── 11_multi-technique-dmp/
│   └── scenario.md
└── 13_post-workshop-action-plan/
    └── rdm_action_plan_template.md
```

---

# PART 1: Research Data Management Principles (60–75 min)

Part 1 follows the **research data lifecycle** — planning, collecting, storing, and sharing — so that participants see how RDM applies at every stage of a project.

---

## Episode 1: Why Does Research Data Management Matter? (15 min)

**Teaching: 10 min | Exercises: 5 min**

### Objectives

- Define "research data" and "research data management"
- Explain why good data management matters for you, your group, and the wider community
- Recognise the consequences of poor data management

### Content Ideas

**What counts as research data?**
Not just spreadsheets — raw instrument output, code, lab notebooks, simulations, images, survey responses, samples, etc.

**The research data lifecycle.**
Introduce a lifecycle diagram (Plan → Collect → Process/Analyse → Store → Share/Preserve → Reuse). Emphasise that RDM applies at every stage, not just at publication.

**Horror stories — what happens when it goes wrong.**
Use 2–3 brief, vivid examples to motivate the rest of the workshop:

- *The unreadable tapes:* A major social science dataset stored on magnetic tapes became inaccessible when the hardware to read them was retired — years of expensive data collection lost.
- *The retraction cascade:* A 2024 Royal Society Open Science paper analysed article retractions caused by data management errors. Since 2000, data-related retractions have risen sharply, with the proportion exceeding 75% in 2023. Common causes: data coding errors, incorrect processing, and loss of documentation.
  - Reference: Williams et al. (2024) "Opening the black box of article retractions" — [Royal Society Open Science](https://royalsocietypublishing.org/doi/10.1098/rsos.240844)
- *The overwritten dataset:* A PhD student overwrites their only copy of raw mass spectrometry data with processed data, then discovers a processing error months later. No backup, no raw data, no recovery.

**The reproducibility crisis in science.**
A 2016 Nature survey found that over 70% of researchers had tried and failed to reproduce another scientist's experiments, and more than half couldn't reproduce their own. Chemists had the highest proportion of respondents who had been unable to reproduce someone else's experiment.

- Reference: Baker (2016) "1,500 scientists lift the lid on reproducibility" — [Nature](https://www.nature.com/articles/533452a)

### Challenge 1: Data Audit (5 min)

> **Directory:** `challenge-data/01_data-audit/`
>
> **Think-pair-share:** Take 2 minutes to list all the different types of data you produce or use in your research (raw files, processed data, notes, code, images, metadata, etc.). Share with your neighbour — did they mention any types you missed?

### Key Points

- Research data encompasses far more than final results
- Poor data management can lead to data loss, retractions, and wasted time and money
- The reproducibility crisis affects all of science, including chemistry

### Resources to Signpost

- [UK Data Service — Research Data Lifecycle](https://ukdataservice.ac.uk/learning-hub/research-data-management/)
- [University of Toronto — Data Loss Horror Stories](https://mdl.library.utoronto.ca/mdl-blog/data-loss-horror-stories)

---

## Episode 2: Planning Your Data — DMPs, Budgeting, and Funder Policies (20 min)

**Teaching: 15 min | Exercises: 5 min**

### Objectives

- Explain what a Data Management Plan (DMP) is and when to write one
- Identify what a DMP should cover
- Understand how to budget for data management activities
- Understand what major UK funders expect regarding research data
- Know about the EPSRC policy framework and its key principles

### Content Ideas

**What is a DMP?**
A living document that describes how you will handle data during and after a research project. It covers what data you'll collect, how you'll organise and store it, who will have access, and how it will be preserved and shared.

**When to write one.**
Ideally at the start of a project, even if your funder doesn't require it. The EPSRC notably does *not* require a DMP at application stage, but strongly recommends writing one — and you still need to budget for RDM and include a data access statement in publications.

**DMPonline.**
The Digital Curation Centre's free tool ([DMPonline](https://dmponline.dcc.ac.uk/)) provides funder-specific templates and guidance. Walk through a quick demo or screenshots of the interface.

**Budgeting for RDM.**
RDM is not free. Most funding bodies permit the inclusion of data management costs in grant applications, provided they are reasonable, proportionate, and incurred before the end of the project. Costs to consider include:

- **Data documentation and description:** Low or no additional cost if done during data creation, but significantly higher if retrospective
- **Data storage:** Your institution likely offers free storage within limits, but large-scale or specialised storage may incur costs
- **Transcription and anonymisation:** Costs vary — anonymising qualitative data can be particularly challenging and expensive
- **Staff time:** e.g. to prepare data for sharing/archival, data management personnel
- **Data preservation and sharing:** Most public repositories are free, but some charge fees
- **Software licences:** For specialist data management or analysis tools

Useful budgeting tools:

- [UK Data Service Costing Tool and Checklist](https://ukdataservice.ac.uk/learning-hub/research-data-management/plan-to-share/costing/)
- [OpenAIRE RDM Costing Tool](https://www.openaire.eu/)

Budget during the proposal stage — developing a DMP can help identify which activities are needed and estimate costs.

**EPSRC/UKRI policy framework — the key principles:**

1. EPSRC-funded research data is a public good and should be made openly available
2. Sufficient metadata should be recorded and made openly available to allow others to discover and reuse the data
3. Published results should always include information on how to access the supporting data
4. All publications must contain a **data access statement**
5. Data should be preserved for a minimum of **10 years** after its last use by the original researchers or a third party
6. Researchers must have a plan for data management and should consider costs in their grant applications

Note: EPSRC expects a DMP to be in place but does not require one at application stage (unlike BBSRC, CRUK, and NERC, which do). However, funding for RDM costs (staff time, storage, etc.) can be requested as part of the full economic cost.

Metadata must be made freely available on the internet within 12 months of data generation. This metadata must be sufficient to allow others to understand what data exists, why and how it was generated, and how to access it.

**Other major UK funders — key variations:**
While the general expectations are similar (plan, preserve, share), the detail varies:

- **BBSRC, NERC, MRC, ESRC:** All require a DMP at application. Preservation period: 10 years. All expect timely data sharing.
- **CRUK:** Requires a DMP. Policy covers all high-quality data regardless of publication status. Data retention: minimum 5 years (10 years recommended).
- **Wellcome Trust:** Requires a DMP for grants over £100k. Expects data to be shared as widely and rapidly as possible.
- **Horizon Europe:** Requires a DMP (using the template provided). Open access to data is the default under the "as open as possible, as closed as necessary" principle.
- **BHF:** Currently has no formal data management policy (but supports the principle of open access to data).

The key message: **always check your specific funder's requirements**, as they differ in detail. [DMPonline](https://dmponline.dcc.ac.uk/) provides funder-specific templates that help you meet the right requirements.

**UKRI policy evolution.**
UKRI is currently developing a new integrated research data policy (expected to be published in early 2026 and implemented later in 2026). This will replace individual council-level policies.

- Reference: [UKRI — Developing UKRI's research data policy](https://engagementhub.ukri.org/ukri-openresearch/developing-ukris-research-data-policy/)

### Challenge 2: DMP Speed Round (5 min)

> **Directory:** `challenge-data/02_dmp-speed-round/`
>
> **Group exercise:** You've just been awarded a 3-year EPSRC grant to study novel catalytic materials. In groups of 3–4, spend 5 minutes brainstorming: What data will you generate? Where will you store it? How will you share it? What might it cost? Report back one surprising thing your group identified.

### Key Points

- A DMP is a living document, not a box-ticking exercise
- Plan your data management (and budget for it) from the start
- DMPonline provides free templates aligned to UK funder requirements
- Know your funder's data policy — ignorance is not an excuse
- EPSRC requires open data, data access statements, and 10-year preservation
- Policies are evolving; keep up to date

### Resources to Signpost

- [DMPonline](https://dmponline.dcc.ac.uk/)
- [DCC — Guidance and Example DMPs](https://www.dcc.ac.uk/resources/data-management-plans/guidance-examples)
- [NFDI4Chem — Data Management Plans for Chemistry](https://knowledgebase.nfdi4chem.de/knowledge_base/docs/dmp/)
- [UKRI/EPSRC Policy Framework on Research Data](https://www.ukri.org/who-we-are/epsrc/our-policies-and-standards/policy-framework-on-research-data/)
- [UKRI/EPSRC Policy Principles](https://www.ukri.org/who-we-are/epsrc/our-policies-and-standards/policy-framework-on-research-data/principles/)

---

## Episode 3: FAIR Data Principles (15 min)

**Teaching: 10 min | Exercises: 5 min**

### Objectives

- Explain the four FAIR principles (Findable, Accessible, Interoperable, Reusable)
- Assess how FAIR your own data is
- Understand that FAIR does not necessarily mean "open"

### Content Ideas

**The FAIR principles in plain language:**

- **Findable:** Data has a persistent identifier (e.g. a DOI), is described with rich metadata, and is registered in a searchable resource.
- **Accessible:** Data can be retrieved via a standard protocol (even if authentication is needed). Metadata remains accessible even if data is no longer available.
- **Interoperable:** Data uses formal, shared vocabularies and standards. It can be combined with other data and work with tools and workflows.
- **Reusable:** Data has a clear licence, detailed provenance, and meets community standards.

**FAIR ≠ Open.**
Data can be FAIR but not open (e.g. behind a login for ethical reasons). The metadata should always be open, even if the data isn't.

**Why FAIR matters for chemistry.**
Chemistry produces diverse data types (spectra, structures, reaction conditions, computed properties) in many different formats. Without FAIR practices, data becomes siloed and unreusable.

### Challenge 3: Spot the Data Access Statement (5 min)

> **Directory:** `challenge-data/03_data-access-statements/`
>
> **Exercise:** Open `data_access_statements.md`. It contains three fictional data access statements from chemistry papers. For each one, discuss with your neighbour:
>
> 1. Does it meet the EPSRC/UKRI requirements?
> 2. Could you actually find and access the data based on this statement?
> 3. How would you improve it?
>
> **Example fictional statements to include in the file:**
>
> *Statement A:* "Data is available from the authors upon reasonable request."
>
> *Statement B:* "The raw NMR, IR, and mass spectrometry data supporting this study are deposited in the Chemotion Repository at <https://doi.org/10.14272/xxxxx> under a CC-BY 4.0 licence. Computational input/output files are available on Zenodo at <https://doi.org/10.5281/zenodo.xxxxx>."
>
> *Statement C:* "All data are included in the supplementary information."

### Key Points

- FAIR is a set of guiding principles, not a standard or a specification
- FAIR and open are related but different concepts
- Making data FAIR requires effort throughout the research lifecycle, not just at publication
- All UKRI-funded publications must include a data access statement — even if there is no data

### Resources to Signpost

- [GO FAIR — FAIR Principles](https://www.go-fair.org/fair-principles/)
- [ARDC — FAIR Data Self-Assessment Tool](https://ardc.edu.au/resource/fair-data-self-assessment-tool/)

---

## Episode 4: Data Storage, Security, and Organisation (15 min)

**Teaching: 10 min | Exercises: 5 min**

### Objectives

- Apply good practices for file naming and folder organisation
- Understand the 3-2-1 backup rule
- Distinguish between active storage and long-term preservation

### Content Ideas

**File naming conventions.**
Consistent, descriptive names with dates (ISO 8601: YYYY-MM-DD), version numbers, and meaningful abbreviations. Avoid spaces and special characters.

Example:

```
BAD:  final_data_v3_FINAL_really final (2).xlsx
GOOD: 2025-03-15_catalyst-screening_NMR_Cu-series_v02.xlsx
```

**Folder structures.**
Show a good example folder structure for a chemistry project:

```
project-name/
├── 01_raw-data/
│   ├── NMR/
│   ├── IR/
│   └── mass-spec/
├── 02_processed-data/
├── 03_analysis/
├── 04_manuscripts/
├── 05_documentation/
│   ├── README.md
│   └── data-dictionary.csv
└── 06_outputs/
```

**The 3-2-1 backup rule.**
3 copies, on 2 different media types, with 1 offsite. Discuss institutional provision (e.g. university-managed storage, OneDrive/SharePoint) vs. personal solutions. Emphasise that USB drives and laptop hard drives are not a backup strategy.

**Portable storage devices — a cautionary note.**
Many researchers keep copies on personal laptops, external hard drives, and USB sticks. These can be useful for transporting or backing up data but should never be relied upon as a primary storage method: data on USBs can easily become corrupted, personal devices can be lost or stolen, and portable devices break with use. Use them as a secondary option alongside institutional storage.

**Institutional storage.**
Most UK universities provide managed research data storage (often with a free allocation per project). Encourage participants to find out what their institution offers — it is usually more reliable, backed up, and compliant with funder requirements than personal solutions.

**Version control.**
Briefly mention that version control (e.g. Git) is an option for code and text files — don't go deep, but signpost it for interested participants.

**Security considerations.**
Sensitive data (e.g. proprietary compounds, data under NDA) needs access controls. Encryption for data in transit and at rest. Know your institution's policies. Commercial cloud storage (Google Drive, Dropbox, etc.) may not be appropriate for sensitive or confidential data — check your institutional policy.

### Challenge 4: How FAIR Is Your Data? (5 min)

> **Directory:** `challenge-data/04_fair-self-assessment/`
>
> **Exercise:** Open `fair_checklist.md`. Using this simplified FAIR self-assessment checklist, rate a recent dataset you've produced against each of the four principles. Score each F, A, I, R out of 5. Discuss with your neighbour — where are your weaknesses?
>
> **Checklist contents:**
>
> | Principle | Question | Score (1–5) |
> |-----------|----------|-------------|
> | **F** | Does your data have a persistent identifier (DOI)? | |
> | **F** | Is it described with rich metadata? | |
> | **A** | Can someone find and download it using a standard method? | |
> | **I** | Is it in a standard, non-proprietary format? | |
> | **I** | Does it use standard vocabularies/identifiers? | |
> | **R** | Does it have a clear licence? | |
> | **R** | Is its provenance documented? | |

### Key Points

- Good organisation and naming save enormous time in the long run
- Follow the 3-2-1 backup rule — your laptop is not a backup
- Use your institution's managed storage where possible

### Resources to Signpost

- [UK Data Service — Format Your Data](https://ukdataservice.ac.uk/learning-hub/research-data-management/format-your-data/)

---

## Episode 5: Sharing, Preserving, and Licensing Your Data (15 min)

**Teaching: 10 min | Exercises: 5 min**

### Objectives

- Explain why and how to share research data
- Choose an appropriate data repository
- Select an appropriate licence for your data
- Understand what a DOI is and why it matters

### Content Ideas

**Why share data?**
Funder requirements, journal policies, reproducibility, citation credit, community benefit, and efficiency (others don't have to repeat your experiments).

**The spectrum of data sharing.**
Data sharing is not all-or-nothing. There are several approaches, roughly ordered from most to least desirable:

1. **Deposit in a data repository** (best practice) — makes data discoverable, citable (via DOI), and preserved long-term
2. **Informal/collaborative sharing** — within a research group or with collaborators, using shared storage with access controls and clear agreements
3. **Controlled/restricted access** — some repositories (e.g. UK Data Service) provide tiered access for sensitive data, where users must register or sign a data-sharing agreement
4. **Supplementary information** — some journals host small datasets alongside the paper, but this is not recommended: discoverability is limited, no DOI, no long-term preservation guarantee
5. **"Available on request"** — should be a last resort. Evidence shows that requests often go unanswered, contact details go stale, and data may no longer be available

**Choosing a repository.**
Hierarchy of preference:

1. **Domain-specific repository** (best for discoverability and community standards)
2. **Institutional repository** (often required by your university — most UK universities have one)
3. **General-purpose repository** (e.g. Zenodo, Figshare) — always available as a fallback

Key repositories to highlight:

- [Zenodo](https://zenodo.org/) — general purpose, free, CERN-hosted, DOI minting
- [Figshare](https://figshare.com/) — general purpose, good visualisation
- Institutional repositories — varies by university
- Chemistry-specific repositories — covered in detail in Part 2

**Digital Object Identifiers (DOIs).**
A DOI is a persistent identifier for your dataset. It makes data citable, discoverable, and linkable. Most repositories mint DOIs automatically.

**Licensing your data.**
Without a licence, others legally cannot reuse your data. Common options:

- **CC0** (public domain dedication) — maximum reuse, recommended for data
- **CC-BY** — requires attribution
- **CC-BY-SA** — attribution + share-alike
- **CC-BY-NC** — restricts commercial use (may limit reuse)

General advice: use the most permissive licence your situation allows. CC0 or CC-BY are the most common for research data.

**Data Access Statements.**
All articles published by UKRI-funded researchers must include a Data Access Statement, even where there are no data associated with the article. A good data access statement should include: how the data can be accessed (with a DOI or persistent link), the terms under which data can be used, and an explanation if data cannot be shared. This is a simple but commonly overlooked requirement.

**Data preservation.**
EPSRC requires 10 years minimum. Consider format obsolescence — prefer open, non-proprietary formats (e.g. CSV over .xlsx, JCAMP-DX over vendor-specific spectral formats). Include documentation (README files, data dictionaries) so that future users can understand the data.

### Challenge 5: Fix This Folder (5 min)

> **Directory:** `challenge-data/05_fix-this-folder/messy-project/`
>
> **Hands-on exercise:** Open the `messy-project/` folder on your laptop. It contains a set of badly named files, duplicates, and no documentation from a fictional chemistry project. In pairs, reorganise the files into a sensible structure and rename them following the conventions discussed. You can create new folders, rename files, and add a README. We'll compare solutions afterwards.
>
> **Example contents of the messy folder:**
>
> ```
> messy-project/
> ├── data final.xlsx
> ├── data final v2.xlsx
> ├── data final v2 CORRECTED.xlsx
> ├── nmr tuesday.zip
> ├── NMR_compound1.zip
> ├── compound1_IR
> ├── mass spec results.csv
> ├── mass spec results (1).csv
> ├── notes.txt
> ├── analysis_old.py
> ├── analysis.py
> └── image001.png
> ```

### Key Points

- Share your data — it's increasingly required and benefits everyone
- Choose domain-specific repositories where possible
- Always apply a licence — no licence = no reuse
- A DOI makes your data citable — include it in your publications

### Resources to Signpost

- [re3data.org](https://www.re3data.org/) — Registry of Research Data Repositories
- [Creative Commons — Choose a Licence](https://creativecommons.org/choose/)
- [Zenodo](https://zenodo.org/)
- [DataCite](https://datacite.org/)

---

## Part 1 Wrap-Up and Challenge 6: Sharing, Licensing, and Repositories (15 min)

**Teaching: 0 min | Exercises: 15 min**

This is a capstone exercise for Part 1 that ties together sharing, licensing, and repository selection. All groups work through all three sub-challenges sequentially.

### Challenge 6a: Choosing a Licence (5 min)

> **Directory:** `challenge-data/06_sharing-licensing-repositories/06a_licensing/`
>
> **Exercise:** Open `scenario.md`. A research group has produced a dataset of UV-Vis absorption spectra for 30 novel organic dye molecules, along with the Python scripts used for fitting and analysis. They want to share both the data and the code, but their industrial collaborator has asked that commercial use be restricted for 12 months.
>
> In pairs, discuss:
>
> 1. Which Creative Commons licence would you recommend for the spectral data?
> 2. Would you use the same licence for the Python scripts, or a different one (e.g. MIT, GPL)? Why?
> 3. How would you handle the 12-month commercial restriction — can you do this with a CC licence?

### Challenge 6b: Writing a Data Access Statement (5 min)

> **Directory:** `challenge-data/06_sharing-licensing-repositories/06b_data-access-statement/`
>
> **Exercise:** Open `scenario.md`. You are about to submit a paper to an RSC journal. Your study involved:
>
> - ¹H and ¹³C NMR spectra for 15 compounds (deposited in the Chemotion Repository)
> - DFT calculations (input/output files on Zenodo)
> - A proprietary catalyst formulation that cannot be disclosed due to an NDA with an industrial partner
>
> Write a data access statement for this paper that meets UKRI requirements. Remember: you must address *all* data, including the data you cannot share.

### Challenge 6c: Choosing a Repository (5 min)

> **Directory:** `challenge-data/06_sharing-licensing-repositories/06c_repository-selection/`
>
> **Exercise:** Open `scenario.md`. You have four datasets to deposit. For each one, decide which repository you would use and explain why. Use [re3data.org](https://www.re3data.org/) to help you search.
>
> 1. 50 single-crystal X-ray structures of metal-organic frameworks
> 2. A collection of 200 IR and Raman spectra for polymer characterisation
> 3. Molecular dynamics simulation trajectories (50 GB) for a protein-ligand binding study
> 4. A set of kinetics measurements with the associated Python analysis scripts

---

# PART 2: Chemistry-Specific Data Management (75–90 min)

Part 2 applies the principles from Part 1 to the specific challenges, tools, and opportunities in chemistry research.

---

## Episode 6: The Reproducibility Crisis in Chemistry (15 min)

**Teaching: 10 min | Exercises: 5 min**

### Objectives

- Describe chemistry-specific challenges for reproducibility
- Identify common causes of irreproducible chemistry research
- Explain how good data management practices can help

### Content Ideas

**Chemistry and the replication crisis.**
A 2024 paper in Heliyon reviewed reproducibility specifically in chemistry research, identifying key factors:

- The "publish or perish" culture drives publication of non-reproducible outcomes
- Chemistry papers use more "hyping" language than any other discipline (2.54 hyping terms per 100 words on average)
- Insufficient methods reporting — details that seem minor (exact concentrations, humidity, trace impurities) can be critical
- In supramolecular chemistry, factors like pathway complexity, trace water in organic solvents, or small impurities in building blocks create pitfalls that are often underreported

Reference: "Reproducibility in chemistry research" (2024) — [Heliyon / PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC11305220/)

**Bayer and Amgen studies.**
Bayer HealthCare found only 7% of 67 target validation projects were fully reproducible; in-house and published data agreed in only 20–25% of cases. Amgen found 89% of oncology results couldn't be replicated. While these are pharma/bio examples, they highlight the stakes for chemistry-adjacent work.

**What does good look like?**
Proposals from the community include: mandatory "Failure Analysis" sections in supplementary information, independent replication by external labs, and publishing negative results alongside positive findings.

**The connection to RDM.**
Many reproducibility failures stem from poor data management — incomplete methods, missing metadata, lost raw data, ambiguous processing steps. Good RDM is a direct countermeasure.

### Challenge 7: Reproducibility Detective (5 min)

> **Directory:** `challenge-data/07_reproducibility-detective/`
>
> **Exercise:** Open `fictional_methods_excerpt.md`. It contains an excerpt from a fictional chemistry paper's methods section that is deliberately missing key details. In pairs, identify what information is missing that would prevent you from reproducing the experiment. What metadata should have been recorded?
>
> **Fictional excerpt:**
> *"The catalyst was prepared according to our previously reported method and was used without further purification. NMR spectra were recorded on a standard spectrometer. The reaction was carried out at elevated temperature under inert atmosphere in dry solvent. Yields were determined by standard analytical methods."*
>
> Groups identify missing details: catalyst batch/purity, spectrometer model and frequency, exact temperature, which inert gas, which solvent and how it was dried, concentrations, what analytical methods for yield determination, etc.

### Key Points

- Chemistry is fundamentally a reproducible science, but poor reporting and data management undermine this
- Recording and sharing detailed metadata is essential for reproducibility
- Good RDM practices directly address the root causes of the replication crisis

### Resources to Signpost

- [C&EN — Solving the reproducibility crisis](https://cen.acs.org/research-integrity/reproducibility/Reactions-Solving-reproducibility-crisis-science/103/i8)
- [Heliyon — Reproducibility in chemistry research](https://pmc.ncbi.nlm.nih.gov/articles/PMC11305220/)

---

## Episode 7: Electronic Lab Notebooks for Chemists (12 min)

**Teaching: 12 min | Exercises: 0 min**

### Objectives

- Explain the advantages of electronic lab notebooks (ELNs) over paper notebooks
- Identify key features to look for when choosing an ELN for chemistry

### Content Ideas

**Why move from paper to electronic?**
Searchability, automatic timestamping, backup, data linking, collaboration, integration with instruments, and increasingly a funder/publisher expectation. Paper notebooks degrade, are hard to search, and can't be easily shared or backed up.

**Chemistry-specific ELN features to look for:**

- Chemical structure drawing and searching
- Reaction scheme capture
- Stoichiometry calculators
- Integration with analytical instruments (NMR, MS, etc.)
- Export to repositories (e.g. direct export to Chemotion repository)
- Support for standard chemical identifiers (InChI, SMILES)

**Key ELN options for chemistry researchers:**

| ELN | Chemistry features | Cost | Open source? | Notes |
|-----|-------------------|------|--------------|-------|
| **Chemotion ELN** | Excellent — structure drawing, reaction schemes, analytical data | Free | Yes | Built for chemistry; integrates with Chemotion repository |
| **RSpace** | Good via plugins | Free tier for academics | No | UK-based, good institutional support |
| **eLabFTW** | Basic (general-purpose) | Free | Yes | Flexible, self-hosted, widely used in academia |
| **LabArchives** | Basic | Institutional licence | No | Common at UK/US universities |
| **Signals Notebook** (Revvity) | Excellent — ChemDraw integration | Expensive | No | Enterprise-grade; may be available via institutional licence |
| **Benchling** | Good for bio/chem | Free for academics | No | Popular but data lock-in concerns |

**Practical considerations:**

- Does your institution already have a licence? Check first.
- What happens to your data when you leave? Can you export it?
- Is the ELN actively maintained and supported?
- Can you connect it to your instruments and repositories?

### Key Points

- ELNs improve searchability, backup, and sharing of lab records
- Choose an ELN with chemistry-specific features if your work requires them
- Consider data portability — can you export your data if you switch?
- Check what your institution already provides

### Resources to Signpost

- [Chemotion ELN](https://chemotion.net/)
- [eLabFTW](https://www.elabftw.net/)
- [RSpace](https://www.researchspace.com/)
- [Harvard ELN Comparison Matrix](https://datamanagement.hms.harvard.edu/)

---

## Episode 8: Metadata and Chemical Data Standards (20 min)

**Teaching: 12 min | Exercises: 8 min**

### Objectives

- Explain why metadata is essential for chemistry data
- Use standard chemical identifiers (InChI, SMILES, CAS)
- Understand community metadata standards for common analytical techniques

### Content Ideas

**What is metadata and why does it matter?**
Metadata is "data about data." Without metadata, a spectrum is just a line on a graph — with metadata, it becomes a findable, interpretable, reusable scientific record. Metadata turns files into FAIR data.

**Standard chemical identifiers:**

- **InChI** (International Chemical Identifier): Machine-readable, non-proprietary, maintained by IUPAC. Encodes structure in a standard text string. The key to interoperability.
- **InChIKey**: A fixed-length hash of the InChI — ideal for web searches and database lookups.
- **SMILES**: Widely used line notation. Human-readable. Multiple valid SMILES for one molecule (unless canonical).
- **CAS Registry Numbers**: Widely recognised but proprietary — not ideal for FAIR data.

Reference: IUPAC InChI resources — [IUPAC Digital Standards](https://iupac.org/what-we-do/digital-standards/)

**Metadata for common analytical techniques.**
For each technique, discuss what minimum metadata should be recorded:

| Technique | Essential metadata |
|-----------|--------------------|
| **NMR** | Nucleus, frequency, solvent, temperature, pulse sequence, reference standard, concentration, instrument model |
| **IR** | Mode (ATR/transmission), resolution, range, sample preparation, instrument model |
| **Mass Spec** | Ionisation method, mass range, resolution, instrument model, calibration standard |
| **XRD** | Radiation source, wavelength, temperature, scan range/step size |
| **UV-Vis** | Solvent, path length, concentration, scan range, instrument model |

**IUPAC FAIRSpec.**
IUPAC has developed the FAIRSpec standard — a specification for FAIR management of spectroscopic data in chemistry. It defines metadata elements for general experimental data and technique-specific elements (e.g. for NMR).

Reference: "IUPAC specification for the FAIR management of spectroscopic data" — [De Gruyter](https://www.degruyterbrill.com/document/doi/10.1515/pac-2021-2009/html)

**Standard file formats.**
Prefer open, standard formats where possible:

- **JCAMP-DX**: Standard for spectroscopic data (NMR, IR, MS, UV-Vis)
- **CIF**: Crystallographic Information File (for crystal structures)
- **CML**: Chemical Markup Language
- Vendor formats (e.g. Bruker, Agilent) are acceptable for raw data but should be accompanied by open-format exports

### Challenge 9a: Metadata Bingo (3 min)

> **Directory:** `challenge-data/09_metadata/`
>
> **Exercise:** Open `09a_sample_nmr.jdx` — this is a sample NMR dataset in JCAMP-DX format. Open it in a text editor. Using the metadata table above, identify which metadata items are present in the file header and which are missing. How FAIR is this dataset?

### Challenge 9b: InChI and SMILES (5 min)

> **Directory:** `challenge-data/09_metadata/`
>
> **Hands-on exercise:** Open `09b_inchi_smiles_exercise.md` for instructions. Using the [NCI/CADD Chemical Identifier Resolver](https://cactus.nci.nih.gov/chemical/structure):
>
> 1. Convert the name "aspirin" to an InChI and an InChIKey
> 2. Convert the SMILES `CC(=O)OC1=CC=CC=C1C(=O)O` to a structure — is it the same molecule?
> 3. Search for the InChIKey in Google — what do you find?

### Key Points

- Metadata transforms raw files into FAIR, reusable scientific records
- Use standard chemical identifiers (InChI preferred) for interoperability
- Record technique-specific metadata systematically — build it into your workflow
- Open file formats (JCAMP-DX, CIF) are preferable to proprietary ones

### Resources to Signpost

- [IUPAC — Digital Standards](https://iupac.org/what-we-do/digital-standards/)
- [IUPAC FAIRSpec](https://www.degruyterbrill.com/document/doi/10.1515/pac-2021-2009/html)
- [IUPAC FAIR Chemistry Cookbook](https://iupac.github.io/WFChemCookbook/)
- [NFDI4Chem Knowledge Base](https://knowledgebase.nfdi4chem.de/)

---

## Episode 9: Chemistry Data Repositories and Databases (15 min)

**Teaching: 10 min | Exercises: 5 min**

### Objectives

- Identify domain-specific repositories for chemistry data
- Understand when to use a specialist repository vs. a general one
- Find and evaluate a chemistry repository

### Content Ideas

**Why use a chemistry-specific repository?**
Domain-specific repositories enforce community standards, provide chemistry-aware search (by structure, reaction, etc.), and connect to established databases. They make data more FAIR than a general-purpose repository can.

**Key chemistry repositories and databases:**

| Repository / Database | What it holds | Access | Notes |
|----------------------|---------------|--------|-------|
| [**Chemotion Repository**](https://www.chemotion-repository.net/) | Reaction data, analytical measurements (NMR, MS, IR, etc.) | Free, open | Domain-specific; linked to Chemotion ELN; DOI minting |
| [**Cambridge Structural Database (CSD)**](https://www.ccdc.cam.ac.uk/) | Small-molecule crystal structures | Free to search; academic licence for full access | 900,000+ curated entries; >50 years of data; mandatory deposition for many journals |
| [**NOMAD**](https://nomad-lab.eu/) | Computational materials science data | Free, open | For computational/simulation data; strong metadata standards |
| [**ioChem-BD**](https://www.iochem-bd.org/) | Computational chemistry data | Free, open | Input/output files from DFT, molecular dynamics, etc. |
| [**RADAR4Chem**](https://radar4chem.radar-service.eu/) | General chemistry research data | Free for German institutions; accessible to all | Part of NFDI4Chem infrastructure |
| [**Protein Data Bank (PDB)**](https://www.rcsb.org/) | Protein/macromolecular structures | Free, open | Essential for biochemistry / structural biology |
| [**Zenodo**](https://zenodo.org/) | Anything | Free, open | Good fallback for data types without a specialist repository |

**NFDI4Chem.**
Germany's national initiative for chemistry research data infrastructure. Even though it's German-led, many of its resources (Chemotion, knowledge base, standards) are freely available internationally and represent best practice.

Reference: [NFDI4Chem](https://nfdi4chem.de/)

**Royal Society of Chemistry data sharing policy.**
The RSC expects authors to make supporting data available, and provides guidance on recommended repositories.

Reference: [RSC — Data Sharing](https://www.rsc.org/publishing/publish-with-us/publish-a-journal-article/data-sharing)

### Challenge 10: Find and Evaluate a Repository (5 min)

> **Directory:** `challenge-data/10_find-a-repository/`
>
> **Hands-on exercise:** Open `instructions.md`. Go to [re3data.org](https://www.re3data.org/) and search for repositories relevant to chemistry. Find one repository that would be relevant to your own research area. Note down:
>
> 1. What is it called?
> 2. What data does it accept?
> 3. Does it mint DOIs?
> 4. Is it free to deposit?
> 5. What metadata standards does it use?
>
> Share your findings with your neighbour. Did you find the same repository?

### Key Points

- Use domain-specific repositories as your first choice — they enforce community standards and improve discoverability
- The CSD is mandatory for crystal structure data in most chemistry journals
- Zenodo is a good fallback for data types without a specialist repository
- Explore the NFDI4Chem Knowledge Base for current best practice

### Resources to Signpost

- [re3data.org — Registry of Research Data Repositories](https://www.re3data.org/)
- [NFDI4Chem — Choose a Repository](https://knowledgebase.nfdi4chem.de/knowledge_base/docs/choose_repository/)
- [FAIRsharing.org](https://fairsharing.org/)

---

## Episode 10: Managing Data from Common Chemistry Techniques (20 min)

**Teaching: 12 min | Exercises: 8 min**

### Objectives

- Apply good data management practices to NMR, IR, and mass spectrometry data
- Understand data management challenges at high-throughput and large-scale facilities
- Recognise when "big data" approaches are needed

### Content Ideas

**Scenario-based: a day in the lab.**
Walk through a realistic chemistry workflow — a researcher synthesises a compound, characterises it by NMR, IR, and mass spec, then analyses the data. At each stage, highlight the RDM decisions:

- **Sample preparation:** Record batch number, purity, preparation method. Link to ELN entry.
- **NMR acquisition:** Save raw FID and processed spectrum. Record all acquisition parameters. Use JCAMP-DX export alongside vendor format. Name files consistently.
- **IR measurement:** Record ATR vs. transmission, resolution, sample preparation. Export in open format.
- **Mass spectrometry:** Record ionisation method, calibration, mass range. Be aware of very large file sizes for high-resolution data.

**High-throughput facilities.**
Facilities like the [Rapid Online Analysis of Reactions (ROAR)](https://www.imperial.ac.uk/rapid-online-analysis-of-reactions/) at Imperial College generate data at scale — automated reactions with inline analytics producing thousands of data points per day.

Challenges:

- Volume: terabytes of data per experiment
- Automation: metadata must be captured automatically — manual recording is not feasible
- Standardisation: need consistent naming, formats, and metadata across all runs
- Data pipelines: often require automated processing workflows

**Large-scale facilities.**
Neutron and synchrotron sources (e.g. ISIS, Diamond Light Source) produce enormous datasets. These facilities often have their own data management infrastructure, but researchers need to plan for:

- Data transfer (how to get terabytes of data home)
- Data storage (institutional storage may not be sufficient)
- Metadata standards specific to the facility
- Data embargoes and access policies

**Signpost (don't teach in depth):** tools like Python/pandas, SQL databases, and workflow managers become necessary at this scale — but the principles of good RDM (metadata, naming, backup, documentation) are the same regardless of scale.

### Challenge 11: Data Management Plan for a Multi-Technique Study (8 min)

> **Directory:** `challenge-data/11_multi-technique-dmp/`
>
> **Group exercise:** Open `scenario.md`. Your group has been awarded funding for a project that involves:
>
> - Synthesising 50 new compounds
> - Characterising each by ¹H NMR, ¹³C NMR, IR, and high-resolution mass spectrometry
> - Running 10 of them through a high-throughput screening facility
> - Publishing results in an RSC journal
>
> In groups of 3–4, spend 8 minutes creating a mini data management plan:
>
> 1. What file naming convention will you use?
> 2. What metadata will you record for each technique?
> 3. Where will you store the raw data during the project?
> 4. Which repository will you deposit the data in at publication?
> 5. Estimate the total data volume.

### Key Points

- Apply the same RDM principles to every technique — but adapt the specifics
- High-throughput and large-scale facilities require automated metadata capture
- Plan for large data volumes and transfer from day one
- Open file formats and consistent naming conventions pay off at scale

### Resources to Signpost

- [ISIS Neutron and Muon Source — Data Policy](https://www.isis.stfc.ac.uk/)
- [Diamond Light Source — Data Management](https://www.diamond.ac.uk/)
- [Imperial ROAR Facility](https://www.imperial.ac.uk/rapid-online-analysis-of-reactions/)

---

## Episode 11: PSDI and the Chemistry Data Landscape (10 min)

**Teaching: 10 min | Exercises: 0 min**

### Objectives

- Describe what the Physical Sciences Data Infrastructure (PSDI) is and how it supports researchers
- Identify PSDI tools and resources relevant to your work
- Know where to go for further training and support

### Content Ideas

**What is PSDI?**
The Physical Sciences Data Infrastructure ([PSDI](https://www.psdi.ac.uk/)) is a UK initiative that supports researchers in chemistry and materials science by building on existing data systems. It aims to accelerate research by making data more accessible, interoperable, and reusable.

**Key PSDI resources:**

- **Data Conversion Service:** Tools to convert between chemistry file formats and assess conversion quality. Available as a web app, command-line tool, or Python library.
- **Data Revival:** An AI-powered service that transforms handwritten lab notes into machine-readable data — useful for digitising legacy data.
- **Resource Catalogue:** Curated access to high-quality data sources, both commercial and open.
- **Guidance and Training:** Materials for physical scientists on working with research data, including specific guidance on using PSDI tools.
- **CaMML School:** Chemistry and Materials Machine Learning training school for PhD students.

Reference: [PSDI Resources](https://resources.psdi.ac.uk/)

**PSDI in the wider landscape.**
PSDI works alongside other initiatives like NFDI4Chem (Germany), the broader NFDI, and IUPAC's digital standards work. The goal is a connected ecosystem where chemistry data flows between instruments, notebooks, repositories, and publications.

### Key Points

- PSDI provides practical tools and guidance for chemistry data management in the UK
- The Data Conversion Service and Data Revival tools solve real pain points
- The chemistry data landscape is becoming more connected — get involved

### Resources to Signpost

- [PSDI](https://www.psdi.ac.uk/)
- [PSDI Resources](https://resources.psdi.ac.uk/)
- [PSDI on GitHub](https://github.com/PSDI-UK)

---

## Workshop Close and Post-Workshop Exercise (5 min)

**Teaching: 5 min | Exercises: 0 min (exercise is post-workshop)**

### Content

**Quick recap.**
The research data lifecycle, mapped to everything we've covered:

| Lifecycle Stage | Topics Covered |
|----------------|----------------|
| **Plan** | DMPs, budgeting, funder policies |
| **Collect** | ELNs, file naming, metadata, instrument settings |
| **Process & Analyse** | Version control, documentation, open formats |
| **Store** | 3-2-1 backups, institutional storage, security |
| **Share & Preserve** | Repositories, DOIs, licensing, FAIR principles |
| **Reuse** | Standards, identifiers, community databases |

- Thank participants
- Share the full resource list (link provided below)
- Point to further training opportunities (PSDI, Carpentries, institutional RDM teams)
- Introduce the post-workshop exercise
- Feedback form

### Post-Workshop Exercise: Personal RDM Action Plan

> **Directory:** `challenge-data/13_post-workshop-action-plan/`
>
> **Take-home exercise:** Open `rdm_action_plan_template.md`. Using this template, create a personal RDM action plan with three sections:
>
> 1. **Three things I already do well** (acknowledge your existing good practice)
> 2. **Three things I will change or start doing** (be specific — e.g. "I will start using JCAMP-DX exports for all NMR data" or "I will write a DMP for my current project using DMPonline")
> 3. **One resource I will explore further** (pick from the resources signposted today)
>
> We encourage you to share your action plan with your supervisor or research group.

### Key Points

- Good RDM is a continuous practice, not a one-off task
- Start with small, concrete changes — don't try to overhaul everything at once
- Use the resources and communities available to you

---

# Appendix: Full Resource List

## General RDM

- [UK Data Service — Research Data Management](https://ukdataservice.ac.uk/learning-hub/research-data-management/)
- [DCC — Data Management Plans](https://www.dcc.ac.uk/dmps)
- [DMPonline](https://dmponline.dcc.ac.uk/)
- [GO FAIR — FAIR Principles](https://www.go-fair.org/fair-principles/)
- [ARDC — FAIR Data Self-Assessment Tool](https://ardc.edu.au/resource/fair-data-self-assessment-tool/)
- [re3data.org — Registry of Research Data Repositories](https://www.re3data.org/)
- [Creative Commons — Choose a Licence](https://creativecommons.org/choose/)
- [UK Data Service Costing Tool and Checklist](https://ukdataservice.ac.uk/learning-hub/research-data-management/plan-to-share/costing/)
- [OpenAIRE RDM Costing Tool](https://www.openaire.eu/)

## Funder Policies

- [UKRI/EPSRC Policy Framework on Research Data](https://www.ukri.org/who-we-are/epsrc/our-policies-and-standards/policy-framework-on-research-data/)
- [UKRI — Developing UKRI's research data policy (2025–2026)](https://engagementhub.ukri.org/ukri-openresearch/developing-ukris-research-data-policy/)

## Reproducibility

- Baker (2016) "1,500 scientists lift the lid on reproducibility" — [Nature](https://www.nature.com/articles/533452a)
- "Reproducibility in chemistry research" (2024) — [Heliyon / PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC11305220/)
- Williams et al. (2024) "Opening the black box of article retractions" — [Royal Society Open Science](https://royalsocietypublishing.org/doi/10.1098/rsos.240844)
- [C&EN — Reactions: Solving the reproducibility crisis](https://cen.acs.org/research-integrity/reproducibility/Reactions-Solving-reproducibility-crisis-science/103/i8)

## Chemistry-Specific

- [IUPAC — Digital Standards](https://iupac.org/what-we-do/digital-standards/)
- [IUPAC FAIRSpec](https://www.degruyterbrill.com/document/doi/10.1515/pac-2021-2009/html)
- [IUPAC FAIR Chemistry Cookbook](https://iupac.github.io/WFChemCookbook/)
- [NFDI4Chem](https://nfdi4chem.de/)
- [NFDI4Chem Knowledge Base](https://knowledgebase.nfdi4chem.de/)

## Repositories

- [Chemotion Repository](https://www.chemotion-repository.net/)
- [Cambridge Structural Database (CSD)](https://www.ccdc.cam.ac.uk/)
- [NOMAD](https://nomad-lab.eu/)
- [ioChem-BD](https://www.iochem-bd.org/)
- [Zenodo](https://zenodo.org/)
- [Figshare](https://figshare.com/)

## Electronic Lab Notebooks

- [Chemotion ELN](https://chemotion.net/)
- [eLabFTW](https://www.elabftw.net/)
- [RSpace](https://www.researchspace.com/)

## UK Infrastructure

- [PSDI](https://www.psdi.ac.uk/)
- [PSDI Resources](https://resources.psdi.ac.uk/)
- [Diamond Light Source](https://www.diamond.ac.uk/)
- [ISIS Neutron and Muon Source](https://www.isis.stfc.ac.uk/)
- [Imperial College — Research Data Management](https://www.imperial.ac.uk/research-and-innovation/support-for-staff/scholarly-communication/research-data-management/)

---

# Notes for the Syllabus Author

## On the Imperial College RDM Pages

Content from the following Imperial College RDM pages has been reviewed and incorporated into this syllabus (generalised to be non-institution-specific):

- **What does my funder require?** — Detailed funder-by-funder policy information incorporated into Episode 2
- **Budgeting for RDM Costs** — Specific cost categories and budgeting tools incorporated into Episode 2
- **Storing live data** — Cautionary notes on portable storage and institutional provision incorporated into Episode 4
- **How to share research data** — The spectrum of sharing approaches and Data Access Statements incorporated into Episode 5

Additional Imperial sub-pages that may contain further useful material (not yet reviewed):

- Managing sensitive data
- Organising and describing data
- What does my publisher require?
- Licensing your data
- Archival and preservation

## On the Carpentries Format

The shell-novice lesson structure uses:

- **Episodes** with front matter specifying `teaching` and `exercises` time
- **Objectives** at the start (`::: objectives`)
- **Questions** to frame the episode (`::: questions`)
- **Callout boxes** for asides (`::: callout`)
- **Challenge blocks** for exercises (`::: challenge`)
- **Key points** at the end (`::: keypoints`)

When converting this syllabus to actual lesson materials, the Carpentries Workbench format (Sandpaper) should be used. See the [Carpentries Workbench documentation](https://carpentries.github.io/sandpaper-docs/) for details.

## Timing Summary

| Episode | Topic | Teaching | Exercises | Total |
|---------|-------|----------|-----------|-------|
| 1 | Why RDM Matters | 10 | 5 | 15 |
| 2 | DMPs, Budgeting & Funder Policies | 15 | 5 | 20 |
| 3 | FAIR Data Principles | 10 | 5 | 15 |
| 4 | Storage and Organisation | 10 | 5 | 15 |
| 5 | Sharing and Licensing | 10 | 5 | 15 |
| — | Part 1 Capstone (Challenge 6a–c) | 0 | 15 | 15 |
| | **Part 1 Total** | | | **~95 min** |
| | *Break* | | | *10–15 min* |
| 6 | Reproducibility in Chemistry | 10 | 5 | 15 |
| 7 | Electronic Lab Notebooks | 12 | 0 | 12 |
| 8 | Metadata and Standards | 12 | 8 | 20 |
| 9 | Chemistry Repositories | 10 | 5 | 15 |
| 10 | Data from Chemistry Techniques | 12 | 8 | 20 |
| 11 | PSDI and the Data Landscape | 10 | 0 | 10 |
| — | Workshop Close | 5 | 0 | 5 |
| | **Part 2 Total** | | | **~97 min** |
| | **Workshop Total** | | | **~190–205 min (~3–3.5 hr)** |

**Note on timing:** The current syllabus totals approximately 3–3.25 hours of content (excluding the break). To fit within 2.5 hours, consider:

- Trimming the funder policy detail in Episode 2 (summarise rather than list every funder)
- Reducing Challenge 6 to two sub-challenges instead of three
- Shortening the ELN episode to a brief signpost rather than a full teaching segment
