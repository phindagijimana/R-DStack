# Scientific layer

> *What is true?*

The scientific layer is the layer that keeps you honest about reality. It is the question being asked when you ask *what is actually happening here, beyond what we want to be happening?*

## The four questions

### What is the mechanism?

For any phenomenon, ask: *what is causing what?*

- In biomedical AI, the mechanism question is often pharmacological, neuroanatomical, electrophysiological, or genomic.
- A model that predicts an outcome without addressing mechanism is a useful signal, not an explanation. Be clear which one you have.
- Mechanisms are the parts that survive across datasets, scanners, and decades.

### What evidence supports it?

For every claim, ask:

- What experiments, observations, or analyses make this credible?
- How direct is the evidence? Causal vs. correlational?
- What would the evidence look like if the claim were false?

A claim without traceable evidence is rumour, no matter who said it.

### What are the assumptions?

Every method, model, and dataset carries assumptions. The scientific layer asks:

- What does this approach take as given that might not be true?
- Are the assumptions explicit or implicit?
- Have they been tested in the conditions where we are using them?

The most damaging assumptions are the ones nobody writes down. Surfacing them is a high-leverage skill.

### What are the limitations?

For your own work and others':

- Where does this stop being credible?
- On which populations? Which conditions? Which time windows?
- What kinds of errors are common, and what kinds are catastrophic?

A model with stated limitations is far more useful than a model with hidden ones.

## Habits that strengthen the scientific layer

- **Read methods sections carefully.** They are where mechanism, evidence, and assumptions live.
- **Sit with negative results.** They are usually more informative than positive ones.
- **Distinguish correlation from causation, every time.** It is harder than it looks.
- **Ask "what would change my mind?"** before you start any analysis.
- **Talk to mechanism experts** — clinicians, biologists, physicists. They see assumptions you do not.

## The biomedical version

In biomedical AI, the scientific layer is the layer where you decide whether your model has found a biomarker or a confound. Common confounds masquerading as biomarkers include:

- Scanner manufacturer.
- Field strength.
- Acquisition era.
- Site demographics.
- Cohort selection biases.

A model with apparent biomarker performance that is really driven by scanner type is not just inaccurate — it is *misleading*. The scientific layer is what catches this.

## When the scientific layer is weak

You see it in the work as:

- Strong claims with weak mechanistic grounding.
- Results that swing wildly when you change the dataset.
- Methods sections that gloss over confounds.
- Limitations sections that read like marketing.

Strengthen by reading more deeply, talking to domain experts, and demanding mechanism explanations from yourself.

## Where to next

- [Engineering layer](engineering.md) — the question of whether the truth can be built.
- [Validation layer](validation.md) — the question of whether the built thing actually delivers on the truth.
