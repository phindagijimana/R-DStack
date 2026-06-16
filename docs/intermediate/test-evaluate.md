# 6. Test and evaluate

> Check whether it **actually works.**

Testing and evaluation are the part most projects do too quickly and too narrowly. The questions in this step are the difference between "I built a thing" and "I built a thing that does what I claimed."

## The six questions

For your prototype, you need honest answers to:

### 1. Is it accurate?

- What is the primary metric on the held-out set?
- How does it compare to your baseline?
- How does it compare to chance?
- How does it compare to published results on the same data?

Report numbers with uncertainty (bootstrap CI, cross-validation variance), not point estimates.

### 2. Is it reproducible?

- Can you re-run it from a fresh checkout and get the same result?
- Are random seeds fixed?
- Are dependency versions pinned?
- Does it run on someone else's machine?

If you cannot reproduce your own result, no one else can either.

### 3. Does it generalize?

- How does it perform on a different dataset?
- A different site?
- A different scanner?
- A different population?

If you have not tested any of these, you do not yet know whether your result generalizes. That is fine to admit — it is not fine to claim otherwise.

### 4. Is it better than existing methods?

- Did you re-run the strongest baseline on the same data, the same split, the same metric?
- Or did you compare your number to a published number on different data? (If yes, you have not really compared anything.)

Re-running a baseline is annoying. It is also what separates a real comparison from a sales pitch.

### 5. Is it useful to users?

- Have you shown it to someone outside the project?
- A clinician, a colleague, a target user?
- What did they say?
- What did they do with the output?

A model with great metrics that nobody uses is a development failure, not a research success.

### 6. What are the failure cases?

- Which subjects did it get wrong?
- Is there a pattern? (Demographics, scanner, modality quality, label noise.)
- Are the failures clinically dangerous (e.g., false negatives in screening)?
- Are there systematic biases?

The failure cases tell you more about your method than the successes.

## What "evaluation" actually looks like

A full evaluation produces at minimum:

- A primary results table — your method vs. baseline(s) on the primary metric, with CIs.
- A secondary results table — other metrics, subgroup analyses.
- A failure-case analysis — examples, common patterns, recommended limitations.
- A reproducibility note — exact commit, exact environment, exact data version.
- An external validation result, or an explicit statement that external validation has not been done.

If any of those is missing, the evaluation is incomplete.

## Useful evaluation patterns

- **Hold out by site or subject, not by sample.** Random splits in biomedical data leak information across the split.
- **Compute confidence intervals via bootstrap.** Single numbers without uncertainty are not interpretable.
- **Plot, do not just tabulate.** Distributions, ROC curves, calibration plots, confusion matrices.
- **Report the operating point, not just the curve.** "AUC 0.84" tells a clinician nothing; "sensitivity 0.78 at FPR 0.10" tells them something.

## Common traps

- **Train/test leakage.** Same subject in both splits, or same scanner/site across splits without checking.
- **Cherry-picked metric.** Reporting whichever number looks best.
- **Comparing to a stale baseline.** Make sure your baseline is the *current* best, not a five-year-old paper.
- **No uncertainty.** A single number is rarely defensible.
- **No failure analysis.** Reporting only the average hides systematic failures.

## What to write down

A results document that includes the six question answers, the tables, the plots, and the failure analysis. The document is the artifact you take into [7. Improve](improve.md).

## Where to next

You know what works and what does not. Now iterate: [7. Improve](improve.md).
