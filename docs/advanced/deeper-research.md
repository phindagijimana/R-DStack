# Deeper research

> At the advanced level, **you are no longer just reading papers. You are identifying gaps in the field.**

The shift is from being a consumer of literature to being a critic of it. The same set of papers, read by an intermediate researcher and an advanced one, produces very different reading notes.

## What changes

### From "what do they say?" to "what is missing?"

Intermediate reading asks: *what did the authors do, and what did they find?*

Advanced reading asks: *given everything I have read, what is the field collectively unable to do? What question is nobody framing? What dataset is nobody using? What assumption is everyone making that may be wrong?*

The questions that produce real gaps tend to be:

- *"Existing models work on public datasets but fail in real hospitals. Why?"*
- *"Imaging biomarkers exist but are not clinically integrated. What is the blocker?"*
- *"EEG pipelines exist but are hard to reproduce. What does a reproducible one look like?"*
- *"AI models are accurate but not explainable. What does explainability cost?"*
- *"Datasets are large but poorly standardised. What is the missing standard?"*

Each of those is the start of a research direction, not just a project.

### From "I read it" to "I can argue with it"

Advanced readers carry strong, defensible opinions about specific methods, datasets, and groups. They can say:

- *"This paper's segmentation is reproducible but its evaluation is leaky."*
- *"This dataset is large but skews young and white; using it to claim 'population generalisation' is dishonest."*
- *"This group's reported numbers consistently fail to replicate in other hands."*

These opinions are formed by reading deeply, comparing widely, and — critically — running other people's code.

### From "I'll skim it" to "I'll try to reproduce it"

The single biggest leap from intermediate to advanced reading is **running the paper**. Pull the repo. Run their code. Try to reproduce their headline number on the data they used. About a third of the time, you cannot. That experience is what creates real opinions.

## How to find gaps

Three reliable techniques:

### 1. Read the limitations sections

The limitations section of any honest paper is the next person's research question. A paper that says *"our method assumes single-site training data; multi-site generalisation is left to future work"* has handed you the project.

### 2. Read the failure analyses

If a paper does failure analysis at all, it tells you the failure modes the authors could not solve. Each failure mode is a potential thesis.

### 3. Triangulate from multiple papers

Ten papers in the area all use the same dataset → there is a gap in dataset diversity. Ten papers all report AUC and none report calibration → there is a gap in clinical readiness. Ten papers all use one modality and none use the fusion of two → there is a gap in multimodal modelling.

The pattern that no individual paper has solved, but every paper hints at, is the field-level gap.

## Reading volume at this level

You are reading more than at the intermediate level, but selectively:

- **Daily** — abstract-skim of new arXiv / bioRxiv preprints in your area.
- **Weekly** — one full read of a paper that matters.
- **Monthly** — a deep read of a foundational paper or method, including running its code.
- **Quarterly** — a survey or review to recalibrate your sense of the field.

The volume matters less than the discipline. Same papers, same time, different output.

## Reading notes at this level

Your notes shift from "summary" to "position":

- *Summary* — what does the paper say?
- *Position* — what do I now believe, and what would change my mind?

A good advanced reader's notes file looks more like an evolving worldview than a stack of summaries.

## Where to next

- [Stronger development](stronger-development.md) — the other half: what changes in what you build.
- [PhD level → Depth](../phd/depth.md) — what this looks like when it is your full-time job.
