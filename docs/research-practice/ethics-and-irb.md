# Ethics and IRB

> Research ethics is not a compliance ritual. It is what keeps your work credible — and what keeps people from being harmed by it.

This page covers human-subjects review (IRB), animal-subjects review (IACUC), data sharing, authorship and publication ethics, and conflicts of interest. The standard you should hold yourself to is *higher* than what the institutional minimum requires.

## Institutional review

### IRB — Institutional Review Board

In the U.S., any research involving human subjects requires IRB approval *before* the research begins. The IRB exists to:

- Verify that risks to participants are minimised.
- Verify that risks are reasonable in relation to anticipated benefits.
- Ensure informed consent.
- Protect vulnerable populations.
- Ensure equitable subject selection.
- Ensure adequate provisions for privacy and data security.

Even retrospective work on de-identified clinical data usually requires IRB review (often as exempt or expedited).

Categories you will encounter:

- **Exempt** — minimal-risk research with limited oversight (e.g., analysis of fully de-identified existing data).
- **Expedited** — minimal-risk research with formal review.
- **Full board** — anything else.

Plan submission time into your project timeline. A first IRB submission can take six to twelve weeks; revisions add more.

### IACUC — Institutional Animal Care and Use Committee

If your work involves vertebrate animals, an IACUC protocol is required. The principles (the "3 Rs"):

- **Replacement** — use non-animal alternatives where possible.
- **Reduction** — use the minimum number of animals needed.
- **Refinement** — minimise pain and distress.

Like IRB, IACUC has timelines. Plan ahead.

### International equivalents

- **Europe** — REC / Research Ethics Committees, plus GDPR for data.
- **UK** — HRA and NHS RECs.
- **Canada** — TCPS 2 and REBs.
- Each country has its own specifics; your institution's research office knows them.

## Informed consent

Consent is more than a form. It includes:

- A clear explanation of the study purpose and procedures.
- Risks and benefits.
- Alternatives to participation.
- Voluntariness and the right to withdraw.
- Confidentiality protections.
- Contact for questions.

Special considerations apply to:

- Children (assent + parental consent).
- Cognitively impaired adults (proxy consent).
- Pregnant women, prisoners, students of the investigator (vulnerable populations).
- Genomic data (broad consent and re-contact provisions).

For AI / ML projects that re-use existing clinical data, **secondary-use consent** is a frequent issue. Your IRB will tell you which form of consent or waiver applies.

## Data sharing and privacy

Open data is the default expectation; protecting privacy is the constraint.

### HIPAA (U.S.)

For protected health information:

- **Identifiers must be removed** or the data must be released under a Limited Data Set with a Data Use Agreement.
- **The 18 HIPAA identifiers** include obvious things (name, MRN) and less obvious things (full-face photographs, biometric identifiers, dates more precise than year).
- **De-identification** can be either *Safe Harbor* (remove the 18 identifiers) or *Expert Determination* (statistical re-identification risk assessment).

### GDPR (EU)

Even broader. Health and genetic data are *special category* under Article 9 — requiring explicit consent or another specific legal basis.

### Practical data-handling rules

- **Use the minimum data necessary** for the analysis.
- **Store identifiers separately** from analytic data, behind separate access controls.
- **Use institutional secure storage** (HIPAA-aligned cloud or on-premises).
- **Audit access logs.**
- **Have a data destruction plan** that matches your IRB protocol.

### Data sharing repositories

When the IRB allows:

