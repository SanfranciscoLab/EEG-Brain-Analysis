# EEG Analysis Portfolio

An EEG data analysis portfolio built with Python and MNE-Python.

This portfolio demonstrates EEG preprocessing, spectral analysis,
artifact removal, automated reporting, and motor imagery analysis.

## About This Portfolio

This project collection focuses on practical EEG signal processing
and reproducible analysis workflows.

## Technical Skills

- Python
- MNE-Python
- NumPy
- Pandas
- SciPy
- Matplotlib
- Jupyter Notebook
- EEG preprocessing and quality control
- Power spectral density (PSD) analysis
- Frequency band feature extraction
- Independent Component Analysis (ICA)
- Event annotation and epoch analysis
- Sliding-window spectral analysis

## Projects

### Project 01 - EEG Preprocessing and PSD

EEG preprocessing, filtering, and power spectral density analysis.

[Project 01](./Project_01_EEG_Preprocessing_PSD/)

### Project 02 - EEG Band Power Features

Extraction and visualization of Delta, Theta, Alpha, Beta, and Gamma band features.

[Project 02](./Project_02_EEG_BandPower_Features/)

### Project 03 - ICA Artifact Removal

EEG artifact exploration and ICA-based component removal.

[Project 03](./Project_03_ICA_Artifact_Removal/)

### Project 04 - Automated EEG Analysis Report

Automated EEG quality assessment, band power calculation, and report generation.

[Project 04](./Project_04_Automated_EEG_Report/)

### Project 05 - Motor Imagery EEG Analysis

Exploratory Mu and Beta band power analysis across event conditions
using sliding windows and selected motor-related channels.

[Project 05](./Project_05_ERP_Analysis/)

## Analysis Workflow

1. Load EEG recordings.
2. Inspect channel information and data quality.
3. Preprocess EEG signals.
4. Estimate power spectral density.
5. Extract frequency band features.
6. Explore and remove artifacts using ICA.
7. Generate automated analysis reports.
8. Analyze event-related epochs and time-varying spectral features.

## Important Notes

- Some projects use ICA-cleaned data rather than original raw recordings.
- Project 05 contains exploratory condition-level comparisons.
- Event labels and experimental meanings must be verified against
  the original dataset documentation.
- The results are not clinical findings or validated BCI classification results.
- Data and model files are not included unless sharing is authorized.

## Reproducibility

The analysis notebooks are designed to be executed using Python,
MNE-Python, and the listed scientific computing libraries.

## Disclaimer

This portfolio is an independent learning and technical demonstration
project. It is not intended for clinical diagnosis or medical use.
## Environment Setup

### Requirements

- Python 3.12+
- MNE-Python
- NumPy
- SciPy
- Pandas
- Matplotlib
- Jupyter Notebook

### Install Dependencies

Clone this repository and navigate to the project root directory. Run:

```bash
pip install -r requirements.txt
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the corresponding notebook in the `notebooks/` directory of each project.

### Data Availability

EEG datasets and raw signal files are not included in this public repository. Please refer to each project's README for dataset requirements and data path configuration.

**Note:** Dependency compatibility may vary across Python versions. A clean environment test is recommended before running the notebooks.
