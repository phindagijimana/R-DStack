# R&D vs Research vs Development

The three terms are often used interchangeably. They are not the same thing.

## Side-by-side

| Concept     | Main question                                       | Output                                    |
|-------------|-----------------------------------------------------|-------------------------------------------|
| Research    | What is true?                                       | Knowledge, evidence, paper                |
| Development | What can we build?                                  | Tool, system, product, workflow           |
| R&D         | How do we discover and build something useful?      | New knowledge **plus** usable solution    |

The point of the table is the *output column*. If you finish a project and only the first two cells are filled, you did either research or development — not both. R&D requires both outputs.

## Worked example — hippocampal sclerosis on MRI

The same problem, asked three ways:

### Research

> *Does hippocampal asymmetry identify hippocampal sclerosis?*

**Outputs:**

- Statistical analysis (e.g., asymmetry index per group, ROC curve).
- A paper or report.
- Biomarker evidence.

### Development

> *Can we build a tool that calculates hippocampal asymmetry from MRI?*

**Outputs:**

- A software pipeline (segmentation → asymmetry computation).
- A user interface or CLI.
- A report generator.

### R&D

> *Can we create and validate a clinically useful MRI-based tool for hippocampal sclerosis detection?*

**Outputs:**

- Scientific evidence (the research piece).
- A working AI / biomarker workflow (the development piece).
- A validation study showing it generalises.
- A clinical decision support prototype.

The R&D version is what a PhD-level researcher in biomedical AI is asked to produce. The other two are stepping stones on the way there.

## What counts as "useful"?

"Useful" is doing a lot of work in the R&D definition. It usually means at least one of:

- **Clinically useful** — it changes what a clinician can do or decide.
- **Scientifically useful** — it lets other researchers ask a question they could not ask before.
- **Operationally useful** — it lets a team or hospital do something faster, cheaper, or more reliably.

A finding that nobody can act on is research, not R&D. A tool that does not rest on evidence is development, not R&D.

## Where to next

- [Beginner](../beginner/index.md) — what doing R&D looks like at the entry level.
- [R&D mindset](../mindset/index.md) — the four layers (scientific, engineering, validation, translation) that keep R&D honest.
