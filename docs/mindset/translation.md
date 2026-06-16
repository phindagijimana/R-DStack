# Translation layer

> *Does it matter in the real world?*

The translation layer is the layer that decides whether the work changes anything outside the lab. It is the layer most researchers find unfamiliar — and the one most often missing in projects that produce strong science but no impact.

## The five questions

### Who needs it?

- The actual humans who will use, depend on, or be affected by this work.
- Their role, their workflow, their constraints, their existing tools.
- Whether they are aware they need it, or have grown to accept the status quo.

If you cannot name a real person and a real task, the work does not yet have a translation path.

### Does it improve workflow?

- Does it remove a step, speed up a decision, or reduce an error rate?
- Compared to what currently happens?
- Measurably?

A model whose output is interesting but does not change what anyone does is research, not translation.

### Does it help clinicians or researchers?

- Does it surface something they could not see before?
- Does it confirm something they suspected but could not act on?
- Does it reduce a cognitive load they were carrying silently?

The honest version of this question is *"would they choose to use it next week if you handed it to them today?"*

### Can it be deployed?

- Where will it run? Hospital, cloud, edge device, web tool?
- Who will install and maintain it?
- What does it need from the environment (compute, data access, integrations)?
- What regulatory or governance work is needed before it can be deployed?

A method that requires conditions nobody has is not yet translatable.

### Can it become a product?

- Is there an organisation that would build, maintain, and distribute it?
- A startup? A hospital IT team? An open-source community? A commercial vendor?
- Who pays for it? Who is accountable when it fails?
- What is the long-term home?

Not every project needs to become a product. But every project should have a serious answer to *"who maintains this in three years?"*

## Habits that strengthen the translation layer

- **Spend real time with users.** A day in the clinic is worth a month of literature review for this layer.
- **Build prototypes that users can hold.** A working demo elicits feedback that a paper does not.
- **Talk to the people who would deploy it.** IT, clinical informatics, vendors. Their constraints define the deployment surface.
- **Plan for regulatory paths early.** If the work needs FDA clearance someday, design with that in mind from the start.
- **Track usage when you ship.** Logs, surveys, follow-up conversations. What people actually do with the output is the ground truth.

## The biomedical version

In biomedical AI, translation has a specific shape:

- **Regulatory** — Software-as-a-Medical-Device (SaMD), FDA 510(k), CE marking under MDR, ISO 13485 quality systems.
- **Integration** — PACS, EHR, FHIR, hospital security and identity systems.
- **Reimbursement** — for products, the path from CPT code to insurance coverage.
- **Adoption** — whoever pays for it is not the same as whoever uses it, who is not the same as whoever benefits from it. The translation layer has to satisfy all three.

These are not afterthoughts. They are constraints that determine which research directions are translatable.

## When the translation layer is weak

You see it in the work as:

- Strong publications with no adoption.
- Demos that look great in a slide but do not survive a hospital's network.
- Tools that the authors run but nobody else does.
- Validation that is technically rigorous but missing the questions a deployer would ask.
- A research roadmap with no plan for who picks up the work after the paper.

Strengthen by spending time with users early, defining the deployment surface explicitly, and treating translation as a research output rather than as something that happens after research ends.

## Where to next

- Back to [Mindset → index](index.md) to revisit all four layers.
- [PhD level → Contribution](../phd/contribution.md) — contribution is largely about translation done well.
- [Biomedical AI](../biomedical-ai/index.md) — the field-specific application of all four layers.
