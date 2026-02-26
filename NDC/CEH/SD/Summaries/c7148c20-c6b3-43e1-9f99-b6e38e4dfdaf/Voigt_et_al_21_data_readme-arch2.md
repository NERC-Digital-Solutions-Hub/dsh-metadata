# Past deforestation (2000-2018) and future deforestation probability (2019-2053) for Wallacea

## Overview
- A dataset and modelling framework to assess patterns and drivers of forest loss and fragmentation in Wallacea, Indonesia, and to project deforestation probability to 2053.
- Provides a baseline for monitoring environmental governance and conservation amidst significant policy changes in Indonesia.
- Funded by the Newton Fund’s Wallacea Programme (NERC NE/S007067/1) and the Indonesian Ministry for Research, Technology & Higher Education.

## Data Description
- Files
  - A: forest_2014_18_180m.tif — Primary forest cover in 2014 (coded 1); forest loss between 2000 and 2013 (coded 0); non-forest -9999. Used to train the deforestation model.
  - B: deforestation_2014_18_180m.tif — Primary forest loss from 2014 to 2018 (coded 1); all else -9999. Used to train the deforestation model.
  - C: summed_deforestation_probability_20xx_20xx_Wallacea.tif — Summed probability of deforestation for 5-year intervals from 2019 to 2053; values reflect the number of iterations (out of 100) in which a pixel was deforested.
- Relationship
  - Files A and B, together with predictor variables described in Table 1 of Voigt et al. 2021, were used to produce File C.
- Spatial and temporal characteristics
  - Geographic scope: Wallacea, Indonesia.
  - Resolution: 180 m pixel size; grid size 10102 x 10593.
  - Projection: Asia South Albers Equal Area Conic (EPSG:9001); Units: metres.
  - Data format: GTiff/GeoTIFF; NoData value -9999.
  - Temporal coverage: Training period 2000-2018; projections 2019-2053 in 5-year intervals; 100 model iterations per interval.

## Modelling and Methods
- Forest definition
  - Forest: primary forest defined as mature natural forest >5 ha, with closed canopy (>90%), high carbon stock; mangroves included; excludes plantations, regrowth, agro-forests, and non-vegetated areas.
  - Forest loss: based on Tree Loss dataset v1.6 (Hansen et al.) from Landsat time-series; pixels with >70% canopy cover; aggregated to 180 m to reduce small-scale noise.
- Modelling framework
  - Logistic model for forest loss: Pt loss_x,t = 1 / (1 + exp(-k_x,t)); k_x,t is a linear combination of predictors.
  - Predictor set: as detailed in Voigt et al. 2021 (forest cover and loss, slope, fire activity, accessibility, human population pressure, main commodity, transmigrant settlements, mining, land-use).
  - Model fitting: forward stepwise regression across sub-regions; 56-79 candidate models; parameter estimation via Filzbach (MCMC) to obtain posterior means and credible intervals.
  - Model selection: cross-validation with a 50% holdout to assess predictive power; the best model is chosen based on maximum test likelihood.
- Simulation and uncertainty
  - Simulations update Pt loss_x,t each time step using parameters drawn from the Gaussian distribution of the MCMC results; pixel deforestation is determined by comparing to a random draw (0-1).
  - 100 iterations per time-step to capture uncertainty; results aggregated into summated_deforestation_probability files (File C).
  - Temporal dynamics: all predictors treated as static, except neighbourhood deforestation which is updated each time step.

## Data Processing and Tools
- Data processing and analysis performed in Python and R; geospatial work done in ArcGIS Pro.
- All layers converted to Asia South Albers Equal Area Conic projection; resampled to a common extent and origin, pixel size 180 m (bilinear for continuous predictors, nearest-neighbour for categorical).

## Outputs and Intended Use
- Primary outputs: training data (A and B) and projected, aggregated deforestation probability (C) for 2019-2053 in 5-year intervals.
- Purpose: establish a standardized baseline and enable monitoring of deforestation risk and governance effectiveness over time.
- Outputs support environmental monitoring, planning, and policy evaluation in Wallacea.

## Data Quality and Validation
- Model validation includes cross-validation to ensure predictors have predictive value.
- Uncertainty quantified via multiple (100) simulation iterations, with parameter uncertainty propagated through to the summed probability outputs.

## Funding and Data Provenance
- Funding: Newton Fund Wallacea Programme via NERC (NE/S007067/1) and Indonesian Ministry for Research, Technology & Higher Education.
- Data sources and predictors drawn from established datasets (Giri et al., Hansen et al., Margono et al., MODIS/VIIRS fire data, World Bank/World Resources Institute accessibility data, Indonesian statistics, etc.).
- Related publication: Voigt et al. 2021 (deforestation modelling and predictors).

## Access and Documentation
- Data described with a readme (Voigt_et_al_21_data_readme) and metadata; all files share consistent geographic characteristics and coordinate systems.
- File metadata and references provided to facilitate reproducibility and further use within monitoring and policy analysis workflows.