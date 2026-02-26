# Details of the data-structure and nature of values

## Overview
- A dataset of 14 raster layers (10 ensemble approaches for above-ground carbon stock and water supply) plus a single water-ensemble shapefile, designed for map-based interpretation of ecosystem services in the UK.
- Rasters are 1000 m x 1000 m grid, single-band 32-bit floating point, with projection in British National Grid (EPSG 27700).
- Outputs are relative service delivery, normalised between 0 and 1; NoData value is -999.
- Spatial coverage includes Great Britain, Northern Ireland, and surrounding isles for carbon; water supply covers 519 selected mainland GB and NI catchments.
- A shapefile (UKWaterEnsembles) contains the 14 estimates per watershed polygon, linked to National River Flow Archive catchments.

## Data contents and formats
- 14 tiff raster layers named by carbon ensemble approach (14 rasters total) and their associated world-files.
- One shapefile (UKWaterEnsembles) with polygons per watershed, each containing the 14 ensemble estimates.
- Grid and projection details:
  - Carbon rasters: 1 km2 grid cells (approximately 1,000 m per side), 1-band, 32-bit floating point.
  - Water rasters are ensemble mean values mapped to catchment polygons ( areas converted to 1 km2 units for comparison).
- Area coverage:
  - Carbon: GB, NI, Isles included (including off-shore islands).
  - Water: 519 catchments on mainland GB and NI.

## Origin and authorship
- Originates from the EnsemblES project: using ensemble techniques to capture accuracy and sensitivity of ecosystem service models.
- Partners: Bangor University, UKCEH, subcontractor Lactuca; funded by UKRI Landscape Decisions programme (project NE/T00391X/1).
- Methods and outputs align with Hooftman et al. (2022) and related publication discussions in Ecosystem Services.

## Validation data and polygons (calculation units)
- Carbon validation: Forest Research dataset with 2019 forest compartments (≈ 201,143 compartments, mean size ~4.4 ha). Compartment polygons aggregated to 2,078 forest polygons, then recalculated to full area for mapping.
- Water validation: 519 NRFA hydrometric stations with catchments; from 1,598 potential NRFA catchments (as of Nov 2019), selects catchments >100 km2 (and Welsh catchments >25 km2 to improve representation). In cases of multiple stations, the largest is chosen to avoid pseudoreplication.

## Models and inputs (Table 1)
- A suite of models with varying spatial grain and coverage, including:
  - InVest v3.7.0 (carbon: 25 m grid; water: run-off per cell; full area)
  - LPJ-GUESS (biomass and run-off; grid ~0.5°; full area)
  - LUCI (carbon: 10 m; water: 5 m; GB)
  - Various global and regional datasets and downscaled products (e.g., Copernicus Tree Cover Density, Aqueduct, DECIPHeR, Grid-to-Grid, ARIES, Barredo 2012, National Forest Inventory 2018, WaterWorld, etc.)
- Some inputs are “online tools” or existing datasets; others were generated for this study or repurposed from peer-reviewed sources.

## Data processing and normalisation (per model output)
- Predictions per validation polygon are produced via ArcGIS spatial analyst (Zonal) with a 2.5 m grid setting to minimise edge effects; values are summed over polygons and adjusted for grid size.
- For flow-related models, small-scale routing differences are mitigated by using the maximum flow within 2 km of the NRFA location.
- Normalisation across models and validation data:
  - Outputs are area-corrected to per hectare equivalents where needed.
  - Values are normalised to a 0–1 scale using a Winsorising approach (2.5th and 97.5th percentiles define the 0 and 1 bounds).
- Averages of weights are computed across jack-knifed runs; carbon data also adjusted to 1 km2 resolution.
- A total of 253,802 carbon grid cells (with partial non-sea land cover) are included in the dataset.

## Ensemble modelling approaches (analytical methods)
All ensemble calculations use a bagging-like approach with 50% of spatial polygons for 250 runs; the same subset is used for all model computations per run. Weighting is normalised to sum to 1 and applied to model outputs as in the ensemble equation.

- a) PCA ensemble: deterministic; weights are model loadings on the first principal component (consensus axis) from Matlab princomp.
- b) Correlation coefficient ensemble: deterministic; weights equal to mean correlation of each model with all others (excluding itself).
- c) Regression to the median ensemble: iterative log-likelihood regression to derive weights by regressing models against the median ensemble; no constant term.
- d) Leave-one-out cross-validation ensemble: iterative regression where each model is tested against the remaining models; weights are averaged across all leave-one-out iterations.
- e) Grain-size ensemble: penalises coarser-scale models; weights decrease with larger grain sizes (log10(grain)).
- f) Distinct ensembles (attribute weighting): groups models by 17 attribute categories; computes a distinctiveness factor; weights adjusted to emphasize minority groups or downweight them depending on aim; weights normalised to sum to 1.
- g) Trained/Accuracy-weighted ensembles: uses training data to compute model-specific accuracies (e.g., D1 or Spearman ρ) and uses these as weights for second data points not used in training.
- h) Log-likelihood regression (alternative): similar to c) but regression uses corresponding validation data rather than the median.

- further notes:
  - All weighting schemes are normalised to sum to 1 before applying in the ensemble equation.
  - The approach allows exploring different consensus and variance-reduction strategies.

## Calculation polygons and mapping (scope)
- Validation polygons are the basis for calculation; carbon and water validations are described above.
- Weights derived from ensembles are applied to the corresponding model outputs, producing ensemble maps across the full area (1 km2 resolution for carbon, polygon-based for water).
- Variation among spatial outputs is visualized using the Standard Error of the Mean (SEM).

## Quality control
- Internal team reviews by all authors and external peer review for publication.
- Most input model data come from peer-reviewed sources or well-accepted datasets.

## Funding information
- EnsemblES project: Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models.
- Funded by the UKRI Landscape Decisions programme (project NE/T00391X/1).

## References
- Includes a broad set of foundational and methodological references for ecosystem services, ensemble modelling, and related data sources (e.g., Ahlström et al., Barredo et al., Marmion et al., Grenouillet et al., Dormann et al., Willcock et al., Thomas et al., WaterWorld, DECIPHeR, Copernicus Tree Cover Density, among others).