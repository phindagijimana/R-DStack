# Stronger development

> At the advanced level, **you are no longer just building small scripts. You are building systems.**

The artifact you ship at the advanced level lives a different life than the prototype you shipped at the intermediate level. It is depended on by other people, runs on other people's data, and survives your absence.

## What changes

### From scripts to systems

A script does one thing once. A system does one thing reliably, many times, for many users, across many conditions.

Going from script to system means caring about:

- **Reliability** — what happens when an input is malformed?
- **Reproducibility** — same input today and a year from now should produce the same output.
- **Observability** — when something goes wrong, can you tell what and where?
- **Maintainability** — can someone other than you change it?
- **Scale** — does it still work on 10× the data?
- **Security** — is the data handled in a way that does not get the project shut down?

You do not have to solve all six at once. But ignoring them all is the difference between *"I built a script"* and *"I built a system."*

### Concrete examples of advanced biomedical outputs

The artifacts that earn the label "advanced R&D" tend to look like:

- **A reproducible neuroimaging pipeline** — packaged as a BIDS app, containerised, runnable on HPC or cloud, version-pinned, with a CI build that proves it still works.
- **A validated AI biomarker workflow** — model + evaluation + report generation, run on at least two external datasets, with calibration and subgroup analysis.
- **A clinical decision support prototype** — sits in front of a clinician, surfaces a recommendation, logs everything, is explicit about its uncertainty.
- **A data standardisation platform** — converts the messy reality of clinical data into a canonical form a hundred downstream projects can rely on.
- **A hospital-ready deployment system** — secured, audited, monitored, with a clear interface and a clear on-call plan.
- **A software product around a scientific method** — packaged, documented, marketed, used by people who did not write the paper.

The common thread: these artifacts have *users who are not the author*.

### Engineering practices that show up at this level

If your intermediate prototype used `requirements.txt` and a Makefile, your advanced system probably uses:

- A versioned package (PyPI, conda-forge, or private registry).
- A container image (Docker / Apptainer) and a tagged release.
- A CI pipeline that runs tests on every commit.
- A test suite — unit tests for the core functions, integration tests for the pipeline end-to-end.
- Configuration management that separates code from parameters.
- Logging and structured error reporting.
- A clear data contract (input shape, output shape, both validated).
- A deprecation policy when interfaces change.
- A documented release cadence.

None of these are R&D in itself. All of them are what advanced R&D looks like in practice. Without them, your method is a one-off claim; with them, it is something a community can build on.

### Documentation as deliverable

Documentation moves from *nice-to-have* to *one of the primary deliverables*:

- **User docs** — how a user runs the tool.
- **Developer docs** — how a contributor extends it.
- **Method docs** — how the science is explained for non-authors.
- **Validation docs** — what was tested, on what data, with what limitations.

These are not the same document. Advanced R&D usually needs all four.

## The team you become part of

Advanced development is rarely a one-person job. You start to depend on, and become responsible to:

- Domain experts who validate that your output is clinically meaningful.
- Data engineers who feed you clean, governed data.
- Other researchers who use your output as input.
- Users who file bug reports that are sometimes more valuable than your evaluation.

Your code stops being yours and starts being the team's. Plan accordingly.

## Common traps

- **Over-engineering.** Not everything needs Kubernetes. Match the complexity to the actual usage.
- **Under-engineering.** Putting "research code" in front of clinicians without basic safety, logging, or QC is unsafe.
- **Reinventing infrastructure.** Whatever your problem is, the data engineering for it has been solved by someone — usually badly, but solved. Reuse before you rebuild.
- **Skipping documentation.** Almost every advanced R&D system fails its second year because the original authors moved on and nothing was documented.

## Where to next

- [From scripts to systems](scripts-to-systems.md) — what the architectural shift looks like in more detail.
- [Mindset → Engineering](../mindset/engineering.md) — the engineering layer of the R&D mindset.
