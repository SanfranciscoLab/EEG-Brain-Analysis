# Project 05 - EEG Motor Imagery Analysis

## Project Overview

An exploratory EEG analysis project investigating Mu and Beta band power changes.

## Dataset

- Source file: S001R06.edf
- Sampling rate: 160 Hz
- EEG channels: 64
- Duration: approximately 125 seconds
- Event labels: T0, T1, T2
- Input: ICA-cleaned EEG recording

## Analysis Channels

- C3
- Cz
- C4

## Frequency Bands

- Mu: 8-13 Hz
- Beta: 13-30 Hz

## Workflow

1. Load EEG data using MNE-Python.
2. Extract event annotations.
3. Create epochs.
4. Select C3, Cz and C4 channels.
5. Calculate Mu and Beta band power.
6. Perform sliding-window analysis.
7. Compare task averages with T0.
8. Generate plots and CSV results.

## Main Observations

T1 showed decreases in Mu and Beta power at C3 and C4 relative to T0 averages.
T2 showed more variable temporal patterns.

These are exploratory observations, not statistically validated findings.

## Limitations

- Event definitions require verification against original dataset documentation.
- T0 is a separate condition average, not a trial-specific baseline.
- The number of epochs is limited.
- The analysis uses ICA-cleaned data.
- No classification model or independent test set was evaluated.

## Tools

- Python
- MNE-Python
- NumPy
- Pandas
- SciPy
- Matplotlib
- Jupyter Notebook
