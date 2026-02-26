# Species data

## Overview
- Uses presence-only occurrence data for butterflies and moths, collected from Butterfly Conservation sources.
- Data sources: Butterflies for the New Millennium (butterflies) and National Moth Recording Scheme (NMRS) for moths.
- Outputs include species presence indicators, model variability, and recording priority to guide future data collection.

## Data sources and taxonomic scope
- Butterflies: 66 species, 7,471,102 records.
- Day-flying moths: 43 species, 94,113 records.
- Night-flying moths: 716 species, 11,044,769 records.
- Species lists include 53 specific examples (both butterflies and moths) and detailed common names (e.g., Slender Scotch Burnet, The Cinnabar, Six-Spot Burnet, etc.).
- Day- vs. night-flying status determined via moth expert consultation.

## Environmental and ancillary data
- Climate: HadUKGrid monthly min/max temperature and total rainfall (2010–2019); used to derive WorldClim bioclimatic variables.
- Habitat: UKCEH 2015 Landcover map (GB, 25 m resolution).
- Topography: Copernicus Digital Elevation Map (DEM) for Europe (25 m resolution).
- All environmental layers converted to 100 m resolution for modelling.

## Modelling approach (SDMs)
- Data preparation: remove spatial-temporal duplicates; retain a single observation per 100 m grid cell in GB.
- Background sampling: target-group background with 10,000 pseudoabsences per species (or equal number of presences and pseudoabsences if presences < 10,000).
- Modelling methods: GLM, GAM, Random Forest (RF), and Maxent (ME).
  - Presences and pseudoabsences balanced (except ME, which uses equal numbers).
- Model evaluation: 10-fold cross-validation; AUC averaged across folds.
- Ensemble construction: predictions from 10 models per species; compute mean and standard deviation across models.
  - Model types with mean AUC < 0.75 are removed from the ensemble; if all types are below 0.75, all are retained and flagged as poorly performing.
  - Ensemble values are weighted by mean AUC across model iterations.
- Region and run environment: analyses executed on the JASMIN high-performance computing system.

## Outputs and units
- Grids: 100 m x 100 m, Great Britain, using Ordnance Survey National Grid.
- Core derived products:
  - Species richness: sum of predicted occurrence probabilities across species within a taxonomic group.
  - Model variability: sum of standard deviations across the 10 model predictions for each grid cell.
  - DECIDE recording priority: model variability scaled by inverse months since last record (with nearby cells similarly down-weighted via smoothing).
- Interpretation: higher variability indicates more uncertain predictions; higher DECIDE priority highlights locations needing updating in the field.

## Data structure and file format
- Flat file structure with GeoTIFF (.tif) files in /data/.
- File naming conventions: prefixes indicate taxonomic group and information layer (e.g., butterfly_decide_priority.tif, butterfly_model_variability.tif, butterfly_species_richness.tif; similarly for day-flying and night-flying moths).
- Example file description:
  - butterfly_decide_priority.tif: DECIDE recording priority for butterflies.
  - butterfly_model_variability.tif: SD-based variability for butterflies.
  - butterfly_species_richness.tif: butterfly species richness.
- Loading example (R terra package):
  - terra::rast("butterfly_decide.tif") yields a SpatRaster with 13000 x 7000 cells at 100 m resolution; CRS and extent provided in the metadata.

## Quality control and user access
- Project team reviews model outputs for anomalies via a data end-user interface.
- DECIDE Recorder tool provides interactive access within a 5 km radius; about 5,000 users have used it to date.
- User feedback channels exist for issue reporting and data quality improvements.

## Practical implications for data leadership
- Demonstrates a structured pipeline from raw presence-only data to multi-model SDMs, ensemble aggregation, and actionable priority surfaces (DECIDE).
- Highlights governance aspects: data provenance, deduplication, standardized environmental covariates, and transparent model evaluation criteria (AUC threshold).
- Emphasizes metadata and discoverability through standardized file naming, GeoTIFF outputs, and documented data structure.
- Shows collaboration and resource scaling (HPC usage) to manage large, high-resolution ecological datasets.
- Provides a concrete framework for prioritizing field recording, balancing model uncertainty with temporal gaps in data.