# EEG Motor Imagery Analysis Report

## 1. Project Overview

This project explores EEG frequency-band power changes
under different motor imagery event conditions.

The analysis focuses on:
- C3, Cz, C4
- Mu band: 8–13 Hz
- Beta band: 13–30 Hz
- T1 and T2 event conditions

## 2. Dataset Information

- Source file: S001R06.edf
- Sampling frequency: 160 Hz
- EEG channels: 64
- Duration: approximately 125 seconds
- Event annotations: T0, T1, T2
- Data used for analysis: ICA-cleaned EEG

The exact experimental meaning of T0, T1 and T2
should be confirmed against the original dataset documentation.

## 3. Analysis Workflow

1. Load ICA-cleaned EEG data.
2. Extract event annotations.
3. Create event-related epochs.
4. Select C3, Cz and C4 channels.
5. Calculate Mu and Beta band power.
6. Apply sliding-window analysis.
7. Compare task-condition averages with T0 averages.
8. Visualize temporal power changes.

## 4. Main Observations

Under T1, C3 and C4 show decreases in both Mu and Beta
band power relative to the T0 condition averages.

Under T2, the temporal patterns are more variable.

These are exploratory observations and have not been
validated through inferential statistical testing.

## 5. Important Limitations

- The exact event definitions require dataset documentation.
- The number of epochs is limited.
- T0 is a separate condition average, not a trial-specific
  pre-stimulus baseline.
- The analysis uses ICA-cleaned data rather than the original
  unprocessed recording.
- No classification model or independent test set was evaluated.
- The results do not establish causal or clinical conclusions.

## 6. Output Files

- EEG_Mu_Beta_Time_Changes.csv
- EEG_Mu_Beta_Time_Comparison.png

## 7. Conclusion

This project demonstrates an exploratory EEG analysis workflow
for comparing Mu and Beta band power over time across event
conditions and selected motor-related EEG channels.