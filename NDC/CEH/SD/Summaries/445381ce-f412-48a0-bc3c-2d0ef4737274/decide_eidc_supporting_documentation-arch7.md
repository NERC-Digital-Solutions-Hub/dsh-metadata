# Species data

## Overview
- Presents presence-only species data for butterflies and moths in Great Britain, used to build and map species distribution models (SDMs) and to inform DECIDE recording priorities.
- Outputs are map-based raster layers at 100 m resolution, designed for GIS use and end-user exploration.

## Data sources
- Butterfly data: presence-only records from Butterflies for the New Millennium dataset (Butterfly Conservation).
- Moth data: presence-only records from the National Moth Recording Scheme (NMRS).
- Species counts: butterflies = 66 species; day-flying moths = 43 species; night-flying moths = 716 species.
- Species list includes a wide range of named taxa across both groups (illustrative examples provided).

## Environmental data and processing
- Temperature and rainfall: HadUKGrid (monthly min/max temperatures and total rainfall) for 2010–2019; used to derive WorldClim bioclimatic variables.
- Habitat and topography: UKCEH 2015 Landcover Map (LCM) at 25 m; Copernicus DEM (V1.1) at 25 m.
- All environmental layers resampled or converted to a uniform 100 m resolution for SDMs.
- All models use the same environmental layers.

## Modeling approach
- Data preparation: remove spatial-temporal duplicates, leaving one observation per 100 m grid cell across GB.
- Background data: target-group background with 10,000 pseudoabsences per species (or equal numbers to presences when presences < 10,000).
- Models used per species: GLM, GAM, Random Forest (RF), MaxEnt (ME).
- Balancing: presences and pseudoabsences weighted to be equal in all models (except MaxEnt, which requires equal numbers).
- Model validation: 10-fold cross-validation; AUC scores averaged across folds.
- Predictions: probability of presence generated across GB for each model type; mean and standard deviation maps produced per species and model type.
- Ensemble: mean probability and mean SD across model types; models with mean AUC < 0.75 removed from the ensemble; if all model types < 0.75, all models retained but flagged as performing poorly.
- Model variability: quantified as the standard deviation across the ensemble predictions for each species.
- Overall strategy: generate a robust, multi-model, spatially explicit view of species distributions and model uncertainty.

## Outputs and interpretation
- Outputs are 100 × 100 m grid cells over Great Britain in GeoTIFF (.tif) format.
- Key layers per taxonomic group:
  - DECIDE recording priority (priority to record where needed)
  - Species distribution model variability
  - Species richness (stacked probability of occurrence across all species within the group)
- Species richness example: sum of predicted occurrence probabilities across species (e.g., three species with 0.5 probability yield a richness of 1.5 at a cell).
- DECIDE recording priority: scaled to reflect urgency of recording, incorporating time since last record; calculated as model variability multiplied by 1/(months since last record) with spatial smoothing (neighboring cells down-weighted).
- Data are produced separately for butterflies, day-flying moths, and night-flying moths.

## Quality control and accessibility
- Project team reviews model outputs via a data end-user interface to identify anomalies.
- Outputs are accessible through the DECIDE Recorder tool with a local extent (approximately a 5 km radius); around 5,000 users have engaged to date, with feedback mechanisms for issues.

## Data structure and formats
- File organization: flat file structure; all .tif files located in the /data/ folder.
- Format: GeoTIFF (.tif).
- Naming convention: files labeled by taxonomic group and information layer, e.g.:
  - butterfly_decide_priority.tif
  - butterfly_model_variability.tif
  - butterfly_species_richness.tif
  - day_flying_moth_decide_priority.tif
  - day_flying_moth_model_variability.tif
  - day_flying_moth_species_richness.tif
  - night_flying_moth_decide_priority.tif
  - night_flying_moth_model_variability.tif
  - night_flying_moth_species_richness.tif
- Example R loading: terra::rast("butterfly_decide.tif") demonstrates how to read a file as a SpatRaster; details include 13000 × 7000 grid, 100 m resolution, and the 7-digit coordinate reference system in the sample metadata.

## Technical details
- Computations performed on the JASMIN high-performance computing facility.
- Coordinate reference and grid: outputs use 100 m cells on the Ordnance Survey National Grid; example R output shows a Transverse Mercator projection with specific central meridian and parameters.
- Extent and resolution: 100 m resolution; grid extent covers GB (with the specified X and Y extents in the example).