- **[OpenNeuro](https://openneuro.org)** — neuroimaging.
- **[PhysioNet](https://physionet.org)** — clinical signals (credentialed access).
- **[dbGaP](https://www.ncbi.nlm.nih.gov/gap)** — genomics (controlled access).
- **[ImmPort](https://www.immport.org)** — immunology.
- **[Zenodo](https://zenodo.org)** / **[OSF](https://osf.io)** — generic, supports DOIs.

Public-access plans (PAPs) and data-management plans (DMPs) are now standard with most grants — start them at proposal time.

## Authorship — the ICMJE criteria

The International Committee of Medical Journal Editors defines a working definition of authorship that journals widely adopt:

> 📚 **[ICMJE Recommendations](https://www.icmje.org)**

All four must hold to be a listed author:

1. **Substantial contributions** to conception/design, OR acquisition/analysis/interpretation of data.
2. **Drafting or critically revising** the work for important intellectual content.
3. **Final approval** of the version to be published.
4. **Agreement to be accountable** for all aspects of the work.

People who do not meet all four should be acknowledged but not listed as authors. Common cases:

- A clinician who provided data but did not review the manuscript → acknowledgment.
- A senior PI who funded the work but did not engage with the science → not an author.
- A student who ran scripts under direction but did not draft, revise, or approve → not an author.

The author list is a statement of responsibility, not a courtesy list.

## Publication ethics — COPE

The Committee on Publication Ethics is the canonical body for navigating publication-integrity questions:

> 📚 **[COPE — Committee on Publication Ethics](https://publicationethics.org)**

COPE flowcharts and case studies cover:

- Plagiarism and self-plagiarism.
- Duplicate or salami publication.
- Authorship disputes.
- Ghost / guest / gift authorship.
- Conflicts of interest.
- Data fabrication and falsification.
- Image manipulation.
- Retractions and corrections.

When you face a borderline case, COPE's flowchart almost certainly addresses it.

## Conflicts of interest

A conflict of interest is **any relationship that could bias your work or its interpretation**. It does not require wrongdoing — it requires disclosure.

Common COIs in biomedical AI:

- Equity in a company whose product the work could affect.
- Consulting income from a company in the area.
- Patent applications or licenses tied to the methods.
- Grant funding from an entity that has a stake in the outcome.

Disclosing does not bar you from doing the work in most cases. Failing to disclose does.

## Reporting integrity — EQUATOR

Many published failures of integrity are honest failures of *reporting* — not enough detail, missing baselines, vague methods. The reporting guidelines on EQUATOR exist specifically to make integrity tractable:

> 📚 **[EQUATOR Network — Reporting Guidelines](https://www.equator-network.org)**

Use them. Reviewers do.

## Generative AI in research

A rapidly moving area. Current consensus from major venues and publishers (as of 2025–2026):

- **Disclose use** of generative AI in writing, analysis, or figure generation.
- **AI tools are not authors** — they cannot consent to ICMJE criteria 3 and 4.
- **Authors remain fully responsible** for everything the manuscript contains.
- **Confidential review material** must not be fed to external AI tools (see COPE).

Specific policies vary; check the journal.

## When something goes wrong

If you discover an error in your own published work:

- **Correct it.** Contact the journal for an erratum or correction notice.
- **For substantive errors** that invalidate the conclusions, request a retraction.

If you discover misconduct by a collaborator:

- **Do not handle it alone.** Talk to your institution's research integrity office.
- **Document what you saw and when.**
- **COPE flowcharts cover** what to do as an author, reviewer, or editor.

## Further reading

- **[ICMJE Recommendations](https://www.icmje.org)** — authorship, conflicts, responsibilities.
- **[COPE](https://publicationethics.org)** — publication ethics flowcharts and case studies.
- **[EQUATOR Network](https://www.equator-network.org)** — reporting guidelines.
- **[NIH Office of Research Integrity](https://ori.hhs.gov)** — U.S. federal guidance on research integrity.
- *On Being a Scientist: A Guide to Responsible Conduct in Research* — National Academies Press. Free PDF, short, widely assigned.
- *Making the Right Moves: A Practical Guide to Scientific Management* — HHMI. Free PDF, especially the chapter on mentorship and lab culture.

## Where to next

- [Peer review](peer-review.md) — where many of these standards land in practice.
- [Mindset → Translation](../mindset/translation.md) — translation work introduces its own regulatory layer (FDA / CE).
- Back to [Research practice → index](index.md) to see how ethics interconnects with the rest of the section.
