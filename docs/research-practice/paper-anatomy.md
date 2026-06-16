# Anatomy of a scientific paper

> Almost every research paper in the biomedical and natural sciences has the same skeleton. Knowing it makes papers faster to read, faster to write, and easier to review.

## IMRaD

The dominant structure is **IMRaD**:

- **I**ntroduction — what was known, what is missing, what we did.
- **M**ethods — exactly what we did, in enough detail to reproduce.
- **R**esults — what we found, factually.
- **a**nd
- **D**iscussion — what it means, in context.

Plus a Title, Abstract, References, and often Supplementary Material.

This structure is so deeply embedded that journals and reporting guidelines assume it. Reviewers expect it. Even when papers do not literally use the headings, the section *roles* are present.

## Title

A scientific title is not a marketing tagline. It is a query.

A strong title:

- States the finding, not the method.
- Names the population.
- Uses concrete words a search engine can match.

| Weak                                                 | Strong                                                                                                  |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Deep learning for medical imaging                    | A CNN trained on T1 MRI lateralises seizure onset in 87% of MRI-negative epilepsy patients              |
| Studies on the hippocampus                           | Subfield-level hippocampal asymmetry distinguishes hippocampal sclerosis on 3T T1 MRI                  |

The second version of each is longer. It is also far more useful.

## Abstract

The abstract is the only section most readers will ever read.

A structured abstract (used by most clinical journals) has five labelled paragraphs:

- **Background** — what is the problem.
- **Methods** — what you did.
- **Results** — what you found, with one or two headline numbers.
- **Conclusions** — what it means.
- **Funding / registration** — increasingly required.

An unstructured abstract (used by methods and many CS journals) has the same content in three to four paragraphs.

Keep it to about 250 words. Numbers in the abstract must match numbers in the results. If they do not, reviewers will catch it.

Write the abstract *last*, after the paper is complete. Writing it first leads to a paper that describes the abstract instead of the work.

## Introduction

A working introduction has four moves:

1. **Establish the importance** of the broad area in two to three sentences.
2. **Summarise what is known** — the current state of the field, citing the strongest existing work in three to six citations.
3. **Identify the gap** — what is missing, in one or two sentences. This is the heart of the introduction.
4. **State your contribution** — what this paper does, what data and methods it uses, and what it found. End with a one-paragraph contribution roadmap.

Together these are sometimes called the "CARS" (Create A Research Space) model after John Swales. CLIMB also covers this pattern in detail.

If the introduction does not name a gap, a reader cannot tell what the paper is *for*.

## Methods

The methods section is where rigor lives. It has to satisfy two readers:

- **A reviewer**, who is looking for design flaws, statistical errors, and missing baselines.
- **A future replicator**, who needs enough detail to reproduce the work.

Standard subsections in biomedical AI:

- **Study design and ethics** — IRB approval, consent, registration.
- **Data and participants** — inclusion / exclusion, sample size, demographics, source datasets.
- **Acquisition** — for imaging or signal data, scanner / equipment, parameters.
- **Preprocessing** — every step, software version, parameters.
- **Model or analysis** — architecture or statistical procedure, training, inference.
- **Evaluation** — metrics, primary outcome, splits, baselines.
- **Statistical analysis** — tests, confidence intervals, corrections.
- **Code and data availability** — links.

Use **reporting guidelines** from the EQUATOR Network as a checklist:

- **[CONSORT](https://www.consort-statement.org)** for randomised trials.
- **[STROBE](https://www.strobe-statement.org)** for observational studies.
- **[TRIPOD+AI](https://www.tripod-statement.org)** for prediction-model studies including AI. This one is required reading for biomedical AI authors.
- **[PRISMA](https://www.prisma-statement.org)** for systematic reviews.

> 📚 **[EQUATOR Network — Reporting Guidelines](https://www.equator-network.org)**

Following the relevant guideline is the cheapest way to avoid most reviewer-driven revisions.

## Results

Results are factual. Interpretation belongs in the Discussion.

Structure:

- **A short paragraph describing the analysed sample** — N, demographics, exclusions.
- **The primary result** — your headline finding with effect size and confidence interval.
- **Secondary results** — supporting analyses.
- **Subgroup or sensitivity analyses** — these usually live here, not in supplementary, when the paper is honest about its scope.

Every figure and table should have a caption that tells the story even if you read only the caption. The reader who only skims figures is your most common reader.

## Discussion

A working discussion has five moves:

1. **One-sentence summary** of the main finding.
2. **Place the finding in context** — how it relates to prior work cited in the introduction.
3. **Mechanistic interpretation** — *why* the finding is what it is, if you have a hypothesis.
4. **Limitations** — real, specific, named. Not boilerplate.
5. **Future work and implications** — for the field, the clinic, the methods.

Avoid two failure modes:

- **Repeating the results** in prose form. The reader just read them.
- **Sliding into salesmanship**. Discussion is where overclaiming gets caught.

## References

- Use a reference manager and a Citation Style Language. Hand-formatting is a time sink and an error source.
- Cite primary literature, not Wikipedia or web pages, for scientific claims.
- Re-check that every citation is *actually* about what you say it is about — citation drift is rampant.

## Supplementary material

Use it for:

- Extra evaluation tables (e.g., subgroup performance).
- Reproducibility appendices (configs, hyperparameters, environment).
- Long methodological derivations.

Do not use it to hide weaknesses. Reviewers will read the supplementary anyway.

## Author affiliations and contributions

Most journals require:

- **CRediT taxonomy** for author contributions (Conceptualisation, Methodology, Investigation, Writing — original draft, etc.).
- **ICMJE-compliant authorship**: substantial contribution, drafting/revising, final approval, accountability. See [Ethics and IRB](ethics-and-irb.md).
- **Funding and conflicts of interest** disclosed.

Decide authorship *before* drafting, not after.

## Where to next

- [The paper writing process](paper-writing-process.md) — how to actually produce the document.
- [Peer review](peer-review.md) — what happens after you submit.
- [Writing fundamentals](writing-fundamentals.md) — sentence-level craft for any section.
