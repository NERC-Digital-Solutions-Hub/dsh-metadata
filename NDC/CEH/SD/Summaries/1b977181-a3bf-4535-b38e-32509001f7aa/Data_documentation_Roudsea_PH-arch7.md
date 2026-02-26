# Soil pH at Roudsea Wood National Nature Reserve 1961

## Overview
- Historic soil pH dataset from Roudsea Wood, Cumbria, collected in August 1961.
- Measurements taken at 5–10 cm depth along transects and from under oak trees.
- Digitised from an original map and provided as a GIS-ready shapefile.

## Dataset details
- Geographic coverage: Roudsea Wood, Cumbria, England. Grid reference SD347807.
- Time period: August 1961.
- Data format: ESRI Shapefile (Roudsea_soil_pH_1961.shp).
- Key fields:
  - pH: soil pH value.
  - TYPE: "TRANSECT" (mean pH along transect points) or "UNDER OAK" (spot pH under oak trees).
  - Point_X: OSGB 1936 Easting (metres).
  - Point_Y: OSGB 1936 Northing (metres).

## Data content and sampling design
- Two data categories:
  - TRANSECT: mean pH from soil samples along transect points.
  - UNDER OAK: single spot pH sample under oak trees.
- Sampling depth: 5–10 cm.
- Transect points: mean of 3 samples per point.
- Under oak samples: single sample per location.
- Original map scale: 1:25,000 (map enlarged for digitising).

## Methods and data provenance
- Origin: A. Carlisle, Woodlands Research Section, The Nature Conservancy, Merlewood Research Station.
- Background: post-1955 research at Roudsea Wood; routine pH measurements conducted in 1961.
- Measurement technique: pH determined from fresh soil using a 1:2 soil:distilled water mixture with a glass electrode.
- Data source: original map stored at Centre for Ecology & Hydrology, Lancaster; points digitised into ArcMap.
- Spatial accuracy: estimated to be within less than 50 meters.

## Quality and limitations
- Quality information about sampling practices not on record.
- Samples were not retained after measurement.
- Data values quality-checked against the original map; entry checks performed (range checks and cross-verification).

## GIS considerations
- Coordinate reference: OSGB 1936 Easting/Northing (metres) stored in Point_X and Point_Y.
- Suitable for layering with other UK GIS data; ensure appropriate projection transforms when combining with non-OSGB data.
- Provides spatially explicit pH information for visualization and spatial analysis (e.g., transect vs. under oak contrasts).

## Related reading
- Carlisle, A., & Brown, A. H. F. (1965). The assessment of the taxonomic status of mixed oak (Quercus spp.) populations. Watsonia, 6(2), 120-127.