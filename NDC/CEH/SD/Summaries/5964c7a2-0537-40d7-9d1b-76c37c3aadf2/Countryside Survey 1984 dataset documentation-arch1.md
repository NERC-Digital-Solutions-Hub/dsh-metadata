# Broad Habitat Area Estimates by Land Class for Great Britain 1984

## Overview
- National estimates of Broad Habitat stock for Great Britain in 1984, calculated using the 1998 ITE Land Classification.
- Provided as a CSV with total areas (in 000s ha) for each Broad Habitat and Land Class, including 95% confidence intervals (lower and upper estimates).
- Also provided as a 1 km resolution raster (cs1984_stock.tif) where each 1 km pixel contains a mean percentage estimate of habitat within that cell, with bands corresponding to Broad Habitat classes.
- Data derived from Countryside Survey 1984 and linked to established Land Classification schemes (Bunce et al. 1996; Bunce et al. 1981; Bunce et al. 1998).

## Data Files

- CS1984_Broad_Habitat_Stock.csv
  - Columns:
    - YEAR: Survey year
    - LAND_CLASS: ITE Land Class (Bunce et al. 1996; 1981; 1998)
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat description (Jackson, 2000)
    - LAND_CLASS_AREA: Total area of relevant Land Class (000s ha)
    - MEAN_ESTIMATE: Mean area of Broad Habitat for the relevant Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% CI of Broad Habitat area (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI of Broad Habitat area (000s ha)

- cs1984_stock.tif
  - Raster with 1 km pixel size; each band corresponds to a Broad Habitat class.
  - In each band, pixels contain the mean percentage of habitat within that 1 km square, based on 1 km survey squares sampled within each Land Class strata.
  - Band-to-Habitat mapping (examples):
    - Band 2: Broad Habitat 1 (Coniferous Woodland); Broad Habitat 2 (Broadleaved Mixed and Yew Woodland)
    - Band 3: Broad Habitat 1 (Boundary and Linear Features); Broad Habitat 1–3 combinations shown in accompanying mapping
    - Bands 4–17: correspond to other habitat classes as listed (e.g., Arable, Grasslands, Wetlands, Water, Urban, etc.)
  - Spatial Reference: 1 km pixel, British National Grid, Transverse Mercator, extent Great Britain

## Methodology

- Estimates are national totals for Broad Habitats (1–17) derived from the 1998 ITE Land Classification.
- National stock and per-Land Class Broad Habitat areas are provided with means and 95% confidence intervals.
- The 1 km raster estimates reflect mean habitat percentages within 1 km survey squares across Land Class strata; the 1 km sampling framework underpins the reported means and uncertainties.

## Spatial Information

- Pixel size: 1 km (1000 m)
- Coordinate system: British National Grid (OSGB36)
- Projection: Transverse Mercator
- Extent: Great Britain

## Usage, Access, and Acknowledgement

- All CS data must be acknowledged as Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Copyright: Countryside Survey © NERC-CEH; All rights reserved.
- Data may be used for landscape-scale analyses, historical habitat assessments, and cross-walks with Land Classification schemes, with awareness of 1984 date and 1998 ITE integration.

## References and Related Publications

- Carey et al. (2008). Countryside Survey: UK Results from 2007; background and methods.
- Scott (2007). CS Technical Report No. 4/07: Statistical report — methodology for generating national estimates from 1 km survey squares.
- Bunce et al. (1981, 1996, 1998). ITE Merlewood Land Classification of Great Britain and related classifications.
- Jackson (2000). Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
- Additional CS-related references and links to the Countryside Survey project and methodology.