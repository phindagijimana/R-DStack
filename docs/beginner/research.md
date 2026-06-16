# Doing research as a beginner

> Research is about **asking questions and finding reliable answers.**

At the beginner level, you are not expected to discover something new. You are expected to find out what is already known well enough that you can summarise it in your own words and defend the summary with a citation.

## What you actually do

### 1. Ask questions

Write the question down before you go looking. The act of writing forces you to be specific.

Weak questions tend to be:

- Too broad: *"Can AI help epilepsy?"*
- Untestable: *"Is the brain interesting?"*
- About you, not the field: *"What should I learn next?"*

Better questions:

- *"What MRI features have been associated with hippocampal sclerosis in adults?"*
- *"How does FreeSurfer's hippocampal subfield segmentation compare to manual tracing on the same dataset?"*
- *"Which public datasets include both 3T T1 MRI and surgical pathology labels?"*

A good beginner research question is **specific, answerable from existing literature, and small enough to finish in a week.**

### 2. Read papers

You do not need to read every paper. You need a reading workflow:

1. **Find** — Google Scholar, PubMed, the references section of a review you already trust.
2. **Skim** — abstract, then figures, then limitations.
3. **Decide** — is this worth a full read? If yes, read methods next.
4. **Note** — one short summary in your own words, with the citation.

Aim for **five papers around your question** before you commit to a direction. Fewer than that and you are guessing; more than that and you are stalling.

### 3. Study existing knowledge

Papers are sharp but narrow. Round them out with:

- A recent review article in the area.
- One textbook chapter on the underlying method.
- The official documentation for any tool you plan to use.

This is the difference between knowing a technique exists and knowing how it actually behaves.

### 4. Collect data

Even at beginner level, you should touch real data. Options:

- A public dataset (OpenNeuro, UK Biobank Showcase, Kaggle, PhysioNet).
- A small fixture dataset shipped with a tool you are studying.
- A handful of subjects from a tutorial.

You are not running a clinical study. You are getting comfortable with the file formats, the shapes, and the things that go wrong.

### 5. Analyze results

For a beginner research task this usually means:

- One or two summary statistics.
- One or two plots.
- One or two sanity checks (e.g., does my computed volume match what FreeSurfer reports?).

Resist the urge to do everything. Pick the smallest analysis that actually answers your question.

### 6. Draw conclusions

Conclusions at this level are short, honest, and bounded:

- *"In this sample of N=20 subjects from OpenNeuro dataset X, hippocampal volume was lower on the affected side (mean Y vs Z, p=...)."*
- *"FreeSurfer and HippUnfold gave hippocampal volumes that agreed within 5% on this dataset; they disagreed more on subjects with motion artifacts."*
- *"Of the five papers I read, three reported asymmetry index as the most useful single feature; the other two preferred shape descriptors."*

Notice what the conclusions do **not** say. They do not claim to generalise. They do not claim novelty. They report what *this* analysis showed, on *this* data, with *these* assumptions.

That honesty is the thing you are practising.

## What success looks like

You finish a beginner research task when you can produce a one-page document with:

- The question (one sentence).
- What you read (five citations and a one-line note each).
- What you did (the analysis, in three to five lines).
- What you found (a number, a plot, or a table).
- What you would do differently next time.

That document is the seed of every future research artifact you will write — a methods section, a paper, a thesis chapter.

## Where to next

- [Doing development as a beginner](development.md) — how to turn what you learned into something runnable.
- [Your first R&D project](first-project.md) — the end-to-end walkthrough.
