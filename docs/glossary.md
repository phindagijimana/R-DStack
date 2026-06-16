# Glossary

Definitions of terms used across this hub. Where definitions vary between communities, the meaning given is the one intended in this hub.

---

**Advanced R&D**
: The stage where you create new systems, methods, or products that solve important problems better than existing approaches. See [Growth path → Advanced](growth-path/advanced.md).

**Aims page**
: The one-page Specific Aims section of an NIH grant, generally considered the single most important page in the application. See [Research practice → Grant writing](research-practice/grant-writing.md).

**APC (Article Processing Charge)**
: The fee an author pays for gold open-access publication, typically $1,500–$11,000 depending on journal.

**ICMJE authorship criteria**
: The four-part definition of authorship (substantial contribution, drafting/revising, final approval, accountability) maintained by the International Committee of Medical Journal Editors. See [Research practice → Ethics and IRB](research-practice/ethics-and-irb.md).

**Baseline**
: A reference method against which a new method is compared. A *strong* baseline is the current best published method, re-run on the same data with the same evaluation protocol. A *weak* baseline is a strawman that makes the new method look better than it is.

**Beginner R&D**
: The stage where you learn the field's concepts and produce a small end-to-end artifact. See [Growth path → Beginner](growth-path/beginner.md).

**BIDS** (Brain Imaging Data Structure)
: A specification for organising neuroimaging data so that pipelines and tools can find and consume it consistently. The de facto standard for sharable neuroimaging datasets.

**Biomarker**
: A measurable indicator of a biological state or condition. In biomedical AI, often a quantity derived from imaging, electrophysiology, or omics that correlates with pathology, prognosis, or treatment response.

**Calibration**
: The property that a model's predicted probabilities match the empirical rates of the predicted event. A model can have high discrimination (AUC) and poor calibration.

**Confound**
: A variable that correlates with both the input and the outcome of interest and thereby distorts the apparent relationship between them. In biomedical AI, common confounds include scanner, site, age, sex, and acquisition era.

**COPE**
: Committee on Publication Ethics. The canonical body for publication-integrity guidance, including flowcharts for plagiarism, duplicate publication, conflicts of interest, and authorship disputes. See <https://publicationethics.org>.

**CONSORT**
: Reporting guideline for randomised controlled trials, maintained by the EQUATOR Network.

**CSL (Citation Style Language)**
: The XML format used by Zotero, Mendeley, Paperpile, and Pandoc to render citations in thousands of journal styles. See [Research practice → Note-taking and references](research-practice/note-taking.md).

**Contribution**
: At PhD level, the thing your work gives the field — a paper, tool, dataset, method, framework, or biomarker — that someone else can use, build on, or argue with. See [PhD → Contribution](phd/contribution.md).

**Cross-validation**
: A resampling procedure where the dataset is split into multiple train / test folds to estimate performance variance. Important note: cross-validation by sample can leak across subjects, sites, or sessions; in biomedical data, split *by subject* or *by site*.

**Data contract**
: A documented specification of the shape, types, units, and acceptable ranges of inputs and outputs between two components of a system. Surfaces silent data-shape bugs at the boundary instead of deep in downstream code.

**Decision support tool**
: A clinical artifact that surfaces information to a human decision-maker (often a clinician) to support, not replace, their judgment. Distinct from "autonomous AI" both technically and regulatorily.

**Depth**
: At PhD level, the quality of understanding the problem and field more deeply than the people you are talking to about it. See [PhD → Depth](phd/depth.md).

**Development**
: The part of R&D that asks *"what can we build?"* Outputs are tools, systems, products, and workflows.

**Discrimination**
: A model's ability to separate positives from negatives. Often summarised by AUC. Distinct from calibration.

**EQUATOR Network**
: Enhancing the QUAlity and Transparency Of health Research — the umbrella organisation maintaining reporting guidelines (CONSORT, STROBE, TRIPOD+AI, PRISMA, and many others). See <https://www.equator-network.org>.

**External validation**
: Evaluation of a model on data the model has never seen and the analyst has never opened — ideally from a different site, scanner, or population. The single biggest separator between published-only and deployable systems.

**Falsifiability**
: The property of a hypothesis that some possible result would refute it. Introduced by Karl Popper as the demarcation between science and non-science. See [Research practice → Scientific method](research-practice/scientific-method.md).

**Failure analysis**
: A study of the cases a model gets wrong, looking for patterns by demographic, scanner, modality quality, or label noise. Often more informative than the success cases.

**FreeSurfer**
: A widely used open-source toolkit for structural MRI analysis, including cortical reconstruction, regional volumetry, and hippocampal subfield segmentation.

**Hippocampal sclerosis**
: The most common pathology in temporal-lobe epilepsy, characterised by neuronal loss and gliosis in the hippocampus. Often associated with hippocampal atrophy and asymmetry on MRI. Used as the running case-study problem in this hub.

**HippUnfold**
: An open-source tool that unfolds the hippocampus into a surface representation and segments its subfields. An alternative to FreeSurfer's hippocampal segmentation.

**HIPAA**
: U.S. Health Insurance Portability and Accountability Act. Defines the 18 identifiers that must be removed (or covered by a Limited Data Set + DUA) before protected health information can be shared.

**IMRaD**
: Introduction, Methods, Results, and Discussion — the dominant structure of a scientific paper. See [Research practice → Anatomy of a scientific paper](research-practice/paper-anatomy.md).

