# Methods for Modelling Species Distributions from Unstructured Environmental Record Centre Data

- The R package speciesRecordTools provides functions to examine distributions of unstructured (opportunistic) species records, assess sampling trends and biases, and build correlative presence-background species distribution models (SDMs) to predict species distributions across landscapes.
- Data focus is on ERCCIS opportunistic records for Cornwall and the Isles of Scilly; higher-quality data should use alternative modelling approaches. Environmental predictors (e.g., land cover, climate) must be prepared beforehand.

## Data Setup and Loading

- Define focal species (binomial name preferred) and set a focal time period (start year to end year) to filter records for modelling.
- Decide grid resolution at start (options include 1 km, 2 km, 4 km; other grids can be created with makeGrid) to balance management needs and data quality.
- Load ERCCIS data from a .sqlite database and transform to projected coordinates (sf object) using a regional reference CRS.
- Example workflow parameters:
  - Focal species: Muscardinus avellanarius
  - Grid resolution: 1000 m
  - Time window: 2000–2020

## Visualising Distribution and Sampling

- Intersect species records with a study-area grid to visualize spatial distribution and data precision (in meters) within the focal time period.
- Functions illustrate:
  - Spatial distribution of records for the focal species
  - Sampling bias within the focal species group
- Spatial maps help identify data gaps and areas with little to no sampling coverage.

## Assessing Sampling Bias

- Opportunistic data lack explicit effort measures; assess broad spatial sampling bias by estimating sampling completeness for the entire species group.
- A rarefaction-based sampling completeness approach highlights areas with strong sampling bias, indicating the need for bias correction in SDMs.
- Example finding: pronounced spatial bias with many areas lacking sampling coverage.

## Modelling Species Distributions (SDMs)

- A broader context is used by augmenting ERCCIS records with GBIF data and modelling across England to predict distribution in a focal area (e.g., Cornwall).
- Create a systematic spatial blocking grid to structure modelling and cross-validation.
- Environmental data preparation is key: process landcover and climate rasters into grids; consider using principal components to reduce dimensionality.
- Prepare presence-background datasets for combinations of filter distance (fdist) and buffer distance (bdist); these datasets are used to tune models and reduce effects of spatial sampling bias.
- Practical note: for efficiency, GBIF data can be excluded (gbif_include = FALSE), though broader geographic context is preferable.

## Predictor Variables and Data Preparation

- Use functions to grid environmental data:
  - landcover_to_grid
  - climate_to_grid
- Optionally derive principal components (PCA) to summarize major landcover and climate gradients.
- Assemble predictor datasets (x) and region grids for modelling.

## Model Tuning and Algorithms

- SDM tuning is performed with sdm_tune_ssb, which:
  - Tunes multiple SDM algorithms to optimize performance for each presence-background dataset
  - Identifies the best sampling-bias correction approach
  - Produces a model per data fold to capture uncertainty
- Four high-performing algorithms included:
  - Random Forest (down-sampled) [RF]
  - Generalised Additive Models (with regularisation) [GAM]
  - Generalised Boosted Models [GBM]
  - MaxEnt
- Evaluation metrics:
  - RF and MaxEnt: mean AUC across data blocks
  - GBM: mean cross-validated (cv) error
  - GAM: tuned with mgcv’s GCV method and regularisation to shrink unimportant parameters

## Predictions and Ensemble Modelling

- Predictions are based on ensemble models, averaging across algorithms weighted by model performance (AUC).
- To explore uncertainty, return:
  - IQR (interquartile range) of weighted mean environmental suitability
  - Hotspots (upper quartile) of weighted mean suitability
  - CV (coefficient of variation) of weighted mean suitability
  - Hotspots (upper quartile) of CV
- Ensemble outputs provide both mean suitability and associated uncertainty for landscape-wide planning.

## Visualising Model Predictions in GIS

- Visualisation options for focal windows include:
  - Weighted mean environmental suitability
  - IQR of suitability
  - Hotspots for weighted mean suitability
  - CV of suitability
  - Hotspots for CV
- Outputs support map-based decision making and identification of priority areas for management or further field validation.

## Practical GIS Workflow Considerations

- Define grid resolution and time period early to balance spatial scale with data quality and ecological relevance.
- Integrate ERCCIS with supplementary data sources (e.g., GBIF) to improve geographic extent and model robustness.
- Use spatial blocking and cross-validation to quantify uncertainty and prevent overfitting.
- Apply bias-corrected SDMs where sampling bias is evident; visualise bias and model adjustments in GIS to communicate uncertainty.
- Produce map-rich outputs suitable for policy colleagues, clients, or the public, with clear indications of where predictions are most reliable and where uncertainties are high.