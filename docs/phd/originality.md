# Originality

> You contribute **something new.**

Originality is the most misunderstood PhD-level quality. New does not mean unrecognisable. It means *something the field did not have before, that someone with expertise can identify as new, and that you can defend as new.*

## What counts as new

A PhD-level contribution can be original along any of these axes:

### A new hypothesis

You name a relationship that nobody has named, and you frame it sharply enough to be tested.

Example: *Hippocampal subfield asymmetry is more predictive of seizure laterality than whole-hippocampus asymmetry, especially in MRI-negative patients.*

### A new method

You design an algorithm, statistical procedure, or experimental protocol that did not exist.

Example: *A self-supervised pretraining scheme for T1 MRI that uses surgical-outcome labels as a weak signal during fine-tuning.*

### A new dataset

You assemble, label, or release data the field did not have access to.

Example: *A multi-site cohort of 800 epilepsy patients with paired structural MRI, functional MRI, scalp EEG, and surgical pathology, BIDS-compliant and openly released.*

### A new benchmark

You define a task and an evaluation protocol that gives the field a common measuring stick.

Example: *A leakage-controlled, multi-site, calibration-aware benchmark for MRI-based seizure-onset lateralisation.*

### A new workflow

You design a process — analytical, computational, or clinical — that integrates existing pieces into something the field can adopt.

Example: *An end-to-end pipeline from routine clinical T1 MRI to a clinician-readable hippocampal asymmetry report, validated against pathology in two hospitals.*

### A new theoretical insight

You offer an explanation or framework that reshapes how others think about a problem.

Example: *A unified account of why deep-learning biomarkers for epilepsy generalise poorly across scanners, linking it to specific preprocessing assumptions.*

### A new clinical validation study

You take an existing method and prove (or disprove) that it works in conditions where it had not been tested.

Example: *An external validation of a published hippocampal-sclerosis classifier on 1.5T MRI from a community hospital cohort, showing 12-point AUC drop and identifying the cause.*

Any one of these is a real PhD-level contribution. You do not need to do all seven.

## What does not count as originality

- **Applying X to Y for the first time.** Sometimes this is original; usually it is just one more X-on-Y paper. To count as a contribution, the application has to *uncover something*, not just exist.
- **A bigger version of an existing study.** Larger N is incremental, not original, unless the increase enables a qualitatively new analysis.
- **A more recent baseline.** Updating a comparison is useful but not by itself a thesis.
- **A new framework wrapper.** Reimplementing a published method in PyTorch is engineering, not research.

The test: *if your contribution disappeared, what would the field be unable to do or say?* If the answer is *"not much"*, it is not yet original.

## Where originality comes from

Original contributions come from three reliable places:

1. **The seam between two fields.** Methods routine in one community are new in another.
2. **The unspoken assumption.** Every field assumes things that nobody bothers to write down. Naming and testing one of those is often original.
3. **The failure case.** A method that works *almost* everywhere has a story to tell about why it does not work in the remaining cases.

You will not find these by reading more. You find them by reading deeply, running other people's code, and having strong opinions.

## How to defend originality

When you claim a contribution is new, be ready to:

- Name the closest related works (at least three).
- Explain in one sentence each how yours differs.
- Predict the reviewer who will say *"this looks like Smith 2022"*, and have your answer ready.

The most credible originality claims acknowledge the closest neighbours rather than hiding them.

## Common traps

- **Overclaiming.** Saying your work is *"the first ever"* when it is the second or third. Reviewers find this.
- **Underclaiming.** Burying a real contribution because you are afraid of overclaiming. Both are bad.
- **Surface novelty.** New buzzwords on the same method.
- **Missing the closest neighbour.** Failing to cite the paper that already did 80% of what you did.

## Where to next

- [Rigor](rigor.md) — once you have an original claim, you have to prove it.
- [Depth](depth.md) — originality only matters if you understand the field deeply enough to know it is original.
