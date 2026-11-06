# Project 05 — Motor Imagery Band-Power Analysis

## Project Overview

An exploratory EEG analysis project investigating Mu and Beta band-power patterns across different event conditions using sliding-window spectral analysis.

The project focuses on selected motor-related EEG channels and compares condition-level spectral features. It is intended as a practical demonstration of event-based EEG analysis rather than a validated BCI system.

## Dataset

- Source file: `S001R06.edf`
- Sampling rate: 160 Hz
- EEG channels: 64
- Recording duration: approximately 125 seconds
- Event annotations: T0, T1, T2
- Input: ICA-cleaned EEG recording

## Analysis Channels

- C3
- Cz
- C4

## Frequency Bands

- Mu: 8–13 Hz
- Beta: 13–30 Hz

## Analysis Workflow

1. Load EEG data using MNE-Python.
2. Inspect event annotations.
3. Extract epochs from event annotations.
4. Select C3, Cz, and C4 channels.
5. Calculate Mu and Beta band power.
6. Perform sliding-window spectral analysis.
7. Compare T1 and T2 condition averages with T0.
8. Generate visualizations and CSV results.

## Sliding-Window Parameters

- Window length: 1 second
- Step size: 0.5 seconds
- Frequency estimation: Welch-based spectral analysis
- Frequency resolution parameter: `n_fft = 256`

## Main Observations

- T1 showed decreases in Mu and Beta band power at C3 and C4 relative to the T0 condition average.
- T2 showed more variable temporal patterns.

These observations are exploratory and have not been established through statistical validation.

## Output Files

- `results/EEG_Mu_Beta_Time_Changes.csv`
- `figures/EEG_Mu_Beta_Time_Comparison.png`
- `reports/Motor_Imagery_BandPower_Report.md`

## Limitations

- Event definitions require verification against the original dataset documentation.
- T0 is a separate condition average, not a trial-specific pre-stimulus baseline.
- The number of epochs is limited.
- The analysis uses ICA-cleaned EEG data.
- No statistical significance testing was performed.
- No classification model or independent test set was evaluated.
- The findings should not be interpreted as validated ERD/ERS effects or BCI performance.

## Tools

- Python
- MNE-Python
- NumPy
- Pandas
- SciPy
- Matplotlib
- Jupyter Notebook
