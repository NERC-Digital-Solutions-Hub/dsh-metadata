# Land Use Mapping Methodology

## Objective
- Create a land cover map for the Rio Santa catchment using Landsat 8 data from June–July 2019 with minimal cloud cover.
- Avoid Landsat 7 issues; utilize Landsat 8 coastal aerosol band to improve mapping of water and snow land covers.
- Produce a self-serve data product (raster map) with accompanying styling information.

## Data Inputs
- Landsat 8 GeoTIFF: LU_Landsat8.tif (land cover data at 30 m resolution; Rio Santa catchment)
- Layer/style files: RioSanta_landcover_laydef.qlr (style information for the land cover map)

## Data Processing Workflow
- Acquire Landsat 8 data from USGS Earth Explorer; mosaic bands using the mean operator to handle overlaps.
- Gap filling in ArcGIS Pro:
  - Measure maximum fill distance
  - Apply focal statistics (mean, circular neighborhood, ignore NoData)
  - Use Null tool to identify gaps
  - Apply conditional raster logic (con tool) to fill gaps with focal statistics output where appropriate

## Training Data and Signature Creation
- Field collection (Nov 2019 and Nov 2020): GPS points labeled by land cover type
  - 20 agriculture, 30 forest, 22 glacier, 12 grassland, 25 natural vegetation, 15 orchard, 21 water, 78 wetland, 908 barren land
- Supplementary data from Google Earth to identify additional land cover types due to field inaccessibility
- Used these points to build a signature file for classification

## Classification Approach and Normalization
- Create signatures using Landsat 8 data and training points
- Normalize spectral energy per band to reduce shadow effects:
  - 1 0 0 * (bandN / (b1 + b2 + b3 + b4 + b5 + b7))
- Apply Maximum Likelihood classifier with all normalized bands
- If classification misclassifies certain classes, broaden the class definitions (e.g., from individual crops to “arable”)

## Output Products and Map Production
- Produces a land cover raster for the Rio Santa catchment
- Use extract-by-mask with the catchment boundary to derive the final map
- Excluded land cover class: Urban (poor accuracy)
- Associated style file provided for visualization (QLR)

## Land Cover Classes Used
1. Barren
2. Forest
3. Agriculture
4. Grassland
5. Orchard
6. Glacier
7. Water
8. Natural vegetation
9. Wetland

## Data Accessibility and Visualization
- Output includes styling information (layer definition) to enable consistent display and interpretation
- Focus on producing a usable product for further analysis and interpretation across stakeholders

## Notes and References
- Base methodology and referenced approach: Jamal, S. and Ahmad, W.S., 2020. Assessing land use land cover dynamics of wetland ecosystems using Landsat satellite data. SN Applied Sciences, 2(11), p.1-24.