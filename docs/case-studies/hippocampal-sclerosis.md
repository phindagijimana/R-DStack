# Case study — hippocampal sclerosis on MRI

The same problem, seen at four levels of R&D.

## The problem

**Detecting hippocampal sclerosis from MRI.**

Hippocampal sclerosis (HS) is the most common pathology in temporal-lobe epilepsy. Identifying it pre-surgically from structural MRI guides surgical planning and predicts outcome. Some cases are obvious on MRI; many are subtle, and the variability in radiologist agreement is substantial.

## Beginner view

> *Use AI to detect abnormal hippocampus.*

What this looks like in practice:

- A graduate student or new research engineer hears "AI + epilepsy" and wants to try.
- They pick a public dataset with HS labels, load a few subjects, and train a small classifier on whole-brain features.
- They report an AUC and produce a confusion matrix.
- The result is reproducible on their laptop and nowhere else.
- It is a learning exercise. They have closed the R&D loop once.

What they have:

- Vocabulary (T1, FreeSurfer, hippocampus, sclerosis).
- Practice with the toolchain.
- A concrete artifact, however small.

What they do not have yet:

- Defensible methodology.
- External validation.
- A user.
- A claim to originality.

## Intermediate view

> *Calculate hippocampal volume and asymmetry from MRI and compare left vs right.*

What this looks like in practice:

- The same person, two years later, runs FreeSurfer or HippUnfold on a curated cohort.
- They compute hippocampal volumes by subfield, then a left-right asymmetry index per subfield.
- They compare patients (n ≈ 50–100) to controls with proper statistics.
- They write a reproducible pipeline in Python with a Makefile, a README, and a few tests.
- They report results with confidence intervals and discuss limitations.

What they have:

- A clear scientific question with measurable answer.
- A reproducible pipeline.
- A real result — say, AUC 0.78 [0.70 – 0.86] on internal data.
- Documentation good enough for a colleague to use.

What they do not have yet:

- Evidence that this works across datasets and scanners.
- Integration into a clinical workflow.
- A field-level contribution beyond reproduction.

## Advanced view

> *Develop a reproducible pipeline using segmentation, asymmetry indices, normative thresholds, and visualization.*

What this looks like in practice:

- The same person, four to six years in, builds a full pipeline that integrates multiple analyses.
- The pipeline accepts BIDS input, runs containerised segmentation (FreeSurfer + HippUnfold), computes asymmetry indices across subfields, compares them to normative thresholds derived from a healthy reference cohort, and renders a one-page clinician-readable report.
- It has been validated on internal data and on a second cohort from a different institution with different scanners.
- It runs on HPC and on cloud, with CI tests and a tagged release.
- It is used by at least one other research group; it has its own documentation site.
- They have published one method paper and one external-validation paper.

What they have:

- A working system other people depend on.
- Multi-site validation.
- A real contribution to the field — they did not just improve numbers; they delivered a usable artifact.
- Engagement with clinicians using the output.

What they do not have yet:

- Mechanism-level explanation linking imaging features to pathology and outcome.
- Integration with EEG, PET, or other modalities.
- Surgical-outcome validation.
- A clear regulatory path to deployment.

## PhD-level view

> *Create and validate a clinically interpretable biomarker system that links MRI-derived hippocampal asymmetry with pathology, EEG, seizure laterality, and surgical outcomes across datasets and institutions.*

What this looks like in practice:

- A coherent research program — usually a PhD plus postdoc — that builds and validates a multimodal biomarker framework.
- MRI-derived asymmetry is tied to surgical pathology in a cohort with histology.
- The same biomarker is correlated with seizure laterality from intracranial recording.
- The asymmetry plus EEG features are jointly predictive of one-year post-surgical seizure freedom.
- Validation spans three or more institutions, multiple scanners, multiple acquisition protocols, and includes calibration and subgroup analyses.
- The work is released as an open BIDS app, a public dataset, a methods paper, two validation papers, and a clinical decision support prototype.
- The output is being integrated into pre-surgical planning at one academic medical centre and is in early conversation with regulatory authorities.

What they have:

- Originality — a new biomarker framework linking imaging, electrophysiology, and outcome.
- Rigor — multi-site validation with calibration, subgroups, and external testing.
- Depth — they can defend every method choice, including the boring ones.
- Contribution — other groups now use their framework as a baseline; the released cohort accelerates a dozen downstream projects.
- Independence — they defined the direction, articulated why it mattered, and produced a thesis-defensible body of work.

## What changes between the levels

Same problem, four very different projects. What moves:

| Dimension          | Beginner       | Intermediate    | Advanced              | PhD level                                      |
|--------------------|----------------|-----------------|-----------------------|------------------------------------------------|
| Question scope     | "try AI"       | "is asymmetry predictive?" | "is the pipeline usable and validated externally?" | "is the multimodal biomarker framework clinically meaningful and generalisable?" |
| Data               | 10–30 subjects | 50–200 subjects | 500+ across two sites | 1000+ across three or more sites               |
| Artifact           | Script         | Pipeline         | System                | Framework + dataset + decision-support prototype |
| Validation         | Internal only  | Internal with CIs| Internal + external   | Multi-site, calibration, outcome-linked         |
| Audience           | Self           | Colleagues       | Other research groups | Field, clinicians, regulators                  |
| Originality        | None claimed   | None claimed     | Real but bounded      | Field-shaping                                  |
| Time horizon       | Weeks          | Months           | A year or two         | Five+ years                                    |

The *problem* did not change. The *project around it* changed every time.

## How to use this case study

When you start a new project:

- Pick the level the project is actually at. Be honest.
- Make sure the artifact, validation, and audience match the level. Mismatch is the most common source of stuck projects.
- When you finish, ask whether the project earned the right to move up a level.

You do not have to do every level in order on the same problem. But understanding the levels means you can choose, deliberately, where to spend the next year.

## Where to next

- [PhD level](../phd/index.md) — the five qualities you would need to operate at the top of this case study.
- [Biomedical AI → R&D outputs](../biomedical-ai/rd-outputs.md) — the kinds of artifacts that compose into a PhD-level result like the one above.
- [Growth path](../growth-path/index.md) — the same progression abstracted away from any single problem.
