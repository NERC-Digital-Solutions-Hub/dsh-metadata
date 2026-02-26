# Hooftman et al. Global ensembles of Ecosystem Service map outputs modelled at 1km resolution for water supply, recreation, carbon storage, fuelwood and forage production

## Overview
- Global ensemble dataset of ecosystem service (ES) maps at approximately 1-km resolution, covering recreation, carbon storage (above-ground carbon), fuelwood, forage production, and water supply.
- Includes 28 raster layers (tiff) for multiple ensemble approaches and one water-supply shapefile; also provides a map of variation among models (SEM).
- Originates from the EnsemblES project and related collaborations; methodologies described and validation discussed in Willcock et al. (2023) and related works.

## Data structure and content
- Raster data: 28 tiff files with 0.008333° grid (~1 km at the equator), 32-bit floating point, no-data value -999, global coverage with some island exclusions.
- Water supply: one shapefile (WaterSupply_Ensembles_HydroSHEDS) with catchment polygons (15,289 globally defined HydroSHEDS catchments); each polygon contains 6 ensemble estimates and SEM.
- Projection: WGS 84 (EPSG 4326). Grid size and dimensions: 43,200 x 18,600 cells for rasters.
- Units: relative service delivery, normalized to 0–1. Data are standardized across models to support comparability.
- Data availability: licensing restricted for some source datasets; full model list and links are provided in Table 1; some inputs are global, others are regional or constrained by data availability.

## Origin and contributors
- Outputs come from six ensemble approaches within the EnsemblES framework, combining models from multiple sources (e.g., InVEST, ARIES, WaterWorld, Co$ting Nature, LPJ-GUESS, TEEB, Scholes, Aqueduct, FAO livestock, ESACCI biomass, GFW, JRC, etc.).
- Ensemble frameworks reflect different modeling philosophies and input data origins; additional supporting information and model references are provided.

## Data sources and model frameworks
- Models span a range of ES: water supply, recreation, above-ground carbon, forage, and fuelwood.
- Some models operate globally (e.g., InVEST, ARIES, WaterWorld, FAO livestock distributions); others are regional (e.g., ESACCI biomass for Europe; JRC biomass; Chaplin-Kramer inputs for recreation).
- Table 1 (not fully reproduced here) summarizes models, ecosystems served, resolutions, and access details; licensing varies by model/data source.

## Data processing, normalisation, and ensemble construction
- All individual model outputs are normalised to 0–1 to enable cross-model comparability; normalisation uses a double-sided Winsorising approach (2.5th and 97.5th percentiles) to mitigate extreme values.
- Normalisation occurs prior to ensemble calculation.
- Ensemble strategies include:
  - Unweighted ensembles: mean and median per gridcell (ArcGIS or Python workflows); memory-efficient bagging with 1,000,000 data points across 250 runs.
  - Weighted ensembles (untrained): several deterministic and iterative consensus approaches:
    - PCA ensemble: weights by loadings on the first principal component (consensus axis).
    - Correlation coefficient ensemble: weights proportional to each model’s average correlation with others.
    - Regression to the median ensemble: iterative log-likelihood regression to maximize agreement with the median ensemble.
    - Leave-one-out cross-validation ensemble: iterative regression excluding one model at a time; average coefficients used as weights.
- All weighting calculations are implemented in Matlab; code and scripts are available in GitHub (GlobalEnsembles repositories).

## Uncertainty and quality control
- Uncertainty is quantified via the Standard Error of the Mean (SEM) across contributing models and ensemble approaches.
- Extensive quality control:
  - Internal team reviews (11 authors) and external peer review for Science Advances.
  - Most input data come from peer-reviewed or well-accepted sources; licensing considerations noted.

## Accessibility, reproducibility, and governance
- Reproducibility supported by publicly available code repositories:
  - Python and ArcGIS workflows for unweighted ensembles.
  - Matlab code for weighted ensembles.
  - Winsorising normalisation workflow available on GitHub.
- Some source datasets may have licensing restrictions; full model provenance and data linkages are documented in Table 1 and accompanying references.
- The work is funded by the UKRI Landscape Decisions programme (EnsemblES) with additional MobilES and RUST support.

## Funding and references
- Funding: EnsemblES project, UKRI Landscape Decisions programme (NE/T00391X/1), MobilES (ES/R009279/1), RUST (ES/T007877/1).
- Key references: Willcock et al. (2019, 2020, 2023), Hooftman et al. (2022), and linked model and biomass datasets from Avitabile et al. (2016), Gassert et al. (2015), Barredo et al. (2012), among others.