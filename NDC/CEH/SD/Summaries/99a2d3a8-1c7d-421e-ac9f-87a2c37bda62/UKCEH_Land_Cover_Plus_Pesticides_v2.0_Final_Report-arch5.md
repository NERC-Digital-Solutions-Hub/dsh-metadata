# Dataset Documentation

- This document outlines the methodology, data sources, product specifications, and validation for CEH Land Cover Plus: Pesticides v2.0, covering England, Scotland and Wales at 1 km resolution for 2012–2017.

## Purpose and scope
- Updates v1.0 to include Scotland and extend temporal coverage to 2012–2017.
- Produces high-resolution maps of average pesticide applications (kg active ingredient per year) for 162 active ingredients.
- Includes accompanying uncertainty maps to quantify confidence in estimates.
- Aims to enable applications in exposure assessment, runoff modelling, intervention targeting, and wildlife impact studies.

## Data sources and lineage
- Primary data: Pesticide Utilisation Surveys (PUS) for England, Wales, and Scotland (years 2012, 2013 fodder, 2014, 2016; Scotland also 2017 fodder; some years limited by crop type).
- Crop area data: CEH Land Cover Plus: Crops to provide crop presence per 1 km square.
- Boundaries and geographies: English/Welsh county centroids; Scottish Local Authorities; Boundary Line shapefiles; SASA data for Scotland.
- Organic areas masked in England using Organic Farming Scheme agreements; Wales/Scotland masking not applied in this version.

## Product specification
- Output resolution: 1 km; units: kg active ingredient per year per 1 km2.
- Two output layers per file: 
  - Layer 1: estimated application (kg/yr) for each active ingredient.
  - Layer 2: uncertainty (percentage) associated with the estimate.
- Coverage: England, Wales, Scotland; 162 active ingredients (herbicides, insecticides, molluscicides, fungicides, etc.).
- Temporal snapshot: average applications across 2012–2017, derived from Crops data for 2015–2017 (to reflect cropping) and PUS years for application rates.
- Data formats: TIFF or shapefiles; coordinate system: British National Grid.
- Data gaps: cells with no relevant crops or no data (e.g., mountains, urban areas) show no data.

## Methodology (high level)

- Data collation
  - Compile annual total active ingredient applications (kg) by crop and county/LA; derive annual application rates (kg/km2) per crop.
  - Exclude active ingredients with fewer than 10 observations; 171 ingredients progressed to modelling (18 removed).
  - Map county/LA locations to spatial coordinates (centroids).

- Modelling
  - For each active ingredient, model annual application rate (kg/km2 per crop) as a lognormal function of crop and location.
  - Include a continuous spatial field with a Gaussian Markov Random Field (INLA) to capture geographic variation; assume spatial pattern common across crops.
  - Treat different years as independent replicates due to limited data for temporal trend estimation.

- Predictions
  - Predict across England, Scotland, and Wales by combining per-crop application rates with 1 km2 crop-area data from LC Plus Crops.
  - Use average crop areas from 2015–2017 to reflect typical cropping and compute total annual applications per 1 km2.
  - Mask England organic areas; not masked for Wales/Scotland in this version.
  - For crops with multiple rate estimates, average estimates to avoid double counting.

- Uncertainty estimation
  - Draw 100 samples from model parameter distributions to produce 100 estimates per 1 km2 cell.
  - Compute 2.5th and 97.5th percentiles to form a 95% CI; express uncertainty as a percentage of the mean estimate.
  - Maps produced for each active ingredient showing uncertainty.

## Validation and quality checks

- Validation approach
  - Regional totals comparison with PUS statistics (for 11 selected ingredients across English regions and Scotland/Wales).
  - Posterior predictive checks to assess RMSE against null models (constant across space or crops).
- Outcomes
  - 9 of 162 models passed both validation tests; 9 excluded due to poor performance.
  - 162 ingredients retained in final product, including 36 new ingredients not in v1.0.
- Limitations
  - No national independent validation data available; validation based on regional totals and internal RMSE tests.
  - PUS data themselves contain measurement uncertainty; comparisons reflect that uncertainty.
  - Some crops (soft fruits, vegetables, etc.) may be underrepresented, leading to underestimation in some regions.

## Differences from v1.0

- Scotland included, expanding GB coverage.
- Modelling updates: removal of a global intercept; reframed spatial extent to GB-wide consistency; may increase uncertainty in areas with limited data.
- Temporal coverage extended to 2012–2017; some ingredients’ patterns differ due to Scotland data and seed-potato practices.
- 36 new active ingredients added; overall set expanded to 162.
- Differences in data handling for seed potatoes and the “other” crop category, affecting some ingredient totals.

## Data provenance and reproducibility

- Clear data provenance: PUS data, crop area data, boundary data, masking rules, and year conventions are documented.
- Modelling approach and assumptions are described, including the use of INLA, the spatial field, and cross-year replication.
- Documentation notes that some variability stems from differences in regional data availability and crop coverage.

## Usage, access, and citation

- Data access: Environmental Information Data Centre (EIDC CEH) with possible licence fees for some users.
- Citation: Jarvis, S.G.; Redhead, J.W.; Henrys, P.A.; Risser, H.A.; Da Silva Osório, B.M.; Pywell, R.F. (2020). CEH Land Cover plus: Pesticides 2012-2017 (England, Scotland and Wales). NERC Environmental Information Data Centre. https://doi.org/10.5285/99a2d3a8-1c7d-421e-ac9f-87a2c37bda62.
- Data are published as factual outputs to support research, policy, and environmental management; users should acknowledge PUS data provenance and model assumptions.
- Example outputs: maps showing spatial distribution of pesticide applications and associated uncertainties (e.g., diflufenican) with higher applications in central/eastern GB and Scotland, and higher uncertainty in areas with more variable crop practices.

## Acknowledgements and references

- Acknowledges contributions from Fera, SASA, CEH, and supported data sources.
- References include ASSIST tool, INLA methodology, and related environmental impact studies.