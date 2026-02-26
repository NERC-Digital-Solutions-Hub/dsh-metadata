# Land Use Mapping Methodology

## Overview
- The document documents a land use/land cover mapping workflow for the Rio Santa catchment using Landsat 8 data (June–July 2019) and ArcGIS Pro tools. It details data acquisition, preprocessing, collection of training data, and classification to produce a map with nine land cover classes.

## Data sources
- Landsat 8 imagery obtained from USGS Earth Explorer with <10% cloud cover; chosen to avoid Landsat 7 scanline errors and to leverage a coastal aerosol band for water and snow mapping.
- Output layers:
  - LU_Landsat8.tif: GeoTIFF of land cover at 30 m resolution.
  - RioSanta_landcover_laydef.qlr: Layer definition file providing style information (land cover key) for the GeoTIFF.

## Data preparation and processing
- Bands in Landsat data mosaicked using the mean operator to handle overlapping polygons.
- Gap filling in ArcGIS Pro (steps):
  1) Measure the maximum fill distance.
  2) Apply focal statistics (mean, circle neighbourhood, ignore NoData) with the measured radius.
  3) Use the null tool on the mosaicked raster restricted to the raster extent.
  4) Use the con tool to replace Null outputs with the focal statistics results (value = 1) and retain the mosaicked raster otherwise.

## Ground truth data collection
- Land cover training points collected in the field (Nov 2019 and Nov 2020) using GPS.
- Additional land cover types inferred from Google Earth imagery due to field access limitations.
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
- When needed, known land cover points were used as references in Google Earth to identify further points.

## Classification method
- A signature file was created with ArcGIS using Landsat 8 data and the collected land cover points.
- Normalisation to reduce shadow effects:
  - 1 0 0 *("bandn" / ("b1"+ "b2"+ "b3"+ "b4"+ "b5"+ "b7"))
- Maximum Likelihood classification applied to all normalised bands in numerical order.
- If certain classes were not classified correctly against field data, the signature file was broadened (e.g., from individual crops to a broader "arable" class).
- After classification, a vector boundary for the Rio Santa catchment was used with the extract by mask tool to produce the catchment land cover map.
- The class “urban” was excluded due to poor mapping accuracy.

## Outputs and layers
- Resulting land cover map for the Rio Santa catchment.
- Class mapping used in the map:
  1) Barren
  2) Forest
  3) Agriculture
  4) Grassland
  5) Orchard
  6) Glacier
  7) Water
  8) Natural vegetation
  9) Wetland
- Style and display information provided via RioSanta_landcover_laydef.qlr.

## Class definitions
- Land cover classes employed in the final map are:
  - Barren
  - Forest
  - Agriculture
  - Grassland
  - Orchard
  - Glacier
  - Water
  - Natural vegetation
  - Wetland

## Reference
- Jamal, S. and Ahmad, W.S., 2020. Assessing land use land cover dynamics of wetland ecosystems using Landsat satellite data. SN Applied Sciences, 2(11), pp.1-24.