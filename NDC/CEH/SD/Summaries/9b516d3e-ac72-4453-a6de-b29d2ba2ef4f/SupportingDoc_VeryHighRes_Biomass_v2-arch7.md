# Units of Recorded Values

- Biomass raster values are dry biomass in tonnes per hectare (t/haUS).

## Analytical Methods

- Biomass maps produced using random forest regression models implemented in R to predict biomass for each Zone of Interest (ZOI).
- Training data: 134 biomass plots distributed across four ZOIs, with attributes including location, land cover type (closed canopy, tree fallow, shrub fallow, tany maty), measurement method, elevation, and biomass components (trees >5 cm DBH, understory, samplings, total above-ground biomass).
- Average aboveground biomass values calculated for each land cover type across ZOIs and overall; units in t/ha.
- Training data preparation:
  - Point shapefiles (one per ZOI) created in QGIS for biomass predictions.
  - Aboveground biomass used as the training label; a single pixel per point represents the training data.
  - 4-band multispectral image at 6 m resolution used as predictor variables.
  - Land cover image derived from very high-resolution imagery used to mask clouds; 1.5 m land cover pixels aggregated to 6 m resolution using the mode function.
- Modeling workflow:
  - Relationships between image spectral signatures and biomass training data established for each ZOI.
  - The resulting regression model used to predict biomass for every pixel.
  - Random forest regression applied independently for each ZOI.

## Quality Control

- Accurate biomass calculations require training data that capture most image variation; ZOIs are heterogeneous and training points are limited, so some spectral values may be underrepresented and erroneous values may exist.

## Data Structure

- The dataset comprises four raster files in .tif format, one for each ZOI.