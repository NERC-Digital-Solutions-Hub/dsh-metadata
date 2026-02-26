# Working Title Component model iterations for inputs into a multi-scale model describing the effect of host conditions on Hendra virus shedding, eastern Australia, 2008-2019

## Overview
- A set of model iteration objects and raster data designed to run a multi-scale model predicting how host conditions influence the probability of Hendra virus shedding in eastern Australia (2008–2019).
- Combines three host-condition proxies (food shortage, rehabilitation admissions, formation of a new roost) with roost suitability predictions to generate space-time prevalence predictions.
- Includes 1,000 iterations to quantify uncertainty and is linked to code for running analyses on GitHub.

## Data objects and formats
- Model outputs:
  - FoodShortageModels (1000 Iteration_*.Rdata)
  - NewRoostModels (1000 Iteration_*.Rdata)
  - RehabModels (1000 Iteration_*.Rdata)
- Roost suitability:
  - Roost SDM Iterations: BatRoostPredictions_YYYY.tif (2007–2020; 14 files per Iteration folder)
- File formats:
  - .Rdata for model objects
  - .TIF for Roost SDM rasters
- File organization:
  - /FoodShortageModels/ Iteration_*.Rdata (1–1000)
  - /NewRoostModels/ Iteration_*.Rdata (1–1000)
  - /RehabModels/ Iteration_*.Rdata (1–1000)
  - /RoostSDMIterations/ Iteration_*/ BatRoostPredictions_YYYY.tif (2007–2020)

## Spatial and temporal scope
- Spatial resolution: 5 km
- Spatial coverage: eastern Australia (as defined by Roost SDM rasters and associated models)
- Temporal coverage:
  - Training/inputs span monthly data across multiple components (1996–2021 for environmental features; specific model periods include 1996–2021 for roost distribution, 2002–2019 for new roosts, 1998–2020 for food shortage, 2005–2020 for rehabilitation)
  - Predictions cover January 2008 to December 2019 (monthly)

## Modeling approach and hyperparameters
- Software: R (v4.3.2)
- Modeling packages: gbm (v2.1.8.1), caret (v6.0-86); FoodShortage uses XGBoost (xgbBooster)
- Hyperparameters (selected via grid search and diagnostics):
  - Roost Distribution Model: learning rate 0.01, max depth 4, min observations in a node 2, 200,000 trees
  - Bat Rehab: learning rate 0.0001, max depth 2, min obs per node 10, 150,000 trees
  - New Overwinter Roosts: learning rate 0.0001, max depth 2, min obs per node 2, ~123,533 trees
  - Food Shortage: learning rate 0.001, max interaction depth 4, subsample 1, colsample_bytree 0.5, min_child_weight 1, gamma 0.5, 15,000 trees
- Output types: model objects (gbm/xgb) and associated evaluation/hyperparameters
- Model purpose: compare eight multi-scale structures combining host-condition proxies with roost suitability (including a null roost SDM-only model) to predict Hendra virus shedding
- Uncertainty handling: bootstrap input data 1,000 times for each host-condition model; generate 1,000 roost-location realizations per month; exclude zero prevalences from averages

## Input data and sources
- Environmental features (Table 1) and training data (Table 2) sourced from figshare
- Key environmental features (examples):
  - Climate: maximum/minimum temperature, precipitation and anomalies, NDVI
  - Soil and moisture: soil moisture at 1 m, vapor pressure, potential evapotranspiration
  - Vegetation and land cover: forest cover, urban area, crop area, pasture area
  - Sun/climate indices: Oceanic Niño Index (ONI), Southern Annular Mode (SAM)
  - Other: solar exposure, crop/pasture fractions, etc.
- Data sources include:
  - Australian Gridded Climate Data (AGCD v1)
  - NOAA, BAS
  - Dynamic Land Cover Dataset (DLCD)
  - Additional datasets and derived values deposited in figshare
- Training data (Table 2) characteristics:
  - Roost Distribution Model: 18,861 data points; monthly; 1996–2021; 5 km resolution; sources NFFMP and ARS
  - Bat Rehab: 10,150 data points; monthly; 2005–2020; town polygons; WIRES
  - New Overwinter Roosts: 195 data points; monthly; 2002–2019; 5 km
  - Food Shortage: 267 data points; monthly; 1998–2020; single area; NECT

## Output data and usage
- Outputs are not modified within this dataset; intended for multi-scale Hendra shedding predictions
- Prediction framework:
  - Evaluate eight model structures by combining host-condition predictions (A: rehab, R: new roost, F: food shortage) and a null roost-SDM
  - For each space-time point, compute C_xt from the selected combination and apply P_xt = C_xt × MaxP (MaxP = 66.6%)
  - Generate monthly landscape predictions by averaging 1,000 realizations per month over 2008–2019
  - Exclude zero roost prevalences to maximize informative signal
- Outputs support replication and comparison across model structures; linked to manuscript details for full methodology
- Quality control: model fit assessed using AUC

## Access, provenance, and reuse
- Data sources and supporting materials:
  - FigShare data repository for input environmental features and training data
  - GitHub repository: hanlab-ecol/BatOneHealth (code to run models and analyses)
- Reproducibility:
  - 1,000 bootstrap iterations per host-condition model to quantify uncertainty
  - 1,000 roost-location realizations per month to generate prevalence maps
- References and methodological grounding provided within the dataset (papers and software package references)