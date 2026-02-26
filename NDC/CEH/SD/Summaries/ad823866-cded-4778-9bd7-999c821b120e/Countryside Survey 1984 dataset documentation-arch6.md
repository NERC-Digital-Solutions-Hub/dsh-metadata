# Broad Habitat Area Estimates by Land Class for Great Britain 1984

## Overview
- A Countryside Survey dataset providing national estimates of Broad Habitat stock (Habitat codes 1–17) for Great Britain in 1984.
- Estimates are calculated using the 1998 ITE Land Classification and are presented as total area (in thousands of hectares) per Broad Habitat and Land Class, including 95% confidence intervals.
- Two data products are provided:
  - A CSV file (cs1984_Broad_Habitat_Stock.csv) with tabular estimates by Year, Land Class, and Broad Habitat.
  - A 1 km raster (cs1984_stock.tif) with mean percentage estimates of habitat within each 1 km pixel, across Broad Habitat bands.
- Data derived from Countryside Survey 1984; methodology and crosswalks to Land Classification documented in referenced publications.

## Data Files and Structure

- cs1984_Broad_Habitat_Stock.csv (CSV)
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class (per Bunce et al. references)
    - BROAD_HABITAT: Broad Habitat code (1–17)
    - BROAD_HABITAT_NAME: Description of Broad Habitat
    - LAND_CLASS_AREA: Total Area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for relevant Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% confidence limit (000s ha)
    - UPPER_ESTIMATE: Upper 95% confidence limit (000s ha)
- cs1984_stock.tif (TIFF raster)
  - Spatial resolution: 1 km per pixel (1000 m)
  - Coordinate system: British National Grid (OSGB36), Transverse Mercator
  - Extent: Great Britain
  - Bands: Each band corresponds to a Broad Habitat class; bands contain the mean percentage value of the amount of that habitat within each 1 km pixel.
  - Band-to-habitat mapping: The notes describe crosswalks for how Broad Habitat classes map to bands within the raster, e.g., “Band 2” corresponds to a specific habitat/class combination as outlined in the dataset documentation. The exact crosswalk is described in the notes (e.g., Broad Habitat 2, Broad Habitat 1 conventions for Coniferous Woodland, Boundary and Linear Features, etc.).

## Spatial and Technical Details

- Pixel size (raster): 1 km (1000 m)
- CRS: OSGB1936 / British National Grid
- Projection: Transverse Mercator
- Extent: Great Britain
- Data use: Acknowledgement required — “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © NERC”
- Units:
  - CSV: area in thousands of hectares (000s ha)
  - Raster: percentage estimates per pixel for each Broad Habitat band

## How to Use the Data

- Data alignment and integration
  - Use the CSV to obtain national and per-Land Class estimates of Broad Habitats with associated confidence intervals.
  - Use the raster to visualize and summarize habitat distribution at 1 km resolution across Great Britain.
  - Cross-wwalk between LAND_CLASS and BROAD_HABITAT in the CSV to aggregate or compare by class and habitat.
- Potential data products
  - Dashboards or pivot tables showing area by Land Class x Broad Habitat with uncertainty.
  - Maps displaying the spatial distribution and concentration of Broad Habitats across Great Britain.
  - Time-slice comparisons (if additional years are available) by comparing MEAN_ESTIMATE and confidence intervals.
- Validation and quality considerations
  - Estimates are based on the 1998 ITE Land Classification crosswalk; consider limitations when applying to non-1984 contexts.
  - The raster bands reflect mean percentages derived from 1 km survey squares within Land Class strata; interpret pixel values as habitat density within the band’s Broad Habitat class.
  - All outputs should include the required Countryside Survey acknowledgement.

## Use-Cases for Data Support

- Facilitating discovery and reuse: provide clear data dictionary, crosswalks, and example queries to enable end users to explore habitat stock by land class.
- Data cleaning and preparation: join the CSV with other Countryside Survey outputs by Year, Land Class, or Broad Habitat; harmonize units if integrating with other datasets.
- Communicating insights: create dashboards that highlight national totals, regional patterns, and confidence intervals; develop maps to show habitat distribution and concentration.

## Acknowledgements and References

- Data provenance: Countryside Survey 1984; national estimates of Broad Habitat stock derived from the ITE Land Classification (Bunce et al.; Scott, 2007).
- Key references include:
  - Bunce et al. 1996, 1998: ITE Merlewood Land Classification
  - Scott 2007: Statistical framework for CS national estimates
  - Jackson 2000: Guidance on interpretation of Biodiversity Broad Habitat Classification
  - Carey et al. 2008: Countryside Survey UK Results from 2007 (background methodology references)
- Access and usage: Data must be acknowledged as Countryside Survey data owned by NERC - CEH; Countryside Survey © NERC-CEH. Links and publication references are provided in the dataset notes.