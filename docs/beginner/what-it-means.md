# What R&D means at the beginner level

> At the beginner level, R&D is basically: **learn something deeply, then build something useful from it.**

That is the whole definition for now. It is intentionally lightweight. You are not optimising anything. You are not chasing publication. You are putting the two halves of R&D — research and development — into one project so the loop becomes muscle memory.

## The two halves

### Research at this level

Research as a beginner is about **asking questions and finding reliable answers**, where "reliable" mostly means "I can point to where I got it from."

Examples of beginner-level research:

- Why does this disease happen? (Read a clinical review.)
- Which method works better for hippocampal segmentation — FreeSurfer or HippUnfold?
- What data do we need for a small EEG seizure-detection study?
- What pattern exists in this small dataset I pulled from OpenNeuro?
- What has already been discovered about MRI biomarkers for epilepsy?

What you do:

- Read papers — at least the abstract, methods, and limitations.
- Study existing knowledge — textbooks, reviews, tutorials.
- Ask questions and write them down in your own words.
- Collect a small amount of data.
- Analyze it.
- Draw conclusions you can defend with a number or a figure.

### Development at this level

Development as a beginner is about **building something practical**, where "practical" mostly means "it runs without crashing and a friendly reviewer can follow the code."

Examples of beginner-level development:

- A Python script that loads a NIfTI file and prints volume per region.
- A notebook that downloads a public dataset and plots two distributions.
- A FastAPI prototype that wraps a single function behind one endpoint.
- A small data pipeline that converts DICOM to BIDS for ten subjects.
- A report generator that turns a JSON result into a one-page PDF.

What you do:

- Designing — sketch it on paper before you code.
- Coding — write it.
- Testing — at least run it end-to-end with one realistic input.
- Improving — fix the obvious bugs.
- Documenting — a README that explains *what it does* and *how to run it*.

## Why "deeply, then usefully"

The order matters. If you skip the learning, you build the wrong thing. If you skip the building, you forget what you learned.

A beginner R&D project is not graded on impact. It is graded on whether you closed the loop:

- *Did you read enough to know what you were doing?*
- *Did you build something concrete from what you read?*
- *Can you say in one paragraph what you now understand that you did not understand before?*

If you can answer yes to all three, you have done R&D at the beginner level — even if the artifact is tiny.

## Where to next

- [Doing research as a beginner](research.md) — what reading and analyzing actually look like.
- [Doing development as a beginner](development.md) — what designing, coding, and documenting actually look like.
- [Your first R&D project](first-project.md) — a concrete walk-through.
