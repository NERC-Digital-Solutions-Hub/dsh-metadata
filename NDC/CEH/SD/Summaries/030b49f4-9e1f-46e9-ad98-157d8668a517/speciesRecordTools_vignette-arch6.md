# Methods for Modelling Species Distributions from Unstructured Environmental Record Centre Data

## Overview
- R package speciesRecordTools enables examination of unstructured opportunistic records, assessment of sampling trends and biases, and creation of correlative presence-background species distribution models (SDMs) for predicting species distributions across landscapes.
- Designed to work with Environmental Record Centre for Cornwall and the Isles of Scilly (ERCCIS) opportunistic data; for higher-quality data, alternative modelling approaches are advised.
- Requires environmental predictors (e.g., land cover, climate) prepared in advance.

## Data sources and focal setup
- Data source: ERCCIS opportunistic records; augmented with GBIF data for broader England context.
- Focus: a focal species (binomial name preferred) and its records, sampling bias, and potential predicted distributions.
- Study scale and grid: analyses run on predefined grids (default options include 1 km, 2 km, and 4 km resolutions); other grids possible via makeGrid.
- Temporal focus: specify start and end year to balance record sufficiency with temporal relevance.
- Data loading: ERCCIS data loaded from a .sqlite database (requires path and species group); records are converted to a spatial object (sf) projected to a chosen CRS.

## Data preparation and quality considerations
- Intersect focal records with a study-area grid to visualize distribution and sampling bias within the specified time period and precision.
- Sampling bias assessment: evaluate spatial sampling completeness for a broader species group (using rarefaction-based approaches) to infer likely biases affecting the focal species.
- Outputs highlight areas with strong spatial sampling bias, indicating where bias correction will be needed in SDMs.

## Modelling workflow
- Spatial structuring: build a blocking grid (blockGrid) across the region to support cross-validation and model evaluation; grid resolution should exceed that of environmental data.
- Environmental data preparation: grid land cover (landcover_to_grid) and climate (climate_to_grid) into terra spatrast objects; consider using principal components (PCA) to reduce dimensionality while capturing key gradients.
- Presence-background data preparation: use prepare_sdm_data to create presence-background datasets for combinations of fdist (filter distance) and bdist (buffer distance); example uses a single configuration for efficiency.
- Data scope: you can run with ERCCIS only or include GBIF data (gbif_include option) for broader geographic context.
- Model tuning and selection: sdm_tune_ssb tunes multiple SDM algorithms to optimize performance for each presence-background dataset and identifies the best sampling-bias correction approach.
- Model algorithms included:
  - Random Forest (down-sampled)
  - Generalised Additive Models (GAM) with regularisation
  - Generalised Boosted Models (GBM)
  - MaxEnt
- Model evaluation: performance metrics differ by algorithm (e.g., AUC for RF and MaxEnt; cross-validated error for GBMs; GAMs use GCV with regularisation).

## Predictions and uncertainty
- Predictions are ensemble-based, averaging across models weighted by performance.
- Uncertainty assessment includes:
  - Interquartile range (IQR) of weighted predictions
  - Coefficient of variation (CV)
  - Hotspots identified in upper quartiles for both mean suitability and CV
- Outputs enable exploration of relative site suitability and associated uncertainties across the landscape.

## Visualisation and data products
- Spatial and temporal visualisations of predicted distributions and sampling bias.
- Example visualisation tools include focal_mapping-based outputs and related plotting functions to display:
  - Weighted mean environmental suitability
  - IQR and hotspots for suitability
  - CV and hotspots for prediction uncertainty
- Generated maps and summaries support decision-making and communication of results to stakeholders.

## Practical considerations and applications
- Augmenting ERCCIS with GBIF data can improve model robustness by extending geographic context.
- Environmental data preparation is a major step; computationally intensive but streamlined by dedicated functions.
- Bias correction is often required due to uneven sampling effort in opportunistic records; sampling completeness informs bias mitigation strategies.
- Outputs (SDMs, maps, and uncertainty metrics) are suitable as data products for planning, conservation, and policy discussions, particularly for local councils or organizations with broad data-use needs.

## How this supports data work (Data Support perspective)
- Integrates disparate data sources (ERCCIS and GBIF) into coherent SDMs, enabling end users to explore distribution patterns and uncertainty.
- Produces ready-to-use data products (predictive maps, bias assessments, and summaries) that can be shared with non-technical stakeholders.
- Documents a transparent workflow (data preparation, bias assessment, model tuning, ensemble predictions) that can be replicated or extended for other species or regions.
- Highlights data quality issues (e.g., spatial sampling bias) and provides a pathway for bias-aware decision-making and model refinement.