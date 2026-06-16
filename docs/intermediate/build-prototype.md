# 5. Build a prototype

> Create a **working version** of the idea.

A prototype is not the final system. It is the smallest thing that demonstrates the idea end-to-end, runs on real data, and produces a real result you can evaluate.

## What "working" means

A prototype is working when:

- It runs end-to-end without manual intervention.
- It accepts the inputs your method design specified.
- It produces the outputs your evaluation step needs.
- It can be re-run by you, tomorrow, without remembering eight things.

It does **not** need to:

- Be fast.
- Be pretty.
- Handle every edge case.
- Be production-ready.
- Be a polished software product.

## Common biomedical prototype shapes

- **A Python script** — for an analysis, biomarker, or statistical study.
- **A machine learning model** — a notebook plus a checkpoint and an evaluation script.
- **A FastAPI backend** — for any system a clinician or another tool will hit over HTTP.
- **A React interface** — for anything a human will look at directly.
- **A neuroimaging workflow** — chained command-line tools, usually orchestrated by a Makefile, Snakemake, or Nextflow.
- **A report generator** — turns numerical output into something humans can read.

Pick the shape that matches your method, not the one you find most interesting.

## Build in slices

The single most useful prototype habit is **vertical slicing**: get a thin slice from input to output working first, then thicken it.

For a hippocampal-asymmetry biomarker tool:

1. **Slice 1** — script that takes one T1, returns a hard-coded number 42. (Verifies you can read input and write output.)
2. **Slice 2** — same script, but the number is the actual computed asymmetry index. (Verifies the math.)
3. **Slice 3** — adds a one-page PDF report. (Verifies the output shape.)
4. **Slice 4** — runs over a folder of subjects. (Verifies batching.)
5. **Slice 5** — adds a config file for parameters. (Verifies configurability.)

Each slice ends with a runnable, demoable artifact. If you stop after slice 2, you still have a working thing.

## Code at this stage

You are not writing production code. But you are also not writing throwaway notebook spaghetti. Aim for:

- A clear separation between *configuration*, *I/O*, and *the function you actually care about*.
- A `requirements.txt` or `environment.yml`.
- A single command (`make run` or `python -m mymodule`) that reproduces the analysis.
- A git repo with meaningful commit messages.

You do not need:

- A class hierarchy.
- An ORM.
- Microservices.
- A CI pipeline (yet).
- Docstrings on every function.

If the prototype's main script is two hundred lines of straight-line Python, that is fine. Refactor only when the next slice tells you to.

## When to stop building and start testing

Stop when:

- The full slice runs end-to-end on at least one realistic input.
- The output has the shape your evaluation step expects.
- You can re-run it from a fresh shell without remembering tricks.

That is the bar. The next step, [6. Test and evaluate](test-evaluate.md), is where you find out whether what you built actually answers the question.

## Common traps

- **Polishing before evaluating.** If you spend three weeks refactoring and you have not measured anything yet, you have stopped doing R&D.
- **Adding features before vertical slicing.** "Let me first add a database" — no, get the first thin slice working.
- **Premature framework adoption.** A 50-line script does not need Hydra, Pydantic, and FastAPI.

## Where to next

The prototype runs. Now check whether it works: [6. Test and evaluate](test-evaluate.md).
