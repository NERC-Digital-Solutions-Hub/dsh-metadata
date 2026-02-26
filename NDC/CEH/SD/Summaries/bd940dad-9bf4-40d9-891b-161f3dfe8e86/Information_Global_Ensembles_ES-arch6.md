# Global ensembles of Ecosystem Service map outputs modelled at 1km resolution for water supply, recreation, carbon storage, fuelwood and forage production

## Overview
- Global ecosystem service maps produced at ~1-km resolution across five services: water supply, recreation, above-ground carbon, forage, and fuelwood.
- Uses six ensemble approaches to capture uncertainty and improve accuracy.
- Outputs include 28 raster layers plus one catchment-based shapefile for water supply, with an accompanying map of variation among models (SEM).
- Normalised units (0–1; relative service delivery); NoData value is -999.

## Data content and formats
- 28 TIFF raster layers with 32-bit floating point values, each named Ensemble_Approach_Service_Ensemble_Publish.tif.
- One water supply shapefile (WaterSupply_Ensembles_HydroSHEDS) with catchment polygons; 15,289 HydroSHEDS catchments used.
- Gridded rasters use a fixed grid 0.0083333° × 0.0083333° (approx. 1 km at the equator); raster dimensions are 43,200 × 18,600.
- Projection: World Geodetic System 1984 (EPSG 4326).
- Units: Relative service delivery; scale 0–1.
- Data coverage: Global, with exclusion of smaller islands lacking data coverage for the respective ecosystem service.

## Origin and inputs
- Originates from the EnsemblES project, funded under the UKRI Landscape Decisions programme, with additional funding from MobilES and RUST.
- Ensemble maps reflect multiple modelling approaches to assess ES, integrating outputs from various models.
- Model frameworks and their validations were prepared (as of 2023) and are described in Willcock et al. (2023); related Matlab and ArcGIS Python codes are available at the GlobalEnsembles repository.
- Model inputs include a broad set of ecosystem service models; not all inputs cover the entire globe.

## Models and inputs (per service)
- Multi-service frameworks include ARIES, Co$ting Nature, InVEST, LPJ-GUESS, TEEB, Scholes, Aqueduct, FAO livestock distributions, ESACCI Biomass, GEOCARBON, Global Forest Watch, JRC Above Ground Biomass, Chaplin-Kramer et al., WaterWorld, and others.
- Services covered per model vary; water supply ensembles often use catchments (HydroSHEDS), while others use global datasets or regional maps.
- A detailed table (Table 1) lists model name, service, resolution, and data sources; licenses may apply.

## Data processing per model outputs
- For each raster model output, predictions are calculated per gridcell.
- Water supply processing differs by model (e.g., maximum per catchment polygon for some accumulated-flow models; others sum grid values to an outlet pour point).
- A 0.001° grid size is used to minimize edge effects during aggregation.

## Normalisation and data preparation
- All model outputs are standardised by normalising within each model to enable comparability across models with different units.
- Normalisation follows a Winsorising approach (2.5th and 97.5th percentiles) to define 0 and 1, reducing the influence of extreme values.

## Ensemble approaches
- Unweighted ensembles: mean and median across models per grid cell (ArcGIS cell statistics); a bootstrapped approach (1,000,000 points, 250 runs) ensures memory efficiency and comparability.
- Weighted ensembles (untrained; without external validation data):
  - PCA ensemble: weights proportional to models’ correlation with the first principal component.
  - Correlation coefficient ensemble: weights based on each model’s average correlation with all others.
  - Regression to the median ensemble: iterative, log-likelihood-based weighting toward the median ensemble.
  - Leave-one-out cross-validation ensemble: iterative regression excluding one model at a time; weights averaged across models.
- Weights are computed in Matlab, normalised to sum to 1, and stored per run; final weights are averaged across runs for mapping.
- Implementations: ArcGIS for unweighted ensembles; Matlab and Python scripts (GitHub) for weighted ensembles.

## Uncertainty and quality control
- Uncertainty is described by the Standard Error of Mean (SEM) across contributing models and ensemble approaches.
- All methods and outputs underwent internal review by the authors and external peer review for publication in Science Advances.
- Many input models come from peer-reviewed or well-accepted sources; quality control emphasizes reproducibility and transparency.

## Reproducibility and access
- Code and workflows for ensemble generation are available on GitHub (GlobalEnsembles repositories) including Python and Matlab scripts.
- Supplementary information lists data sources and processing steps; some sources have licensing restrictions.

## Funding and references
- Funded by the EnsemblES project (UKRI Landscape Decisions programme NE/T00391X/1) with additional support from MobilES and RUST.
- Key references include Willcock et al. (2023) on model ensembles and related methodological works (e.g., Hooftman et al., Dormann et al., Marmion et al.).