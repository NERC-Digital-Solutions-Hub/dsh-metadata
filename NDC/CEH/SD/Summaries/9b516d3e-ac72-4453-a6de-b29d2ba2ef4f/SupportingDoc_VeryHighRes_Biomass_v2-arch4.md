# Units of Recorded Values

- Biomass raster values represent dry biomass in tonnes per hectare (t/ha), using US units.

## Analytical Methods

- Biomass maps produced with random forest regression models implemented in R.
- Training data: 134 biomass plots distributed across four Zones of Interest (ZOIs).
- Training data per point includes: unique label, town location, land cover type (closed canopy, tree fallow, shrub fallow, tany maty), geographic coordinates, biomass measurement method (plot or transect), elevation, and biomass components (trees >5 cm DBH, understory, samplings, total above-ground biomass).
- Predictor data: a 4-band multispectral image at 6 m resolution; land cover image used to mask clouds and resampled from 1.5 m to 6 m using the mode function.
- For each ZOI, relationships between spectral signatures and biomass training data are learned; the resulting model predicts biomass per pixel.

## Data Inputs and Training Data

- Training data is derived from aboveground biomass measurements used as the response variable.
- A separate model is built for each ZOI.
- Point shapefiles were created in QGIS for each ZOI to serve as training data.

## Data Outputs and Aggregated Statistics

- Outputs: four rasters in TIFF format, one per ZOI, containing predicted biomass per pixel.
- Training data coverage is heterogeneous; the area within ZOIs is relatively diverse, and the limited number of training points may not capture the full spectral variability, risking some erroneous values.
- Average aboveground biomass values by land-cover type and ZOI (t/ha):
  - ZOI 1: Closed Canopy Forest ~63; Tree Fallow ~6; Shrub Fallow ~4; Tany Maty ~3.
  - ZOI 2: Closed Canopy Forest ~61; Tree Fallow ~14; Shrub Fallow ~13; Tany Maty ~8.
  - ZOI 3: Closed Canopy Forest ~136; Tree Fallow ~26; Shrub Fallow ~18; Tany Maty ~11.
  - ZOI 4: Closed Canopy Forest ~101; Tree Fallow ~19; Shrub Fallow ~14; Tany Maty ~10.
  - All zones combined: Closed Canopy Forest ~87; Tree Fallow ~16; Shrub Fallow ~12; Tany Maty ~8.

## Quality Control

- Accurate biomass calculations require training data that captures most spectral variation; with limited training points and heterogeneous area, some predicted values may be inaccurate.
- Cloud masking and pre-processing steps introduce potential biases if not representative of all spectral classes.

## Data Structure

- The dataset comprises four raster files in TIFF format, one for each ZOI.