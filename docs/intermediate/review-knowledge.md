# 2. Review existing knowledge

> Before you build, find out **what has already been done.**

This step is the literature review, but it is also the tool review, the dataset review, and the method review. The output is a clear answer to: *given what already exists, what is the gap I would be filling?*

## The five questions

For your chosen problem, answer:

1. **What has already been done?** Methods, papers, products, pipelines.
2. **What methods exist?** Statistical, algorithmic, clinical.
3. **What are their limitations?** Where do they fail? On what data?
4. **What datasets are available?** Public, internal, clinical.
5. **What are the gaps?** What does nobody seem to have done yet?

Each one deserves a short paragraph in your notes.

## How to actually do it

### Reading

Aim for breadth first, depth second.

- **Breadth (one or two days).** Read three to five recent reviews to learn the vocabulary, the major methods, and who the field's main groups are.
- **Depth (one to two weeks).** Read the ten or fifteen papers everyone cites. Read their methods sections in detail. Note which datasets they used and what their reported numbers were.

If the same five papers keep appearing in everyone's citations, you have found the foundational set.

### Tooling review

Methods papers tell you what is known; tools tell you what is *available* to use today.

- Are there open-source implementations?
- Are they maintained? When was the last release?
- Do they have a permissive license?
- Have other groups successfully reproduced their results?

A method that exists only in a 2014 MATLAB repo with no documentation is, in practice, much less available than a method that ships as a BIDS app.

### Dataset review

You cannot do R&D without data. List:

- Public datasets relevant to the problem (OpenNeuro, UK Biobank, ADNI, ABCD, PhysioNet, TCIA, etc.).
- What each contains (modalities, sample size, labels, demographics).
- Their access rules.
- Known biases (e.g., demographic skew, scanner heterogeneity, label noise).

If your problem requires a kind of data that does not exist in any public dataset, that itself is a finding worth noting.

## Finding the gap

The gap is the difference between *what your problem needs* and *what currently exists*. Common gap shapes in biomedical AI:

- **Existing models work on public data but fail in real hospitals.**
- **Imaging biomarkers exist but are not clinically integrated.**
- **EEG pipelines exist but are hard to reproduce.**
- **AI models are accurate but not explainable.**
- **Datasets are large but poorly standardised.**
- **A method exists for one modality but not for the modality your clinicians actually use.**

Your job is to name the gap *for your specific problem* in one sentence.

!!! example "Worked gap statement"

    *"Hippocampal asymmetry has been validated for hippocampal sclerosis detection on research-grade datasets (HCP, ADNI), but no open tool runs the analysis end-to-end from a routine clinical MRI in under ten minutes with a single-page report."*

That sentence names:

- What has been done (validated on research-grade datasets).
- The gap (no open end-to-end tool, no clinical-grade speed, no clinical-grade report).
- The implicit contribution you would make if you closed it.

## What to write down

A two-page knowledge review with:

- **Field summary** (two paragraphs).
- **Key papers** (ten citations with one-line notes).
- **Available tools** (table with name, license, status, fit).
- **Available datasets** (table with name, modality, N, access).
- **Identified gap** (one sentence).

That document anchors the rest of the project.

## Where to next

You know the gap. Now turn it into a question you can actually answer: [3. Form a research question](research-question.md).
