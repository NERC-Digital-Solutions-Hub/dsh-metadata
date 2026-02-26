# Riparian Wooded Areas in Great Britain (1km Raster)

## Overview
- Provides a 1km resolution raster coverage of wooded areas within riparian zones across Great Britain.
- Riparian zones are defined by a 50-metre buffer around the CEH 1:50,000 watercourse network.
- Wooded areas identified using Land Cover Map 2007 (LCM2007) as coniferous or deciduous woodland.
- Output expresses, for each 1km square, the proportion of woodland within the riparian area as a percentage.

## Data Inputs and Provenance
- CEH 1:50,000 watercourse network (Moore, Morris, & Flavin, 1994); derived from Ordnance Survey 1:50,000 maps.
- Land Cover Map 2007 (LCM2007) GB 25m raster, v1.2; data released via NERC EIDC; based on satellite imagery and UK Biodiversity Action Plan habitats.
- Spatial Reference System: OSGB 1936 / British National Grid.
- Output format: 1km resolution geotiff (.tif).

## Processing and Data Quality
- Processing steps:
  - Buffer the CEH watercourse network by 50 metres.
  - Dissolve the buffered area into a single polygon (ArcMap 10.3).
  - Clip LCM2007 (25m) raster to the buffered polygon.
  - Extract woodland classes (LCM07: 1 = Coniferous, 2 = Deciduous) from the clipped raster.
  - Sum woodland areas and express as the percentage of woodland within each 1km riparian cell.
- Data quality considerations:
  - Based on 25m resolution LCM2007 data; aggregation to 1km may mask fine-scale variation.
  - Woodland classification depends on LCM2007 accuracy (coniferous vs deciduous).
  - Method relies on a fixed 50m buffer, which may not capture all riparian dynamics.

## Data Structure and Access
- File format: 1km resolution GeoTIFF (.tif).
- Cell values: percentage of riparian area that is woodland within each 1km square.
- CRS: OSGB 1936 / British National Grid.

## Governance, Metadata and Sharing Considerations
- Documentation and provenance are anchored in primary data sources (CEH watercourse network; LCM2007) with clear processing steps.
- Licensing and access terms should be verified with source repositories (CEH data and NERC EIDC); ensure proper attribution.
- Update and maintenance: dataset can be reprocessed when input datasets (watercourses, LCM2007) are updated; track versions and dates.
- Data stewardship considerations: maintain metadata detailing inputs, methods, scale, and limitations; assess data discovery, storage, and long-term preservation.

## References
- ESRI (2016) ArcGIS Desktop: Release 10.3.
- Moore, R.V., Morris, D.G., & Flavin, R.W. (1994). Sub-set of UK digital 1:50,000 scale river centreline network. NERC, Institute of Hydrology, Wallingford.
- Morton, R.D., Rowland, C.S., Wood, C.M., Meek, L., Marston, C.G., & Smith, G.M. (2014). Land Cover Map 2007 (25m raster, GB) v1.2. NERC EIDC.