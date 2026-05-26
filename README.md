# Feature-selected PET/CT Radiomics Dataset for NSCLC Prediction Tasks

## Overview
The files provided in this repository are feature-selected matrices used for model construction, not raw PET/CT imaging data.
This repository provides the feature-selected data matrices used in our study on dual-modal PET/CT-based prediction of EGFR mutation status and pathological subtype in non-small cell lung cancer (NSCLC).

The data in this repository are not raw PET/CT images. Instead, they consist of processed and feature-selected radiomic, metabolic, and clinical variables used for model construction and evaluation.

In the original study, PET-derived features, CT radiomic features, and clinical variables were extracted from NSCLC patients across three retrospective cohorts. Feature selection was performed separately for two prediction tasks:

1. EGFR mutation prediction
2. Pathological subtype classification

For PET features, Recursive Feature Elimination with Cross-Validation (RFECV) was used to identify the optimal feature subset. For CT radiomic features, a two-step feature selection strategy was adopted. First, the Minimum Redundancy Maximum Relevance (mRMR) algorithm was used to retain the top-ranked features. Subsequently, least absolute shrinkage and selection operator (LASSO) regression was applied, and features with non-zero coefficients were retained for model construction.

## Data Files

| File | Description |
|---|---|
| `PET_clinical_selected_feature_matrix.xlsx` | Feature-selected PET-derived metabolic heterogeneity features combined with clinical variables. |
| `EGFR mutation prediction CT feature.xlsx` | Selected CT radiomic feature matrix for EGFR mutation prediction. |
| `Pathological subtype classification CT feature.xlsx` | Selected CT radiomic feature matrix for pathological subtype classification. |

## Feature Selection Strategy

Feature selection was performed independently for the EGFR mutation prediction task and the pathological subtype classification task.

For PET features, RFECV was applied to reduce the initial PET feature set. The initial 20 PET features were reduced to 6 features for EGFR mutation prediction and 5 features for pathological subtype classification.

For CT radiomic features, mRMR was first used to screen 130 candidate CT features, and the top 20 features were retained for each region-specific feature set. LASSO regression was then used for further dimensionality reduction, and only features with non-zero coefficients were retained.

For EGFR mutation prediction, the final CT_reg1, CT_reg2, CT_reg5, CT_reg6, and CT_reg_all feature sets contained 8, 2, 5, 6, and 7 features, respectively. The PET-clinical and PET-CT-clinical feature sets contained 9 and 19 features, respectively.

For pathological subtype classification, the final CT_reg1, CT_reg2, CT_reg5, CT_reg6, and CT_reg_all feature sets contained 5, 7, 5, 6, and 9 features, respectively. The PET-clinical and PET-CT-clinical feature sets contained 8 and 13 features, respectively.

## Intended Use

These feature matrices were used for developing and evaluating machine learning and deep learning models for:

- EGFR mutation status prediction
- Pathological subtype classification
- PET/CT multimodal feature fusion
- Radiomics-based model construction
- Comparative analysis of different feature combinations

## Data Privacy Statement

All data have been de-identified before sharing. The files in this repository do not contain raw PET/CT images, DICOM files, patient names, hospital IDs, examination IDs, or other direct personal identifiers.

The shared files only contain processed feature matrices used for model development. The original imaging data are not publicly available due to patient privacy protection and institutional data-sharing restrictions.

## Citation

If you use these feature matrices or refer to this dataset structure, please cite the associated manuscript:

[Manuscript information to be added after publication]