**IRB (Institutional Review Board)**
: The committee that reviews and approves research involving human subjects before the work begins. See [Research practice → Ethics and IRB](research-practice/ethics-and-irb.md).

**IACUC**
: Institutional Animal Care and Use Committee. The animal-research equivalent of the IRB.

**Impact factor**
: A bibliometric proxy for a journal's average citation rate. A coarse signal of reach; widely abused as a measure of paper or author quality.

**Independence**
: At PhD level, the ability to define and lead a research direction yourself rather than executing one given to you. See [PhD → Independence](phd/independence.md).

**Intermediate R&D**
: The stage where you improve existing work and build reproducible systems with documentation and evaluation. See [Growth path → Intermediate](growth-path/intermediate.md).

**Junior R&D**
: The stage where you reproduce existing work, learn the field's tooling, and understand limitations through hands-on practice. See [Growth path → Junior](growth-path/junior.md).

**Mechanism**
: The causal process underlying a phenomenon. In biomedical AI, often the biological / clinical reason a biomarker correlates with an outcome. Mechanistic claims are more durable than purely predictive ones.

**Mindset (the four layers)**
: Scientific, engineering, validation, translation. The four perspectives that R&D requires running simultaneously. See [Mindset](mindset/index.md).

**Open access**
: Publishing models where the published paper is free to read. Variants: *gold* (journal makes it free; author pays APC), *green* (author self-archives an accepted manuscript), *diamond* (free to read and to publish).

**Originality**
: At PhD level, the quality of contributing something the field did not have — a new hypothesis, method, dataset, benchmark, workflow, insight, or validation study. See [PhD → Originality](phd/originality.md).

**Peer review**
: The process by which experts evaluate a manuscript or grant application before publication or funding. See [Research practice → Peer review](research-practice/peer-review.md).

**Predatory journal**
: A pay-to-publish outlet that solicits submissions, promises rapid review, and lacks meaningful peer review. Check DOAJ and Cabells to vet.

**Preprint**
: A manuscript posted publicly before peer review, typically on arXiv, bioRxiv, or medRxiv. See [Research practice → Preprints and publishing](research-practice/preprints-and-publishing.md).

**PRISMA**
: Reporting guideline for systematic reviews and meta-analyses.

**Pre-registration**
: Writing down the analysis plan before looking at the data, protecting against post-hoc storytelling. Can be formal (OSF, AsPredicted) or informal (a dated, unchanged document in the repo).

**Prototype**
: A working version of the idea that runs end-to-end on realistic input and produces a real output that can be evaluated. Distinct from a "system," which has users, reproducibility, and maintenance.

**R&D (Research & Development)**
: The disciplined process of creating new knowledge and turning it into useful solutions, tools, products, methods, or systems. The combination of research and development with the explicit intent that each feeds the other.

**Research**
: The part of R&D that asks *"what is true?"* Outputs are knowledge, evidence, papers, and findings.

**Reference manager**
: Software that stores citations, attached PDFs, and tags — and inserts formatted citations into manuscripts. Zotero, Paperpile, EndNote, Mendeley. See [Research practice → Note-taking and references](research-practice/note-taking.md).

**Reporting guideline**
: A structured checklist for what to include in a publication of a given study type. See EQUATOR.

**Research question**
: A specific, answerable, falsifiable, bounded, and worth-answering question that drives a project. See [Intermediate → Research question](intermediate/research-question.md).

**Resubmission**
: The (usually) one allowed second submission of an NIH grant after an unfunded review, with an introduction addressing prior reviewer concerns.

**Rigor**
: At PhD level, the quality of proving a claim carefully enough that experts cannot dismiss it. Includes strong study design, correct statistics, proper baselines, reproducibility, error analysis, sensitivity analysis, bias analysis, and external validation. See [PhD → Rigor](phd/rigor.md).

**Sensitivity analysis**
: Investigating how a result changes under reasonable alternative analytic choices (preprocessing, model size, threshold, etc.). Evidence that a finding is not an artifact of one set of arbitrary decisions.

**Site effect**
: A systematic difference in data caused by the institution or scanner where it was collected. A frequent confound in multi-site biomedical AI.

**Specific Aims**
: The one-page section opening an NIH grant application that summarises the importance, gap, hypothesis, aims, and innovation. See [Research practice → Grant writing](research-practice/grant-writing.md).

**STROBE**
: Reporting guideline for observational studies, maintained by the EQUATOR Network.

**Subgroup analysis**
: Reporting performance separately for clinically or demographically meaningful subgroups. Important for surfacing bias and for clinical safety.

**System**
: Software that has users beyond its author, runs on shared infrastructure, has clear interfaces and reproducibility, and is maintained. Distinct from a script. See [Advanced → From scripts to systems](advanced/scripts-to-systems.md).

**Translation**
: The activity of moving R&D output into the real world — into clinical workflows, products, deployments, or community adoption. The fourth layer of the R&D mindset. See [Mindset → Translation](mindset/translation.md).

**TRIPOD+AI**
: Reporting guideline for prediction-model studies, including those that use AI. Required reading for biomedical AI authors. See <https://www.tripod-statement.org>.

**Validation**
: The activity of demonstrating that a built thing does what is claimed. Distinct from training (fitting parameters) and testing (a single held-out evaluation). See [Mindset → Validation](mindset/validation.md).
