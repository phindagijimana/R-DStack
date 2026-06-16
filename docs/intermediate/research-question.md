# 3. Form a research question

> A strong research question is **specific.**

The research question is what turns the gap you identified in step 2 into something you can actually plan a project around. Get this wrong and every later step bends toward the wrong target.

## Weak vs strong

**Weak (too broad):**

> *Can AI help epilepsy?*

You cannot answer this in a year. You cannot answer this in ten years. There is no version of "yes" or "no" that means anything.

**Better:**

> *Can MRI-derived hippocampal asymmetry improve detection of hippocampal sclerosis in epilepsy patients?*

This names:

- The signal (MRI-derived hippocampal asymmetry).
- The task (detection of hippocampal sclerosis).
- The population (epilepsy patients).
- The implicit baseline (whatever "improve" is measured against).

You can plan a study around it.

## The five properties of a good question

1. **Specific.** Names the data, the task, the population, and ideally the metric.
2. **Answerable.** With realistic data, time, and tools.
3. **Falsifiable.** There is a result that would mean *no*.
4. **Bounded.** You can finish it without solving a larger ten-year problem first.
5. **Worth answering.** Either yes or no would tell someone something they did not already know.

If you can put a checkmark next to all five, the question is ready.

## Sharpening a question

Take your draft question and apply each filter:

- **Specific?** What modality, what task, what population, what metric? Add the missing nouns.
- **Answerable?** Do the datasets exist? Do the tools exist? Can you finish in the time you have?
- **Falsifiable?** What numerical result would make you say "no, this doesn't help"?
- **Bounded?** Can you state the scope in one sentence? If you need a paragraph, narrow it.
- **Worth answering?** Who learns something from either outcome?

Most questions need at least two rounds of sharpening.

## Biomedical examples

| Weak                                    | Strong                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Can deep learning predict outcomes?     | Can a CNN trained on baseline T1 MRI predict one-year seizure freedom in temporal-lobe epilepsy patients undergoing surgery?           |
| Is EEG useful for seizure detection?    | Does a transformer trained on routine 21-channel scalp EEG detect interictal epileptiform discharges with sensitivity ≥ 0.85 at FPR ≤ 0.1? |
| Do biomarkers work?                     | Does a multimodal biomarker combining hippocampal asymmetry and FDG-PET asymmetry outperform either alone for lateralising seizure onset?  |

## Hypothesis vs question

Sometimes you state a question; sometimes you state a hypothesis. They are equivalent but oriented differently.

- **Question:** *Does X help Y?*
- **Hypothesis:** *X improves Y by Z compared to baseline B.*

Hypotheses are sharper and easier to evaluate against. Questions are more honest when you genuinely do not know the answer. Either is fine for an intermediate-level project — write one explicitly.

## What to write down

A one-paragraph question statement:

- The question itself, in one sentence.
- The hypothesis, in one sentence (if you have one).
- The metric that would decide it.
- The threshold you would consider a meaningful result.
- The dataset(s) you will use.

This paragraph goes at the top of every later document.

## Where to next

You have a question. Now decide how to answer it: [4. Design a method](design-method.md).
