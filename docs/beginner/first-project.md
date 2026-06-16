# Your first R&D project

This page is a worked walkthrough. The setting is biomedical AI, but the shape generalises.

## The setting

You are a graduate student or research engineer who has just been told:

> "Take a look at hippocampal asymmetry in epilepsy and see if there is anything there."

That is a real-sounding ambiguous prompt. Your job is to convert it into a small, finishable R&D project.

## Step 1 — Narrow the question

"Anything there" is not a question. Convert it.

After ten minutes of thinking and one search:

> *Does the left-right asymmetry of hippocampal volume on T1 MRI separate patients with hippocampal sclerosis from healthy controls in a small public dataset?*

That is specific, answerable, and small.

## Step 2 — Read five papers

Skim, decide, note. Five citations later, you know:

- Hippocampal asymmetry has been studied for decades.
- The most common metric is *AI = (L − R) / ((L + R)/2)*.
- Public datasets like the Epilepsy Imaging Initiative include both groups.
- FreeSurfer's `hippocampal-subfields` and HippUnfold both segment the hippocampus from T1.
- People report AUCs in the 0.7 – 0.9 range, with a lot of variance across datasets.

You now know enough to do the analysis honestly.

## Step 3 — Collect a small dataset

You pull twenty subjects: ten with diagnosed hippocampal sclerosis, ten controls. You verify each one has a usable T1.

You spend more time than expected on file formats, BIDS layout, and which subjects to throw out for motion. That is normal.

## Step 4 — Build the smallest pipeline

You write a script that:

1. Loads a subject's T1.
2. Runs FreeSurfer's hippocampal subfield segmentation (or HippUnfold).
3. Extracts left and right hippocampal volumes.
4. Computes the asymmetry index.
5. Writes one row per subject to a CSV.

You run it on one subject. Then on five. Then on all twenty.

## Step 5 — Analyze

In a notebook, you:

- Plot the distribution of AI for each group.
- Compute a t-test or a Mann-Whitney U.
- Plot an ROC curve.
- Report the AUC.

You get something like AUC ≈ 0.81 on 20 subjects.

## Step 6 — Sanity-check

Before you believe it, you check:

- Does the metric direction make sense? (Affected hippocampi should be *smaller* on the affected side.)
- Are the worst-classified subjects ones that had motion artifacts?
- Does FreeSurfer's volume agree with the literature's expected range?
- Did you accidentally include the same subject twice?

You find one duplicate. You re-run. AUC drops to 0.78. That is honest research.

## Step 7 — Write it up

A one-page document:

- Question.
- Five citations.
- Sample (N=20 from dataset X, criteria Y).
- Pipeline (FreeSurfer → AI → ROC).
- Result (AUC 0.78 [0.65 – 0.91 bootstrap], one figure).
- Limitations (small N, single dataset, no external validation).
- Next steps.

## Step 8 — Ship the code

You push the repo to GitHub with:

- A README.
- A `requirements.txt`.
- A `Makefile` or shell script that reproduces the analysis from the CSV.
- An example output figure.

## What you just did

You closed the R&D loop at beginner level:

- **Research** — you asked a specific question, read the field, ran an analysis, drew a bounded conclusion.
- **Development** — you built a small pipeline, sanity-checked it, documented it, and made it runnable by someone else.

You did not invent anything. You did not validate it on a hospital cohort. You did not write a paper. That is fine. Those come at the intermediate, advanced, and PhD levels respectively — see [Intermediate — the process](../intermediate/index.md) next.

## Where to next

- [Intermediate — the process](../intermediate/index.md) — the eight-step workflow that names everything you just did.
- [Growth path → Beginner](../growth-path/beginner.md) — what to focus on next.
