# Doing development as a beginner

> Development is about **building something practical.**

At the beginner level, your goal is not a polished product. It is a small, working artifact that a friendly reviewer can read, run, and understand.

## What you actually do

### 1. Design

Before you write code, sketch the thing on paper or in a markdown file:

- What is the input? (A NIfTI file? A folder of subjects? A CSV?)
- What is the output? (A number? A plot? A report?)
- What is the *single function* that turns one into the other?

If you cannot describe the input, output, and core function in three lines, you are not ready to code yet.

### 2. Code

Pick the smallest thing that solves the problem. For a beginner-level biomedical project, that is almost always:

- A single Python script or notebook.
- Standard libraries you already know (`numpy`, `pandas`, `nibabel`, `matplotlib`).
- One or two well-known third-party tools called from the command line.

Resist:

- Premature abstraction (no class hierarchies for a 50-line script).
- Premature optimisation (correctness before speed).
- Premature configuration (hard-code defaults; pull them out later if you need to).

### 3. Test

For beginner work, "testing" usually means three things, in order:

1. **Run it end-to-end on one realistic input.** Does it produce output? Does the output look sane?
2. **Run it on an edge case.** What happens with a missing file, an empty image, a subject with one modality missing?
3. **Compare against ground truth or a known-good tool.** If you computed hippocampal volume, does FreeSurfer's number for the same subject roughly agree?

You do not need a `pytest` suite yet — but you do need to *do these checks*, even if just in a notebook cell.

### 4. Improve

After the first end-to-end run, you will see:

- One thing that is slow.
- One thing that is confusing.
- One thing that is wrong.

Pick the one that hurts the most. Fix it. Re-run. Move on.

Do **not** rewrite the whole thing. R&D at this level is about closing the loop, not about producing perfect code on the first pass.

### 5. Document

A beginner development artifact is "done" when it has:

- A **README** with three sections: *what it does*, *how to install it*, *how to run it*.
- An **example command** that a stranger could copy-paste.
- A **list of assumptions** — what data shape, what tools, what OS.

If a friend can clone your repo and reproduce your output in fifteen minutes, you have crossed the bar.

### 6. Deploy

"Deploy" at this level is **make it runnable somewhere other than your laptop**. That can be as simple as:

- A `requirements.txt` or `environment.yml` so anyone can recreate the environment.
- A short note about how to run it on the lab's HPC cluster, if relevant.
- A container (Docker or Apptainer) if the dependencies are messy.

You do not need a CI pipeline or a Kubernetes deployment. You need someone else to be able to run the thing.

### 7. Maintain

For a beginner project, maintenance is one habit: **when you change something, update the README.**

That is the entire contract for now. Larger maintenance practices come at the intermediate level.

## What good beginner development looks like

A small Python script that:

- Takes one input and produces one output.
- Has a README that says how to run it.
- Has been run on at least two different inputs.
- Has at least one sanity check against a known-good tool.
- Is in a git repo with a meaningful commit history (not one giant "initial commit").

That is enough. Anything beyond that is bonus.

## Where to next

- [Doing research as a beginner](research.md) — the other half of the loop.
- [Your first R&D project](first-project.md) — putting both halves together.
