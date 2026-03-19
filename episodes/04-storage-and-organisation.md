---
title: "Data Storage, Security, and Organisation"
teaching: 10
exercises: 10
---

::::::::::::::::::::::::::::::::::::::: objectives

- Apply consistent file naming conventions to research data
- Identify the risks of relying on a single storage location and explain how to mitigate them
- Choose appropriate storage solutions for different types of research data

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- How should I name and organise my research files?
- How do I make sure my data is backed up and protected against loss?
- When is it appropriate to use cloud storage or portable devices?

::::::::::::::::::::::::::::::::::::::::::::::::::

## File Naming

Good file names are one of the simplest and most impactful things you can do for your data. The goal is a name that is unambiguous, sortable, and meaningful to someone who has never seen the file before including your future self.

A few principles that work well together:

- **Use ISO 8601 dates** (YYYY-MM-DD) at the start of the filename, so files sort into chronological order automatically.
- **Avoid spaces and special characters.** Spaces and characters like `(`, `)`, `&`, and `#` cause problems in scripts, command-line tools, and some operating systems. Use hyphens (`-`) or underscores (`_`) instead.
- **Be descriptive but concise.** Include enough information to identify what the file contains: The technique, sample or compound, and what stage of processing it is at.
- **Use version numbers consistently**, and avoid the word "final". Files named `final`, `final2`, and `FINAL_really_final` are a sign that version control has broken down. Use `v01`, `v02` instead.

For example:

```
BAD:  final data (IR) copper series v3 FINAL.xlsx
GOOD: 2025-03-15_IR_Cu-series_catalyst-screening_v02.xlsx
```

The naming convention you choose is less important than picking one and using it consistently across a project. Document it in a README so anyone joining the project later knows what to expect.

## Folder Structure

A consistent folder structure makes it easy to find files, understand what is in a project, and hand things over to someone else. There is no single correct structure, but a few principles help:

- Keep raw data in a dedicated folder and treat it as **read-only**: never overwrite it.
- Separate raw data, processed data, analysis scripts, and documentation.
- Include a `README.md` at the root of every project explaining what is in each folder.

Here is an example structure for a simple chemistry project:

```
project-name/
├── README.md
├── 01_raw-data/
│   ├── NMR/
│   ├── IR/
│   └── mass-spec/
├── 02_processed-data/
├── 03_analysis/
├── 04_manuscripts/
└── 05_documentation/
    ├── data-dictionary.csv
    └── protocols/
```

Numbered prefixes ensure folders appear in a logical order rather than alphabetically. Adapt the structure to your project. The key is that you can explain it to someone else in two minutes.

## Backup and Storage

The core principle of data backup is simple: **a single copy is a single point of failure.** A laptop can be stolen, a hard drive can fail, a USB stick can be left in a jacket pocket and put through the wash. None of these are unusual events and they happen regularly! The question is not whether it will happen to you, but whether you will lose data when it does.

The practical minimum is to ensure that at least one copy of your data exists in a different physical location and is managed independently of your local machine. This does not require anything complicated: most institutional storage solutions and cloud services already provide this automatically. If your data is synced to university-managed storage, it is most likely offsite and backed up.

:::::::::::::::::::::::::::::::::::::::  challenge

## Check Your Understanding: Is Your Data Safe?

Think about your most important dataset from the past six months. Then answer these questions:

1. How many separate copies of it exist right now?
2. Are any of those copies in a different physical location (e.g. cloud storage, a university server)?
3. If your laptop was stolen tomorrow, what would you lose?

Discuss your answers with a neighbour. If the answer to question 1 is "one", what is the simplest change you could make this week?

:::::::::::::::  solution

## Discussion Points

Most people, when they first think about this, realise they have fewer copies than they assumed. Common situations:

- Data on a laptop, with "a copy" on an external drive kept next to the laptop -- this is still a single physical location.
- Data on a university workstation that is backed up by IT -- this is probably fine, but worth confirming with your IT team.
- Data that exists only in a shared lab folder on a network drive -- better, but worth knowing what the retention policy is.

The simplest improvement for most researchers is to sync active project data to institutional cloud storage (e.g. university-managed OneDrive or SharePoint). This is usually free, automatic once configured, and already satisfies most funder requirements for active data backup.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

### Institutional storage

Most UK universities provide managed research data storage, typically accessed via the institution's network or a web portal, backed up automatically, and compliant with funder requirements. Find out what your institution offers before your project starts: it is usually more reliable, more secure, and better supported than personal solutions.

:::::::::::::::::::::::::::::::::::::::::  callout

## Ask Before You Need To

It is much easier to set up institutional storage at the start of a project than to migrate data mid-way through. Find out:

- What storage your institution provides and how to access it
- Whether there is a free allocation per project and what it covers
- What the retention policy is (how long are files kept after a project ends?)
- Whether your storage qualifies as research data storage for funder compliance purposes

Your institution's library, IT services, or research data management team are the right contacts.

:::::::::::::::::::::::::::::::::::::::::::::::::

### Portable storage

USB drives, external hard drives, and personal laptops are useful for transporting data and working away from the office -- but they should never be your only copy. USB drives are easily lost, corrupted, or forgotten in a pocket. Personal devices can be stolen (as Aisha in our learner profiles discovered). Use portable devices as a working copy alongside institutional storage, not as a primary backup.

### Cloud storage

