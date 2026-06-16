# Biomedical AI — research questions

What does a strong biomedical AI research question look like? Six families that show up repeatedly, with examples.

## 1. Can AI detect disease earlier?

The earlier-detection question is the most common in screening and triage.

Examples:

- *Can a deep model on routine chest X-rays flag early-stage lung cancer years before clinical presentation?*
- *Can baseline structural MRI features predict conversion from MCI to Alzheimer's disease?*
- *Can a wearable signal predict atrial fibrillation onset hours before symptom onset?*

Strong versions of this question name the population (who is being screened), the timing (how much earlier), and the metric (sensitivity at clinically acceptable false-positive rates).

## 2. Can MRI biomarkers predict pathology?

The biomarker question is about non-invasively predicting something that today requires biopsy, surgery, or invasive monitoring.

Examples:

- *Can multi-parametric MRI features predict tumour IDH mutation status without biopsy?*
- *Can MRI-derived hippocampal asymmetry predict surgical pathology in hippocampal sclerosis?*
- *Can quantitative MRI predict tissue cellularity in glioma?*

Strong versions name the modality, the imaging feature class, the pathology, and the validation cohort. Honest versions name the limits — biomarkers rarely *replace* pathology; they triage who needs it.

## 3. Can EEG models localize seizure onset?

The localization question is about the spatial source of an electrophysiological phenomenon.

Examples:

- *Can scalp EEG features alone localize seizure onset zone with accuracy approaching intracranial monitoring?*
- *Can a transformer trained on routine 21-channel EEG detect interictal epileptiform discharges with sensitivity ≥ 0.85 at FPR ≤ 0.1?*
- *Can multimodal MRI + EEG fusion lateralise seizure onset better than either alone in MRI-negative patients?*

Strong versions specify the recording montage, the comparison standard (intracranial, surgical outcome), and the patient subgroup.

## 4. Can clinical notes predict outcomes?

The clinical-NLP question is about extracting predictive signal from free-text electronic health records.

Examples:

- *Can admission notes predict 30-day readmission risk better than structured features alone?*
- *Can pre-treatment oncology notes predict immunotherapy response?*
- *Can outpatient psychiatric notes flag patients at elevated suicide risk for follow-up?*

Strong versions handle privacy, demographic bias, and the fact that notes are *clinician-mediated* — they reflect the writer's attention as well as the patient's state.

## 5. Can genomics identify treatment response?

The genomics-AI question is about using molecular data to personalise treatment.

Examples:

- *Can tumour transcriptomic profiles predict response to checkpoint inhibitors?*
- *Can polygenic risk scores stratify patients for prevention trials?*
- *Can pharmacogenomic features predict adverse drug events?*

Strong versions name the ancestry distribution of the cohort, the validation strategy across cohorts, and the comparison to existing clinical predictors.

## 6. Can models generalize across hospitals?

The generalisation question is increasingly the most important one. It tests whether a model trained at one site survives deployment at another.

Examples:

- *Does a model trained on one hospital's MRI cohort maintain performance on a different hospital's cohort with different scanners?*
- *Can domain adaptation methods close the gap?*
- *What design choices make a model robust to scanner and protocol drift?*

This question is often the difference between an interesting paper and a deployable system. A PhD thesis can be built around it alone.

## What turns a question into a contribution

For any of these, a strong R&D question:

- Has a yes / no answer that someone would actually act on.
- Specifies the data, population, baseline, and primary metric.
- Defines the threshold where the answer changes from "no" to "yes."
- Is bounded — finishable in a defined time, on accessible data.
- Has a stake — yes or no would change what the field or a clinic does.

A question that fails any of these tests is not yet sharp enough to drive R&D.

## Where to next

- [Development outputs](development-outputs.md) — what you build when answering these questions.
- [R&D outputs](rd-outputs.md) — what counts as a finished contribution.
