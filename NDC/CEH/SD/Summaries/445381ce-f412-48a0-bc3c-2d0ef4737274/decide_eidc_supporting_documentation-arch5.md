# Species data

## Overview
- Presence-only occurrence data for butterflies and moths in Great Britain, compiled by Butterfly Conservation.
- Three taxonomic groups: butterflies (66 species, 7,471,102 records), day-flying moths (43 species, 94,113 records), night-flying moths (716 species, 11,044,769 records).
- Day vs night flying status determined by moth experts.
- Outputs include species distribution models (SDMs), model variability, and DECIDE recording priority maps at 100 m resolution.

## Data sources and taxa
- Butterflies: presence-only data from the Butterflies for the New Millennium dataset.
- Day-flying moths: data from NMRS (National Moth Recording Scheme) and related sources.
- Night-flying moths: data from NMRS.
- Representative species listed (examples include Zygaena loti, Tyria jacobaeae, Heliothis maritima, Archiearis parthenias, and others).

## Environmental data and processing
- Climate: HadUKGrid monthly min/max temperatures and rainfall (2010–2019); used to derive WorldClim bioclimatic variables.
- Land cover: UKCEH 2015 Land Cover Map (LCM) at 25 m resolution for habitat classes.
- Topography: Copernicus DEM v1.1 for Europe at 25 m resolution.
- All environmental layers resampled to 100 m resolution; identical layers used for all SDMs.

## Species distribution modelling (SDMs)
- Spatial data handling: removed spatial-temporal duplicates; each species has at most one observation per 100 m grid cell in GB.
- Pseudoabsences: target-group background generating 10,000 pseudoabsences per species; if a species has more than 10,000 presences, equal numbers of pseudoabsences used.
- Models fitted per species ( four types): GLM, GAM, Random Forest (RF), and Maxent (ME).
- Data balancing: presences and pseudoabsences weighted to equal numbers in all models (except ME, which uses equal numbers by design).
- Validation: 10-fold cross-validation; average AUC used to assess performance.
- Ensemble: predictions from 10 models per model type; mean and standard deviation across folds produced; ensemble weights based on mean AUC across model iterations. If a model type’s mean AUC < 0.75, that type is removed from the ensemble; if all types < 0.75, all are retained and flagged as performing poorly.

## Outputs and units
- Outputs are 100 m x 100 m grid cells across GB (GeoTIFF format).
- Key output layers per group:
  - DECIDE recording priority (e.g., butterfly_decide_priority.tif)
  - SDM model variability (e.g., butterfly_model_variability.tif)
  - Species richness (e.g., butterfly_species_richness.tif)
- Values and interpretation:
  - Species richness: sum of predicted occurrence probabilities across species (e.g., 50% probability for three species = 1.5 richness units).
  - Model variability: sum of standard deviations across the 10 models; higher values indicate greater predictive disagreement.
  - DECIDE recording priority: scaled with time since last record; priority down-weighted as the time since last observation in the vicinity increases, with smoothing across neighboring grid cells.
- Data extents and format: based on the Ordnance Survey National Grid; 100 m resolution; GeoTIFFs with standard naming conventions.

## Data structure and access
- Flat file structure with all outputs stored in /data/ as GeoTIFF (.tif) files.
- Filenames encode taxonomic group and information layer (e.g., butterfly_decide_priority.tif, day_flying_moth_model_variability.tif).
- Example loading in R (terra package):
  - terra::rast("butterfly_decide.tif") shows SpatRaster with dimensions around 13000 x 7000 and 100 m resolution.

## Quality control and user access
- Project team reviewed model outputs via a data end-user interface to identify anomalies.
- DECIDE Recorder tool provides interactive access locally (within ~5 km) and allows user feedback; used by around 5,000 users to date.

## Data governance and reuse
- Outputs are designed for broad reuse in GIS and statistical environments (e.g., R, Terra).
- Built on standardized spatial grids and consistent environmental layers to facilitate interoperability and comparability across taxa.
- Emphasis on documenting processing steps and providing clear metadata through file naming and in-tool descriptions.

## Challenges and considerations for data stewardship
- Incomplete picture of user needs and priorities; ongoing alignment with user requirements needed.
- Timely data acquisition from data providers and ensuring data creators meet metadata and standardization requirements.
- Heterogeneous data sources and formats; large datasets requiring significant transfer and processing resources.
- Managing outdated or legacy databases that may require bespoke interoperability solutions.
- Ensuring ongoing data quality and updates, and maintaining accessible, well-documented data products for discovery and reuse.