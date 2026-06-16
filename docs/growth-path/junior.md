# Junior R&D

> You **reproduce existing work.**

Reproducing is the underrated skill. It is the cheapest way to learn how a field actually behaves — separately from how its papers describe themselves.

## Focus

- Read papers.
- Reproduce methods.
- Run experiments.
- Understand limitations.
- Build small prototypes.

The shift from beginner is that you are no longer following tutorials — you are following *papers*, with all their gaps, ambiguities, and missing details.

## What you actually do

- Pick a published method in your area and reproduce its headline result, ideally on the data the authors used.
- When the paper does not give enough detail, fill in the gap with a defensible choice and document it.
- Compare your number to the paper's number. Investigate any disagreement.
- Run the same method on a different dataset and report what happens.
- Read the paper's limitations section and identify which limitations you observed in practice.
- Write a one-page replication note describing what you did, what worked, and what did not.

## Example output

> *Reproduce a published hippocampal asymmetry analysis on a small dataset.*

Concretely: you take a paper that reports an asymmetry-based classifier for hippocampal sclerosis. You re-run their pipeline on a public dataset (or the same dataset, if it is public). You report:

- Their headline number.
- Your number.
- The gap, and your honest analysis of where it comes from.
- Three things the paper did not specify that you had to guess.

That document is the deliverable.

## Why reproduction matters

Most papers are not perfectly reproducible. The gap between "the method as written" and "the method as it actually behaves" is where R&D understanding lives. You will not see this gap from reading. You will only see it from running.

Reproducing also teaches you:

- Which methods are actually available as code.
- Which datasets are actually usable in practice.
- Which authors give detailed methods and which do not.
- Which preprocessing choices matter and which do not.
- How long real things take.

That tacit knowledge is what separates a junior researcher who can plan a project from one who cannot.

## Signal that you are ready for the next stage

You have crossed into Intermediate R&D when:

- You have reproduced at least one published result and can articulate exactly where you and the paper disagreed.
- You can read a paper and predict, before running anything, which of its details will be hard to reproduce.
- You can spot an evaluation flaw — a leaky split, a weak baseline, a missing CI — in a paper at first read.
- You can choose between two methods for a new problem and defend the choice.

## Where to next

- [Intermediate R&D](intermediate.md) — the next stage.
- [Intermediate — the process](../intermediate/index.md) — the conceptual section, which becomes much more navigable after you have reproduced a couple of papers.
