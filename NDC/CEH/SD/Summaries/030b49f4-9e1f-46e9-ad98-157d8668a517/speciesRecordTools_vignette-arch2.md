# Methods for Modelling Species Distributions from Unstructured Environmental Record Centre Data

- Purpose and scope
  - R package speciesRecordTools provides tools to explore distribution of unstructured (opportunistic) species records, examine sampling trends and biases, and build presence-background species distribution models (SDMs) to predict species distributions across landscapes.
  - Primarily demonstrated with Environmental Record Centre for Cornwall and the Isles of Scilly (ERCCIS) opportunistic records; higher-quality data should use alternative modelling approaches.

- Setup and data prerequisites
  - Define focal species (prefer binomial/scientific name) and set a focal time window (start_year to end_year) and a grid resolution that balances management needs with data quality (default options include 1km, 2km, 4km; custom grids can be created).
  - Prepare environmental predictors (e.g., land cover, climate) to be used in the SDMs.
  - Data should be accessible as an ERCCIS .sqlite database; load with species_record_load and project to a chosen CRS, returning a spatial object.

- Data preparation and exploration
  - Intersect focal species data with a study-area grid to visualize distribution and sampling precision; filter by time period.
  - Assess sampling bias and completeness:
    - Directly evaluating spatial sampling bias for a single species is difficult due to unknown effort.
    - Use sampling completeness at the group level (rareﬁaction-based) to infer broad spatial bias patterns.
    - Example outputs indicate strong spatial bias with many areas lacking sampling coverage, implying bias corrections are needed for SDMs.

- Modelling framework and data augmentation
  - Optionally augment ERCCIS records with GBIF data to model across England while focusing predictions back to Cornwall.
  - Create a systematic spatial blocking grid (blockGrid) larger than predictor data resolution to support cross-validation and model evaluation.
  - Prepare gridded environmental data:
    - Use landcover_to_grid and climate_to_grid to convert predictors to grids.
    - Consider principal components (PCA) to reduce dimensionality if many predictors are used.

- Presence-background data preparation
  - Use prepare_sdm_data to generate presence-background datasets for each combination of fdist (filter distance) and bdist (buffer distance).
  - For efficiency, a single PB dataset can be produced by using a single fdist/bdist; GBIF data can be included or excluded (gbif_include) as needed.
  - Parameters include region, grain, time window, precision, occFilter, occBuffer, blockGrid, and nfolds for cross-validation.

- Model fitting and tuning
  - Run sdm_tune_ssb to tune multiple SDM algorithms for each PB dataset and identify the best spatial sampling bias (SSB) correction approach.
  - Algorithms included:
    - Random Forest (RF)
    - Generalised Additive Models (GAM)
    - Generalised Boosted Models (GBM)
    - MaxEnt
  - Models are tuned to maximize predictive performance, with evaluation metrics:
    - RF and MaxEnt: mean AUC across data blocks
    - GBMs: mean cross-validation error
    - GAMs: guided by generalized cross-validation (GCV) with regularisation
  - Outputs are ensemble-ready models and predictions for each data fold, enabling exploration of data uncertainty.

- Predictions and ensemble
  - Generate predictions using ensemble modeling that averages across models weighted by performance (e.g., AUC).
  - Assess uncertainty via:
    - Interquartile range (IQR) and coefficient of variation (CV) of ensemble predictions
    - Hotspots based on upper quartiles of mean predictions and CV
  - The ensemble framework provides a robust estimate of site suitability and associated uncertainty across the landscape.

- Visualization and outputs
  - Visualize model predictions across focal windows with options including:
    - Weighted mean environmental suitability maps
    - IQR and CV maps to illustrate uncertainty
    - Hotspot maps for high suitability and high uncertainty
  - Example visualization workflows include focal_mapping-based plots and exporting results for reporting.

- Practical considerations and interpretation
  - Grid resolution should be chosen to balance management needs and ecological realism; ensure environmental predictors align with the chosen resolution.
  - Incorporating a broader geographic context (e.g., GBIF data) can improve model generality but increases computational demand.
  - Expect biases due to opportunistic data; apply sampling bias corrections and consider focusing on landscape-level inferences when data are sparse.
  - The workflow supports generating informative, policy-relevant outputs (distribution predictions, uncertainty, and hotspot regions) to monitor environmental health and guide decisions.