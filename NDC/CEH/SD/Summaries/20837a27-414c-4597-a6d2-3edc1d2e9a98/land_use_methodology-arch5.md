# Land Use Mapping Methodology

## Overview
- Produces a land cover map for the Rio Santa catchment using Landsat 8 data (30 m resolution) and nine land cover classes.
- Outputs: LU_Landsat8.tif (GeoTIFF) with a corresponding RioSanta_landcover_laydef.qlr for styling.
- Class descriptions covered: Barren, Forest, Agriculture, Grassland, Orchard, Glacier, Water, Natural vegetation, Wetland.

## Data provenance and sources
- Landsat 8 data acquired for June–July 2019 with less than 10% cloud cover from USGS Earth Explorer.
- Rationale for Landsat 8: avoids Landsat 7 scanline errors; includes coastal aerosol band to improve water and snow/land cover mapping.

## Data processing workflow
- Band mosaic: individual Landsat bands mosaicked using the mean operator to handle overlapping areas.
- Gap filling in ArcGIS Pro:
  - Measure maximum fill distance.
  - Apply focal statistics (mean) with circle neighbourhood, ignore NoData, radius set to measured distance.
  - Use null tool on mosaicked raster, extent limited to raster extent.
  - Apply con tool to replace null outputs with focal statistics results; otherwise retain mosaicked raster.
- Normalization: per-band normalization to reduce shadow effects using the formula: 1 0 0 * (bandn / (b1 + b2 + b3 + b4 + b5 + b7)).
- Signature creation: using ArcGIS create signatures with normalised bands and field data points to generate the spectral signatures.
- Classification: maximum likelihood classifier; input bands entered in numerical order after normalization.
- Iteration: if misclassification occurred, revise by creating a broader signature (e.g., replace individual crop types with the broader class “arable”).
- Post-classification processing: extract by mask with the Rio Santa catchment boundary; exclude the urban class due to poor accuracy.

## Field data collection and reference data
- Ground truth: land cover training points collected in November 2019 and November 2020 via GPS, across multiple land cover types.
- Point counts across classes (example): Agriculture 20, Forest 30, Glacier 22, Grassland 12, Natural vegetation 25, Orchard 15, Water 21, Wetland 78, Barren 908.
- Supplementary data: additional reference points derived from Google Earth imagery when field access was limited.

## Data classification scheme
- Nine classes defined and used for the map:
  1) Barren
  2) Forest
  3) Agriculture
  4) Grassland
  5) Orchard
  6) Glacier
  7) Water
  8) Natural vegetation
  9) Wetland
- Urban class explicitly excluded due to poor mapping accuracy.

## Metadata and documentation
- Layer styling provided by RioSanta_landcover_laydef.qlr to define the land cover key for the GeoTIFF.
- References: Jamal, S. and Ahmad, W.S. (2020). Assessing land use land cover dynamics of wetland ecosystems using Landsat satellite data. SN Applied Sciences, 2(11), 1-24.

## Data Governance and reuse considerations
- Emphasizes reproducibility through documented processing steps, normalization approach, and signature-based classification.
- Clear data products and classification schema enhance discoverability and reuse, with metadata tied to styling definitions.
- Limitations to consider for uptake: exclusion of the urban class due to poor accuracy; potential misclassifications addressed by broader class definitions; reliance on field and Google Earth imagery for training data where field access was constrained.