# Units of Recorded Values

## Purpose and Scope
- Produce biomass maps to quantify dry aboveground biomass (t/ha, US units) across four Zones of Interest (ZOI) using standardized, repeatable methods for environmental monitoring.

## Data and Units
- Unit: dry biomass in tonnes per hectare (t/ha), US units.
- Data format: four rasters in .tif, one per ZOI.

## Analytical Methods
- Biomass maps created with random forest regression models implemented in R.
- Training data: 134 biomass plots across the four ZOIs.
- Training point details captured: unique label, town location, land cover type (closed canopy, tree fallow, shrub fallow, tany maty), latitude/longitude, biomass measurement method, elevation, biomass components (trees >5 cm DBH, understory, sampling, total above-ground biomass).
- Modeling approach: only aboveground biomass used as training data; each training point assigned to a single pixel.
- Predictors: a 4-band multispectral image at 6 m resolution.
- Cloud masking: land cover image derived from very high-resolution imagery; cloud pixels masked.
- Pre-processing: land cover pixels aggregated from 1.5 m to 6 m resolution using mode.
- For each ZOI, relationships between image spectral signatures and biomass training data were learned; the resulting model predicted biomass for every pixel.

## Outputs and Interpretation
- Output data: four biomass rasters (one per ZOI).
- Outputs include average aboveground biomass values per land-cover type for each ZOI and overall.
- Example/overall means (All zones):
  - Closed Canopy Forest: ~87 t/ha
  - Tree Fallow: ~16 t/ha
  - Shrub Fallow: ~12 t/ha
  - Tany Maty: ~8 t/ha
- Per-ZOI and land-cover means show higher biomass in closed canopy forests and lower values in fallows and tany maty; specific per-ZOI numbers exist (e.g., CIF around 60–140 t/ha, Tree Fallow around 6–26 t/ha, Shrub Fallow around 4–18 t/ha, Tany Maty around 3–11 t/ha), with All zones values as above.

## Quality Control and Uncertainty
- Accuracy depends on capturing spectral variability; given relatively heterogeneous ZOIs and limited training points, some predictions may be erroneous if the spectral range is not adequately represented in the training data.

## Data Structure
- Four raster datasets in .tif format, one for each ZOI.

## Challenges and Data Accessibility
- Goal to increase dataset value by integrating with other relevant data beyond single-use applications.
- Emphasis on enabling access to the underlying data used to create the final outputs to support broader use and policy monitoring.