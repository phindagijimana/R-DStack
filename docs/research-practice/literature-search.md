# Searching the literature

> Finding the work that exists is the bottleneck step that no one teaches you and that quietly shapes the next two years of your project.

If you start a project without a literature search, you are guessing at the gap. If you start with a poor one, you are guessing at the gap with extra confidence. Both are worse than going slowly the first time.

## The right databases

Pick the right tool for the question:

- **[PubMed](https://pubmed.ncbi.nlm.nih.gov)** — the canonical biomedical database. Indexed by MeSH terms. Best for clinical and biological work.
- **[Google Scholar](https://scholar.google.com)** — broad coverage, citation counts, "cited by" tracing. Best for discovery and citation tracing.
- **[Semantic Scholar](https://www.semanticscholar.org)** — AI-summarised, links related work, often easier than Scholar for navigating an unfamiliar subfield.
- **[Connected Papers](https://www.connectedpapers.com)** — visual map of papers around a chosen seed paper. Excellent for "what else am I missing?"
- **[arXiv](https://arxiv.org)** / **[bioRxiv](https://www.biorxiv.org)** / **[medRxiv](https://www.medrxiv.org)** — preprints. Where the field actually is now, ahead of journal publication.
- **[Web of Science](https://www.webofscience.com)** — paid but excellent for systematic citation tracking and bibliometrics.
- **[Embase](https://www.embase.com)** — biomedical, complements PubMed especially for European literature and drug studies.
- **[OpenAlex](https://openalex.org)** — open, programmable index. Useful when you need to query the literature graph from code.

For a clinical biomarker question, PubMed + Scholar + Connected Papers is usually enough. For methods, add Semantic Scholar and arXiv.

## Query design

A well-constructed query saves you days. The principles are field-agnostic:

- **Use Boolean operators** explicitly: `AND`, `OR`, `NOT`.
- **Group synonyms with OR**: `"hippocampal sclerosis" OR "mesial temporal sclerosis"`.
- **Combine concepts with AND**: `("hippocampal sclerosis" ...) AND (MRI OR neuroimaging) AND (deep learning OR machine learning)`.
- **Use MeSH terms in PubMed** for canonical concept matching.
- **Limit by date**, study type, and species when noise is high.
- **Save the query** — searches need to be reproducible too, especially if you write a systematic review.

A search query is a research artifact. Treat it as one.

## Citation tracing

Two directions, both essential:

### Backward — read the citations *out of* a paper

- Pick a recent paper that is close to your question.
- Read its references section.
- Pull every reference that looks load-bearing.
- Read those, and so on, until you reach the foundational papers.

This finds the *history* of the question.

### Forward — read who cites the paper

- Use "Cited by" on Scholar, Web of Science, or Semantic Scholar.
- Look at recent papers that cite a foundational reference.
- See how the field has used it since.

This finds the *current state* of the question.

You are done when these two passes converge — when you keep meeting the same handful of papers from different directions.

## Citation chasing tools

- **Connected Papers** — start with a seed paper, see the graph neighborhood.
- **Inciteful** — multi-seed citation graph builder.
- **ResearchRabbit** — recommendation engine seeded by your library.
- **Litmaps** — visual citation graph with alerts.

These are not substitutes for reading. They are accelerators for *finding* what to read.

## Alerts and saved searches

After the initial search, you need to stay current. Set up:

- **PubMed saved searches** with email alerts on a weekly or monthly cadence.
- **Google Scholar alerts** on your key terms.
- **arXiv / bioRxiv subject-area RSS feeds**.
- **Author alerts** on three to five researchers whose work matters to you.
- **Journal table-of-contents alerts** for one or two key journals.

Run this for six months and your reading queue starts to predict what the field will care about next quarter.

## Knowing your journals

Every subfield has a stable of journals that matter. For biomedical AI:

- **Clinical**: *Lancet, New England Journal of Medicine, JAMA*.
- **Specialty (epilepsy/neurology)**: *Brain, Epilepsia, Neurology, Annals of Neurology*.
- **Neuroimaging**: *NeuroImage, Human Brain Mapping, Medical Image Analysis*.
- **AI methods**: *NeurIPS, ICML, ICLR, MICCAI* (conferences are first-tier here).
- **General science**: *Nature, Science, PNAS, Nature Medicine, Nature Methods*.

Knowing which journal a paper is in is part of evaluating its credibility, audience, and likely review depth.

## Predatory and low-quality outlets

Not every "journal" is a journal. A few signs to flag:

- Solicitation by email.
- Promise of fast review.
- Vague editorial board, missing affiliations.
- Pay-to-publish with no apparent peer review.
- Not indexed in PubMed, Web of Science, or DOAJ.

When in doubt, check **[DOAJ — Directory of Open Access Journals](https://doaj.org)** and **[Cabells Predatory Reports](https://www.cabells.com)** (or your library's equivalent).

## Systematic reviews

If your project is a *review of evidence* rather than new evidence, you cross into systematic-review territory:

- Pre-register the search and inclusion criteria (PROSPERO).
- Follow **[PRISMA](https://www.prisma-statement.org)** reporting guidelines from EQUATOR.
- Use two independent reviewers for screening.
- Use Covidence, Rayyan, or DistillerSR to manage the workflow.

Even if you are not writing a systematic review, knowing the standard makes your routine literature reviews more honest.

## A realistic cadence

- **Project start**: a two-to-three-week intensive search.
- **Ongoing**: thirty to sixty minutes per week scanning alerts.
- **Pre-submission**: a final sweep to catch papers published while you were writing.

Less than this and the work drifts. More than this and you stall.

## Where to next

- [A reading strategy](reading-strategy.md) — what to do with the papers you found.
- [Note-taking and references](note-taking.md) — where to put what you read.
- [Intermediate → Review existing knowledge](../intermediate/review-knowledge.md) — the gap-identification step that depends on the search.
