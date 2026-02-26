# Working Title Component model iterations for inputs into a multi-scale model describing the effect of host conditions on Hendra virus shedding, eastern Australia, 2008-2019

## Overview
- A data package of model iteration objects and rasters to run a multi-scale model predicting how host conditions influence Hendra virus shedding in eastern Australia (2008–2019).
- Combines four component models (roost distribution, rehabilitation admissions, new roost formation, food shortage) to produce monthly, spatially explicit predictions of Hendra virus shedding.
- Includes 1,000 bootstrap iterations to quantify uncertainty and 1,000 realizations of roost locations per month.

## Data and inputs
- Component model outputs:
  - FoodShortageModels (.Rdata)
  - NewRoostModels (.Rdata)
  - RehabModels (.Rdata)
  - Roost SDM iterations (.TIF rasters; BatRoostPredictions_YYYY.tif per year)
- Input data sources and environmental features (Table 1) and training data (Table 2) are hosted in figshare.
- Model code and run framework available at GitHub: hanlab-ecol/BatOneHealth.
- Data points per component:
  - Roost Distribution Model (18,861 points; occupancy 1/0; 1996–2021; monthly; 5 km)
  - Bat Rehab (10,150 points; admissions; 2005–2020; town polygons)
  - New overwinter roosts (195 points; 2002–2019; 5 km)
  - Food Shortage (267 points; 1998–2020; single area)
- Training data derived from public and study datasets (NFFMP, ARS, WIRES, NECT, etc.).

## Spatial and temporal coverage
- Geography: Eastern Australia; 5 km spatial resolution.
- Spatial reference options:
  - GDA2020/SA Lambert (EPSG:8059) with bounds xmin 1355974, xmax 3083174, ymin 1277763, ymax 3818683.
  - WGS84 bounds: xmin 138.2032, xmax 158.3999, ymin -38.46121, ymax -14.19466.
- Temporal scope:
  - Roost SDM iterations: 1996–2021 (monthly)
  - Food Shortage: 1998–2020 (monthly)
  - Rehab: 2005–2020 (monthly)
  - New Roosts: 2002–2019 (monthly)
  - Bat predictions (BatRoostPredictions_YYYY.tif): 2007–2020 (14 years)
- Outputs synthesized monthly for 2008–2019 through 1,000 realizations per month.

## Models and methodology
- Component models and algorithms:
  - Roost Distribution Model: GBM with specified hyperparameters
  - Rehab Models: GBM with specified hyperparameters
  - New Roost Models: GBM with specified hyperparameters
  - Food Shortage Models: XGBoost with specified hyperparameters
- Hyperparameters (selected via grid search and evaluation):
  - Roost SDMIternations: learning rate 0.01, max depth 4, min observations 2, 200,000 trees
  - RehabModels: learning rate 0.0001, max depth 2, min observations 10, trees 150,000
  - NewRoostModels: learning rate 0.0001, max depth 2, min observations 2, trees 123,533
  - FoodShortageModels: learning rate 0.001, max depth 4, subsample 1, colsample_bytree 0.5, min_child_weight 1, gamma 0.5, trees 15,000
- Host condition aggregation:
  - C_xt combines P(rehab) A_xt, P(new roost) R_xt, and P(food shortage) F_t via:
    C_xt = 1 - (1 - sqrt(P(A_xt) P(R_xt))) (1 - P(F_t))
  - Null model (roost SDM only) included for comparison.
- Prediction and uncertainty:
  - For each month and location, P_xt = C_xt × MaxP (MaxP is the maximum observed roost prevalence, 66.6% from Field et al. 2015).
  - 1,000 roost location maps per month are generated, predictions within each tessellation are averaged across realizations.
  - Zero prevalences (roost absence) excluded from averages.
  - Uncertainty captured by bootstrapping input data for each model (1,000 bootstrap samples).

## Outputs and GIS relevance
- Outputs are multi-scale predictions of Hendra virus shedding for landscape mapping and spatial analysis.
- Formats:
  - Model outputs: .Rdata (GBM/XGBoost objects) for each component
  - Roost SDM rasters: .TIF (0–1 suitability)
- GIS use:
  - Create monthly risk surfaces and roost-specific prevalence maps
  - Compare model structures (eight configurations including null roost SDM)
  - Assess spatial-temporal patterns of host-condition stress and predicted virus shedding
- Data organization:
  - 1,000 iterations of each model and 1,000 roost realizations per month to support uncertainty analyses

## Quality control and references
- Model fit evaluation metric: AUC (area under the ROC curve)
- References and data sources include:
  - R packages: xgboost, gbm, caret
  - Datasets and publications detailing data sources and prior work (Field et al. 2015; Eby et al. 2022; etc.)
- Access points:
  - figshare data repository for input environmental features and training data
  - GitHub repository for reproduction of analyses

## Access and additional notes
- File naming conventions:
  - FoodShortageModels/ NewRoostModels/ RehabModels: Iteration_*.Rdata (1–1000)
  - RoostSDMIterations/: Iteration_*/ BatRoostPredictions_YYYY.tif (2007–2020; 14 files per folder)
- The dataset is designed to be used in GIS workflows to explore how host-condition stress proxies influence Hendra virus shedding across space and time in eastern Australia.