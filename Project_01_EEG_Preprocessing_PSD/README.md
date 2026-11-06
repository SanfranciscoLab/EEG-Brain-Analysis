# Project 01 - EEG Preprocessing and PSD

## Overview

This project demonstrates EEG data loading, basic quality inspection,
band-pass filtering, and power spectral density (PSD) visualization.

## Technical Workflow

1. Load EEG recording using MNE-Python.
2. Inspect sampling frequency, channels, and recording duration.
3. Apply high-pass filtering at 1 Hz and low-pass filtering at 40 Hz.
4. Save the filtered EEG recording.
5. Calculate and visualize power spectral density.

## Dataset Information

- EEG channels: 64
- Sampling frequency: 160 Hz
- Number of samples: 20,000
- Recording duration: 125 seconds

## Outputs

- `results/EEG_filtered_raw.fif` - filtered EEG data.
- `results/day1_data_overview.txt` - data overview.
- `results/params_project01.json` - processing parameters.
- `figures/psd.png` - PSD visualization.

## Tools

- Python
- MNE-Python
- NumPy
- Matplotlib
- Jupyter Notebook

## Notes

This project demonstrates a basic EEG preprocessing workflow.
Filtering parameters should be selected according to the research
question and dataset characteristics.

This is an independent learning project, not a clinical analysis.
