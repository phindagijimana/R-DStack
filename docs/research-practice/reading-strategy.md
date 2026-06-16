# A reading strategy

> You will not read everything. The discipline is *deciding what to read deeply and what to skim or skip.*

A working researcher who reads every paper in their inbox does no other work. A working researcher who reads nothing slowly falls behind. The middle path is a graded reading strategy.

## The three-pass read

Adapted from Srinivasan Keshav's widely cited *"How to Read a Paper"*. Each pass takes longer and is reserved for fewer papers.

### Pass 1 — the five-minute decide-to-read

Goal: decide whether to spend more time.

What you read:

- Title.
- Abstract.
- Section headings.
- Figures and their captions.
- Conclusion.

What you write down:

- One-sentence summary in your own words.
- Whether to escalate to pass 2.
- Why.

After pass 1 you either close the paper or pull it into your active reading list. Most papers stop here.

### Pass 2 — the systematic read

Goal: understand what the authors did and whether it is sound, without verifying every detail.

What you read:

- Introduction in full.
- Methods in full, taking notes.
- Results, reading every figure and table.
- Discussion, especially limitations.

What you write down:

- The research question, in one sentence.
- The method, in one paragraph.
- The result, with the headline number.
- Strengths.
- Weaknesses.
- Questions or doubts.

A pass 2 read takes 60–120 minutes for a typical biomedical AI paper. Reserve it for papers that materially affect your project.

### Pass 3 — the deep read with reproduction

Goal: understand the paper well enough to re-implement it, defend it, or argue with it credibly.

What you do:

- Read every sentence including supplementary materials.
- Pull the code, run it on the authors' data.
- Try the method on your own data.
- Walk through the maths or proofs.
- Identify the design choices the authors did not explain.

A pass 3 read takes a week to a month. You will do at most a handful per year — usually the foundational papers in your subfield and the papers you compare yourself against.

## Volume and cadence

A working researcher's reading week often looks like:

- **20–40 papers at pass 1** (mostly from alerts, conference proceedings, recommendations).
- **2–5 papers at pass 2** (the ones that survived pass 1).
- **0–1 papers at pass 3** (only if needed for the current project).

The mistake is treating every paper as a pass 3 read. The other mistake is treating every paper as a pass 1 read. Calibrate.

## What to read in each section

When you do read methods in detail, look for:

- **The actual sample size**, not the recruited sample size. (Exclusions matter.)
- **The split logic**: by subject, by site, by time? Random splits in biomedical data leak.
- **The baselines**: are they the strongest, re-run by these authors?
- **The metric**: is the headline metric clinically meaningful?
- **The confidence intervals**: are they reported?
- **The preprocessing pipeline**: is it specified in enough detail to reproduce?

When you read results, look for:

- **Effect size + uncertainty**, not just *p*-values.
- **Subgroup performance**, not just aggregate.
- **Calibration**, not just discrimination.
- **External validation** or its absence.
- **Failure cases** discussed honestly.

When you read discussion, look for:

- **Limitations** that are real, not performative.
- **Generalisation claims** that match the evidence.
- **What the authors think they did not solve.** That is often your next question.

## Reproducing a paper as a reading method

The fastest way to learn a method deeply is to run its code on data slightly different from what the paper used. Set aside a day:

- Clone the repo.
- Install the dependencies (this often takes longer than expected).
- Reproduce the headline number on the authors' data.
- Run it on a dataset of yours.
- Note every gap between *"the paper says X"* and *"in practice Y."*

You will discover assumptions the authors did not state and limitations the authors did not foresee. This is the highest-value reading you can do.

## Reading for different goals

- **Reading to orient** in a new subfield → reviews and textbooks.
- **Reading to design a study** → close-comparison papers; pass 2.
- **Reading to write a paper** → the five to ten papers you must cite.
- **Reading to defend a thesis** → the foundational works; pass 3.
- **Reading to mentor someone** → reviews; one pass 2 paper per concept.

## Reading groups and journal clubs

Reading is mostly solitary, but a weekly journal club is one of the highest-leverage habits in research:

- One paper, one presenter, 45 minutes.
- The presenter does a pass 2 read, prepares slides.
- The group discusses for 15 minutes.

You learn as much from listening to other people's pass 2 reads as from doing your own. Bonus: it builds the muscle of articulating what is good and bad about a paper in front of peers.

## Further reading

- *How to Read a Paper* — Keshav S, *ACM SIGCOMM Computer Communication Review* 37(3), 2007. Free PDF; the canonical three-pass paper.
- *The Craft of Research* — Booth, Colomb, Williams. Chapter on engaging with sources.
- The PubMed and Scholar interfaces themselves — both have tutorials worth thirty minutes.

## Where to next

- [Note-taking and references](note-taking.md) — where the output of reading lives.
- [Writing fundamentals](writing-fundamentals.md) — the next thing you do with what you read.
- [Searching the literature](literature-search.md) — the upstream skill.
