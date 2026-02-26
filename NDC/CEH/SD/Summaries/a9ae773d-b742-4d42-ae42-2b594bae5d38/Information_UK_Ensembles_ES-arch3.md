# Ensembles of ecosystem service models for Great Britain

- Purpose and scope
  - This dataset provides ensemble-based maps of ecosystem service outcomes to assess and compare policy-relevant environmental health measures, focusing on above-ground carbon stock and water supply in the United Kingdom.
  - It uses multiple model ensembles to capture uncertainty and variance across different modelling frameworks.

- Data contents
  - 14 raster layers (1,000 m x 1,000 m grid, 32-bit floating point) representing outputs from 10 different ensemble approaches for above-ground carbon stock, including a variation map among models and among ensembles.
  - One shapefile (UKWaterEnsembles) with polygons per watershed for water supply service, containing the 14 ensemble estimates per catchment.
  - Projections: British National Grid (EPSG 27700). Unit: relative service delivery, normalised to a 0–1 scale. No-data value: -999.
  - Area covered: above-ground carbon stock for Great Britain, Northern Ireland, and associated islands; water supply for 519 selected catchments on GB and Northern Ireland.

- Origin of model outputs
  - Derived from the EnsemblES project: ensembles combining outputs from Bangor University, UKCEH, and Lactuca, funded under the UKRI Landscape Decisions programme.
  - Ten ensemble approaches were created to reflect different modelling strategies for ecosystem services; some inputs were pre-existing outputs, others generated for this study.
  - Carbon maps use 1-km² resolution; weights from validation are transferred to the full area, with SEM used to show variation across ensembles.

- Data processing and normalisation
  - For each model output, predictions were made per validation polygon using nearest-point resampling to a 2.5 m grid to minimise edge effects; values summed and area-corrected to per-hectare units.
  - Outputs were normalised per model and per validation dataset to address different units and scales; a double-sided Winsorising protocol (2.5th and 97.5th percentiles) was applied to limit extreme values.
  - Weights for ensemble combination were normalised to sum to 1 and applied across polygons; in carbon data, weights from validation were transferred to 1 km² grid aggregation.

- Models and existing outputs used
  - A mixture of models with varying grid grain sizes and coverages, including InVest, LPJ-GUESS, LUCI, $-benefit transfer, Aqueduct, ARIES, Barredo, Copernicus Tree Cover Density, DECIPHeR, Grid-to-Grid, Henrys, National Forest Inventory, Scholes Growth Days, and WaterWorld, among others.
  - Some models contributed outputs specifically for this work; others were existing datasets used as inputs.

- Calculation polygons and mapping
  - Validation datasets:
    - Carbon stock validation from Forest Research: 2019 forest compartments in England and Scotland (about 201,143 compartments; aggregated into 2,078 forest polygons for mapping).
    - Water supply validation from National River Flow Archive (NRFA): 519 hydrometric stations with catchments >100 km² (Welsh catchments included to avoid underrepresentation).
  - Validation data underpin weighting and comparison of ensemble predictions.

- Analytical approaches for generating Ensemble Models
  - A bagging framework with 50% spatial data polygons, across 250 jackknife runs; all calculations per run used the same data subset; mean weights were averaged across runs.
  - Unweighted ensembles
    - Mean Ensemble: per-polygon mean across models.
    - Median Ensemble: per-polygon median across models.
  - Untrained weighted ensembles (no external validation data required)
    - PCA ensemble: weights based on each model’s correlation with the first principal component (consensus axis).
    - Correlation coefficient ensemble: weights based on a model’s mean correlation with all other models.
    - Regression to the median ensemble: iterative log-likelihood regression to weights that best reproduce the median ensemble.
    - Leave-one-out cross-validation ensemble: iterative regression excluding one model at a time; average coefficients across iterations to obtain weights.
    - Grain-size ensemble: penalises coarser-grained models by weights proportional to 1/log10(grain size).
    - Distinct ensembles (attribute-based weighting): groups models by 17 attribute categories; weights adjusted to emphasize minority or majority groups depending on the chosen approach; normalised to sum to 1.
    - Trained/Accuracy-weighted ensembles: uses model-specific validation accuracy (e.g., D, Spearman ρ) on the second validation subset as weights.
    - Log-likelihood regression: similar to regression to the median but regresses the validation data directly against model outputs; coefficients normalised to sum to 1.
  - Trained ensembles with validation data
    - Accuracy-weighted ensembles using the same 50% data subset and the remaining data as validation; weights reflect predictive accuracy on the held-out data.
  - Additional explanatory approaches
    - Several methods combine or compare results using different consensus-building strategies (e.g., distinctiveness weighting, training data splits) to assess robustness and uncertainty.

- Quality control and governance
  - Internal team review by all authors and external peer review for publication.
  - Most input data originate from peer-reviewed or widely accepted sources.

- Funding and acknowledgments
  - Funded by the EnsemblES project: Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models, under the UKRI Landscape Decisions programme (project NE/T00391X/1).

- References
  - The dataset and methods build on a broad set of cited literature across ecosystem services modelling, ensemble methods, and validation practices.