# 1. Identify a problem

> R&D starts with a **real need.**

The most common mistake at this stage is starting from a method rather than from a problem. "I want to try graph neural networks" is not a problem. "Clinicians at our hospital cannot quickly compare a new patient's hippocampus to a normative cohort" is.

## What a real problem looks like

A real problem has three properties:

1. **Someone has it.** A clinician, a researcher, a patient, an operator — not just you in the abstract.
2. **It hurts.** There is a cost to the current state: missed diagnoses, slow workflows, unreproducible analyses, manual labour.
3. **It can be described in one sentence.** If you cannot describe it in one sentence to someone who is not a specialist, you do not yet understand it.

## Biomedical examples

- *Clinicians need a faster way to detect hippocampal sclerosis from brain MRI.*
- *Our lab's diffusion MRI pipeline takes three days per subject and crashes on 10% of cases.*
- *EEG epileptiform discharges are detected manually, and inter-rater agreement is low.*
- *Genomic variants found in one cohort do not validate in another, and we do not know why.*
- *Radiologists cannot tell, before surgery, which tumours will respond to immunotherapy.*

Each one names a person, names what hurts, and is one sentence.

## How to find one

You will not invent problems sitting at your desk. The reliable sources are:

- **Sit next to a clinician for a day.** Watch what they do twice and ask why both times.
- **Read incident notes or QA reports from a pipeline.** Failure logs are problem statements in disguise.
- **Ask your PI or team lead what they keep getting asked to do that they wish was automated.**
- **Listen for the word *manual* in any workflow.** Anything manual is a candidate problem.
- **Read the discussion / limitations section of recent papers in your area.** Limitations are unsolved problems.

## What to write down

Once you think you have a problem, write a short problem brief — no more than half a page:

- **Who has the problem.** Roles, not people.
- **What they currently do.** The status quo, in concrete steps.
- **What hurts about it.** Time? Cost? Errors? Unreliability?
- **What "solved" would look like.** A measurable change.
- **Why it has not been solved already.** This forces you to think about constraints.

The last bullet is the most important. If a problem looks obvious and has not been solved, there is usually a reason — limited data, regulatory hurdles, no good algorithm, no one cared. Knowing that reason before you start saves you weeks.

## Common traps

- **Starting from a method.** "Let's apply transformers to EEG" is not a problem.
- **Starting from a dataset.** "We have UK Biobank, what should we do?" is not a problem.
- **Starting from a tool.** "I want to make a dashboard" is not a problem.

Method, dataset, and tool come *after* you know what need they serve.

## Where to next

You have a problem. Now find out what is already known about it: [2. Review existing knowledge](review-knowledge.md).
