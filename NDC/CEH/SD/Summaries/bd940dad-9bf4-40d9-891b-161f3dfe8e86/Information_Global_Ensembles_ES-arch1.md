# Hooftman et al. Global ensembles of Ecosystem Service map outputs modelled at 1km resolution for water supply, recreation, carbon storage, fuelwood and forage production

- Purpose and scope
  - Global ensemble maps of Ecosystem Services (ES) at ~1 km resolution for water supply, recreation, carbon storage (AG carbon), fuelwood, and forage production.
  - Includes 28 raster layers (ensemble approaches for five ES) and one catchment-based water supply shapefile with six ensemble estimates and uncertainty (SEM).
  - Outputs standardised to relative, 0–1 units; no-data value is -999; projection is WGS84 (EPSG 4326).
  - Global coverage with data gaps for very small islands; grid size ~0.008333° (≈1 km at the equator); water data per HydroSHEDS catchments.

- Data content and structure
  - Rasters: ensemble outputs for five ES across six among-model ensemble approaches, plus SEM maps of variation among models and approaches.
  - Shapefile: Water supply ensembles by HydroSHEDS catchments (15,289 worldwide), containing six ensemble estimates and SEM.
  - Inputs and model outputs span multiple widely used ES models and datasets (e.g., InVEST, ARIES, WaterWorld, Co$ting Nature, LPJ-GUESS, TEEB, Scholes, Aqueduct, FAO livestock distributions, ESA CCI Biomass, Global Forest Watch, JRC biomass maps).

- Origin and modelling context
  - Created within the EnsemblES project: using ensemble techniques to capture accuracy and sensitivity of ES models.
  - Funded by UKRI Landscape Decisions programme, with additional support from MobilES and RUST.
  - Methodology and validation discussed in Willcock et al. 2023 (Science Advances); related Matlab and ArcGIS Python codes available on GitHub (GlobalEnsembles).

- Ensemble modelling approaches
  - Unweighted ensembles: mean and median across models for each gridcell.
  - Weighted ensembles: four methods to assign model weights (normalized to sum to 1) and produce a weighted ES value:
    - PCA ensemble: weights based on correlation with the first principal component (consensus axis).
    - Correlation coefficient ensemble: weights based on mean correlation of each model with all others.
    - Regression to the median ensemble: iterative log-likelihood regression to maximize explanation of the median ensemble; weights from regression coefficients.
    - Leave-one-out cross-validation ensemble: iterative regression across models with one model left out at a time; weights averaged across iterations.
  - General ensemble form: E(x) = sum_i (omega_i / sum_i omega_i) * Y_i(x), where Y_i are model outputs and omega_i are model weights.
  - Tools: ArcGIS used for mean/median; Matlab used for calculating weights; Python scripts available in the project repositories.

- Data processing and normalisation
  - Per-model processing: predictions per gridcell; water models use max per HydroSHEDS polygon pour point for accumulated flow, others sum grid values to pour point.
  - Normalisation: all model outputs normalised to 0–1 using a Winsorising approach (2.5th and 97.5th percentiles mapped to 0 and 1) to handle outliers; normalisation applied before ensemble construction.
  - Memory considerations: use of bagging with 1,000,000 data points across 250 runs to enable memory-efficient computations; weights averaged across runs.

- Uncertainty and quality control
  - Uncertainty presented as Standard Error of Mean (SEM) among contributing models and among ensemble approaches.
  - Quality control includes internal team reviews by the Willcock et al. authors and external peer review; most input data come from peer-reviewed or widely accepted sources.

- Data processing specifics (selected examples)
  - Water supply: accumulated flow handled by max per catchment polygon (pour point approach) or summed per pour point for non-accumulated models; forced 0.001° grid to minimise edge effects.
  - Model coverage varies by service: eight water models, five recreation models, fourteen AG carbon models, nine fuelwood models, twelve forage models included in the ensemble.

- Access, reproducibility and code
  - Related code and workflows are hosted on GitHub:
    - GlobalEnsembles: Python and ArcGIS related scripts for generating ensembles.
    - EnsembleCreation: Matlab-based weight calculation and ensemble construction.
    - PythonCodesArcPro: ArcGIS Pro compatible scripts.
  - Data sources and models cited with links to input datasets and licensing considerations.

- Applications and implications
  - Ensemble maps aim to reduce uncertainty and provide robust global estimates of ES for decision-making in land use, conservation, water management, and policy.
  - The framework demonstrates how combining multiple models can reveal consensus patterns and highlight uncertainties across services and regions.

- Funding and references
  - Funded under EnsemblES (UKRI Landscape Decisions; NE/T00391X/1) with additional support from MobilES and RUST.
  - References cover major ES modelling sources and ensemble methodology (e.g., Willcock et al., Dormann et al., Marmion et al., Gassert et al., Avitabile et al., Barredo et al., Costanza et al., etc.).