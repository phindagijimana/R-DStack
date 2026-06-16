# Note-taking and reference management

> Notes you take today are the citations you reach for in three years. Build the system once, then trust it.

The point of taking notes is not to copy the paper. It is to record *your own thinking about the paper* in a form your future self can search, cite, and compose into something new.

## Reference managers

Pick one and live in it. Switching costs are real; reasonable choices are all good enough.

- **[Zotero](https://www.zotero.org)** — free, open source, plugin ecosystem, generous storage tier. The most common choice in academia.
- **[Mendeley](https://www.mendeley.com)** — free, owned by Elsevier, integrated with their literature graph. Adequate.
- **[Paperpile](https://paperpile.com)** — paid, browser-first, very good Google Docs integration. Popular among clinicians and ML researchers.
- **[ReadCube Papers](https://www.papersapp.com)** — paid, polished UI, good annotation tools.
- **[EndNote](https://endnote.com)** — paid, dominant in many medical schools through institutional licenses.

Whichever you pick, it should do four things:

1. Capture metadata from a browser button.
2. Attach the PDF.
3. Sync across devices.
4. Export BibTeX, RIS, and a citation style language (CSL) of your choice.

If your tool does fewer than three of these, switch.

## A citation database that compounds

The point of a reference manager is not just to format citations. It is to be your *personal literature database*, query-able years later. To get there:

- Save every paper you read into the manager, not just the ones you currently cite.
- Tag aggressively (`hippocampus`, `epilepsy`, `MRI`, `external-validation`, `weak-baseline`).
- Use folders for active projects.
- Sync the attached PDFs.
- Back it up.

After two or three years of this discipline, you have a private database that beats any open one for your specific area.

## PDF annotation workflows

Reading and note-taking are easier together:

- **Highlight inside the reference manager's PDF viewer** so highlights are persistent and searchable. Zotero, Paperpile, ReadCube all support this.
- **Use colour with meaning**: e.g., yellow = key finding, green = method detail, red = doubt or pushback.
- **Write margin notes in your own words**, not quoted text.
- **Export the highlights** periodically to your notes app.

## Knowledge management apps

A second-brain app holds your *synthesis* — your understanding of the field, not just per-paper notes:

- **[Obsidian](https://obsidian.md)** — local-first, plain markdown, plugin ecosystem. Strong support for `[[wikilinks]]` between notes. The most flexible.
- **[Notion](https://www.notion.so)** — block-based, collaboration-friendly, weaker on backlinks.
- **[Logseq](https://logseq.com)** — outline-first, daily-journal-oriented.
- **[Tana](https://tana.inc)** — newer, supersedes outliner-style apps.
- **[Roam Research](https://roamresearch.com)** — the app that popularised backlinks; smaller community now.

Two principles regardless of tool:

1. **One note per concept**, not one per paper. Concept notes pull citations from multiple papers and let your understanding deepen over time.
2. **Backlinks beat folders.** Concepts connect to each other; folders force a single hierarchy.

## A simple note structure

For each paper, a per-paper note. For each idea, a concept note. The per-paper note is short:

```
# Smith et al. (2023) — Hippocampal subfields predict outcome

- Question: Do subfield volumes predict surgical outcome?
- Sample: N=120, single-site, 3T.
- Method: FreeSurfer subfields → logistic regression with cross-validation.
- Result: AUC 0.78 [0.69-0.86].
- Strengths: clear pre-registration; subfield-level analysis.
- Weaknesses: single-site; no external validation; cohort heavily right-handed.
- Cite for: subfield biomarker prior work, baseline AUC for comparison.
- Links: [[hippocampal asymmetry]], [[external validation]], [[FreeSurfer subfields]]
- Zotero key: smithHippocampalSubfields2023
```

That note is searchable, citable, and feeds your concept notes.

The concept note is the long-form view: *what do I now believe about hippocampal asymmetry, and which papers do I cite for each part of that belief?*

## Cite-while-you-write

When drafting a paper or grant, do not stop to find citations — drop the reference manager's key inline and let the citation processor render them at compile time:

- **LaTeX**: BibTeX or BibLaTeX with `\cite{smithHippocampalSubfields2023}`.
- **Word**: the Zotero / EndNote / Paperpile add-in.
- **Google Docs**: Paperpile or Zotero plugins.
- **Markdown / Pandoc**: `[@smithHippocampalSubfields2023]` with a CSL.

This discipline keeps writing flow uninterrupted and makes journal-format swaps trivial.

## Citation styles

Different journals require different formats. The Citation Style Language (CSL) repository — used by Zotero, Mendeley, Paperpile, Pandoc — supports thousands of styles. Save yourself the future scramble by attaching a CSL to your manager and *never* hand-formatting bibliographies.

## Backing up the database

Reference manager databases include years of work. Treat them as you would code:

- Sync to cloud (Zotero Storage, Google Drive, iCloud).
- Periodic local export of the BibTeX file into a git-tracked notes repo.
- A second sync target as a hedge.

## Further reading

- *Tiago Forte, "Building a Second Brain"* — the popular framing for personal knowledge management. Useful as a model even if you do not adopt the full system.
- The Zotero documentation — practical, complete, free.
- *Obsidian for Academics* — community-maintained guides.

## Where to next

- [A reading strategy](reading-strategy.md) — what to read.
- [Writing fundamentals](writing-fundamentals.md) — what to do with your notes.
- [Paper writing process](paper-writing-process.md) — citation workflow in a real manuscript.
