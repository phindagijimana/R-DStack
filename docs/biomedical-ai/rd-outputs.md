# Biomedical AI — R&D outputs

What counts as a finished R&D contribution in biomedical AI? Eight common output classes, what each requires, and how they compose.

## 1. Publications

The base currency of academic R&D:

- Peer-reviewed papers in clinical, methods, or interdisciplinary journals.
- Preprints on arXiv, bioRxiv, medRxiv.
- Conference proceedings (MICCAI, NeurIPS, ICML, AMIA, IEEE EMBC).
- Workshop and short papers.

A publication becomes an R&D output when it ties to a real method or system that others can act on. Publications without artifacts are research; publications with artifacts are R&D.

## 2. Patents

In biomedical AI, patents matter when:

- The output is intended to become a product.
- The novelty is in a specific algorithm, system architecture, or data handling.
- A commercial partner will license, develop, or deploy it.

Patents and papers are not mutually exclusive — many groups file a provisional, then publish, then build out the patent. The choice depends on the deployment path.

## 3. Open-source tools

Many of the highest-impact biomedical AI contributions are open-source tools:

- BIDS apps for imaging.
- Pipelines for EEG / MEG / fNIRS.
- Pretrained model releases (e.g., MONAI, nnU-Net, fMRIPrep).
- Visualization, QC, and analysis utilities.

An open-source tool is a real R&D output when it has:

- A maintained release process.
- Documentation users can follow.
- A test suite and CI.
- A community of users beyond the authoring lab.

## 4. Clinical prototypes

A prototype that sits in front of a real clinician, in a real workflow, with real (or carefully de-identified) data. Prototypes are the bridge between research and clinical R&D.

A clinical prototype as an R&D output requires:

- An IRB or equivalent approval.
- A defined clinical task.
- A defined user (role and workflow).
- A clear failure mode and safety story.
- Feedback collection from the users.

Many high-impact projects produce papers and prototypes simultaneously.

## 5. Commercial products

When the output crosses into a regulated, sold, or supported product:

- Software-as-a-Medical-Device (SaMD).
- Hospital-deployed analytics platforms.
- Cloud-hosted research tools with paid tiers.
- Devices with embedded AI.

A commercial product as an R&D output requires regulatory paths, quality systems, support staff, and a sustaining engineering plan. Most academic projects do not need to ship products — but the projects that do shape the field for years.

## 6. Validated biomarkers

A biomarker becomes an R&D output when:

- It is defined in terms of measurable inputs.
- It is linked to a clinically meaningful outcome.
- It is validated across multiple cohorts, sites, and ideally protocols.
- It is released as a runnable workflow other groups can use.
- It is endorsed by clinical or regulatory stakeholders.

Validated biomarkers are among the highest-impact R&D outputs in biomedical AI because they unlock new clinical use cases.

## 7. Startup technology

Sometimes the R&D output becomes the foundation of a company:

- A core algorithm or model.
- A dataset asset.
- A workflow that incumbents cannot easily replicate.
- A regulatory clearance.

This output exists at the edge between research and commercialisation. Many biomedical AI faculty operate on both sides simultaneously.

## 8. Hospital-integrated systems

The most operational form of R&D output: a system actually deployed inside a hospital's IT environment, integrated with PACS / EHR, used in routine workflow.

This requires everything else on this list plus:

- Hospital IT and security review.
- Clinical change management.
- Ongoing monitoring and recall procedures.
- Documented integration with existing clinical workflows.

A single hospital-integrated R&D output is often the capstone of years of research.

## How outputs compose

A mature R&D effort in biomedical AI usually produces a *stack* of outputs, not a single one:

1. A paper that establishes the method.
2. A second paper that validates it on external data.
3. An open-source tool that lets others reproduce both.
4. A patent or license that enables a commercial path, where appropriate.
5. A clinical prototype that translates the method into a workflow.
6. A hospital-integrated system that lands the prototype at scale.

Each output reinforces the others. A method paper without code is half-credit. A tool without validation is half-credit. A system without a paper underneath is half-credit.

The compounded combination is what makes biomedical AI R&D distinctive.

## Where to next

- Back to [Biomedical AI → index](index.md).
- [Case study — hippocampal sclerosis](../case-studies/hippocampal-sclerosis.md) — the worked example tying all of this together.
- [PhD level → Contribution](../phd/contribution.md) — what these outputs need to be in order to count as a PhD-level contribution.
