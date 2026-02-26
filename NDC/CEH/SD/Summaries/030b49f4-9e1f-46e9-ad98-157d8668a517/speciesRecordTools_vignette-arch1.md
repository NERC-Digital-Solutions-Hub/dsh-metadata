# Methods for Modelling Species Distributions from Unstructured Environmental Record Centre Data

## Overview
- Introduces the R package speciesRecordTools for analyzing unstructured (opportunistic) species records.
- Aims to understand sampling trends and biases and to build correlative presence-background species distribution models (SDMs) to predict species distributions across landscapes.
- Primarily designed to work with Environmental Record Centre for Cornwall and the Isles of Scilly (ERCCIS) data; higher-quality data may require different modelling approaches.
- Requires environmental predictors (e.g., land cover, climate) prepared in advance.

## Data inputs, focal species, and temporal scope
- Focus on a focal species (binomial/scientific name preferred) with examination of raw records, sampling bias, and predicted distributions.
- Set a grid resolution at the start (options include 1 km, 2 km, 4 km; other grids can be created with makeGrid).
- Define the focal period with start_year and end_year to balance having enough records against representing the focal time window.
- ERCCIS data loaded via species_record_load from a .sqlite database, returning a spatial object (sf) projected to a chosen CRS.
- Example focal species: Muscardinus avellanarius; grid resolution example: 1000 m.

## Data preparation and grid design
- Create a study-area grid (e.g., England) and a blocking grid (blockGrid) for cross-validation.
- Prepare environmental data:
  - Landcover and climate rasters (terra spatrast objects) gridded as predictors.
  - Optionally reduce dimensionality with PCA to capture key gradients.
- Presence-background data preparation:
  - use prepare_sdm_data to generate PB datasets for combinations of fdist (filter distance) and bdist (buffer distance).
  - Can include or exclude GBIF data (gbif_include); currently example uses ERCCIS only for efficiency.
- Align data to the chosen resolution (grainkm) and region (region_sf, e.g., eng1kmGrd).

## Visualizing distribution and sampling bias
- Intersect focal records with the study grid and filter by time and precision to visualize distribution.
- Assess sampling bias by estimating sampling completeness for a broader species group (e.g., Terrestrial Mammals) using a rarefaction-based approach.
- Outputs indicate spatially biased sampling (areas with little or no coverage), signaling the need for bias correction in SDMs.

## Modelling approach
- Augment ERCCIS records with GBIF data to model across a broader context (England) and predict for a focal area (e.g., Cornwall).
- Grid-level systematic blocking: create a blockGrid to separate data for model testing.
- Environmental data preparation: process landcover and climate rasters into grids; option to use PCA components as predictors.
- Build presence-background data for each PB dataset, which is then used in model tuning.

## Model tuning and algorithms
- Use prepare_sdm_data to generate datasets for model tuning across different fdist/bdist scenarios.
- Run sdm_tune_ssb to tune SDM algorithms and identify the best spatial sampling bias (SSB) correction approach.
- Four high-performing algorithms included:
  - Random Forest (RF, down-sampled)
  - Generalised Additive Models (GAM)
  - Generalised Boosted Models (GBM)
  - MaxEnt
- Model performance is evaluated by:
  - AUC for RF and MaxEnt
  - cross-validated error for GBMs
  - mgcv’s GCV with regularisation for GAMs

## Predictions and uncertainty
- Predictions are based on ensemble models that average across algorithms weighted by performance.
- Predict across data folds to capture data-driven uncertainty.
- Uncertainty metrics provided:
  - IQR (interquartile range) of weighted mean suitability
  - CV (coefficient of variation) of weighted mean suitability
  - Hotspots (upper quartile) for both mean suitability and CV
- Outputs include an ensemble object that can be used for further analysis and mapping.

## Visualization and outputs
- Visualize model predictions for a focal window using:
  - Weighted mean environmental suitability
  - IQR of suitability
  - Hotspots based on mean suitability
  - CV of suitability
  - Hotspots based on CV
- Example plotting workflows (e.g., focal_mapping) demonstrate generating maps and interpreting spatial patterns and uncertainty.

## Practical considerations and limitations
- Data availability and scale: unstructured data can be biased and unevenly sampled; bias correction steps are essential.
- Computational demands: environmental data processing and model tuning across multiple PB datasets can be time-consuming.
- Data integration: GBIF data can broaden geographic context but may increase complexity; efficiency can be improved by focusing on ERCCIS data.
- Data preparation requirements: sqlite data, appropriate CRS, and grid resolutions consistent with management needs.
- The approach emphasizes transparent reporting of data sources, model choices, and uncertainty to support practical decision-making.