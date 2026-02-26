# Species data

## Data sources and taxonomic groups
- Presence-only occurrence data for GB butterflies and moths from:
  - Butterflies for the Millennium dataset
  - National Moth Recording Scheme (NMRS)
- Species counts:
  - Butterflies: 66 species, 7,471,102 records
  - Day-flying moths: 43 species, 94,113 records
  - Night-flying moths: 716 species, 11,044,769 records
- Moth life-stage classification (day vs night) determined in consultation with moth experts
- Example species list includes multiple butterfly and moth species (e.g., Six-Spot Burnet, Cinnabar, Broad-bordered Bee Hawk-moth)

## Data processing and environmental covariates
- Environmental covariates:
  - Temperature and rainfall from HadUKGrid (2010–2019)
  - WorldClim bioclimatic variables derived from HadUKGrid data
  - Habitat classes from UKCEH 2015 Landcover Map (LCM), 25 m resolution
  - Topography from Copernicus Digital Elevation Map (DEM), 25 m
- All environmental layers resampled to 100 m resolution and used consistently across SDMs
- Grids reference GB using Ordnance Survey National Grid
- Spatial-temporal duplicates removed so each species has a single observation per 100 m grid cell

## Species distribution modelling (SDMs)
- Background and sampling approach:
  - Target-group background to generate 10,000 pseudoabsences per species (or equal presences if species has >10,000 presences)
- Modelling methods (for each species):
  - Generalised Linear Model (GLM)
  - General Additive Model (GAM)
  - Random Forest (RF)
  - Maxent (ME)
- Model training and evaluation:
  - Weights applied so presences and pseudoabsences are balanced; ME uses equal numbers
  - 10-fold cross-validation; models evaluated with AUC; results averaged over folds
  - Predictions produced across GB for each model type; mean and standard deviation calculated across 10 model runs
- Ensemble construction:
  - For each species, mean presence probability and associated SD are combined across model types
  - Model-type maps weighted by mean AUC; if a model type’s mean AUC < 0.75, it is removed from the ensemble for that species
  - If all model types have AUC < 0.75, all models are retained but flagged as poorly performing
- Cross-species metric:
  - Ensemble model variability (SD of predictions across 10 model runs) used to support a composite recording priority
  - Variability can be weighted to reflect preferences for common vs. rare species

## Outputs: values and interpretation
- Grid outputs are 100 x 100 m cells across GB
- Species richness:
  - Sum of predicted probabilities across all species within a target group (e.g., 0.5 probability for three species yields richness 1.5)
- Model variability:
  - Sum of SDs across the 10 models for each species per grid cell; higher values mean more uncertainty in predictions
- DECIDE recording priority:
  - Scaled to the same range as model variability
  - Down-weighted by recency of records using 1 / (months since last record)
  - Smoothing applied so nearby cells also down-weight, but less strongly
  - Example: a record yesterday yields priority near zero; no recent record yields priority equal to the model variability

## Quality control and accessibility
- Outputs reviewed by the project team via a data end-user interface to identify anomalies
- DECIDE Recorder tool provides interactive, location-based access (within a 5 km radius) and supports user feedback
- Tool usage: ~5,000 users to date

## Data structure and file formats
- Flat file structure with all outputs stored as GeoTIFF (.tif) in the /data/ folder
- File naming convention reflects taxonomic group and information layer, e.g.:
  - butterfly_decide_priority.tif
  - butterfly_model_variability.tif
  - butterfly_species_richness.tif
  - day_flying_moth_decide_priority.tif
  - day_flying_moth_model_variability.tif
  - day_flying_moth_species_richness.tif
  - night_flying_moth_decide_priority.tif
  - night_flying_moth_model_variability.tif
  - night_flying_moth_species_richness.tif
- Example R usage with terra:
  - terra::rast("butterfly_decide.tif") showing a SpatRaster with 13000 x 7000 cells at 100 m resolution

## Practical usage notes
- All models and predictions were run on the JASMIN high-performance computing platform
- Outputs provide both mean presence probability and uncertainty to inform data-driven recording and prioritisation decisions
- The DECIDE framework enables targeted data collection in areas with high predicted priority and low recent sampling