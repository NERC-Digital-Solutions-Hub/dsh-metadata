# Land Use Mapping Methodology

## Overview
- Describes a GIS-based approach to map land use/land cover for the Rio Santa catchment using Landsat 8 imagery.
- Rationale includes improved data quality: Landsat 8 avoids Landsat 7 scanline artifacts and includes a coastal aerosol band beneficial for distinguishing water and snow/ice.

## Data sources and timing
- Landsat 8 imagery acquired for June–July 2019 with <10% cloud cover from USGS Earth Explorer.
- Data chosen to minimize scanline errors and to leverage additional spectral information.

## Data processing and gap filling
- Images mosaicked using the mean operator to handle overlapping polygons.
- Gap filling in ArcGIS Pro via a multi-step workflow:
  - Measure maximum fill distance.
  - Apply focal statistics (mean) with circular neighborhood, ignore NoData, radius equal to measured distance.
  - Use Null tool to set gaps to NoData, constrained to raster extent.
  - Use Con tool to replace gaps with focal statistics outputs where appropriate.
- Resulting raster prepared for classification.

## Field data collection and reference data
- Land cover training points collected in the field (Nov 2019 and Nov 2020) using GPS:
  - 20 agriculture, 30 forest, 22 glacier, 12 grassland, 25 natural vegetation, 15 orchard, 21 water, 78 wetland, 908 barren land points.
- When field points were insufficient, additional points were identified in Google Earth imagery; some land cover types were broadened (e.g., from specific crops to “arable”) to improve classification.

## Land cover classification workflow
- Created a spectral signature file with Landsat 8 data and the field/reference points.
- Normalisation of spectral energy per band to reduce shadows:
  - Formula: 1 0 0 * (bandn / (b1 + b2 + b3 + b4 + b5 + b7)).
- Maximum Likelihood classifier used to produce the land cover map.
- If initial signatures misclassified classes, the signature file was broadened and re-run (e.g., refining from specific crops to a broader “arable” class).

## Output and map product
- Generated a land cover raster for the Rio Santa catchment.
- An extracted vector boundary was used with the “extract by mask” tool to produce the catchment-specific map.
- The urban class was excluded due to poor mapping accuracy.

## Land cover classes
1. Barren
2. Forest
3. Agriculture
4. Grassland
5. Orchard
6. Glacier
7. Water
8. Natural vegetation
9. Wetland

## Data governance and monitoring relevance
- Emphasizes the need for robust metadata, data quality, and reproducibility in monitoring frameworks.
- Open data considerations handled via sharing of reference data and signatures, with acknowledgment that some classes were broadened to improve accuracy.
- Highlights potential challenges relevant to monitoring programs: data gaps, reliance on ground truth/field data, integration with diverse datasets, and the need to document processing steps for transparency.

## References
- Jamal, S. and Ahmad, W.S., 2020. Assessing land use land cover dynamics of wetland ecosystems using Landsat satellite data. SN Applied Sciences, 2(11), pp.1-24.