# 8. Communicate results

> Share what you learned.

Communication is the step that converts private work into public knowledge. If nobody outside the project knows what you found, you did the work for one person. R&D ends at impact, and impact requires communication.

## The channels

You communicate R&D results through:

- **Papers** — peer-reviewed publications, preprints.
- **Posters** — conference posters, internal poster sessions.
- **Reports** — internal reports, technical memos, white papers.
- **Documentation** — READMEs, user guides, API docs.
- **GitHub repositories** — code, models, configs, fixtures.
- **Presentations** — lab meetings, conference talks, stakeholder demos.
- **Products** — released tools, hosted services.
- **Clinical demos** — show-and-tell with the target users.

Pick the channels that match your audience and your medium. A clinical tool with no paper underneath is dismissable; a paper with no code is irreproducible. R&D usually needs *both*.

## What to communicate

For each artifact, communicate at least:

- **The problem.** One sentence.
- **The question.** One sentence.
- **What you did.** Three to five sentences.
- **What you found.** The headline numbers with uncertainty.
- **Why it matters.** Who can do something different now?
- **What you did not show.** Limitations and the next obvious experiment.

The last bullet is the credibility multiplier. Honest limitations sections age much better than triumphant ones.

## Writing patterns that work

- **Lead with the conclusion.** Inverted-pyramid structure. The reader who reads only the first paragraph should still know what you found.
- **Anchor each claim to a number.** Vague claims age badly.
- **Show, do not just tell.** A figure or table for every key claim.
- **Use the active voice.** "We computed" beats "computation was performed."
- **Write before you finish.** Drafting the abstract early forces you to know what the result is.

## Repository hygiene at the end of a project

A good R&D repo at this stage has:

- A README that explains what the project did and how to reproduce it.
- A clear `data/`, `src/`, `notebooks/`, `results/` layout.
- A `requirements.txt` or `environment.yml`.
- A `Makefile` or `run.sh` that reproduces the headline result.
- A frozen version tag at the point of submission or release.
- A note on data access (what is public, what is restricted, how to request).
- A LICENSE file.

Anyone landing on the repo should be able to answer "what is this?" in thirty seconds and "how do I reproduce the result?" in five minutes.

## Documentation as a first-class output

Documentation is the part of communication that most projects underweight. For an R&D project, documentation includes:

- A **getting-started** page so a new user can run the tool in fifteen minutes.
- A **how-it-works** page so a technical reader can understand the method without reading the paper.
- A **limitations** page so an honest user knows where it will break.
- An **API reference** if you ship a library.

Documentation is also the thing that lets the project survive your departure.

## Common traps

- **Saving up the writing for the end.** Write as you go.
- **Overclaiming.** Match the strength of the claim to the strength of the evidence.
- **Burying the limitations.** Put them where reviewers will see them.
- **Shipping the paper without the code.** Half-credit.
- **Shipping the code without the paper.** Also half-credit.
- **Writing only for experts.** Most readers, including future you, will not be experts in this specific subarea.

## You are now at the end of one R&D cycle

You finished. The next cycle starts with a new problem — often one you uncovered while doing this one.

## Where to next

- Back to [the process overview](index.md) to recap the eight steps.
- Up to [Advanced — innovation](../advanced/index.md) when the structured cycle starts to feel routine and you want to push toward new methods and systems.
