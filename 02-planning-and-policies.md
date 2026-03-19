---
title: "Planning Your Data: DMPs, Budgeting, and Funder Policies"
teaching: 15
exercises: 10
---

::::::::::::::::::::::::::::::::::::::: objectives

- Explain what a Data Management Plan is and when to write one
- Identify the key requirements of the EPSRC policy on research data
- Understand what costs are associated with research data management and how to budget for them

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What is a Data Management Plan and do I need one?
- What does my funder require me to do with my data?
- How much does research data management cost, and can I claim it on a grant?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Who Is This Episode For?

As a Masters student, PhD student or postdoc, you are probably not the person writing grant
applications. That job typically falls to your PI. So why should you care
about DMPs and funder policies?

Because the decisions these documents describe -- what formats to save data
in, how to name files, where to back things up, what to deposit at the end
of the project -- are decisions that you carry out every day. A DMP is only
as good as the research practices it describes. If the people closest to
the data are not familiar with what is expected, the plan cannot be followed.

There is also a practical benefit: when you move on to your own independent
research, or collaborate across groups and institutions, you will need to
navigate these requirements yourself. Building familiarity now pays dividends
later.

## Data Management Plans

A **Data Management Plan (DMP)** is a document that describes how you will handle
data during and after a research project. A good DMP covers:

- What data you will collect or generate, and in what formats
- How the data will be organised, named, and documented
- Where it will be stored and how it will be backed up
- Who will have access to it, and under what conditions
- How and where it will be shared at the end of the project
- How long it will be preserved, and who is responsible for it

A DMP is not a one-off form to be filed and forgotten. It is a **living document**
that you return to and update as your project evolves.

### When to write one

Ideally, at the start of a project, before you begin collecting data. Writing
a DMP early forces you to think through decisions that are much harder to
make retrospectively -- which formats will you use? Where will you store
large files? What is your backup strategy?

Some funders require a DMP at the grant application stage. Even when they do
not, having one is good practice and increasingly expected.

### DMPonline

