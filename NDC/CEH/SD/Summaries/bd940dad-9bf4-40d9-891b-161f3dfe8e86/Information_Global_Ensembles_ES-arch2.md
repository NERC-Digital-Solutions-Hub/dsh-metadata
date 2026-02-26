# Global ensembles of Ecosystem Service map outputs modelled at 1km resolution for water supply, recreation, carbon storage, fuelwood and forage production

## Overview
- Global dataset of ensemble ecosystem service maps for five services: water supply, recreation, above-ground carbon (AG carbon), forage, and fuelwood.
- Outputs produced at about 1 km resolution (0.008333° grid) or catchment-based for water supply.
- Each service includes multiple ensemble approaches to capture uncertainty and improve robustness.
- Normalised to a 0–1 scale to allow cross-model comparability; uncertainty shown as the Standard Error of the Mean (SEM).

## Data content and structure
- 28 raster (TIFF) layers plus world-files for five ES services across six among-model ensemble approaches; each raster contains per-cell ensemble estimates.
- 1 shapefile for water supply at catchment scale (HydroSHEDS catchments), with six ensemble estimates and SEM per catchment.
- Grid and coverage:
  - Rasters: global, except smaller islands with no data coverage; exact grid 0.0083333333° (~1 km at equator); dimensions 43,200 x 18,600.
  - Water supply: catchment polygons for 15,289 HydroSHEDS catchments worldwide.
- Units: Relative service delivery, normalised to 0–1.
- No-data value: -999.

## Data sources and model frameworks
- Origin: EnsemblES project, integrating ensemble techniques to quantify ES model accuracy and sensitivity.
- Participating models and outputs include: InVEST, ARIES, WaterWorld, Co$ting Nature, LPJ-GUESS, TEEB, Scholes, Aqueduct, FAO livestock distributions, and biomass/forest datasets (e.g., ESA CCI, GEOCARBON, Global Forest Watch).
- Model counts per service vary:
  - Water supply: 8 models
  - Recreation: 5 models
  - Above-ground carbon: 14 models
  - Forage: 9 models
  - Fuelwood: 12 models
- Some inputs are online tools or existing outputs; licenses may apply.

## Processing and normalisation
- Per-model predictions are computed per gridcell; for accumulated water models, maximum per HydroSHEDS polygon; non-accumulated water models summed to the pour point.
- Gridding: forced 0.001° grid to minimise edge effects.
- Normalisation: within-model normalisation to 0–1 using a Winsorising approach (2.5th and 97.5th percentiles) to limit extreme values; normalization applied before ensemble creation.
- Documentation and code: Matlab and ArcGIS Python/ArcPro code available; normalization approach described and implemented via GitHub (GlobalEnsembles/Winsorising).

## Ensemble methods
- Unweighted ensembles: mean and median across models (ArcGIS cell statistics); memory-efficient with a bagging approach (jackknife over 1,000,000 points, 250 runs); weights averaged across runs.
- Weighted ensembles (untrained/without validation data):
  - PCA ensemble: weights proportional to model loadings on the first principal component (consensus axis).
  - Correlation coefficient ensemble: weights based on each model’s mean correlation with all others.
  - Regression-to-the-median ensemble: iterative log-likelihood regression to derive weights that best approximate the median ensemble; no intercept.
  - Leave-one-out cross-validation ensemble: iterative regression leaving out one model at a time; mean coefficients across models used as weights.
- Equation framework: ensemble value per location x is a weighted sum of model outputs Y_i with weights ω_i normalized to sum to 1.
- Weights are computed per run and averaged for mapping.

## Uncertainty and quality control
- Uncertainty captured as Standard Error of the Mean (SEM) across contributing models and across ensemble approaches.
- Quality control: full internal team review (11 authors) and external peer review; most input models are peer-reviewed or widely accepted.
- Supporting information includes extensive model references and data sources; documents multiple data provenance checks.

## Output interpretation and use
- Outputs provide a consistent, comparable view of ES delivery across time and space, enabling monitoring of environmental health and policy performance.
- Water supply is provided per catchment; other services are global rasters at ~1 km resolution.
- SEM maps allow users to assess agreement among models and identify areas of higher uncertainty.
- Suitable for integration with other environmental datasets to enhance monitoring, reporting, and decision-making.

## Access, use and licensing
- Data sources and some inputs may be subject to license restrictions.
- Original code and workflows are available via GitHub (GlobalEnsembles) and related repositories; data provenance is documented in the Supplement and Table 1.
- Funded under the EnsemblES project and related UKRI/MobilES/RUST programs.

## Funding and references
- Funding: EnsemblES project—Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models; UKRI Landscape Decisions programme (NE/T00391X/1); MobilES (ES/R009279/1); RUST (ES/T007877/1).
- Key references cover ensemble methods, ES modeling frameworks, and supporting biodiversity/biomass datasets used as inputs.