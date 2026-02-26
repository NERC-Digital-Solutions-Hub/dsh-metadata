# Species data

## Overview
- Presence-only occurrence data for two taxonomic groups:
  - Butterflies: 66 species, 7,471,102 records
  - Day-flying moths: 43 species, 94,113 records
  - Night-flying moths: 716 species, 11,044,769 records
- Data collated by Butterfly Conservation from the Butterflies for the New Millennium dataset and the National Moth Recording Scheme (NMRS)
- Day vs. night classification for moths determined through expert consultation
- Outputs include species distribution estimates, model variability, and recording priority

## Data sources and taxonomic detail
- Presence-only occurrence data from established citizen-science and monitoring programs
- Species lists and status defined per group (example species names provided for moths)

## Environmental data and processing
- Climate: HadUKGrid (monthly min/max temperature and total rainfall) for 2010–2019
- Bioclimatic variables: derived from HadUKGrid data using WorldClim suite
- Habitat: UKCEH 2015 Landcover Map (GB, 25 m resolution)
- Topography: Copernicus Digital Elevation Map V1.1 (Europe, 25 m)
- All environmental layers converted to 100 m resolution
- Same environmental layers used across all Species Distribution Models (SDMs)

## Species distribution modelling (SDMs)
- Data preparation: remove spatial-temporal duplicates; retain a single observation per 100 m grid cell in GB
- Background: target-group approach generating 10,000 pseudoabsences per species (or equal numbers if presences exceed)
- Models fitted (per species): GLM, GAM, Random Forest (RF), Maxent (ME)
- Balancing: presences and pseudoabsences weighted to equalize numbers; ME forced to equal numbers
- Validation: 10-fold cross-validation; models evaluated with AUC; mean AUC across folds used
- Predictions: probability of presence across GB for each model type; compute mean and standard deviation across 10 model iterations
- Ensemble construction: mean probability and mean SD across model types, weighted by mean AUC
- Model inclusion: if a model’s mean AUC < 0.75, it is removed from the ensemble; if all models fall below 0.75, all are retained but flagged as performing poorly
- Predictive accuracy metric: model “variability” (standard deviation) of the ensemble for each species
- Computing environment: runs on the JASMIN high-performance computer

## Nature and units of recorded values
- Outputs are 100 m x 100 m grid cells across Great Britain (OS National Grid)
- Species richness: sum of predicted probability of occurrence across all species in a group
  - Example: three species with 50% predicted presence → richness = 1.5
- Model variability: total SD across the 10 models (for each species, per grid cell)
- DECIDE recording priority: same scale as model variability
  - Down-weighting by time since last record in the vicinity; smoothing applied to neighboring cells
  - Priority scaled by multiplying variability by 1 / (months since last record)
  - Example: a record yesterday yields priority near zero; no recent records yields priority equal to the variability

## Quality control
- Data end-user interface used by the project team to identify anomalies
- DECIDE Recorder tool provides interactive access (limited to a ~5 km radius per location)
- Approximately 5,000 users; feedback mechanism for issue reporting

## Data structure and file format
- Flat file structure with all .tif files in the /data/ folder
- GeoTIFF format (.tif)
- Filenames reflect taxonomic group and information layer, e.g.:
  - butterfly_decide_priority.tif
  - butterfly_model_variability.tif
  - butterfly_species_richness.tif
  - day_flying_moth_decide_priority.tif
  - day_flying_moth_model_variability.tif
  - day_flying_moth_species_richness.tif
  - night_flying_moth_decide_priority.tif
  - night_flying_moth_model_variability.tif
  - night_flying_moth_species_richness.tif
- Data can be loaded in GIS or statistical software (example provided for R using the terra package)

## How to read the data (example)
- GeoTIFF files can be loaded as raster objects; example complexity shown indicates 100 m resolution and the NGRS coordinate framework

## Additional notes
- The approach emphasizes standardized, comparable outputs (richness, variability, and recording priority) to support monitoring and policy evaluation
- All modelling and outputs are designed to support a consistent, transparent monitoring framework with quality control and user accessibility through the DECIDE platform