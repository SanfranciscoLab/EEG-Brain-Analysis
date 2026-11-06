# Project 03: EEG Artifact Identification and ICA Cleaning

## 1. Project Overview

本项目使用 MNE-Python 对 EEG 数据进行质量控制、
独立成分分析（ICA）以及疑似眼动伪迹识别与清理。

项目目标：
- 检查 EEG 数据质量
- 建立标准电极位置信息
- 使用 ICA 分离独立成分
- 识别疑似眼动相关伪迹
- 验证清理前后的信号变化
- 保存可复现的处理结果

## 2. Dataset Information

- EEG channels: 64
- Sampling rate: 160 Hz
- Number of samples: 20,000
- Duration: 124.994 seconds
- NaN values: 0
- Inf values: 0

## 3. Preprocessing

- EEG average reference
- Standard 10-05 montage assignment
- ICA decomposition using FastICA
- Number of ICA components: 28

## 4. ICA Component Assessment

ICA component 000 was selected for further assessment.

Observed evidence:
- Frontal-dominant spatial distribution
- Strong low-frequency activity
- Large transient activity around 102.7–103.5 seconds
- Similar abnormal activity across frontal electrodes
- Reduced frontal transient amplitude after component removal

The component was considered highly suspected to be ocular-related.

Important limitation:
No independent EOG channel or video recording was available.
Therefore, the ocular origin cannot be conclusively confirmed.

## 5. ICA Cleaning

ICA component 000 was excluded in a copy of the original
referenced and montage-corrected EEG data.

The cleaned dataset was saved as:

results/ICA_model/EEG_ICA_cleaned_raw.fif

## 6. Before-and-After Comparison

The following frontal channels were compared:

- Fp1
- Fp2
- Fpz

Analysis interval:
100–106 seconds

Suspected artifact interval:
102.7–103.5 seconds

The large transient activity was visibly reduced after
ICA component 000 removal.

Figure files:

- figures/ICA/ICA000_before_after_comparison.png
- figures/ICA/ICA000_before_after_comparison.pdf

## 7. Data Validation

The saved cleaned dataset was reloaded successfully.

- Channels: 64
- Sampling rate: 160 Hz
- Data shape: (64, 20000)
- NaN count: 0
- Inf count: 0

## 8. Limitations

- No independent EOG channel was available.
- The ocular origin of ICA000 remains a well-supported
  hypothesis rather than a confirmed diagnosis.
- Only ICA000 was excluded.
- The overall PSD changed only slightly; this does not
  establish that all artifacts were removed.
- Further validation using EOG, video, and additional
  physiological data is recommended.

## 9. Conclusion

This project demonstrates an EEG quality-control and ICA
artifact-assessment workflow using MNE-Python.

The results show that ICA component 000 removal substantially
reduced a large transient in frontal EEG channels.

The cleaned data and analysis records were saved for
reproducibility and further analysis.
