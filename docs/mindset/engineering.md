# Engineering layer

> *Can we build it?*

The engineering layer is the layer that decides whether truth can be made operational. A finding that nobody can run is a finding that mostly stays in the paper.

## The five questions

### Is the system reliable?

- Does it produce the same output for the same input, every time?
- Does it fail loudly when inputs are bad, instead of silently producing nonsense?
- Does it have a clear failure mode when its assumptions are violated?

Unreliable systems get distrusted faster than they can be debugged.

### Is it reproducible?

- Can a stranger, given the code and a frozen dataset, get the same headline number?
- Are dependencies pinned, containers built, seeds set?
- Is the path from raw input to final figure runnable by one command?

Reproducibility is the lowest bar of credibility for engineering. Without it, every other claim is hearsay.

### Can others use it?

- Is there a clear interface (CLI, API, library)?
- Is there documentation a user can actually follow?
- Are there examples a stranger can copy-paste?
- Is there a place to ask questions and report bugs?

A system that only its author can run is not yet engineering. It is private craft.

### Can it scale?

- Does it still work on 10× the data?
- 100×?
- On HPC? On cloud?
- Does the cost grow sensibly with the workload?

Scale matters even at the research stage, because researchers run a lot of experiments.

### Can it be maintained?

- Can someone other than the author make a non-trivial change without breaking it?
- Is there a test suite that catches regressions?
- Is there a release process so changes are versioned?
- Is there a clear owner?

Maintenance is the long-tail cost. Projects that fail at this stage are usually projects that succeeded scientifically and then quietly rotted.

## Habits that strengthen the engineering layer

- **Containerise early.** Reproducibility gets exponentially harder later.
- **Pin everything.** Dependencies, container images, dataset versions, seeds.
- **Write tests as you go.** Even one or two integration tests per system catch most regressions.
- **Treat the README as a primary deliverable.** Update it whenever behaviour changes.
- **Use a CI pipeline.** It is the cheap insurance.
- **Refactor when the next change becomes painful**, not before.

## The biomedical version

In biomedical AI, the engineering layer has extra constraints:

- **PHI and consent** — code that touches patient data has data-handling requirements that recreational software does not.
- **Heterogeneous inputs** — DICOM, NIfTI, BIDS, EDF, CSV, free text, all under one roof.
- **Long runtimes** — single-subject pipelines can take hours; batching design matters.
- **Multi-site deployment** — what works in your lab may not work in another hospital's scanner / pipeline ecosystem.

These are not blockers. They are the part of the engineering layer that is biomedical-specific.

## When the engineering layer is weak

You see it in the work as:

- Code that runs once and is impossible to re-run.
- README files that are out of date or missing.
- Hard-coded paths to "/home/me/..."
- Versions of dependencies that conflict in confusing ways.
- Systems that fall over the moment input data is slightly different from what the author used.

Strengthen by treating engineering as a primary deliverable, not as overhead to be minimised.

## Where to next

- [Scientific layer](scientific.md) — what you build has to be grounded in truth.
- [Validation layer](validation.md) — whether what you built does what you claim.
