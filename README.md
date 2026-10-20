# CropTypeGodagari
## Functional Data Analysis and Machine Learning for Remote Sensing-Based Crop-Type Mapping in Smallholder Farms of Bangladesh

### Overview

This research project develops a phenology-informed crop-type mapping workflow that combines functional data analysis (FDA), multi-temporal satellite remote sensing, and machine learning to classify six Rabi crops in smallholder farming systems in Godagari Upazila, Rajshahi, Bangladesh.

The workflow integrates Sentinel-2 optical indices and Sentinel-1 radar backscatter time series, functional representations of seasonal crop development, and machine-learning classifiers to investigate crop separability and improve crop-type classification.

### Research objectives

- Map six Rabi crops: rice, wheat, lentil, maize, mustard, and potato.
- Represent seasonal satellite-index trajectories as smooth functional curves using B-splines.
- Evaluate crop-specific temporal differences and spectral-radar separability.
- Compare machine-learning classifiers using functional principal component features.
- Assess model generalization using spatial-block and leave-one-year-out cross-validation.
- Demonstrate the potential of functional time-series analysis for crop-type mapping in smallholder landscapes.

### Study area and data

**Study area:** Godagari Upazila, Rajshahi, Bangladesh.

**Study period:** Three Rabi seasons, 2020–21 to 2022–23.

**Satellite sources:** Sentinel-1 radar and Sentinel-2 optical observations.

**Reference data:** Field-reference points screened using the Dynamic World land-cover product and additional quality-control procedures.

After quality screening, 1,290 reference points were retained for the analysis.

Satellite indices were summarized into regular 15-day composites from November through April, producing 12 temporal observations per index and reference point. Twelve optical and radar indices were then represented as smooth seasonal functions.

### Methodological workflow

1. **Reference-data quality control:** Screen field-reference points for duplicates, mixed pixels, low vegetation, and potential inconsistencies using the documented quality-control procedures.
2. **Satellite time-series construction:** Prepare Sentinel-1 and Sentinel-2 index composites at 15-day intervals throughout the Rabi growing season.
3. **Functional representation:** Smooth seasonal index trajectories using B-spline basis functions.
4. **Functional statistical analysis:** Apply functional analysis of variance (FANOVA) to assess differences among crop-specific temporal trajectories and use the Jeffries–Matusita distance to investigate class separability.
5. **Feature extraction:** Derive functional principal component scores as compact representations of seasonal trajectories.
6. **Machine-learning classification:** Compare five classifiers and tune the selected LightGBM model.
7. **Model validation:** Evaluate predictive performance using spatial-block and leave-one-year-out cross-validation.
8. **Crop mapping:** Apply the selected model to produce crop-type maps and estimate the relative distribution of Rabi crops for the 2022–23 season.

### Key findings

The reported results demonstrate the potential of combining functional statistics with optical-radar time series for crop-type mapping.

| Performance measure | Reported result |
|---|---:|
| Overall accuracy | 0.860 |
| 95% confidence interval for overall accuracy | 0.841–0.878 |
| Cohen's kappa | 0.821 |
| Macro-averaged F1-score | 0.838 |
| Rice F1-score | 0.94 |
| Potato F1-score | 0.91 |
| Lentil F1-score | 0.70 |

Functional ANOVA indicated significant differences among crops for all 12 indices (p < 0.001). The first functional component of Sentinel-1 VV backscatter was identified as the most influential feature in the selected model.

For the 2022–23 season, the resulting upazila-level estimates indicated that rice and mustard accounted for 32.0% and 22.5% of the mapped Rabi crop distribution, respectively.

These findings are from an ongoing research project and should be interpreted in the context of its study area, reference data, and validation design.

### Research contributions

The project brings together:

- Functional data analysis of multi-temporal satellite observations.
- Phenology-informed machine learning for crop-type classification.
- Integration of optical and radar remote sensing.
- Reference-data quality control.
- Spatial and temporal model-validation strategies.
- Geospatial mapping of smallholder agricultural systems.

The broader research motivation is to develop robust, transferable methods for crop monitoring in data-constrained agricultural settings.

### Repository contents

The repository contains the research code and supporting materials associated with this workflow.

**Repository structure:** Add a directory tree reflecting the actual files in this repository. For each notebook or script, briefly describe its purpose, required inputs, and outputs.

### Data availability

Document the satellite-data sources, reference-data provenance, access requirements, and any restrictions on sharing field-reference data. Do not include sensitive field locations or institutionally restricted data without authorization.

### Software and reproducibility

Document the programming language, package dependencies, software versions, and required inputs. Provide setup and execution instructions that match the actual code and repository structure.

Where full reproduction requires external datasets, credentials, or unavailable reference data, explain these limitations explicitly.

### Research status

**Manuscript status:** In preparation; not yet submitted for publication.

This repository supports an ongoing research project. Reported findings have not yet undergone journal peer review.

### Contact

**Researcher:** Istiak Ahmed  
**Affiliation:** Bangladesh Agricultural Research Institute (BARI), Bangladesh  
**GitHub:** https://github.com/istiak-ahmed1
