# Interpretable Machine Learning for Cross-Material Structure-Property Relationships in Air Filtration Media
[![DOI](https://zenodo.org/badge/1247237937.svg)](https://doi.org/10.5281/zenodo.20357451)
## Overview
This repository contains the dataset and analysis code for the manuscript
" Interpretable Machine Learning for Cross-Material Structure-Property Relationships in Air Filtration Media". The study applies
interpretable machine learning to predict and explain air filtration
performance across 227 filter media samples spanning 23 material families
and seven architectural configurations.

## Repository Structure
- final_dataset.csv — curated dataset of 227 samples with 41 features
- step1_EDA.ipynb — exploratory data analysis
- step2_preprocessing.ipynb — feature engineering and target transformation
- step3_baseline_rf.ipynb — baseline Random Forest models
- step4_nested_cv.ipynb — nested cross-validation with RF, XGBoost, and LASSO/ElasticNet
- step5_shap.ipynb — SHAP feature importance and interaction analysis
- step6_validation.ipynb — bootstrap stability, subgroup analysis, physics checks, and design map

## How to Run
Run notebooks in order from step1 through step6. Each notebook saves
outputs that are loaded by subsequent steps.

## Data Notes
- The pressure_drop column in the raw CSV may load as string type in some
  environments. The preprocessing notebook (step2) converts it to numeric
  automatically.
- Missing values in the raw dataset are handled by KNN imputation (k=5)
  inside each cross-validation fold during step4.
- All target transformations use the natural logarithm (base e).

## Requirements
Python 3.9 or later. Install dependencies with:
pip install -r requirements.txt

## Citation
[To be added after publication]

## License
This project is licensed under the MIT License. See LICENSE for details.
