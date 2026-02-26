# Land Use Mapping Methodology

## Overview
- Objective: produce a land cover map for the Rio Santa catchment using Landsat 8 imagery from 2019 and a supervised classification workflow.
- Rationale for data choice: Landsat 8 avoids Landsat 7 scanline errors and includes a coastal aerosol band that improves mapping water and snow/land cover types.

## Data acquisition and sources
- Landsat 8 data sourced from USGS Earth Explorer for June–July 2019 with <10% cloud cover.
- Data prepared as a GeoTIFF (LU_Landsat8.tif) and accompanied by a layer definition file (RioSanta_landcover_laydef.qlr) for styling.

## Data processing workflow
- Bands mosaicked using the mean to handle overlapping polygons.
- Gap-filling steps in ArcGIS Pro:
  1. Measure maximum fill distance.
  2. Apply focal statistics (mean) with a circular neighborhood, ignoring NoData, radius set to measured distance.
  3. Use the null tool to identify gaps within the raster extent.
  4. Use the Con tool to replace nulls with focal statistics results; otherwise keep the mosaicked raster.
- This produces a continuous raster suitable for classification.

## Land cover data collection and reference data
- Field collection of land cover training points conducted in November 2019 and November 2020 (GPS points documenting local land cover types).
- Supplementary points added via interpretation of Google Earth imagery due to field access limitations; additional types identified (barren land, ice/snow, water, wetlands).
- Training point counts by class:
  - Agriculture: 20
  - Forest: 30
  - Glacier: 22
  - Grassland: 12
  - Natural vegetation: 25
  - Orchard: 15
  - Water: 21
  - Wetland: 78
  - Barren land: 908
- These points underpin the development of the spectral signature for classification.

## Land cover classification methodology
- Signature file created in ArcGIS Pro using Landsat 8 data and collected land cover points.
- Spectral normalization applied per band to reduce shadow effects:
  - Normalization formula applied to each band (described in the document) prior to classification.
- Maximum Likelihood classification used to generate the land cover map for the Rio Santa catchment.
- If classes were misclassified, the signature file was broadened (e.g., initial crop types collapsed into a broader “arable” class).
- Post-classification processing:
  - Clip the map to the Rio Santa catchment boundary (extract by mask).
  - Exclude the urban class due to poor accuracy.

## Output and classes
- Generated raster output depicting land cover for the catchment.
- Defined classes:
  1) Barren
  2) Forest
  3) Agriculture
  4) Grassland
  5) Orchard
  6) Glacier
  7) Water
  8) Natural vegetation
  9) Wetland
- Visualization styling provided via RioSanta_landcover_laydef.qlr.

## References
- Jamal, S. & Ahmad, W.S., 2020. Assessing land use land cover dynamics of wetland ecosystems using Landsat satellite data. SN Applied Sciences, 2(11), pp.1-24.