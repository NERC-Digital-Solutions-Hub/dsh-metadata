# Global ensembles of Ecosystem Service map outputs modelled at 1km resolution for water supply, recreation, carbon storage, fuelwood and forage production

## Overview
- Global ensemble dataset of Ecosystem Services (ES) maps at approximately 1-km resolution.
- Covers five ES: water supply, recreation, above-ground carbon (AG carbon), forage, and fuelwood.
- Each ES includes multiple model ensembles and a variation-among-models (SEM) layer.
- Data are normalized to a 0–1 scale with a single NoData value (-999).

## Data content and structure
- 28 TIFF raster layers plus world-files for five ES and six ensemble approaches across the ES, with SEM (variation among models).
- One water supply shapefile with catchment polygons (HydroSHEDS v1 definitions) containing six ensemble estimates and SEM.
- Spatial details:
  - Raster grids: 0.0083333333° × 0.0083333333° (≈1 km at the equator).
  - Raster dimensions: 43,200 × 18,600 grid cells.
  - CRS: World Geodetic System 1984 (EPSG 4326).
  - Areas: Global coverage with some small island exclusions due to data gaps.
  - Units: Relative service delivery; normalized to 0–1.
  - NoData value: -999.

## Origin of model outputs
- Based on the EnsemblES project: ensemble techniques to capture accuracy and sensitivity of ES models.
- Collaborating groups: Bangor University, UK CEH, and Lactuca; funded by UKRI Landscape Decisions, MobilES, and RUST.
- ES ensemble outputs and methodologies (and validations) are under revision as of 2023; related codes available on GitHub (GlobalEnsembles).
- Model inputs include a wide range of established ES models and datasets (e.g., InVEST, ARIES, WaterWorld, Co$ting Nature, LPJ-GUESS, TEEB, Scholes, Aqueduct, FAO livestock, ESACCI biomass, GFW, JRC biomass, etc.). Not all inputs cover the entire globe.

## Data processing of individual model outputs
- Per-gridcell processing for each raster model output.
- Water supply processing:
  - Accumulated flow models (WaterWorld, Aquastat): use maximum value per HydroSHEDS polygon pour point.
  - Differences in pour point routing not fully corrected due to lack of exact pour-point location in HydroSHEDS.
  - Non-accumulated water models: sum grid values to accumulate flow through the pour point (ArcGIS Zonal tool).
  - A fixed 0.001° grid size used to minimize edge effects.
- Table 1 (Models and outputs) lists multiple models per service (e.g., 8 water models, 5 recreation models, 14 AG carbon models, 12 forage models, 9 fuelwood models). Models include the same list of major tools and datasets as described above.
- Normalisation prior to ensemble:
  - All model outputs are normalized to 0–1 using a Winsorising approach (2.5% and 97.5% percentiles) to minimize the influence of extreme values.
  - Normalisation per model follows Willcock et al. (2019).
  - Winsorising protocol available in GitHub: GlobalEnsembles/Winsorising.

## Analytical approaches for generating Ensemble Models
- Unweighted ensembles (mean and median) computed per gridcell using ArcGIS Cell Statistics; memory-efficient via a 1,000,000-point bagging approach across 250 runs; mean weights averaged across runs for comparability.
- Untrained weighted ensembles (no external validation data assumed) with four deterministic/iterative approaches:
  - PCA ensemble: weights derived from correlation to the first PCA axis (consensus axis); models closer to the consensus get higher weights.
  - Correlation-coefficient ensemble: weights based on mean correlation of each model with all others (excluding itself).
  - Regression-to-median ensemble: iterative log-likelihood regression to maximize explanation of the median ensemble; weights derived from nlmefit with 200 iterations; no constant term.
  - Leave-one-out cross-validation ensemble: iterative consensus where each model is alternately left out; weights are derived from regressions against the remaining models; final weights are averaged across all iterations.
- Weighting details:
  - Weights are normalized to sum to 1 for each data point.
  - Weights per run are stored; average weights used for spatial mapping.

## Quality control
- All methods and outputs underwent internal team review (Willcock et al. 2023 authors) and external peer review for Science Advances.
- Most input model data are derived from peer-reviewed or widely accepted sources.

## Data accessibility and code
- Analytical codes for generating ensembles available on GitHub:
  - Python/ArcGIS integration: https://github.com/GlobalEnsembles
  - Ensemble creation scripts: https://github.com/GlobalEnsembles/EnsembleCreation
  - Winsorising helper: https://github.com/GlobalEnsembles/Winsorising
- Supporting information and model details referenced via project-related links and datasets (e.g., EnsemblES, WaterWorld, InVEST, Aqueduct, ESBI datasets).

## Funding and affiliations
- Project: EnsemblES — Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models.
- Funded by UKRI Landscape Decisions programme (project NE/T00391X/1) with additional support from MobilES (ES/R009279/1) and RUST (ES/T007877/1).

## Practical implications for GIS specialists
- Provides a global, 1-km ES mapping framework with multiple model inputs and quantified uncertainty via SEM.
- Data are suitable for map-based visualization and exploration of spatial patterns in ES delivery and uncertainty.
- Normalized 0–1 units facilitate cross-service comparisons and overlay analyses in GIS.
- Shapefile for water supply enables catchment-level analyses and aggregation.
- Ensemble methodologies offer robust composite surfaces and explicit transparency about how consensus and uncertainty are derived.
- Requires handling large raster datasets (approx. 43k × 19k cells per raster); consider performance and storage planning.
- Licensing restrictions may apply depending on source data; always verify data licenses before reuse.

## References (selected)
- Willcock et al. (2019, 2020, 2023) on validation and ensemble methods.
- Hooftman et al. (2022) on weighted ensembles.
- Avitabile et al. (2016), Barredo et al. (2012), Gassert et al. (2015), Mulligan (2013, 2015), Scholes (1998), and others for input datasets.
- Chaplin-Kramer et al. (2022) and related works on ecosystem services mapping and natural assets.