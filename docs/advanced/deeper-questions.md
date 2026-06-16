# Asking deeper questions

At the advanced level, you stop asking *"can I build this?"* and start asking the questions that determine whether building it is worth anything.

## The seven questions

These are not asked in sequence. They are weighed constantly against each other throughout the work.

### 1. What is the unmet need?

Who actually needs this and is not getting it today? If the answer is "no one," stop. If the answer is "me," that is a red flag worth examining — is the need real, or are you scratching your own itch?

The most credible unmet needs are:

- Articulated by someone in the target role (a clinician, an oncologist, an EEG technologist).
- Quantifiable (time, cost, error rate, miss rate).
- Persistent (not solved last year by a paper you missed).

### 2. What is scientifically unknown?

Where is the genuine knowledge gap? "Nobody has applied X to Y" is rarely a genuine gap unless you can also say *why* it has not been applied and *what would change if it were*.

The most credible scientific unknowns are:

- Pointed at by multiple recent reviews.
- Acknowledged by senior people in the field.
- Connected to a mechanism you can argue about, not just a missing data point.

### 3. What is technically possible?

What can current methods, compute, and data actually support? An idea is not advanced R&D if it requires technology that does not exist yet — that is research toward technology, which is a different scope.

Test: *can you sketch a method, with current tools, that has a reasonable chance of working?* If no, the project is too early; come back when the tooling has caught up.

### 4. What is clinically useful?

For biomedical AI specifically: does any of this change what a clinician can do or decide?

- Does it improve a decision (diagnosis, prognosis, treatment selection)?
- Does it speed up a workflow (segmentation, reporting, triage)?
- Does it reduce a risk (missed diagnosis, unnecessary treatment)?

If you cannot trace a clear line from your output to a clinical decision, the work is research, not translational R&D.

### 5. What is commercially viable?

Not every project needs to be a product. But for projects that are products, ask:

- Who would pay for this?
- What is their alternative?
- What is the regulatory path?
- What is the deployment surface (hospital, cloud, edge device)?

A no-money-attached version of this question is: *who would maintain this in three years?* Maintenance is the long-term proxy for viability.

### 6. What is ethically acceptable?

- Does the data have informed consent for this use?
- Does the model encode demographic biases that would harm patients?
- Is the deployment surface one where errors are recoverable?
- Are you accountable for failure modes you cannot detect?

The honest version of "is this ethical?" is *"if this fails, who gets hurt, and how do we know?"*

### 7. What can be validated and trusted?

Validation is what turns *"my model has AUC 0.84 on a held-out split"* into *"this biomarker is reliable enough for someone to make a decision with."*

The validation question forces you to think about:

- External datasets.
- Multi-site studies.
- Calibration, not just discrimination.
- Subgroup performance.
- Drift over time.
- Failure mode characterisation.

If you cannot validate it, you cannot ship it as advanced R&D — at best it is interesting research.

## Using the seven questions

At the start of a project, walk through the list once. If you cannot answer three or more of them, refine the project until you can.

During the project, revisit the list quarterly. The answers will change as you learn — most often, "what is clinically useful" sharpens and "what is technically possible" widens.

At the end of the project, present each answer as part of how you communicate the work. Reviewers will weigh these questions whether you address them or not; addressing them explicitly buys credibility.

## Where to next

- [Deeper research](deeper-research.md) — what asking these questions does to your reading and analysis practice.
- [Stronger development](stronger-development.md) — what it does to what you build.
