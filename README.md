# PET/CT Dataset for Dual-task Prediction of EGFR Mutation Status and Pathological Subtype in NSCLC

## Overview

This repository provides the dataset documentation and metadata used in our study on dual-modal PET/CT-based prediction of pathological subtypes and EGFR mutation status in non-small cell lung cancer (NSCLC).

The study included 384 patients with pathologically confirmed NSCLC from three independent retrospective cohorts. CT images were used to extract sub-regional radiomic features, while PET images were used to characterize spatial metabolic heterogeneity. These data were used to develop and validate a Dual-Modal Dual-task Prediction (DMDP) model for simultaneous prediction of EGFR mutation status and pathological subtype.

Due to patient privacy and institutional restrictions, raw PET/CT images and identifiable clinical information are not publicly released in this repository. Only de-identified metadata, feature descriptions, data organization information, and usage instructions are provided.

## Dataset Description

The dataset consists of paired PET/CT imaging-derived features from 384 NSCLC patients. Each patient was associated with two prediction labels:

1. EGFR mutation status
2. Pathological subtype

The dataset was divided into three independent cohorts for model development and validation.

## Data Modalities

- CT imaging features: sub-regional radiomic features extracted from tumor regions.
- PET imaging features: metabolic parameters and spatial heterogeneity descriptors.
- Clinical labels: EGFR mutation status and pathological subtype.
- Cohort information: training, validation, or external testing cohort.

## File Structure

| File | Description |
|---|---|
| `metadata.csv` | De-identified patient-level metadata |
| `ct_radiomics_features.csv` | CT-derived sub-regional radiomic features |
| `pet_metabolic_features.csv` | PET-derived metabolic and heterogeneity features |
| `labels.csv` | Prediction labels including EGFR mutation status and pathological subtype |
| `cohort_split.csv` | Cohort assignment for training, validation, and testing |

## Variable Description

| Variable | Description |
|---|---|
| `patient_id` | De-identified patient identifier |
| `cohort` | Cohort assignment |
| `egfr_status` | EGFR mutation status |
| `pathological_subtype` | Pathological subtype of NSCLC |
| `ct_feature_*` | CT-derived radiomic features |
| `pet_feature_*` | PET-derived metabolic or heterogeneity features |

## Intended Use

This dataset was used for developing and validating a dual-modal dual-task deep learning model for:

- EGFR mutation status prediction
- Pathological subtype prediction
- PET/CT multimodal feature fusion
- Radiomics and metabolic heterogeneity analysis
- Model interpretability analysis using Grad-CAM

The dataset is intended for academic and research purposes only.

## Data Privacy and Ethics

All patient-related data were retrospectively collected and de-identified before analysis. Direct personal identifiers, including name, hospital ID, examination ID, date of birth, and contact information, were removed or anonymized.

Raw PET/CT images are not publicly available in this repository due to patient privacy protection and institutional data-sharing restrictions. Access to the original imaging data may be subject to institutional review board approval and data use agreements.

## Citation

If you use this dataset description, feature structure, or related code, please cite the associated manuscript:

[Manuscript information to be added after publication]
