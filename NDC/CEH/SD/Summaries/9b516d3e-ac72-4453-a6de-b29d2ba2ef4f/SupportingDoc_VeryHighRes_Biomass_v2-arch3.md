# Biomass Maps Methodology and Data Structure

- Purpose and unit
  - Biomass maps represent dry biomass in tonnes per hectare (t/ha) for each Zone of Interest (ZOI).

- Overall approach
  - Biomass values are estimated with random forest regression models implemented in R.
  - Training data consist of biomass plots collected across four ZOIs to calibrate the model and predict biomass at the pixel level.

- Training data
  - 134 biomass plots distributed roughly equally across the four ZOIs.
  - For each plot: a unique label, location (town), land cover type (closed canopy, tree fallow, shrub fallow, tany maty), latitude/longitude, biomass measurement method (plot or transect), elevation, and biomass components (trees >5 cm DBH, understory, and total above-ground biomass).

- Land cover and spectral data
  - A 4-band multispectral image with 6 m resolution used as predictor variables.
  - High-resolution land cover image used to mask cloud pixels; 1.5 m land cover pixels aggregated to 6 m resolution by taking the mode value to align with the multispectral image.

- Model specifics
  - Random forest regression models are trained for biomass prediction within each ZOI.
  - Training data are used to establish relationships between image spectral signatures and biomass across all classes within a ZOI.
  - The resulting model is then applied to predict biomass for every pixel, producing a biomass raster per ZOI.

- Training data preparation
  - For modeling, only aboveground biomass is used as the training target.
  - The training biomass value is assigned to a single pixel per training point to create the dataset.

- Output data structure
  - Four rasters in TIFF format, one per ZOI, containing predicted biomass values.

- Quality control and limitations
  - Accuracy hinges on capturing the full variation present in the imagery with the limited number of training points.
  - Heterogeneous ZOIs and sparse training data may lead to erroneous biomass estimates for some spectral values.

- Additional data handling notes
  - A point shapefile for each ZOI was created in QGIS to serve as training data for biomass predictions.
  - The process emphasizes careful data preprocessing, alignment of resolutions, and documentation of inputs to support reproducibility.