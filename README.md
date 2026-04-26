# Reproducing and Analyzing ROCKET for Time Series Classification

**Author:** Kalyan Kumar Bhumaiahgari (25234940)  
**Module:** COMP41850: AI for Time Series, University College Dublin  

## Project Overview
This repository contains the code, raw results, and generated figures for a reproducibility study of the paper:
> *"ROCKET: Exceptionally fast and accurate time series classification using random convolutional kernels"* (Dempster et al., 2020).

Using the `aeon` Python library, this project reproduces the canonical ROCKET baseline across seven UCR benchmark datasets. Furthermore, it includes three extended ablation studies:
1. **Efficiency Improvement:** Benchmarking MiniROCKET against the canonical baseline.
2. **Classifier Head Ablation:** Comparing the default Ridge regression classifier against Random Forest and XGBoost (with `StandardScaler`).
3. **Feature Ablation:** Isolating the Proportion of Positive Values (PPV) and Maximum (Max) features to replicate the original paper's findings on pooling mechanisms.

## Repository Contents
* `COMP41850_AI_for_Time_Series.ipynb`: The main Google Colab Jupyter Notebook containing all experimental code, pipeline construction, and evaluation loops.
* `results.csv`: The raw numerical outputs including test accuracies and training times across 3 random seeds.
* `accuracy_comparison.png`, `time_comparison.png`, `ppv_vs_max.png`: Generated visualizations of the experimental results.

## Requirements
To run this code, you will need Python 3.12+ and the following libraries:
* `aeon` (v1.4.0)
* `scikit-learn`
* `xgboost`
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`

## How to Run / Reproduce
1. Clone this repository to your local machine or upload the `.ipynb` notebook file to Google Colab.
2. Install the required dependencies:
   ```bash
   pip install aeon scikit-learn xgboost pandas numpy matplotlib seaborn
