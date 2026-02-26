# Methods for Modelling Species Distributions from Unstructured Environmental Record Centre Data

## Overview
- Describes the R package speciesRecordTools for analyzing unstructured (opportunistic) species records.
- Focuses on understanding sampling trends, biases, and building presence-background species distribution models (SDMs).
- Uses Environmental Record Centre for Cornwall and the Isles of Scilly (ERCCIS) data, with guidance to use higher-quality data when available.
- Requires preparation of environmental predictors (e.g., land cover, climate) for SDMs.

## Data Sources and Setup
- Focal species is the report subject; use binomial/scientific name preferentially.
- Analyses run on a predefined spatial grid; common resolutions include 1 km, 2 km, and 4 km (custom grids possible via makeGrid).
- Define focal period with start year and end year to balance record numbers with temporal relevance.
- ERCCIS data loading assumes a .sqlite file; results are returned as an sf object projected to a chosen CRS.

## Data Loading and Visualisation
- Load ERCCIS data with species_record_load (requires path to ERCCIS sqlite database and target group/species).
- Intersect data with a study area grid to inspect distribution and sampling bias within the specified time window and precision.
- Visualise spatial distribution of focal records and sampling bias for the focal species group.

## Bias Assessment
- Spatial sampling bias is challenging to quantify directly from effort data in opportunistic records.
- Estimate sampling completeness for an entire species group (rareification-based approach) to infer broad spatial bias patterns.
- Visuals (e.g., Figure 3) indicate strong spatial bias with areas lacking coverage, signaling the need for bias-correction in SDMs.

## Modelling Approach and Data Augmentation
- Build SDMs for Cornwall while incorporating broader context by augmenting ERCCIS records with GBIF data and modeling across England.
- Create a grid across the region for systematic blocking; grid resolution should exceed environmental data resolution.
- Prepare environmental predictors (land cover, climate) and optionally reduce dimensionality with PCA.
- Use a presence–background framework, generating datasets for combinations of filter distance (fdist) and buffer distance (bdist).

## Data Preparation for SDMs
- prepare_sdm_data creates presence-background datasets for each scenario of fdist and bdist (examples may use a single scenario for efficiency).
- Optionally limit to ERCCIS records (gbif_include = FALSE) for computational efficiency; broader analyses can include GBIF data for context.
- Inputs include focal species data, region, grain, coordinate system, and temporal window, plus parameters for occFilter, occBuffer, and cross-validation folds.

## Modelling Algorithms and Tuning
- Four high-performing SDM algorithms included:
  - Random Forest (down-sampled)
  - Generalised Additive Models (GAM)
  - Generalised Boosted Models (GBM)
  - MaxEnt
- Models are tuned to optimize predictive performance using data withheld in blocks.
- Evaluation: AUC for RF and MaxEnt; cross-validated error for GBMs; GAMs tuned with mgcv’s GCV and regularisation.
- Predictions are ensemble-based, averaging across models weighted by performance.

## Predictions and Uncertainty
- Ensemble predictions (sp.ens) provide a robust distribution forecast.
- Uncertainty metrics returned: interquartile range (IQR), coefficient of variation (CV), and hotspots (upper quartile) for both mean suitability and CV.
- Outputs enable assessment of relative site suitability and the confidence in predictions.

## Visualisation and Practical Outputs
- Visualisation options for predictions across a focal window include:
  - Weighted mean environmental suitability
  - IQR of suitability
  - Hotspots for mean suitability
  - CV of suitability
  - Hotspots for CV
- Functions (examples) support mapping focal species predictions over the study area.

## Practical Considerations and Takeaways
- SDM building is data- and compute-intensive; integrating broader data (e.g., GBIF) can improve context and robustness.
- Address spatial sampling bias explicitly via sampling completeness to improve model reliability.
- Choice of grid resolution and temporal window should balance management needs, data quality, and ecological relevance.
- Use ensemble predictions to explore uncertainty and identify robust hotspot areas for conservation or management.