# Land Use Mapping Methodology

## Objective
- Develop a 30 m resolution land cover map for the Rio Santa catchment using Landsat 8 data from 2019.

## Data sources
- Landsat 8 imagery (June–July 2019, <10% cloud) from USGS Earth Explorer; advantages include absence of Landsat 7 scanline errors and a coastal aerosol band useful for water and snow/water mapping.
- Layer style files: RioSanta_landcover_laydef.qlr for land cover key and styling.

## Processing workflow
- Mosaicking: individual Landsat bands mosaicked with the mean operator to handle overlapping polygons.
- Gap filling in ArcGIS Pro:
  - Measure maximum fill distance.
  - Apply focal statistics (mean, circular neighborhood, ignore NoData).
  - Use null tool to identify gaps.
  - Use con tool to fill gaps with the computed statistics where applicable.
- Final raster extent aligned to the mosaic; gaps filled to produce a continuous dataset.

## Field data collection and training points
- Land cover training points collected in Nov 2019 and Nov 2020 via GPS.
  - Initial attempts at identifying plant types shifted to broader land cover categories due to classification errors.
  - Additional land cover types inferred from Google Earth imagery when field access was limited.
- Training point counts by class:
  - Agriculture 20
  - Forest 30
  - Glacier 22
  - Grassland 12
  - Natural vegetation 25
  - Orchard 15
  - Water 21
  - Wetland 78
  - Barren land 908

## Signature creation and normalization
- Signature file created in ArcGIS Pro using Landsat 8 data and training points.
- Normalization to reduce shadow effects:
  - 1 0 0 * (bandn / (b1 + b2 + b3 + b4 + b5 + b7))
- All normalized bands fed into the maximum likelihood classification.

## Classification approach
- Maximum Likelihood classifier applied to the input bands (in numerical order after normalization) to produce the land cover raster.
- If classifications did not match field data, a new broader signature file was created (e.g., replacing detailed crop types with the broader class "arable").
- Spatial masking with the Rio Santa catchment boundary to extract the catchment land cover map.
- Urban class excluded from the study due to poor accuracy.

## Output products
- GeoTIFF: LU_Landsat8.tif (land cover raster for the Rio Santa catchment).
- Layer definition: RioSanta_landcover_laydef.qlr (land cover key styling).
- Final product suitable for reporting and analysis at catchment scale.

## Land cover classes (nine categories)
1. Barren
2. Forest
3. Agriculture
4. Grassland
5. Orchard
6. Glacier
7. Water
8. Natural vegetation
9. Wetland
- Urban excluded due to poor mapping accuracy.

## Limitations and considerations
- Urban areas were not mapped due to low accuracy; potential re-inclusion would require refinement or higher-resolution data.
- Heavy reliance on field-access challenges necessitated using imagery-based references (Google Earth) for supplemental training points.
- 30 m resolution limitations may affect accuracy in heterogeneous landscapes; broader class definitions were used when necessary.

## Reference
- Jamal, S. and Ahmad, W.S., 2020. Assessing land use land cover dynamics of wetland ecosystems using Landsat satellite data. SN Applied Sciences, 2(11), pp.1-24.