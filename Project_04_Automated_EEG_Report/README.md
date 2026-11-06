# Project 04 — Automated EEG Analysis Report

## 1. 项目简介

本项目基于经过预处理和 ICA 伪迹清理的 EEG 数据，
建立自动化 EEG 分析流程。

主要功能：
- EEG 数据质量检查
- 逐通道振幅统计
- 五大频段 PSD 特征提取
- 相对频段功率计算
- EEG 数据可视化
- 自动生成 HTML 分析报告

## 2. 分析环境

- Python
- MNE
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

## 3. 分析流程

1. 读取 Project 03 输出的 ICA 清理后 EEG 数据
2. 检查数据维度、采样率、NaN 和 Inf
3. 计算逐通道振幅统计指标
4. 使用 Welch 方法计算功率谱密度（PSD）
5. 提取 Delta、Theta、Alpha、Beta、Gamma 五个频段特征
6. 生成相对功率热图和通道振幅分布图
7. 导出 CSV 数据和 HTML 分析报告

## 4. 频段定义

| 频段 | 范围 |
|---|---|
| Delta | 1–4 Hz |
| Theta | 4–8 Hz |
| Alpha | 8–13 Hz |
| Beta | 13–30 Hz |
| Gamma | 30–45 Hz |

本项目使用各频段内的平均 PSD 作为特征，
并在选定的五个频段之间计算相对功率。
该指标不等同于频段积分功率。

## 5. 项目输出

- `results/EEG_channel_quality_report.csv`
- `results/EEG_band_power_absolute.csv`
- `results/EEG_band_power_relative.csv`
- `figures/EEG_channel_amplitude_overview.png`
- `figures/EEG_relative_band_power_heatmap.png`
- `reports/EEG_Automated_Analysis_Report.html`

## 6. 运行方法

打开 `notebooks/04_Automated_EEG_Analysis_Report.ipynb`，
按顺序运行所有代码单元格。

输入数据为 Project 03 生成的 ICA 清理后 EEG 文件。

## 7. 分析局限

- 本项目使用的数据已经经过预处理和 ICA 清理，并非原始数据全流程处理。
- 振幅阈值仅用于探索性筛查，不能单独作为坏通道判定依据。
- 频段特征不能单独用于判断意识状态或作出临床诊断。
- 分析结果需要结合实验设计、受试者状态和其他证据解释。

## 8. 数据说明

公开项目时，请确保 EEG 数据具有公开授权。
未获得授权时，不上传原始或可识别受试者的数据文件。
