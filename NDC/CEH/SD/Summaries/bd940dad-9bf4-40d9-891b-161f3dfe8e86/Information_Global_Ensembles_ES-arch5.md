# Global ensembles of Ecosystem Service map outputs modelled at 1km resolution for water supply, recreation, carbon storage, fuelwood and forage production

- A global dataset of ecosystem service (ES) maps produced via ensemble modelling across five services: water supply, recreation, above-ground carbon (AG carbon), fuelwood, and forage.
- Provides 28 raster layers (1 km grid, 0.0083333° ≈ 1 km at equator) plus a water supply shapefile with catchment polygons and ensemble estimates.
- Normalised outputs on a 0–1 scale (relative service delivery); NoData value is -999; projection is WGS 84 (EPSG 4326).

## Data structure and content

- 28 TIFF raster layers plus corresponding world files; one shapefile (WaterSupply_Ensembles_HydroSHEDS) with 15,289 HydroSHEDS catchment polygons.
- Grids: 0.0083333° resolution; global coverage with some islands excluded due to data gaps.
- raster naming: Ensemble approach_Service_Ensemble_Publish.tif; shapefile contains six ensemble estimates plus SEM per catchment.
- Units: unitless, normalised 0–1; water supply uses catchment-based aggregation.
- Underlying data include a wide range of model outputs and ensemble variations (SEM maps).

## Origin and data sources

- Originates from the EnsemblES project: “Using ensemble techniques to capture the accuracy and sensitivity of ecosystem service models.”
- Funded by UKRI Landscape Decisions programme (NE/T00391X/1) with additional MobilES and RUST support.
- Model inputs drawn from diverse ES modelling frameworks and data sources (e.g., InVEST, ARIES, WaterWorld, Co$ting Nature, LPJ-GUESS, TEEB, Scholes, Aqueduct, FAO livestock distributions, ESA CCI biomass, Global Forest Watch, JRC, etc.).
- Ensemble maps, methods, and validations described and referenced; overall approach under revision as of 2023.

## Data processing and normalization

- Individual model outputs are per gridcell (or per catchment for water).
- Water models with accumulated flow use maximum per polygon; non-accumulated water models sum grid values to the pour point, with a fixed 0.001° grid to reduce edge effects.
- All model outputs are normalised across models using a 0–1 scale, with Winsorising (2.5th and 97.5th percentiles) to limit extreme values prior to ensemble creation.
- A double-sided Winsorising protocol is applied to ensure comparability across heterogeneous units.

## Models and ensemble methods

- Six ensemble approaches used; sub-set of methods explored in Hooftman et al. (2022):
  - Unweighted ensembles: mean and median (using ArcGIS cell statistics; Python implementations available on GitHub).
  - Weighted ensembles (no external validation data required):
    - PCA ensemble: weights from first principal component (consensus axis).
    - Correlation coefficient ensemble: weights proportional to each model’s mean correlation with all others.
    - Regression to the median ensemble: iterative log-likelihood regression to maximize alignment with the median ensemble.
    - Leave-one-out cross-validation ensemble: iterative regression leaving out one model at a time; final weights are mean coefficients across iterations.
- Weights are normalized to sum to 1; ensembles are computed per data point or polygon.

## Analytical approaches and reproducibility

- Code and workflows:
  - ArcGIS for unweighted ensembles; Python for ArcPro workflows.
  - Matlab v7.0.14 with statistical/parallel toolboxes for weighted ensembles.
  - GitHub repositories: GlobalEnsembles for Python/ArcPro scripts and EnsembleCreation for weighted ensembles; Winsorising script available at GitHub.
- Quality control and transparency:
  - Full internal review by 11 authors; external peer review for publication in Science Advances.
  - Most input data are peer-reviewed or well-accepted; licensing may restrict some inputs.

## Data quality, governance, and provenance

- Data quality vetted through multi-source validation and published methodologies (Willcock et al. 2019, 2020, 2023; related references).
- Provenance: links to source datasets and methodologies provided; extensive supplementary information listing model frameworks, inputs, and processing steps.
- Licensing:
  - License restrictions may apply to some input datasets; ensemble outputs are normalised and documented for reproducibility.
- Documentation and metadata accompany the dataset (origin, processing steps, model details, validation status).

## Accessibility, reuse, and governance implications for Data Stewards

- Clear data structure with both raster and vector components; standardized 0–1 units facilitates discovery and comparability.
- Global coverage with explicit spatial resolution and projection; explicit handling of edge effects and data gaps.
- Updatable framework: ensemble approach can accommodate new models or updated inputs; versioning and provenance should be maintained.
- Considerations for storage and sharing:
  - Large raster stacks and catchment shapefiles require substantial storage; ensure metadata captures model provenance, normalization, and ensemble method used.
  - Document licensing constraints for included input datasets; provide guidance on data reuse and citation.
- Recommended governance actions:
  - Implement metadata standards detailing data origin, processing chain, normalisation, ensemble method, and uncertainty (SEM).
  - Maintain versioned releases and update pathways as new model outputs or inputs become available.
  - Ensure clear data access terms and attribution requirements for contributors.

## Funding and references

- Funding: EnsemblES project; UKRI Landscape Decisions programme (NE/T00391X/1); MobilES (ES/R009279/1); RUST (ES/T007877/1).
- Key references include works by Willcock et al. (2019, 2020, 2023), Hooftman et al. (2022), and foundational ES datasets and models (InVEST, ARIES, WaterWorld, Co$ting Nature, LPJ-GUESS, TEEB, FAO, ESA CCI Biomass, Global Forest Watch, JRC, Aqueduct).