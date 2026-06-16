# Intermediate R&D

> You **improve existing work.**

At the intermediate stage, you are no longer just reproducing what others did — you are making it better, cleaner, or more useful.

## Focus

- Compare methods.
- Clean data.
- Build pipelines.
- Evaluate models.
- Add useful features.
- Write documentation.

The shift from junior is that you start to *own* the work — its outputs, its bugs, its users.

## What you actually do

- Compare two or more existing methods on a single dataset, with a fair, leakage-controlled protocol.
- Take a messy real-world dataset and produce a clean, documented version.
- Build a reproducible pipeline that takes raw data to a finished result with one command.
- Evaluate it rigorously: held-out test set, confidence intervals, subgroup analysis, failure analysis.
- Add at least one feature that meaningfully extends the existing method — better calibration, a new modality, faster runtime.
- Write documentation that someone else could use without asking you.

## Example output

> *Build a reproducible MRI pipeline that calculates hippocampal subfield asymmetry and generates a report.*

Concretely:

- A Python package (or BIDS app) that takes a BIDS-organised dataset of T1 MRIs.
- For each subject, runs segmentation, computes subfield-level asymmetry indices, and writes a one-page PDF report.
- Includes a small fixture dataset, automated tests, and a CI pipeline.
- Has a README that explains what it does, what its limitations are, and how to install it.
- Has been used by at least one person other than the author.

That last bullet is what separates intermediate from junior. The work has a user, not just an author.

## What you are learning at this stage

- How to design a method that is more than a copy of a published one.
- How to evaluate honestly when there is no off-the-shelf evaluation protocol.
- How to handle real-world data shapes — missing modalities, motion artifacts, scanner heterogeneity.
- How to write code that other people will read and run.
- How to document for users, not just for yourself.

## Signal that you are ready for the next stage

You have crossed into Advanced R&D when:

- You can identify a field-level gap, not just an in-paper limitation.
- You can design a study that produces evidence one of the field's open questions does not yet have.
- You can build a system that several people depend on without it falling over.
- You can articulate a research direction that is yours, not just an extension of someone else's project.

## Where to next

- [Advanced R&D](advanced.md) — the next stage.
- [Intermediate — the process](../intermediate/index.md) — the eight-step workflow, now mastered.
