# 4. Design a method

> You decide **how** you will answer the question.

This is the methods-section work — done before you write any code so that you build the right code rather than refactoring after the fact.

## What you decide

A method design covers six things:

### 1. Data selection

- Which datasets?
- Inclusion and exclusion criteria.
- Sample size — how many subjects, scans, sessions?
- Train / validation / test split, or cross-validation strategy.
- How you will hold out an external test set if one exists.

The biggest sin at this step is letting the test set influence anything else. Decide it now and do not touch it.

### 2. Experimental design

- What are the experimental conditions?
- What is the control or baseline?
- What confounds do you need to handle (age, sex, scanner, site)?
- What is randomised, and what is held fixed?

For a biomarker study, the baseline is usually *the current standard of care* or *the strongest published method on the same data*. Comparing only to a weak baseline is a way to lie to yourself.

### 3. Model / analysis choice

- Statistical test, classical ML model, deep learning architecture, or simple thresholding.
- Pick the simplest method that could plausibly answer the question.
- Justify the choice in one sentence — what about the data or task makes this the right tool?

A common trap: choosing a fancy method because it is fashionable. If a logistic regression on three features could plausibly work, run that first; you may be done.

### 4. Statistical analysis

- What test or estimator?
- What multiple-comparison correction (if relevant)?
- How will you report uncertainty — confidence intervals, bootstrap, posterior?
- What is your stopping rule?

### 5. Evaluation metrics

- What is the primary metric (one, ideally)?
- What secondary metrics will you report?
- What are clinically meaningful thresholds for each?

Resist reporting "AUC = 0.84" as if it stands alone. Pair it with sensitivity at a clinically relevant operating point, or with the comparable baseline number.

### 6. Validation strategy

- Internal validation (cross-validation on the training data).
- Held-out test set.
- External validation on a different dataset, ideally a different site.
- Sensitivity analyses (subgroups, scanner, demographics).

External validation is the single biggest separator between intermediate and advanced work. Plan for it from day one even if you cannot do it yet.

## Pre-registration (optional but powerful)

Even informally, writing the method *before* you run anything protects you from p-hacking and post-hoc storytelling. A pre-registration is just a frozen copy of the method design with a date on it. Some venues (OSF, AsPredicted) make this official; an unchanged document in your repo is enough for many projects.

## What to write down

A two-to-three-page method document with each of the six sections above. Be specific enough that someone else could implement it without asking you a single question.

If you finish writing it and you would not know how to implement it yourself, the method is not designed yet.

## Common traps

- **Letting the test set sneak into design decisions.** Pick the test set first, then never look at it.
- **No baseline.** "Better than nothing" is not a benchmark.
- **Too many metrics.** Pick one primary metric and commit.
- **Vague stopping criterion.** "I'll know when I see it" is how projects drift for months.
- **Skipping confound handling.** Age, sex, scanner, and site silently cause most published failures in biomedical AI.

## Where to next

You have a plan. Now build a working version: [5. Build a prototype](build-prototype.md).
