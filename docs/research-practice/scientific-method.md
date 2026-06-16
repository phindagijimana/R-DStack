# The scientific method

> The discipline that turns *a question* into *a defensible answer*.

The scientific method is older than any specific field. In biomedical AI, it does the same work it has always done — keeps you honest about what your data can and cannot say.

## The four moves

The version most working researchers use, in any order, depending on what they have on hand:

1. **Observe** — notice a pattern, a discrepancy, or a clinical phenomenon.
2. **Hypothesise** — propose a specific, falsifiable mechanism or relationship.
3. **Predict** — state what the hypothesis would lead you to see under particular conditions.
4. **Test** — design and run a study (or analysis) that *could* contradict the prediction.

Loop until the evidence either supports the hypothesis, falsifies it, or refines it.

## Falsifiability

A hypothesis only counts if there is a result you would accept as "no."

Examples:

- *"Hippocampal asymmetry is associated with hippocampal sclerosis"* — falsifiable: if the asymmetry distribution overlaps controls, the hypothesis loses support.
- *"Deep learning will revolutionise medicine"* — not falsifiable. No result would settle it.

A useful gut check: *"What would I expect to see if my hypothesis were wrong?"* If you cannot answer, the hypothesis is not yet specific enough.

This is the test introduced by Karl Popper and central to the modern scientific tradition. It is also the discipline most violated by post-hoc storytelling in machine-learning papers, where authors shift the claim until the data fits.

## Controls and confounds

**Controls** isolate the variable of interest. In biomedical AI, that often means:

- A control group matched on age, sex, scanner, site.
- A baseline model evaluated on the same splits.
- A null condition (shuffled labels) to confirm the signal is not noise.

**Confounds** are variables that move with both the input and the outcome and create spurious associations. Common in biomedical AI:

- Scanner manufacturer.
- Field strength.
- Acquisition era.
- Demographics.
- Cohort selection (e.g., only severely affected patients in one group).

A model that learns "scanner type" rather than "pathology" is not wrong about its data — it is wrong about what its data represents. The scientific layer of the [R&D mindset](../mindset/scientific.md) is what catches these.

## Correlation vs causation

Almost every result in biomedical AI is at most a correlation. To claim a cause, you generally need:

- Intervention (you changed something and the outcome changed).
- Or strict natural experiment with strong identifying assumptions.
- Or replication across independent cohorts with consistent direction and effect size.

A correlation is still useful — it can support triage, prediction, or biomarker discovery. But "useful" and "causal" are different claims, and conflating them is one of the most common publication failures.

## Replication and the replication crisis

A finding that does not replicate is not a finding. Since the early 2010s, large-scale replication efforts in psychology, biomedicine, and machine learning have shown that **a meaningful fraction of published results do not hold up** when re-run.

What protects you:

- Pre-registering the analysis plan.
- Reporting effect sizes with confidence intervals, not just *p*-values.
- Running internal replications (different splits, different seeds).
- Running external replications (different datasets, different sites).
- Publishing negative results when they occur.

In biomedical AI specifically, replication usually means external validation on a different site or cohort. See [Mindset → Validation](../mindset/validation.md) and [PhD → Rigor](../phd/rigor.md).

## Evidence hierarchy in biomedical research

When you read or cite evidence, it helps to know where it sits in the hierarchy:

| Level | Type                                           | Example                                                                |
|-------|------------------------------------------------|------------------------------------------------------------------------|
| 1     | Systematic review / meta-analysis of RCTs       | Cochrane review                                                        |
| 2     | Individual randomised controlled trial         | A surgical trial of epilepsy outcomes                                  |
| 3     | Prospective cohort or case-control study       | Multi-site MRI study with pre-registered analysis                      |
| 4     | Retrospective observational study              | Most AI-on-imaging papers                                              |
| 5     | Case series, case reports                       | "We applied X to ten patients..."                                      |
| 6     | Expert opinion, mechanistic reasoning           | A review article without new data                                       |

Most published biomedical AI sits at level 3–4. Knowing this is what lets you read the literature with calibrated confidence — and what helps you set your own work's claim strength appropriately.

## p-values, effect sizes, and uncertainty

A few honest defaults:

- **Report effect sizes**, not just *p*-values. A *p* < 0.05 with an effect size of 0.02 is statistically real and clinically trivial.
- **Report confidence intervals** for any headline number.
- **Treat *p* = 0.04 and *p* = 0.06 as nearly identical evidence** — they are.
- **Multiple comparisons require correction** (FDR, Bonferroni). Especially in high-dimensional biomedical data.
- **Bayesian framings** can be clearer when the question is about beliefs given the data, not about long-run frequencies.

## What the scientific method does not do

- **It does not pick the question for you.** That is a creative act. See [Intermediate → Research question](../intermediate/research-question.md).
- **It does not guarantee a positive result.** A well-designed study can be inconclusive — that is still a contribution.
- **It does not protect against fraud.** Reporting integrity is a separate discipline. See [Ethics and IRB](ethics-and-irb.md).

## Further reading

- *The Logic of Scientific Discovery* — Karl Popper. The canonical statement of falsifiability.
- *Why Most Published Research Findings Are False* — John P. A. Ioannidis. The paper that named the replication crisis in biomedicine.
- *Writing Science* — Joshua Schimel. Chapter 2 in particular on hypothesis structure and story.
- *Statistical Rethinking* — Richard McElreath. A modern, Bayesian, accessible introduction.
- [EQUATOR Network](https://www.equator-network.org) — reporting guidelines that operationalise scientific-method rigor.

## Where to next

- [Searching the literature](literature-search.md) — knowing what others have already tested.
- [Mindset → Scientific layer](../mindset/scientific.md) — the broader mindset application.
- [PhD → Rigor](../phd/rigor.md) — the standard you eventually want to hit.