[DMPonline](https://dmponline.dcc.ac.uk/) is a free tool from the Digital
Curation Centre (DCC) that provides funder-specific DMP templates and
guidance. It is the standard tool used by UK researchers and is the
best place to start if you need to write a DMP. Most UK universities also
have their own guidance layered on top of the standard templates.

:::::::::::::::::::::::::::::::::::::::::  callout

## What Makes a Good DMP?

A DMP that says "data will be stored securely and shared where appropriate"
is not useful. A good DMP is specific:

- *"Raw NMR data (Bruker format, ~50 GB/year) will be stored on the
  university Research Data Store with daily backups. Processed data and
  analysis scripts will be version-controlled on GitHub. At publication,
  all supporting data will be deposited in the Chemotion Repository
  under a CC-BY licence."*

If you cannot be specific yet, the DMP can flag that as something to
resolve, but vagueness is a sign that decisions still need to be made,
not that they can be deferred indefinitely.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## Check Your Understanding: What Makes a Good DMP Statement?

Two of the following statements are reasonable things to include in a Data
Management Plan, and two are not. Can you identify which are which -- and
of the two acceptable answers, which is better, and why?

A. "Data will be stored securely and shared where appropriate."

B. "Raw and processed DFT data (~30 GB/year) will be stored on the
university Research Data Store during the project and deposited in the
NOMAD-lab.eu Repository under a CC-BY licence at the point of publication."

C. "NMR and mass spectrometry data will be stored on university servers
and shared via the Zenodo data repository at the end of the project."

D. "Data management will follow best practices for the discipline."

:::::::::::::::  solution

## Answer

**A and D are inadequate.** They are vague and non-committal -- they do not
tell anyone where data will actually be stored, in what format, or under
what conditions it can be reused. A reviewer reading these would have no
way of knowing whether the data will actually be findable or usable.

**B and C are both reasonable**, but B is stronger:

- C names specific data types and mentions university storage and a
  repository, which is a good start. But it does not specify what licence
  will apply, how much data will be generated,
  or when sharing will happen ("at the end of the project" is vague --
  Does that mean before or after the grant ends?).
- B is specific about volume, format, storage location, the exact
  repository, the licence, and the timing ("at the point of publication"
  is unambiguous).

A useful rule of thumb: if someone could read your DMP statement and still
not know what to do or where to look, it needs more detail.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## Funder Policies

UK research funders have formal expectations about how data from their
grants is managed. Compliance with these policies is
increasingly checked at the point of publication and grant reporting.

### EPSRC

The [EPSRC policy framework on research data](https://www.ukri.org/who-we-are/epsrc/our-policies-and-standards/policy-framework-on-research-data/)
applies to all organisations in receipt of EPSRC funding. Its core
expectations are:

1. A DMP should be in place for every EPSRC-funded project (though one
   is not required at application stage)
2. **Metadata** describing the data must be made freely available on the
   internet within **12 months** of the data being generated, and must be
   sufficient for others to understand what data exists, why and how it
   was generated, and how to access it
3. **Published results** must always include information on how to access
   the supporting data (a data access statement)
4. Data required to validate findings must be **preserved for 10 years**
   after its last use by the original researchers or a third party
5. Data should be made openly available unless there are good reasons not
   to (commercial sensitivity, personal data, national security)
6. RDM costs can be included in grant applications

:::::::::::::::::::::::::::::::::::::::::  callout

## EPSRC Does Not Require a DMP at Application

Unlike several other funders, EPSRC does not ask you to submit a DMP
as part of your grant application. However, it expects one to be in
place once the project starts, and the requirements above still apply.
The practical implication is that you need to budget for data management
in your application even if you do not submit the plan itself.

::::::::::::::::::::::::::::::::::::::::::::::::::

### The UKRI Data Policy

EPSRC is one of nine research councils within UKRI (UK Research and
Innovation). Each council has historically had its own data policy, but
UKRI is currently developing a unified research data policy that will
replace these individual policies. The new policy was under development
at the time of writing. Check the
[UKRI open research pages](https://www.ukri.org/what-we-offer/supporting-healthy-research-and-innovation-culture/open-research/)
for the latest position.

The core expectations across all UKRI councils are broadly consistent:
make data available, preserve it for at least 10 years, include a data
access statement in publications, and budget for RDM in grant
applications.

### Other funders

If you are funded by Wellcome Trust, BBSRC, MRC, NERC, CRUK, or a
European funder such as Horizon Europe, the specific requirements vary
in their details -- for example, whether a DMP is required at application
stage, the minimum retention period, and the expected timescale for
sharing. The best way to find out what your funder requires is to look
up their specific policy on DMPonline, which provides a template for
each funder along with a summary of their requirements.

:::::::::::::::::::::::::::::::::::::::  challenge

## Check Your Understanding: EPSRC Requirements

Which of the following is **not** a requirement under the EPSRC policy
framework on research data?

A. Data required to validate findings must be preserved for 10 years.

B. A Data Management Plan must be submitted with every grant application.

C. Published results must include a data access statement.

D. Metadata describing the data must be made freely available within
12 months of the data being generated.

:::::::::::::::  solution

## Answer

**B** is the odd one out.

Unlike several other UKRI councils, EPSRC does not require a DMP to be
submitted at the grant application stage. It does expect one to be in
place once the project starts, but the plan itself is not submitted as
part of the application.

A, C, and D are all genuine EPSRC requirements that apply to funded
projects.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

## Budgeting for Research Data Management

RDM costs are real and often underestimated. The good news is that most
funders allow them to be included in grant applications, provided the
costs are reasonable and proportionate and are incurred before the end
of the project.

Common costs to consider:

**Data storage** -- Your institution likely provides some free allocation
(often 1-2 TB per project), but large or long-running projects may need
additional paid storage.

**Staff time** -- Time spent organising, documenting, and preparing data
for sharing is a legitimate cost. For large or complex datasets, this
can be significant.

**Data preservation and repository fees** -- Most public repositories are
free to deposit in, but some charge fees. Check before you assume.

**Transcription and anonymisation** -- Converting paper records to digital
formats, or anonymising sensitive data, can be time-consuming and may
require specialist support.

**Software and infrastructure** -- Licences for data management tools,
ELN subscriptions, or specialist storage solutions.

One principle worth remembering:
**it is always cheaper to manage data well from the start than to sort it out later.**
Retrospective documentation, reformatting, and reorganisation take far more time than
doing it right at the point of collection.

:::::::::::::::::::::::::::::::::::::::::  callout

## Useful Budgeting Tools

The [UK Data Service Costing Tool](https://ukdataservice.ac.uk/learning-hub/research-data-management/plan-to-share/costing/)
provides a structured checklist for estimating RDM costs.
The [OpenAIRE RDM Costing Tool](https://www.openaire.eu/rdm-costing-tool)
covers European funder requirements.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## Challenge 2: DMP Speed Round

You have just been awarded a 3-year EPSRC grant to develop novel
heterogeneous catalysts for CO2 reduction. Your project will involve
synthesis, characterisation (NMR, XRD, electron microscopy), and
computational modelling.

In groups of 3-4, spend 5 minutes sketching out answers to these
questions:

1. What types of data will you generate? Make a quick list.
2. How much data do you expect to produce over 3 years? (A rough
   order-of-magnitude estimate is fine.)
3. Where will you store the raw data during the project?
4. What will you do with the data at the end of the project?
5. What costs would you include in the grant application?

Report back one thing your group found unexpectedly tricky to answer.

:::::::::::::::  solution

## Discussion

This exercise tends to surface a few common realisations:

**Data volumes are hard to estimate.** Electron microscopy and
computational data in particular can be very large -- it is worth
checking with your local HPC or instrument facility early on.

**"I'll store it on my laptop"** is not an answer that satisfies funder
requirements. Most UK universities provide managed research data storage;
find out what yours offers before the project starts.

**Sharing data is harder than it sounds** when the project involves
multiple partners, industrial collaborators, or sensitive information.
These constraints need to be identified early and addressed in the DMP.

**RDM costs are easy to overlook** at application stage but can be
substantial for complex projects -- particularly staff time for data
curation and documentation.

:::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: keypoints

- A Data Management Plan describes how you will organise, store, share, and preserve your data. Write one at the start of every project.
- EPSRC requires metadata to be publicly available within 12 months of data generation, a data access statement in every publication, and data preserved for 10 years.
- EPSRC does not require a DMP at application stage, but all other UKRI councils do -- check your specific funder's requirements via DMPonline.
- RDM costs are allowable on most UK grants. Budget for storage, staff time, and repository costs from the start.
- It is always cheaper to manage data well from the start than to sort it out later.

::::::::::::::::::::::::::::::::::::::::::::::::::
