# Component model iterations for inputs into a multi-scale model describing the effect of host conditions on Hendra virus shedding, eastern Australia, 2008-2019

- Purpose
  - Provide model iteration objects and rasters to run a multi-scale model predicting how host condition influences the probability of Hendra virus shedding.
  - Compare multiple model structures (eight combinations of host-condition proxies plus a roost-suitability-only null model) against observed virus shedding to assess whether incorporating host condition improves predictions in space and time.
  - Generate 1,000 iterations to account for uncertainty and produce monthly, spatially explicit predictions across eastern Australia (2008–2019).

- Data and inputs
  - Proxies for host conditions (three components): food shortage, rehabilitation admissions, formation of a new roost.
  - Roost Species Distribution Model (Roost SDM) predictions of roost suitability (occupancy likelihood).
  - Data sources linked to models and analyses via GitHub: hanlab-ecol/BatOneHealth.
  - Input environmental features (Table 1) from AGCD v1, NOAA, BAS, and Dynamic Land Cover Dataset (DLCD); training data (Table 2) from figshare.
  - Spatial and temporal scope of inputs:
    - Environmental features at 5 km resolution; monthly scale; spatial coverage across eastern Australia.
    - Training for Roost SDM (1996–2021; monthly; 5 km).
    - Training for Bat Rehab, New Overwinter Roosts, and Food Shortage models (varies by model; 1996–2021 inputs overall; different temporal extents per model).
  - Data organization:
    - 1,000 iterations of each model type (FoodShortageModels, NewRoostModels, RehabModels).
    - 1,000 RoostSDMIterations folders, each containing BatRoostPredictions_YYYY.tif for 14 years (2007–2020).
    - Model outputs are not modified; outputs feed multi-scale predictions.

- Models and hyperparameters
  - Model types and tools:
    - RoostSDMIternations: gbm-based spatiotemporal roost occupancy models.
    - RehabModels: gbm-based models for rehabilitation admissions.
    - NewRoostModels: gbm-based models for probability of new overwintering roosts.
    - FoodShortageModels: XGBoost-based model for probability of food shortages.
  - Hyperparameters (selected via grid search and evaluation):
    - RoostSDMIternations: learning rate 0.01, max depth 4, min observations in a node 2, 200,000 trees.
    - RehabModels: learning rate 0.0001, max depth 2, min observations per node 10, 150,000 trees.
    - NewRoostModels: learning rate 0.0001, max depth 2, min observations per node 2, ~123,533 trees.
    - FoodShortageModels: learning rate 0.001, max interaction depth 4, subsampling 1, column sampling 0.5, min child weight 1, gamma 0.5, 15,000 trees.
  - Software environment: models built in R (v4.3.2); gbm, caret; FoodShortageModels use XGBoost; references to xgboost package provided.

- Output data and integration
  - Prediction framework:
    - Host-condition predictions (C_xt) derived from combinations of the three proxies and a possible null roost-suitability model.
    - Spatial stress computed as the geometric mean of rehabilitation and new roost formation; combined with food shortage to produce a cumulative stress measure.
    - Combined formulation for all three host-condition components:
      C_xt = 1 - (1 - sqrt(P(A_xt) P(R_xt))) (1 - P(F_t))
    - Monthly landscape prevalence predictions:
      P_xt = C_xt × MaxP, where MaxP is capped at 66.6% to match the highest observed roost prevalence (Field et al. 2015).
    - For each month, 1,000 roost-location realizations to derive P_xt maps; bootstrapped host-condition inputs (1,000 resamples) to propagate uncertainty.
    - Exclusion of zero prevalence values (roost absence) from averages to maximize informative signal.
  - Outputs are used to produce multi-scale predictions of Hendra virus shedding over space and time.
  - Quality control: model fit evaluated via AUC.

- Spatial and temporal coverage
  - Spatial
    - Eastern Australia; Roost SDM rasters with bounds given in GDA2020/SA Lambert projection (EPSG:8059) and WGS84 bounds for mapping.
    - Spatial resolution: 5 km.
  - Temporal
    - Inputs and training data span from mid-1990s to early 2020s (vary by model).
    - Predictions cover monthly time steps from 2008 to 2019 (Roost and host-condition mappings).

- Data sources and accessibility
  - Input environmental features and training data hosted on figshare (data and tables referenced).
  - Roost and host-condition datasets assembled from:
    - National Flying Fox Monitoring Program (NFFMP), ARS roost data, WIRES submissions.
    - Nectar shortage data (NECT), forest cover, urban area, crop area, pasture area (DLCD; NOAA BAS).
  - Code and workflows available on GitHub (hanlab-ecol/BatOneHealth) for running models and analyses.

- Reproducibility and uncertainty
  - Uncertainty captured by 1,000 bootstrap iterations for host-condition models and 1,000 random realizations of roost distributions per month.
  - Predictions include uncertainty propagation and exclusion of non-informative zero roost-absence prevalences to maximize signal.

- Related references and software
  - R packages: xgboost, gbm, caret; cited versions and sources.
  - Key studies and datasets informing model structure and validation (e.g., Field et al. 2015; Eby et al. 2022; related data repositories and methods).