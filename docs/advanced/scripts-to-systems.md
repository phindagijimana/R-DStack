# From scripts to systems

This page is the architectural side of [Stronger development](stronger-development.md). When a piece of R&D becomes a system rather than a script, several specific things change.

## What a script is

A script is a piece of code that:

- Has one author.
- Runs on one machine.
- Is invoked manually.
- Operates on one or a few inputs.
- Produces one output.
- Has no users besides the author.
- Is owned in someone's home directory.

That is fine for prototyping. It is not fine when other people start depending on the output.

## What a system is

A system is a piece of code that:

- Has multiple users (and usually multiple maintainers).
- Runs on shared infrastructure (HPC, cloud, container platform).
- Is invoked by a contract (CLI, API, scheduler, message queue).
- Operates on many inputs continuously or on demand.
- Produces outputs that downstream systems consume.
- Has users besides the author.
- Lives in a versioned, governed repository.

The transition does not happen overnight. It happens when you start adding the pieces below.

## The pieces a script needs to become a system

### Interfaces

A script's "interface" is the function the author remembers. A system has a contract:

- A CLI with stable flags.
- Or an API with versioned endpoints.
- Input and output schemas (e.g., JSON Schema, Pydantic, BIDS).
- Documented behaviour at edge cases.

### Configuration

A script hard-codes paths. A system separates:

- **Defaults** — sensible values shipped with the code.
- **User configuration** — overrides for the operator.
- **Per-run parameters** — what changes between invocations.
- **Secrets** — credentials kept out of the repo.

A common pattern is a layered config: code defaults < repo config file < user config file < command-line flags.

### Data contracts

A script trusts whatever you give it. A system validates:

- The shape of each input.
- Required fields, optional fields, units.
- Acceptable ranges.
- File format and version.

Failure to validate is the single most common cause of "everything worked yesterday" bugs.

### Reproducibility

A script's reproducibility is "it worked when I ran it." A system's reproducibility is provable:

- Pinned dependencies.
- Container image with a digest.
- Locked random seeds for stochastic steps.
- Inputs identified by content hash, not by filename.
- Outputs annotated with the code commit, container digest, and input hashes that produced them.

This is the single biggest jump in engineering rigour from intermediate to advanced.

### Observability

A script writes to stdout. A system writes:

- Structured logs with severity and context.
- Metrics for run time, error rate, throughput.
- Traces for multi-step pipelines.
- Alerts when something the operator cares about happens.

You do not need a full observability stack on day one. You do need a deliberate answer to *"how would I know if this broke last night?"*

### Testing

A script is "tested" by running it once. A system has:

- Unit tests for pure functions.
- Integration tests for end-to-end paths on a fixture dataset.
- Regression tests for previously broken cases.
- Smoke tests for deployment health.

These do not have to be exhaustive. They have to exist and run automatically.

### Deployment

A script lives wherever the author left it. A system has:

- A release process (tag, build, publish).
- A documented install path for users (pip, container pull, BIDS app, helm chart).
- A clear policy for breaking changes.
- A path to roll back if a release is bad.

### Ownership

A script is owned by whoever last touched it. A system has:

- A maintainer (or team) named in the repo.
- An issue tracker that is actually triaged.
- A contributing guide.
- A clear answer to "what happens when the author leaves?"

That last question is the test of whether you have a system or just a script with extra dependencies.

## The cost of becoming a system

These pieces are real engineering work. They cost time that does not directly produce a new result. The temptation is to skip them and keep iterating.

Skip when:

- You are still proving the idea works.
- The user base is one person and that person is you.
- The artifact will be thrown away in a month.

Pay the cost when:

- Other people are starting to depend on outputs.
- The work is being published or shipped externally.
- The artifact is in front of clinicians or patients.
- The result needs to be reproducible by reviewers, regulators, or successors.

The mistake is paying the cost too early (over-engineering a prototype) or too late (failing to harden an artifact that has become load-bearing). Advanced R&D is largely about reading that timing correctly.

## Where to next

- [Mindset → Engineering](../mindset/engineering.md) — the broader engineering layer of R&D.
- [PhD level → Rigor](../phd/rigor.md) — the rigour layer, which is what makes the system worth deploying.
