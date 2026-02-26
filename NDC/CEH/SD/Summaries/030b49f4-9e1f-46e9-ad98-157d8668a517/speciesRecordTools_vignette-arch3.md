# Methods for Modelling Species Distributions from Unstructured Environmental Record Centre Data

## Overview
- Provides a workflow and R tooling (speciesRecordTools) to examine distributions of unstructured (opportunistic) species records, assess sampling trends and biases, and build correlative presence-background species distribution models (SDMs) for landscape prediction.
- Focuses on ERCCIS opportunistic data (Cornwall and Isles of Scilly); higher quality data should use alternative modelling approaches.
- Requires preparatory environmental predictors (e.g., land cover, climate) on a regional grid and a clearly defined focal species.

## Data sources and setup
- Define a focal species (prefer binomial/scientific name) and set the time window (start_year, end_year) to balance record volume with temporal relevance.
- Choose grid resolution (1 km, 2 km, 4 km; other grids possible via makeGrid) to balance management needs, data quality, and biology.
- Load ERCCIS data (sqlite format) as a spatial object (sf) using species_record_load; project to a common crs and subset to the focal species/groups.
- Intersect species records with a study area grid to visualise distribution within the specified period and precision.

## Data preparation and quality considerations
- Ensure data are filtered to the focal time period and precision, and prepared as spatial objects for analysis.
- Recognise metadata limitations and data governance needs (sharing underlying data appropriately, maintaining data quality and provenance).
- Prepare data for subsequent modelling, including consideration of grid alignment and spatial extent.

## Visualising distributions and sampling bias
- Visualise the spatial distribution of focal species records and assess sampling bias by comparing the focal group to a broader study area grid.
- Estimate sampling completeness for the broader species group (rarefaction-based approach) to gauge spatial sampling bias.
- Expect finding strong spatial bias (areas with little or no sampling) which informs the need for bias correction in SDMs.

## Modelling approach
- Augment ERCCIS records with additional data sources (e.g., GBIF) to model distributions across a broader context (England) and predict within the Cornwall region.
- Create a blocking grid for systematic model evaluation; ensure the grid resolution is larger than environmental data resolution.
- Prepare environmental predictors (landcover, climate) on the grid; optionally use PCA to reduce dimensionality.
- Use prepare_sdm_data to generate presence-background datasets for combinations of filter distance (fdist) and buffer distance (bdist) to mitigate spatial sampling bias; initial example uses a single configuration.
- Model tuning and selection via sdm_tune_ssb, which evaluates multiple algorithms and selects the best bias-corrected approach.
- Supported algorithms (high-performing in presence-only SDMs): Random Forest (RF), Generalised Additive Models (GAM), Generalised Boosted Models (GBM), and MaxEnt.
- Model tuning aims to optimize predictive performance (e.g., AUC for RF/MaxEnt; cross-validated error for GBMs; GAMs tuned with GCV and regularisation).

## Predictions, outputs and visualisation
- Generate ensemble predictions by weighting individual model predictions by performance; include uncertainty metrics (e.g., interquartile range, coefficient of variation) and hotspot indicators.
- Visualise spatial predictions via:
  - Weighted mean environmental suitability
  - IQR of suitability
  - Hotspots for weighted mean suitability
  - CV of suitability
  - Hotspots for CV
- Outputs can be mapped to show relative site suitability and the associated uncertainty, supporting management and policy decisions.

## Implications for monitoring frameworks
- Provides a transparent, reproducible workflow to assess species distributions from unstructured data while accounting for sampling bias and data gaps.
- Enables integration of multiple data sources to improve spatial coverage and outlooks for policy decisions.
- Delivers quantifiable measures of uncertainty and spatial bias, essential for evaluating environmental health measures and informing future monitoring decisions.
- Highlights the need for appropriate metadata, data governance, and data-sharing practices to maximize usefulness for oversight and decision-making.