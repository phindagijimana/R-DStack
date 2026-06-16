# Biomedical AI — development outputs

What does development in biomedical AI actually produce? The eight artifact families that show up across most projects.

## 1. AI models

The headline artifact: a trained model that takes biomedical input and produces a prediction.

In practice, "the model" is usually:

- A trained weights checkpoint.
- A model architecture file (config or class definition).
- A preprocessing recipe that *must* match training.
- A postprocessing recipe (thresholds, calibration, aggregation).
- A reference inference script.

Real models in production are bundles. Shipping the checkpoint alone is rarely enough.

## 2. Data pipelines

Models are downstream of pipelines. The pipeline is what turns raw clinical data into model-ready features:

- **Ingestion** — DICOM, EDF, FASTQ, clinical text, lab values.
- **Conversion** — into a canonical form (BIDS for imaging, FHIR for clinical, parquet for tabular).
- **Quality control** — motion, dropout, signal quality, label consistency.
- **Preprocessing** — registration, normalisation, denoising, filtering.
- **Feature extraction** — when classical features are used.

Pipelines are often more complex and more load-bearing than the model itself.

## 3. Imaging workflows

For neuroimaging specifically, an imaging workflow is the orchestration of many preprocessing and analysis tools:

- Container-based (BIDS apps, Apptainer / Singularity).
- Orchestrated by Snakemake, Nextflow, or Makefiles.
- Run on HPC or cloud.
- Produces standardised derivatives.

Building good imaging workflows is its own engineering discipline. A small but well-built workflow can be a research contribution.

## 4. Clinical dashboards

When the audience is a human decision-maker, the model output usually lives behind a dashboard:

- Web-based, often React + FastAPI.
- Surfaces predictions, confidence, key features, comparisons to normative data.
- Logs every interaction so usage and overrides can be analysed.
- Designed to support — not replace — clinical judgment.

A good dashboard turns model output into a decision support tool. A bad one buries the signal.

## 5. Validation platforms

Validation at scale needs infrastructure. A validation platform:

- Holds the test datasets, with their splits frozen and versioned.
- Runs evaluation scripts reproducibly.
- Tracks performance over model versions.
- Produces validation reports automatically.

Mature labs and companies treat the validation platform as a first-class system, separate from the model itself.

## 6. Decision support tools

The full clinical artifact: a system that takes a patient's data, runs the right models, surfaces the right comparisons, and produces output a clinician can act on. Decision support tools include:

- The data ingestion path (often EHR integration).
- The model bundle.
- The dashboard.
- The audit log.
- The deployment surface (on-premises, cloud, edge).
- The clinical governance wrapping (training, monitoring, recall).

A decision support tool is a system, not a script.

## 7. APIs

When the consumer is another piece of software, the artifact is an API:

- A versioned REST or gRPC endpoint.
- A clear input schema (FHIR resource, BIDS-derivative file, DICOM SR).
- Authenticated and rate-limited.
- Documented with examples.

APIs are how biomedical AI artifacts get used by people who did not build them.

## 8. Reports and software packages

The lowest-friction outputs:

- A PDF report generator that turns a single subject's analysis into a one-page summary.
- A pip-installable Python package that exposes the core methods.
- A conda recipe for reproducible environments.
- A BIDS app for community use.

These are the outputs other researchers build on most easily — and the ones that drive citation impact for methods papers.

## How to pick which outputs to produce

Not every project needs all eight. Pick by audience:

- **The user is a clinician** — dashboard + report + decision support wrapper.
- **The user is another researcher** — pipeline + model bundle + Python package + documentation.
- **The user is a downstream system** — API + container + data contract.
- **The user is a regulator** — validation report + traceable lineage + version-controlled releases.

If you cannot name the user, you cannot pick the right output.

## Where to next

- [R&D outputs](rd-outputs.md) — what makes the combination of these artifacts a real R&D contribution.
- [Case study — hippocampal sclerosis](../case-studies/hippocampal-sclerosis.md) — these output types instantiated for one concrete problem.
