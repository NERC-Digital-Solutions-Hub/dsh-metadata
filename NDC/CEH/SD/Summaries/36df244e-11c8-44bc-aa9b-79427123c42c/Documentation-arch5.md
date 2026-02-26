# A land use map of Peninsular Malaysia for the year 2018 (25m grid)

## Overview
- Gridded land use map for Peninsular Malaysia at approximately 25-meter resolution for 2018/2019 baseline.
- Contains nine classes: non-paddy agriculture, paddy fields, rural residential, urban residential, commercial/institutional, industrial/infrastructure, roads, urban, and others.
- Derived from state-level land use polygon data provided by PLANMalaysia, reclassified and rasterized to 25 m.
- Gaps in polygon data (e.g., Kuala Lumpur and parts of several states) filled using reclassified CCI Land Cover (ESA) data, resampled to 25 m.
- Rural vs urban residential areas distinguished using the Global Human Settlement Layer Urban Centre Database (GHS-UCDB).
- Paddy fields integrated from state polygons where available or derived from rice cultivation maps (Begum et al. 2005; FAO 2005) for states lacking detailed paddy data.

## Datasets used
- PLANMalaysia state land use polygons (2018/2019) for 12 Peninsular states: Johor, Kedah, Kelantan, Pahang, Perak, Perlis, Pulau Pinang, Negeri Sembilan, Terengganu, Selangor, Putrajaya, Melaka.
- Climate Change Initiative Land Cover (CCI LC) from ESA (2015) at 300 m resolution; reclassified to three classes (urban, agriculture, others) and resampled to 25 m to fill gaps.
- Global Human Settlement Layer Urban Centre Database (GHS-UCDB R2019A, 2015/2019) for identifying urban areas.
- Paddy field maps: Begum et al. (2005) and FAO (2005) for main rice cultivation areas.
- Additional reference layers: Global Administrative Areas (GADM 2018) for state boundaries.

## Data processing
- a) State land use data: polygons reclassified to match nine classes and rasterized to 25 m; data gaps identified.
- b) Rural vs urban residential: overlaid GHS-UCDB with state data to classify residential areas as urban or rural.
- c) CCI Land Cover: reclassified to urban, agriculture, and others; resampled to 25 m; used to fill gaps in state data.
- d) Paddy fields: incorporated where state data included paddy information; otherwise derived from rice cultivation maps and rasterized to 25 m.
- e) Mosaic creation: merged state data, GHS-UCDB classifications, CCI LC fills, and paddy fields; gaps filled to produce complete land use map.

## Data structure
- Extent: Peninsular Malaysia.
- Format: Raster GeoTIFF with WGS84 CRS.
- Resolution: Approximately 25 meters per pixel.
- Values and classes:
  - 1 = Agriculture (non-paddy) [from state polygon data and CCI LC]
  - 2 = Agriculture (paddy) [from state data, Begum/FAO maps]
  - 3 = Rural Residential [from state data and GHS UCDB]
  - 4 = Urban Residential [from state data and GHS UCDB]
  - 5 = Commercial and Institutional [from state data]
  - 6 = Industrial and Infrastructure [from state data]
  - 7 = Roads [from state data]
  - 8 = Others (forest, lakes/reservoirs, bare land, beach) [from state data and CCI LC]
  - 9 = Urban [from CCI LC]
- File name: Malaysia_land_use_map.tif

## File Name
- Malaysia_land_use_map.tif

## References
- Begum, M., et al. (2005). Weed diversity of rice fields in four districts of Muda rice granary area, North-West Peninsular Malaysia.
- ESA (2017). CCI Land Cover Product User Guide Version 2.
- FAO (2005). ESPIM-related rice cultivation context in Southeast Asia.
- Florczyk, A.J., et al. (2019). GHS-UCDB R2019A.
- Global Administrative Areas (GADM) (2018). Global administrative boundaries.