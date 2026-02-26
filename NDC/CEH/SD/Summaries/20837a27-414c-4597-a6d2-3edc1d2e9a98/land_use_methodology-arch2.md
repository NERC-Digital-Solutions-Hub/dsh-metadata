# Land Use Mapping Methodology

## Data sources and inputs
- Landsat 8 imagery for June–July 2019 (cloud cover <10%) from USGS Earth Explorer; chosen to avoid Landsat 7 scanline issues and to leverage the coastal aerosol band for water and snow mapping.
- Bands mosaicked by mean to handle overlaps.
- Gap filling in ArcGIS Pro using: measure maximum fill distance; focal statistics (mean, circular neighborhood, ignore no data); apply null to gaps; con tool to replace null with focal results where appropriate.
- Field-collected land cover training points (Nov 2019 and Nov 2020) with GPS coordinates; supplementary land cover types identified from Google Earth imagery due to field inaccessibility.
- Training point counts: 20 agriculture, 30 forest, 22 glacier, 12 grassland, 25 natural vegetation, 15 orchard, 21 water, 78 wetland, 908 barren.
- Rio Santa catchment boundary used to clip the final map.
- Layer styling information provided by RioSanta_landcover_laydef.qlr.

## Training data and signature
- Signature file created with ArcGIS using Landsat data and collected land cover points.
- Shadow mitigation via normalisation: 1 0 0 * ("bandn" / ("b1" + "b2" + "b3" + "b4" + "b5" + "b7")).

## Classification and processing
- Maximum Likelihood classification applied using all normalised input bands.
- If signatures misclassify classes, signatures are revised to broader categories (e.g., combining crops into "Agriculture" or similar).
- Urban class excluded due to reported poor accuracy.

## Outputs and styling
- Final output: 30 m resolution land cover raster for the Rio Santa catchment.
- Vector boundary used with extract by mask to produce catchment-specific land cover.
- Urban class not included in the final map.
- Style and legend provided via the QLR layer definition file.

## Land cover classes
- 1 Barren
- 2 Forest
- 3 Agriculture
- 4 Grassland
- 5 Orchard
- 6 Glacier
- 7 Water
- 8 Natural vegetation
- 9 Wetland

## Data management and references
- Method supports standardized, reproducible outputs suitable for monitoring environmental health and policy performance.
- References: Jamal, S. and Ahmad, W.S., 2020. Assessing land use land cover dynamics of wetland ecosystems using Landsat satellite data. SN Applied Sciences, 2(11), pp.1-24.