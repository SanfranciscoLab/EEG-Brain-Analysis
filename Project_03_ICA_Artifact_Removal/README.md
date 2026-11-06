# Project 03 — EEG Quality Control and ICA-Based Artifact Exploration

## 1. Overview

This project demonstrates EEG quality control and Independent Component Analysis (ICA) using MNE-Python.

The workflow includes EEG channel inspection, electrode position assignment, ICA decomposition, suspected artifact assessment, and signal comparison before and after component exclusion.

## 2. Objectives

- Perform EEG data quality assessment.
- Assign standard electrode locations.
- Apply FastICA decomposition.
- Inspect and assess potentially artifact-related components.
- Compare EEG signals before and after ICA component exclusion.
- Validate and save the processed EEG dataset.

## 3. Dataset

| Property | Value |
|---|---:|
| EEG channels | 64 |
| Sampling rate | 160 Hz |
| Recording duration | 124.994 seconds |
| ICA components | 28 |
| ICA method | FastICA |
| Electrode montage | standard_1005 |

## 4. ICA Component Assessment

ICA component 000 was considered highly suspected to be ocular-related based on the following observations:

- **Spatial distribution:** The component showed a frontal-dominant topography.
- **Frequency characteristics:** Its activity was predominantly associated with low-frequency patterns.
- **Temporal characteristics:** A prominent transient was observed around 102.7–103.5 seconds.

These observations supported the decision to exclude component 000 for exploratory artifact reduction.

However, the ocular origin could not be conclusively confirmed because no independent EOG channel or synchronized video recording was available.

## 5. Cleaning Results

After excluding ICA component 000:

- The large transient was visibly reduced in Fp1, Fp2, and Fpz.
- The before-and-after comparison showed changes in frontal EEG activity.
- The cleaned recording retained 64 EEG channels.

The observed reduction supports the effectiveness of this component exclusion for the selected transient. It does not establish that all ocular or other artifacts were removed.

## 6. Project Outputs

Key outputs include:

- `results/ICA_model/EEG_ICA_model.fif`
- `results/ICA_model/EEG_ICA_cleaned_raw.fif`
- `results/ICA_model/ICA_parameters.json`
- `results/ICA_model/ICA_decision_record.json`
- `figures/ICA/ICA000_before_after_comparison.png`
- `figures/ICA/ICA000_before_after_comparison.pdf`

The fitted ICA model, parameter record, decision record, and cleaned dataset support reproducibility of the analysis.

## 7. Limitations

- Only ICA component 000 was excluded.
- The suspected ocular origin was not independently confirmed.
- No dedicated EOG channel or synchronized video was available for validation.
- Visual component interpretation involves uncertainty.
- Further validation with independent physiological measurements is recommended.

## 8. Tools

- Python
- MNE-Python
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

## 9. Conclusion

This project demonstrates a practical ICA-based approach to exploring and reducing suspected EEG artifacts.

The results show a visible reduction in a selected frontal transient after component exclusion. Further validation is required before interpreting the removed component as definitively ocular-related or claiming comprehensive artifact removal.
