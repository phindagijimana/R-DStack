# Validation layer

> *Does it actually work?*

The validation layer is the layer that decides whether your built thing does what you claimed it does. It is the layer most projects underweight, and the one most often raised by reviewers, regulators, and downstream users.

## The five questions

### On which data?

- The training data, the validation data, the test data, and any external datasets.
- The split logic — by subject? By site? By time?
- How representative each dataset is of the population the work will eventually serve.

A model evaluated only on the data it was trained on is not validated. It is *fit*.

### Compared to what?

- The strongest existing method on the same data.
- A naive baseline for floor.
- The current standard of care, where applicable.
- Multiple baselines, all run by you, on the same splits.

"Better than nothing" is not a validation. "Better than the strongest available alternative on the same task" is.

### Under what conditions?

- Which preprocessing choices?
- Which subgroups?
- Which scanners, sites, or operating points?
- Which time windows?

A model that works in one slice of conditions and fails in others has a story to tell. Telling it is part of validation.

### What are the failure cases?

- Which subjects, samples, or cases does it get wrong?
- Are the failures clustered (by demographic, scanner, modality, label noise)?
- Are they recoverable, or catastrophic?
- What kinds of inputs should the system refuse to operate on?

Knowing failure cases is what lets the system be deployed safely — and what lets you defend it under critique.

### Does it generalize?

- Across datasets.
- Across sites and scanners.
- Across populations.
- Over time.
- Under realistic shifts (e.g., new acquisition protocols).

External validation is the single biggest separator between published-only and deployed-anywhere systems.

## Habits that strengthen the validation layer

- **Pre-register the primary metric and threshold.** Decide what success means before you have a number.
- **Split before you preprocess.** Anything that touches the test set leaks information.
- **Bootstrap your confidence intervals.** Single numbers do not validate anything.
- **Plan external validation from day one.** Even if you cannot do it yet, name the dataset you will use.
- **Report calibration, not just discrimination.** AUC alone misses whether the model knows when it does not know.
- **Show subgroup performance.** Aggregate numbers hide the populations the system harms.

## The biomedical version

In biomedical AI, validation is especially load-bearing because:

- The user is making decisions about patients, not products.
- Distribution shift is the rule, not the exception (scanners, sites, populations).
- Regulatory pathways (FDA, CE-mark, MDR) require explicit, documented validation.
- A confidently wrong system can cause harm in ways a confidently wrong recommendation engine cannot.

Validation in this context is a first-class deliverable, not a section near the end.

## When the validation layer is weak

You see it in the work as:

- Headline numbers without confidence intervals.
- "External validation" that is the same site at a different time.
- Subgroup performance that nobody asked about.
- Calibration plots missing entirely.
- Failure analysis missing entirely.
- Baselines that are weak, outdated, or evaluated on different data.

Strengthen by treating validation as a research output in its own right — sometimes the biggest research output of a project.

## Where to next

- [Engineering layer](engineering.md) — what you validate must first be built reliably.
- [Translation layer](translation.md) — validation makes the system trustworthy; translation makes it useful.
