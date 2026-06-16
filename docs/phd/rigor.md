# Rigor

> You prove your claim **carefully.**

Rigor is the discipline that separates PhD-level R&D from confident assertion. An original idea without rigor is a press release. The rigor below is what turns a claim into something an expert reviewer cannot wave away.

## What rigor looks like in practice

### Strong study design

- A clear primary hypothesis and a clear primary metric, named before the data is touched.
- A pre-registered or pre-documented analysis plan.
- Power analysis where applicable.
- Explicit handling of confounds (age, sex, scanner, site, race, comorbidity).
- A baseline that is the *best* existing method, not a convenient one.

### Correct statistics

- The right test or estimator for the data structure.
- Confidence intervals, not just point estimates.
- Appropriate paired vs unpaired analysis.
- Bootstrap or other resampling for uncertainty where parametric assumptions are doubtful.
- Honest reporting of effect sizes alongside significance.

### Proper baselines

- The strongest published method on the same data, re-run by you.
- A naive baseline (random, simple feature) for floor.
- At least one alternative method that is plausible but different in family.
- Comparison on identical splits and metrics.

### Reproducibility

- Code, configs, container, and exact dependencies released.
- A frozen evaluation pipeline that produces the headline tables and figures end-to-end.
- A README that lets someone reproduce the main result in under an hour.
- A statement of what *cannot* be reproduced (e.g., private data) and what fixtures are provided as substitutes.

### Error analysis

- Which subjects, sessions, or cases the model gets wrong.
- Whether errors cluster by demographic, scanner, modality quality, or label noise.
- A characterisation of failure modes, not just success modes.
- A statement of what kinds of inputs the system should *not* be used on.

### Sensitivity analysis

- How the result moves when you vary key choices: preprocessing, model size, learning rate, threshold.
- Whether the conclusion survives reasonable alternative analytic decisions.
- Evidence that the headline number is not an artifact of one set of arbitrary choices.

### Bias analysis

- Subgroup performance: by sex, age band, race, site, scanner manufacturer, field strength.
- Calibration by subgroup, not just overall.
- A statement of populations the work does and does not generalise to.

### External validation

- Performance on data the model has never seen and the analyst has never opened.
- Ideally a different site, scanner, or population.
- An honest report of the gap between internal and external performance.

If you cannot do external validation, *say so* and treat it as the next study, not a footnote.

## What rigor is not

- **Tables to fill in.** Rigor is not a checklist applied at the end. It is a property of the whole design.
- **More metrics.** Reporting eight metrics when you only care about one dilutes, not strengthens.
- **Bigger N.** A larger sample with the same design flaws is still flawed.
- **More citations.** Citations are credit, not rigor.

## The reviewer test

For every claim in your work, ask: *"What is the most aggressive interpretation a hostile reviewer could offer? Have I closed it?"*

Common hostile interpretations:

- *"Your splits leaked."* — Did you split by subject, by site, by time?
- *"Your baseline is weak."* — Did you re-run the SOTA on the same data?
- *"Your improvement is within noise."* — Are your CIs disjoint?
- *"You overfit your method to one dataset."* — Did you test on a second?
- *"You ignored a confound."* — Did you stratify or adjust?
- *"You picked the metric that flatters you."* — Is the primary metric pre-registered?
- *"This will not work in the clinic."* — Have you shown subgroup performance and calibration?

A PhD-level result is one where the answer to each of these is on a slide ready to show.

## Rigor and time

Rigor is expensive. It will take longer than your first guess.

The discipline at the PhD level is to **plan for rigor in the schedule**. Building rigor in at design time costs a fraction of what bolting it on at submission time does. Most PhD students discover this the hard way at least once.

## Where to next

- [Depth](depth.md) — rigor requires depth in both methods and the field.
- [Mindset → Validation](../mindset/validation.md) — the broader validation layer of the R&D mindset.
