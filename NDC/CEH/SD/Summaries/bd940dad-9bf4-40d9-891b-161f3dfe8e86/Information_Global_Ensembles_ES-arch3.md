# Hooftman et al.
Global ensembles of Ecosystem Service map outputs modelled at 1km resolution for water supply, recreation, carbon storage, fuelwood and forage production

## Overview
- A global dataset of Ecosystem Service (ES) maps produced by multiple ensemble modelling approaches, covering water supply, recreation, above-ground carbon, forage, fuelwood, and related variation among models.
- Provides 28 raster layers plus catchment-based shapefile outputs, normalised to a common scale (0 to 1) with per-cell uncertainty information.

## Data content
- 28 raster layers (World 0.0083333° grid; six among-model ensemble approaches per ES) and one shapefile for water supply catchments, each containing six ensemble estimates and their variation (SEM).
- Global coverage with exclusion of data-deficient small islands; grid cells ≈ 1 km at the equator.
- Units are relative service delivery (0–1); a no-data value of -999 is used.
- Variation among model outputs is provided via Standard Error of the Mean (SEM) across contributing models and ensembles.

## Origin of model outputs
- Based on six EnsemblES ensemble approaches, drawing from a wide constellation of ES models (global and continental scale).
- Collaborative project involving Bangor University, UK CEH, and Lactuca; funded by UKRI Landscape Decisions programme with additional MobilES/RUST support.
- Model families and inputs include InVEST, ARIES, WaterWorld, Co$ting Nature, LPJ-GUESS, TEEB, Scholes, Aqueduct, FAO livestock distributions, and biomass/forest datasets (e.g., ESA CCI, Global Forest Watch, JRC, Chaplin-Kramer outputs).
- Data sources are cited, with licenses potentially applying; full list and links are provided in the accompanying materials (Table 1).

## Data processing and normalization
- Individual model outputs are standardized to a common scale via normalisation per model (Winsorising to 2.5th/97.5th percentiles) before ensemble aggregation.
- Double-sided Winsorising prevents extreme values from skewing results while preserving data points.
- For water, some models use max-per-polygon flows; for non-accumulated water models, grid values are summed to the pour point with a 0.001° grid to reduce edge effects.
- For water-only outputs, some inputs are per-catchment; others are per-gridcell, depending on model design.

## Ensemble modelling approaches
- Unweighted ensembles: mean and median across models per cell (ArcGIS cell statistics; Python/ArcPro scripts available).
- Weighted ensembles (untrained): weights assigned to each model via several deterministic/iterative methods:
  - PCA ensemble: weights proportional to model correlation with the first principal component (consensus axis).
  - Correlation coefficient ensemble: weights based on mean correlation of a model with all others.
  - Regression to the median ensemble: iterative log-likelihood regression to maximize explanation by the median comparator; weights derived from regression coefficients.
  - Leave-one-out cross-validation ensemble: iterative regression leaving out one model at a time; weights averaged across iterations.
- All weighting approaches are non-constant, with normalisation of weights to sum to 1; weights are stored per run and averaged for spatial mapping.
- Implementations include ArcGIS tools and Matlab code, with dedicated GitHub repositories:
  - Ensemble creation: GlobalEnsembles/EnsembleCreation
  - Python/ArcPro utilities: GlobalEnsembles/PhytonCodesArcPro
  - Winsorising protocol: GlobalEnsembles/Winsorising

## Quality control and validation
- Full internal team review by the contributing authors plus external peer review for publication.
- Inputs are largely derived from peer-reviewed or widely accepted sources; verification and validation are integral to the workflow.

## Software and reproducibility
- Analyses performed in ArcGIS, Matlab, and Python; code and workflows are publicly hosted.
- Reproducibility emphasis through documented normalization, ensemble schemes, and code repositories.

## Data access, licensing, and supporting information
- Underlying model outputs originate from a mix of publicly available and licensed data sources; licensing restrictions may apply.
- Supporting information lists data sources and links (e.g., Aqueduct, ESACCI Biomass, FAO livestock distributions, GFW, JRC biomass data, WaterWorld, Chaplin-Kramer et al., etc.).
- The ensemble methodology and validation outputs (including code) are described and available via the FAO/Food and Agriculture Organization resources and the GlobalEnsembles GitHub repositories.
- The dataset and metadata aim to facilitate use in monitoring frameworks, policy evaluation, and decision-making processes by offering a harmonized, uncertainty-aware suite of ES maps.

## Funding
- EnsemblES project: Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models; UKRI Landscape Decisions programme (NE/T00391X/1) with additional MobilES (ES/R009279/1) and RUST (ES/T007877/1) funding.

## References and related materials
- Comprehensive references to the individual ES models and biomass datasets used, as well as methodological papers on ensemble approaches and validation (Willcock et al.; Dormann et al.; Marmion et al.; Gassert et al.; Barredo et al.; Avitabile et al.; etc.).