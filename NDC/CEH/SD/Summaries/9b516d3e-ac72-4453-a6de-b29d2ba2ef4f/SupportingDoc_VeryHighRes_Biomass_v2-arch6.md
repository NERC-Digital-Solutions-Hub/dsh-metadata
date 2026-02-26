# Biomass Maps Produced Using Random Forest Regression Models

## Purpose and Outputs
- Biomass maps for four Zones of Interest (ZOIs) produced using random forest regression in R; outputs are per-pixel biomass predictions.

## Data Used and Training Data
- 134 biomass plots distributed across four ZOIs used as training data.
- Each point includes: unique label, town name, land cover type (closed canopy, tree fallow, shrub fallow, tany maty), latitude and longitude, biomass measurement method, elevation, biomass components (trees > 5 cm DBH, understory, sampling, total above-ground biomass).
- Only aboveground biomass used for training; a single pixel was assigned to each training point.

## Predictors and Pre-processing
- 4-band multispectral image at 6 m resolution used as predictor variables.
- Land cover image from very high-resolution imagery used to mask clouds; 1.5 m land cover pixels aggregated to 6 m by taking the mode.

## Modelling Approach
- Random forest regression models built to calculate biomass values for each ZOI; models learn relationships between spectral signatures and biomass training data, then predict biomass for each pixel.

## Outputs and Data Structure
- Outputs: four raster files in .tif format, one per ZOI.
- Biomass units: dry biomass in tonnes per hectare (t/ha).

## Quality Control and Limitations
- Accuracy depends on training data covering the spectral variation; heterogeneous ZOIs and limited training points may lead to erroneous values.
- Full range of spectral variation may not be represented in the training data.

## Additional Context
- QGIS used to create point shapefiles for ZOIs and to prepare training data.
- Training data assigned to a single pixel; relationships between spectral signatures and biomass were established across all classes within each ZOI.