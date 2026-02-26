# Working Title Component model iterations for inputs into a multi-scale model describing the effect of host conditions on Hendra virus shedding, eastern Australia, 2008-2019

- Purpose
  - Provide model iteration objects and spatial rasters to run a multi-scale modelling process predicting how host conditions influence the probability of Hendra virus shedding.
  - Compare eight model structures (three host-condition proxies plus combinations, plus a roost-only null model) against observed virus shedding; quantify uncertainty with 1,000 iterations.

- Data and file formats
  - Model outputs: FoodShortageModels, NewRoostModels, RehabModels stored as .Rdata; Roost SDM outputs as .TIF.
  - Folder and file naming: 1,000 Iteration_*.Rdata files for each of FoodShortageModels, NewRoostModels, RehabModels; RoostSDMIterations contain Iteration_* folders with BatRoostPredictions_YYYY.tif files (YYYY 2007–2020; 14 files per folder).
  - Linked code: analyses runnable via BatOneHealth GitHub repository (hanlab-ecol/BatOneHealth).

- Spatial and temporal coverage
  - Spatial resolution: 5 km grid cells; roost SDMs also in raster format.
  - Spatial bounds: provided in two coordinate reference systems (GDA2020/SA Lambert and WGS84); Roost SDMs cover eastern Australia with 5 km resolution.
  - Temporal scope: monthly data across multiple components:
    - Food Shortage: 1998–2020 (one region)
    - New Roosts: 2002–2019 (5 km grid cells)
    - Bat Rehab: 2005–2020 (town polygons)
    - Roost SDM iterations: 1996–2021
  - Study period focus for predictions: 2008–2019

- Models and hyperparameters
  - Modeling platform: R 4.3.2; gbm and caret (with XGBoost for Food Shortage).
  - Roost Distribution Model (RoostSDMIterations): gbm-based; learning rate 0.01, max depth 4, min observations per node 2, 200,000 trees.
  - Bat Rehab (rehab models): gbm-based; learning rate 0.0001, max depth 2, min obs per node 10, 150,000 trees.
  - New Overwinter Roosts (NewRoostModels): gbm-based; learning rate 0.0001, max depth 2, min obs per node 2, ~123,533 trees.
  - Food Shortage (FoodShortageModels): XGBoost; learning rate 0.001, max depth 4, subsample 1, colsample_bytree 0.5, min_child_weight 1, gamma 0.5, 15,000 trees.
  - Hyperparameters determined via grid search and evaluation; detailed in associated manuscript Supporting Information.

- Input data and features
  - Environmental features (Table 1) drawn from multiple sources: Australian Gridded Climate Data (AGCD v1), NOAA, British Antarctic Survey (BAS), Dynamic Land Cover Dataset (DLCD).
  - Key variables include:
    - Temperature: max (tempMax), min (tempMin), and tempDiff (max−min)
    - Precipitation: total (prec) and precipitation anomaly (prec_anom)
    - Vegetation: NDVI
    - Soil moisture at 1 m
    - Atmospheric variables: vapor pressure (9:00 AM), solar exposure, potential evapotranspiration
    - Oceanic and atmospheric indices: Oceanic Niño Index (ONI), Southern Annular Mode (SAM)
    - Land cover: forest cover, urban area, crop area, pasture area
  - Data resolution and scope: all at 5 km; locations marked for Rehab, New Roosts, and Food Shortage components.
  - Training data sources per component:
    - Roost Distribution Model: NFFMP, ARS
    - Bat Rehab: WIRES
    - New Overwinter Roosts: ARS
    - Food Shortage: NECT (nectar shortage)

- Output data and use
  - Outputs are not modified and are used to generate multi-scale predictions of Hendra virus shedding.
  - Prediction framework:
    - Host condition proxy predictions (P(Ax,t), P(Rx,t), P(Ft)) combined to form Cxt via:
      Cxt = 1 − (1 − sqrt(P(Ax,t) × P(Rx,t))) × (1 − Pt(F))
    - Predicted prevalence Px,t = Cxt × MaxP, with MaxP set to 66.6% based on large roost survey.
    - For each month, 1,000 roost-location maps are produced, host-condition realizations are bootstrapped (1,000 iterations), and prevalence is averaged across realizations.
  - Uncertainty handling: bootstrap host-condition models 1,000 times; each monthly roost map associated with a bootstrapped model; zero prevalences from roost-absent locations excluded from averages.

- Quality control and evaluation
  - Model performance assessed with area under the receiver operating characteristic curve (AUC).

- Reproducibility and references
  - Data and methods reference widely used datasets and tools:
    - xgboost and gbm/caret packages
    - Roost and bat ecology datasets (NFFMP, ARS, WIRES)
    - Supporting literature on Hendra virus spillover and bat ecology
  - Data sources and software references are provided alongside the dataset and model descriptions.