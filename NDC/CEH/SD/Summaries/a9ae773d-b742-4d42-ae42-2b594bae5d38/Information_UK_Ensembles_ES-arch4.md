# Ensembles of ecosystem service models for above ground carbon stock and water supply in the UK

- What is included
  - 14 TIFF raster layers representing 10 ensemble approaches for above-ground carbon stock, plus maps of variation among models and among ensembles. Includes a water supply service shapefile with 519 catchment polygons, each containing the 14 estimates.
  - Grids: carbon data on a 1 km2 grid; water data per 1 km2 catchment polygons; both in British National Grid (OSGB 27700) with 0.9996 scale factor; NoData = -999.
  - Area covered: above-ground carbon stock for Great Britain and Northern Ireland (including Isles) and water supply across 519 catchments in GB & NI.
  - Units: relative service delivery, normalised to 0–1.

- Data origins and purpose
  - Based on ensemble outputs from the EnsemblES project (Bangor University, UKCEH, Lactuca) funded by UKRI Landscape Decisions.
  - Methods and outputs linked to Hooftman et al. (2022); aims to capture accuracy and uncertainty across ecosystem-service models.

- Model inputs and structure
  - Table of models and outputs (Table 1) lists 14 inputs/outputs with varying grain sizes and coverage; includes models such as InVest, LPJ-GUESS, LUCI, Copernicus Tree Cover Density, WaterWorld, among others.
  - Some inputs are coarser or finer in grid size; coverage ranges from full area to regional GB-focused datasets.

- Data processing workflow
  - Individual model outputs projected to OSGB projection; predictions for validation polygons generated using ArcGIS Zonal tool with 2.5 m grid setting to minimize edge effects; predictions aggregated to full-area units (carbon) or catchments (water).
  - Normalisation: outputs converted to comparable units per model and per validation dataset via area-normalisation and Winsorising (2.5th–97.5th percentiles) to map to 0–1.
  - For accumulated flow, adjustments ensure alignment with NRFA gauging-station locations within 2 km.
  - Weights for ensemble averaging are normalised to sum to 1 and vary by ensemble method.

- Ensemble modelling approaches
  - Deterministic consensus methods
    - PCA ensemble: models weighted by loadings on the first principal component.
    - Correlation-coefficient ensemble: weights proportional to mean correlation with other models.
  - Iterative/learned methods
    - Regression to the median ensemble: weights derived via multivariate regression (no constant) against the median ensemble; optimized by iterative log-likelihood maximization.
    - Leave-one-out cross-validation ensemble: weights derived by iterating regressions with one model omitted at a time; mean coefficients used as weights.
  - Scale-aware approach
    - Grain-size ensemble: penalises coarser-resolution models; weights damped by grid grain size (weights proportional to 1/log10(grain)).
  - Attribute-based distinct ensembles
    - Group-based weighting: models grouped by 17 attribute categories; upweighting or downweighting to reflect model distinctiveness within groups; normalised to sum to 1.
  - Training/validation-based ensembles
    - Trained (accuracy-weighted) ensembles: weights derived from model accuracy on a held-back validation set; used to weight model outputs in the ensemble.
    - Accuracy-weighted ensembles (training vs validation data): uses accuracy metrics (e.g., D or Spearman rho) on the validation subset not used in training.
  - Additional approaches
    - Training against validation data (trained ensembles with partial data) to reflect partial data scenarios.
    - Log-likelihood regression: alternative regression-based weighting against corresponding validation data points.

- Validation datasets and polygons
  - Carbon validation: Forest Research dataset with 201,143 forest compartments (England/Scotland, 2019); aggregated into 2,078 forest polygons for map generation.
  - Water validation: 519 hydrometric NRFA catchments with large-area representation; Welsh catchments included to balance representation (41 additional Welsh catchments).

- Quality control and reproducibility
  - Comprehensive internal review by all authors; external peer review for publication.
  - Most input data from peer-reviewed or widely used sources.
  - Analytical code available on GitHub (EnsemblesTypes/EnsemblesTypes).

- Data governance, limitations, and notes for data leaders
  - Normalisation and Winsorising introduce comparability but may influence extreme values.
  - Carbon data mapped to 1 km2 grid; forest-weighting biases may bias non-forested areas downward.
  - Not all input models cover the entire UK; some datasets cover only GB or specific regions.
  - Edge effects minimized via resampling to 2.5 m for validation polygons; some adjustments made for hydrological routing consistency.
  - Outputs are designed for cross-model comparison, uncertainty estimation, and scenario analyses rather than single-model decision-making.

- Access, provenance, and funding
  - Data produced under the EnsemblES project; funding from UKRI Landscape Decisions programme (NE/T00391X/1).
  - Data and methods described with a link to GitHub for code and to primary references (Hooftman et al. 2022 and related sources).

- References and related materials
  - Key methodological and data sources cited in the dataset description (e.g., Willcock et al. 2019/2020; Dormann et al. 2018; Marmion et al. 2009; Grenouillet et al. 2011; multiple foundational ecosystem-service and climate-model references).