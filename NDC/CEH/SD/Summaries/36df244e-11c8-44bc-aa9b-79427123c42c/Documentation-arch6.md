# A land use map of Peninsular Malaysia for the year 2018 (25m grid)

## Overview
- Gridded land use map for Peninsular Malaysia at approximately 25-meter resolution.
- Nine land use classes: non-paddy agriculture, paddy fields, rural residential, urban residential, commercial/institutional, industrial/infrastructure, roads, urban, others.
- Based on detailed state land use polygons for 2018/19 (PLANMalaysia), reclassified and rasterized to 25 m.
- Gaps infilled with reclassified ESA CCI Land Cover 2015 data (300 m) resampled to 25 m.
- Rural vs urban residential areas identified using the Global Human Settlement Layer Urban Centre Database (2015).
- Paddy fields derived from state data where available; otherwise located and vectorised using rice cultivation maps (FAO 2005; Begum et al. 2005) and rasterised to 25 m.
- Produced under the project Malaysia - Flood Impact Across Scales, funded by the Newton-Ungku Omar Fund.

## Datasets used
- State land use polygons for 2018/2019 from PLANMalaysia (twelve states on the Peninsular) and derived paddy field data.
- Climate Change Initiative Land Cover (CCI LC) from ESA (2015), 300 m resolution.
- Global Human Settlement Layer Urban Centre Database (GHS-UCDB R2019A) for urban extents (2015).
- Paddy field maps: Begum et al. (2005) and FAO (2005).

## Data processing
- a) State land use data: polygons reclassified into nine categories and rasterized to 25 m.
- b) Rural/Urban residential: overlaid with GHS-UCDB to differentiate rural vs urban.
- c) CCI Land Cover: reclassified to three classes (urban, agriculture, others) and resampled to 25 m; used to fill gaps.
- d) Paddy fields: detailed state data for some states; for others, vectorised from rice maps and rasterised to 25 m.
- e) Mosaic creation: gaps filled with CCI data, then merged with GHS-derived residential classes and paddy fields to produce final map.
- f) Output: raster GeoTIFF with WGS84; 25 m grid; each cell assigned a single land use value (nine classes).

## Data structure / Output
- File name: Malaysia_land_use_map.tif
- Coordinate reference system: WGS84
- Resolution: approximately 25 meters (grid cells)
- Values correspond to nine land use classes as defined (with sources listed in the processing steps)

## File Name
- Malaysia_land_use_map.tif

## References
- Begum, M. et al. (2005); FAO (2005); ESA (CCI Land Cover v2; 2017/2015); Florczyk et al. (GHS-UCDB 2019); Global Administrative Areas (GADM 2018); PLANMalaysia data; related methodological and dataset references cited in the document.