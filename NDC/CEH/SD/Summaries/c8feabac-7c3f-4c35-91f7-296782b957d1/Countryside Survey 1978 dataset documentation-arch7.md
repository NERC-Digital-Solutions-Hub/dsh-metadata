# Broad Habitat Area Estimates by Land Class for Great Britain

## Overview
- Two data products from Countryside Survey describing Broad Habitat stock for Great Britain, based on 1978 data and the 1990 ITE Land Classification.
- Purpose: enable map-based understanding of Broad Habitat distribution by land class for GIS analysis.
- Excludes Broad Habitats 15 and 20 in the estimates/raster.
- Data are published with methodological references and explicit provenance.

## Data Products

- CS1978_Estimates_by_LC.csv
  - National estimates of Broad Habitat stock (Habitats 1–21, excluding 15 and 20) for 1978.
  - Calculated using the 1990 ITE Land Classification (see Scott, 2007).
  - Columns:
    - YEAR: Year of Survey
    - LAND_CLASS: ITE Land Class (code)
    - BROAD_HABITAT: Broad Habitat code
    - BROAD_HABITAT_NAME: Broad Habitat name
    - LAND_CLASS_AREA: Total area of the Land Class (000s ha)
    - MEAN_ESTIMATE: Mean estimated area of Broad Habitat for the Land Class (000s ha)
    - LOWER_ESTIMATE: Lower 95% CI bound (000s ha)
    - UPPER_ESTIMATE: Upper 95% CI bound (000s ha)

- CS78_BH1_17.tif
  - 1 km pixel raster created by converting Land Class totals to percentages of Broad Habitat per 1 km pixel.
  - Bands (1–16) each represent a Broad Habitat class:
    - Band 1: Broadleaved Mixed and Yew Woodland
    - Band 2: Coniferous Woodland
    - Band 3: Boundary and Linear Features
    - Band 4: Arable and Horticulture
    - Band 5: Improved Grassland
    - Band 6: Neutral Grassland
    - Band 7: Calcareous Grassland
    - Band 8: Acid Grassland
    - Band 9: Bracken
    - Band 10: Dwarf Shrub Heath
    - Band 11: Fen, Marsh, Swamp
    - Band 12: Bog
    - Band 13: Standing Open Waters and Canals
    - Band 14: Rivers and Streams
    - Band 15: Inland Rock
    - Band 16: Urban
  - Pixel size: 1 km (1000 m)
  - Coordinate system / projection: British National Grid (OSGB36), Transverse Mercator for Great Britain
  - Extent: Great Britain

## Data Use, Provenance and Acknowledgement
- All Countryside Survey data must be acknowledged.
- Acknowledgement statement to use on copies, publications, and presentations:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and "Countryside Survey © NERC - Centre for Ecology & Hydrology. All rights reserved."
- Data origin: Countryside Survey, CEH; methodology documented in associated reports and technical papers.

## Related Publications and References
- Countryside Survey website for project overview and methodology documents.
- Wood et al. (2012): Countryside Survey—Measuring Habitat Change Over 30 Years; 1978 Data Rescue (Final Report) CEH Project NEC03689.
- Scott (2007): CS Technical Report No. 4/07 (Statistical Report) on generating national estimates from 1 km survey squares.
- Bunce et al. (1996, 1981): ITE Merlewood Land Classification of Great Britain; descriptions of Land Classes and their relevance to Countryside Survey.
- Jackson (2000): Guidance on interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
- Countryside Survey Technical Reports (e.g., TR1/07 Field Mapping Handbook) and related publications linked from the Countryside Survey website.

## Practical GIS Implications
- Facilitates map-based visualization of Broad Habitat distribution by Land Class at national level (1978 baseline).
- Raster product provides per-pixel composition of Broad Habitats at 1 km resolution, enabling spatial analyses and overlay with other GB GIS layers.
- Useful for trend analyses, habitat change assessment, and policy/client-targeted map visualizations when combined with the underlying Land Classification data and accompanying methodological notes.