Consumer cloud services (Google Drive, Dropbox, personal OneDrive) are convenient, but may not be appropriate for sensitive or confidential research data. Data stored in commercial cloud services may be subject to terms of service that conflict with your institution's data governance policies or a funder's requirements. If your data involves commercially confidential compounds, material under NDA, or personal data from research participants, check your institution's policy before using consumer cloud storage. Institutionally-managed cloud services are generally a safer option.

## Keeping Raw Data Safe

Once raw data is overwritten or deleted, it is often gone for good. Three habits protect against this:

- **Set raw data folders to read-only** after initial transfer from an instrument, so files cannot be accidentally modified.
- **Never process data in place:** copy raw files to a working directory before processing, and keep the originals untouched.
- **Name processed files clearly** to distinguish them from raw data: `2025-03-15_NMR_compound-12_processed.csv` rather than `data_processed.csv`.

## Version Control

For code, analysis scripts, and text files such as README documents or data dictionaries, version control tools such as Git offer a more robust approach than manual `_v01`, `_v02` suffixes. Git tracks every change, records who made it and when, and makes it possible to revert to any previous state. If you are not already using version control for your code, the
[Software Carpentry Git lesson](https://swcarpentry.github.io/git-novice/) is a good starting point. We will not go into the details here, but it is worth mentioning: the difference between "I accidentally deleted this analysis script" and "I accidentally deleted this analysis script but I can get it back in 30 seconds" is having version control set up.

## Security Considerations

Most research data does not require special security measures -- but some does. Data involving commercially sensitive information, proprietary compounds, material under NDA, or personal information about research participants requires additional care:

- **Access controls** -- ensure only authorised people can access sensitive files. Institutional storage typically provides granular access controls; a shared folder visible to everyone in a department is not appropriate.
- **Encryption** -- sensitive data should be encrypted in transit and at rest. Most institutional storage does this automatically; check before assuming it is in place.
- **Deletion** -- deleting a file from a shared drive or cloud service does not always remove it immediately or permanently. Know how your storage handles deletion and what the recovery window is.

If you are unsure whether your data requires special handling, your institution's data protection officer or research data management team can advise.

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge 5: Reorganise This Project

Below is the file listing for a chemistry project, as it was left when the PhD student who ran it moved on.

```
project/
├── data.xlsx
├── data_v2.xlsx
├── data final.xlsx
├── data FINAL (2).xlsx
├── NMR spectra/
│   ├── compound1.fid
│   ├── compound1_processed.fid
│   ├── compound1_REAL.fid
│   ├── comp2.fid
│   └── NEW comp2.fid
├── ms.txt
├── ms backup.txt
├── paper draft.docx
├── paper draft v2.docx
├── paper SUBMITTED.docx
├── figures/
│   ├── fig1.png
│   ├── fig1_new.png
│   └── fig1_final.png
└── misc/
    ├── emails.txt
    ├── old stuff/
    └── todo.txt
```

With a neighbour (or in a small group), discuss:

1. What problems do you see with this structure and naming scheme?
2. What information is missing that would be needed to make sense of this project?
3. Sketch out a better folder structure and suggest a revised naming convention for the NMR files.

:::::::::::::::  solution

## Discussion

**Naming problems:**

- Multiple files with competing "final" labels (`data final.xlsx`, `data FINAL (2).xlsx`) -- there is no way to know which is the version used in the paper without opening each one.
- `compound1_REAL.fid` and `NEW comp2.fid` suggest versions were created in frustration rather than systematically.
- `ms.txt` and `ms backup.txt` at the root level -- no date, no compound name, format unclear.
- Spaces in filenames throughout.

**Structural problems:**

- Raw and processed NMR data are mixed in the same folder with no way to distinguish them.
- Manuscript drafts are mixed in with data files at the root level.
- `misc/` and `old stuff/` are catch-all folders that hide their contents.

**Missing information:**

- No README explaining what the project is, which compounds were made, or what the data files contain.
- No dates on any files.
- No indication of which `data.xlsx` is the one analysed in the paper.

**A better approach:**

```
project-name/
├── README.md
├── 01_raw-data/
│   ├── NMR/
│   │   ├── 2024-05-10_NMR_compound-01_raw.fid
│   │   └── 2024-05-12_NMR_compound-02_raw.fid
│   └── mass-spec/
│       └── 2024-05-10_MS_compound-01.txt
├── 02_processed-data/
│   ├── 2024-05-10_NMR_compound-01_processed.fid
│   └── 2024-05-10_results-summary_v01.xlsx
├── 03_analysis/
├── 04_manuscripts/
│   ├── 2024-09-01_manuscript_v01.docx
│   └── 2024-11-15_manuscript_submitted.docx
└── 05_figures/
    └── 2024-10-01_fig1_scheme.png
```

The single most impactful improvement is the README. Without it, even a well-organised folder is difficult for a newcomer to interpret.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: keypoints

- Use descriptive, consistent file names with ISO 8601 dates, no spaces, and explicit version numbers. Avoid "final".
- Keep raw data in a dedicated, read-only folder, separate from processed data and analysis.
- A single copy is a single point of failure, ensure at least one copy is stored offsite or in managed cloud storage.
- Use institutional research data storage as your primary backup, it is more reliable and funder-compliant than personal solutions.
- Portable storage and consumer cloud services are useful but are not substitutes for institutional storage.
- Sensitive data requires access controls and encryption, check your institution's policy.

::::::::::::::::::::::::::::::::::::::::::::::::::
