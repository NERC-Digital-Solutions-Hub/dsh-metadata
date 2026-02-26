# Units of Recorded Values

## Overview
- Biomass maps express dry biomass values in tonnes per hectare (t/ha) for US units.
- Analytical approach uses random forest regression models implemented in R to estimate biomass within each Zone of Interest (ZOI).

## Data and Training Details
- Training data: 134 biomass plots distributed across four ZOIs, with per-plot information including unique label, location, land cover type (closed canopy, tree fallow, shrub fallow, tany maty), coordinates, biomass components (trees >5 cm DBH, understory, total above-ground biomass), and elevation.
- Target variable: aboveground biomass used for training; each point assigned to a single pixel for model training.
- Land cover and predictors:
  - 4-band multispectral image at 6 m resolution used as predictor variables.
  - Very high-resolution land cover imagery used to mask clouds; 1.5 m land cover pixels re-aggregated to 6 m using mode to match predictor resolution.
- Model training and application:
  - Random forest regression models built per ZOI to relate spectral signatures to biomass training data.
  - The resulting model predicts biomass for each pixel within the respective ZOI.

## Outputs and Data Structure
- Primary outputs: four biomass rasters in .tif format, one per ZOI.
- Supporting data and processing:
  - Point shapefile data for each ZOI used as training data (created in QGIS).
  - Pre-processed predictor layers (4-band multispectral image and land cover, cloud-masked).
  - The dataset structure centers on four spatial rasters corresponding to the ZOIs.

## Quality Control and Limitations
- Model accuracy depends on how well training data capture spectral variation; the ZOIs are heterogeneous and training points are limited, which can lead to erroneous values in some cases.
- Acknowledges potential need for more comprehensive training data to improve reliability across the full spectral range.

## Means and Reporting
- Reported mean biomass values are provided by land cover type and by ZOI:
  - Land cover types include Closed Canopy Forest, Tree Fallow, Shrub Fallow, and Tany Maty.
  - Means are presented for each ZOI and overall (All), illustrating variation across land cover classes and zones.

## Reproducibility and Provenance
- Workflow implemented with R scripts for model training and prediction.
- Shapefiles for training data created in QGIS; predictor data prepared from multispectral imagery; cloud masking informed by high-resolution land cover.

## Governance and Stewardship Implications
- Clear unit standardization (t/ha) supports data sharing and interoperability.
- Comprehensive documentation of data sources, preprocessing steps, and model assumptions enhances discoverability and reuse.
- Data structure (one raster per ZOI) supports versioning, updates, and modular data management.