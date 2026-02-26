# Methods for Modelling Species Distributions from Unstructured Environmental Record Centre Data

## Overview
- Provides an R workflow (via speciesRecordTools) to examine unstructured/opportunistic species records, assess sampling trends and biases, and build presence-background species distribution models (SDMs) for predicting species distributions.
- Focuses on Environment Record Centre for Cornwall and the Isles of Scilly (ERCCIS) data; can incorporate higher-quality data or GBIF data to broaden context.
- Requires preparation of environmental predictor data (e.g., land cover, climate) aligned to model grids.

## Data and Data Preparation
- Data sources
  - Primary: ERCCIS opportunistic records (sqlite database), queried for focal species/groups and returned as spatial (sf) objects projected to a chosen CRS.
  - Optional: GBIF records to broaden geographic coverage (recommended for best practice).
- Focal configuration
  - Choose focal species and a focal time window (start_year, end_year) to balance record numbers with temporal relevance.
  - Use binomial/scientific name for clarity and reproducibility.
- Grid and resolution
  - Analyses run on predefined grid resolutions (1 km, 2 km, 4 km); other grids can be created with makeGrid.
  - Grid resolution chosen to balance management needs, data quality, and biological constraints.
- Data loading
  - Data loaded with functions like species_record_load from an ERCCIS sqlite file; data can be transformed to projected coordinates via regional sf objects.
- Visualisation and exploration
  - Intersections with study-area grids facilitate visualization of distribution and sampling bias.
  - Temporal filtering and precision controls allow focusing on data within the focal period and quality thresholds.

## Spatial and Temporal Configuration
- Grid and time setup
  - Define the spatial grid scope (e.g., England, Cornwall) and resolution appropriate for management questions.
  - Set start_year and end_year to constrain records to a relevant temporal window.
- Spatial extents and projections
  - Outputs are sf objects projected to a user-specified CRS, enabling integration with other spatial datasets.

## Data Quality and Bias Assessment
- Sampling bias challenges
  - Opportunistic records often lack explicit effort measures; spatial bias is common and affects SDMs.
- Assessing bias
  - Use a rarefaction-based approach to estimate sampling completeness at the group level (e.g., terrestrial mammals) to infer likely biases for the focal species.
  - Example outputs indicate strong spatial bias with many areas poorly sampled, signaling the need for bias-correction steps in SDMs.
- Implications for stewardship
  - Document bias estimates and ensure modelling approaches include bias mitigation (e.g., presence-background design, buffering, and thoughtful predictor selection).

## Modelling Approach
- Data preparation for SDMs
  - Create presence-background datasets for combinations of filter distance (fdist) and buffer distance (bdist) to evaluate spatial bias effects on model performance.
  - Option to use ERCCIS data alone for efficiency or include GBIF data for broader context.
- Environmental predictors
  - Prepare gridded landcover and climate rasters; options to use raw predictors or principal components (PCA) to reduce dimensionality.
- Model training and tuning
  - Use prepare_sdm_data to generate PB datasets and sdm_tune_ssb to tune four SDM algorithms and select the best bias-correction approach.
  - Algorithms included: Random Forest (RF), Generalised Additive Models (GAM), Generalised Boosted Models (GBM), and MaxEnt.
  - Evaluation metrics: AUC for RF and MaxEnt; cross-validated error for GBMs; GAMs tuned with mgcv's GCV and regularisation.
- Ensemble predictions and uncertainty
  - Predictions are typically ensemble-based, averaging across models weighted by performance.
  - Uncertainty quantified via metrics such as interquartile range (IQR), coefficient of variation (CV), and hotspots (upper quartile of mean and CV).

## Outputs and Visualization
- Model outputs
  - Ensemble predictions of environmental suitability across the study area and focal window.
  - Separate model realizations (one per data fold) to explore data uncertainty.
- Visualization options
  - Spatial maps of weighted mean suitability, IQR, hotspots for mean suitability, CV, and hotspots for CV.
  - Tools to create focal maps and time-series visualizations to assess temporal variation in records.
- Practical outputs
  - Functions and example workflows (e.g., sp.ens ensemble creation, focal_mapping, and species-specific plotting) facilitate interpretation and communication of results.

## Practical Considerations for Data Stewards
- Standards and governance
  - Ensure data provenance is clear (ERCCIS as primary source; GBIF as supplementary), with appropriate versioning and metadata.
  - Document filtering criteria (time window, spatial precision) and modelling choices (grid resolution, fdist/bdist settings).
- Metadata and reproducibility
  - Capture all steps: data extraction, cleaning, grid creation, predictor preparation, PB dataset construction, model tuning, and ensemble evaluation.
  - Reproducible workflows are essential given the computational intensity (environmental gridding, multiple model runs).
- Interoperability and scalability
  - Grid-based outputs and predictor rasters should be compatible with other datasets and local decision-making tools.
  - While GBIF inclusion can enhance context, the workflow supports ERCCIS-only analyses for efficiency; extending to GBIF requires additional data handling.
- Data quality implications
  - Bias assessments inform the need for bias-corrected modelling and transparent communication of uncertainty to stakeholders.
- Governance of updates
  - When ERCCIS or GBIF data are updated, re-running the workflow with updated records will require versioned outputs and documentation of changes in model results.

## Limitations and Challenges
- Dependence on opportunistic data quality and coverage, which can introduce spatial bias and uneven sampling.
- Requires substantial preprocessing of environmental predictors and careful selection of grid resolution relative to data quality.
- Best practice benefits from integrating broader data sources (e.g., GBIF) to reduce context-specific biases.