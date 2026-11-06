# Project 03: EEG Quality Control and ICA Artifact Removal

## Overview

This project demonstrates EEG quality control and Independent
Component Analysis (ICA) using MNE-Python.

## Objectives

- Perform EEG data quality assessment
- Assign standard electrode locations
- Apply FastICA decomposition
- Assess suspected ocular-related artifacts
- Compare EEG signals before and after ICA cleaning
- Validate and save the cleaned EEG dataset

## Dataset

- EEG channels: 64
- Sampling rate: 160 Hz
- Duration: 124.994 seconds
- ICA components: 28

## Key Result

ICA component 000 was identified as highly suspected
to be ocular-related based on its frontal-dominant
topography, low-frequency activity, and transient
activity around 102.7–103.5 seconds.

After removing this component, the large transient
was visibly reduced in Fp1, Fp2, and Fpz.

The ocular origin was not conclusively confirmed
because no independent EOG channel or video was available.

## Project Structure

- notebooks/: Jupyter Notebook
- reports/: Analysis report
- figures/: Before-and-after comparison figures
- results/: ICA model and cleaned EEG data

## Tools

- Python
- MNE-Python
- NumPy
- Pandas
- Matplotlib

## Reproducibility

The analysis report, ICA parameters, decision record,
and cleaned dataset are provided as project outputs.

## Limitations

Only ICA component 000 was excluded.
Further validation with independent EOG or video data
is recommended.
