# UKWaterEnsembles: Ensemble Outputs for Above Ground Carbon Stock and Water Supply in the UK

- This dataset provides ensemble outputs for above-ground carbon stock and water supply across the United Kingdom, combining multiple modeling approaches and data sources.
- It includes 14 raster layers (10 ensemble approaches with a double option for two approaches) for carbon stock outputs and a shapefile with 14 estimates per watershed (water) linked to NRFA catchments.

## Contents and structure

- 14 tiff raster layers of normalized outputs (carbon stock) from 10 ensemble approaches, with variation maps among models and ensembles.
- One shapefile (UKWaterEnsembles) containing water supply estimates per watershed.
- Grid details: 1000 x 1000 m raster cells (1-band, 32-bit float); NODATA = -999.
- Projection: British National Grid (EPSG 27700) with a scale factor 0.9996; units in metres.
- Area covered:
  - Above-ground carbon stock for Great Britain, Northern Ireland, including Isle of Man, Scilly, Wight, Orkney, Shetland, Inner/Outer Hebrides.
  - Water supply for 519 selected mainland GB and Northern Ireland catchments.
- Units: Relative service delivery, normalized to 0–1.

## Data provenance and origin

- Originates from the EnsemblES project: using ensemble techniques to capture accuracy and sensitivity of ecosystem service models ( Bangor University, UK-CEH, and Lactuca) funded by UKRI Landscape Decisions (project NE/T00391X/1).
- Model outputs reflect multiple existing or freely available model frameworks and outputs; weights and aggregations are transferred to UK-wide maps.
- The carbon outputs use forests-derived weight information extended to the full area, with acknowledgment of potential bias in non-forested areas.

## Data processing and normalization

- Individual model outputs were processed to enable comparability:
  - Predictions per validation polygon via ArcGIS spatial analyst Zonal tool (2.5 m grid cells), with aggregation to the required grid.
  - For accumulated flow models, use of maximum within 2 km of NRFA gauge location.
  - All outputs normalized per model and validation dataset (Willcock et al. 2019) to 0–1 after area-correcting to per-hectare units.
  - Double-sided Winsorising applied using the 2.5th and 97.5th percentiles to mitigate extreme values.
- Normalization ensures cross-model comparability prior to ensemble weighting.

## Models and inputs used

- Table of models and existing outputs used (various grain sizes and coverage):
  - InVest, LPJ-GUESS, LUCI, $-benefit transfer, Aqueduct, ARIES, Barredo, Copernicus Tree Cover Density, DECIPHeR, Grid-to-Grid, Henrys etc., National Forest Inventory, Scholes Growth Days, WaterWorld, among others.
  - Grains range from 1 km2 to fine resolutions (down to 10 x 10 m in LUCI); coverage includes Great Britain, England, Wales, Northern Ireland, or the full area as applicable.
- Outputs include both carbon stock and water-related variables, with various input data sources and validation origins.

## Calculation polygons and validation data

- Carbon stock validation: Forest Research dataset with 201,143 forest compartments (mean area ~4.4 ha; median ~1.6 ha). Forest compartments were spatially joined into 2078 forest polygons for analysis.
- Water validation: 519 NRFA gauging stations with catchments (>100 km2; Welsh catchments included with >25 km2 when necessary) to robustly estimate mean runoff.
- Validation datasets and validations are not fully described in this summary; they underpin the ensemble weighting and evaluation.

## Ensemble modelling approaches

- A single jackknife framework: 50% spatial data polygons used per run (N=250 runs) to generate variation estimates; all model computations used the same data partition per run.
- Unweighted ensembles:
  - Mean ensemble (average) and Median ensemble across models.
- Untrained weighted ensembles (no validation data):
  - PCA ensemble: weights proportional to loading on the first principal component (consensus axis).
  - Correlation coefficient ensemble: weights by mean correlation of each model with others.
  - Regression to the median ensemble: weights from log-likelihood regression against the median ensemble; iterative optimization without a constant term.
  - Leave-one-out cross-validation ensemble: weights derived by regressing each model against the remaining models iteratively and averaging coefficients.
  - Grain-size ensemble: penalizes coarser-grained models; weights inversely related to grain size.
  - Distinct ensembles: weights by model group distinctiveness (groupings based on 17 model attributes; adjustments to upweight or downweight minority/majority groups as appropriate).
- Trained weighted ensembles (validation data present):
  - Data-split ensembles: training on 50% of data, testing on the other 50% to reflect standard species distribution modelling practices; weights derived from training stage and applied to testing data.
  - Accuracy-weighted ensembles: weights weighted by per-model accuracy (e.g., AUC-like metrics) on the validation subset.
  - Log-likelihood regression (trained): regression against validation data points not used in training; weights derived from regression coefficients.
- All weighting schemes normalize weights to sum to 1 and are applied to Eq. 1 to generate ensemble predictions.

## Quality control

- Internal team review by all authors (nine authors in the originating study) and external peer review for publication.
- Most input model data come from peer-reviewed or well-accepted sources.

## Governance, access, and reproducibility

- Coding and ensemble generation are implemented in Matlab (v7.0.14) with statistical and parallel toolboxes.
- Codes for generating ensembles are publicly available on GitHub: github.com/EnsemblesTypes/EnsemblesTypes.
- Data and outputs align to a documented data paper framework and are linked to multiple data sources and references.

## Limitations and considerations for data stewards

- Spatial coverage variation: some input models do not cover all regions (e.g., Northern Ireland, Wales, Scotland, or mainland GB only), which can affect comparability across the full UK extent.
- Weight transfer bias: carbon-weighting approach uses forest-derived weights applied to non-forested areas, potentially biasing non-forest regions.
- Scale differences: carbon outputs at 1 km2 grid cells; water outputs tied to catchment units; cross-scale aggregation may introduce additional uncertainty.
- Ensemble complexity: multiple weighting schemes offer different perspectives on uncertainty; interpretation requires understanding of each scheme’s assumptions and data partitions.

## Funding

- EnsemblES project: Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models; funded by the UKRI Landscape Decisions programme (project NE/T00391X/1).

## Documentation and references

- Dataset references and supporting literature span methods for ensemble modelling, validation approaches, and ecosystem service modelling (e.g., Marmion et al., Grenouillet et al., Dormann et al., Willcock et al., among others).