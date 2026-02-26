# A land use map of Peninsular Malaysia for the year 2018 (25m grid)

## Overview
- Produces a gridded land use map of Peninsular Malaysia at approximately 25-meter resolution for 2018/2019.
- Contains nine land use classes: non-paddy agriculture, paddy fields, rural residential, urban residential, commercial/institutional, industrial/infrastructure, roads, others (forest, water, bare land, beaches), and urban.
- Based on state-level land use polygons from PLANMalaysia (12 states on the peninsula) and augmented with multiple supplementary datasets to fill gaps and provide additional context.
- Gaps in state polygon data (notably Kuala Lumpur and some areas in several states) were infilled using the Climate Change Initiative Land Cover (CCI LC) 2015 raster data (reclassified to fit the schema) and resampled to 25 m.
- Rural vs. urban residential areas were delineated using the Global Human Settlement Layer Urban Centre Database (GHS UCDB 2015/2019) and overlaid with state land use data.
- Paddy fields were sourced from detailed state data where available; for other areas, rice cultivation maps (Begum et al., 2005; FAO 2005) were georeferenced and vectorized to derive paddy field extents.
- Final mosaic map created by merging state polygons, GHS-derived classifications, CCI LC infill, and paddy field layers; produced as a GeoTIFF: Malaysia_land_use_map.tif, in WGS84.

## Datasets used
- a) State land use data: PLANMalaysia polygons for 12 states; reclassified to a common scheme and rasterized to 25 m.
- b) CCI Land Cover (ESA): global 300 m grid (2015); reclassified to three main classes (urban, agriculture, others) and resampled to 25 m to fill gaps.
- c) Global Human Settlement Layer Urban Centre Database (GHS-UCDB R2019A): identifies urban centers in 2015; used to distinguish urban vs. rural residential.
- d) Paddy fields maps: two rice cultivation maps (Begum et al., 2005; FAO, 2005) used to locate main paddy areas where state data lacked paddy detail.

## Data processing
- a) State land use data: PLANMalaysia polygons were reclassified to nine standard classes and rasterized to 25 m; coverage maps show gaps (e.g., Kuala Lumpur, parts of Johor, Kedah, Kelantan, Pahang).
- b) Rural and Urban Residential Areas: GHS UCDB overlaid with state land use data to classify residential areas as rural or urban.
- c) CCI Land Cover: 300 m raster reclassified into three classes (urban, agriculture, others) and resampled to 25 m to fill data gaps in the state polygons.
- d) Paddy fields: Paddy areas extracted from state data where available; for states lacking detail, paddy fields were derived from rice maps and rasterized to 25 m.
- e) Creating the mosaic land use map: Combined state polygons, GHS-derived residential classes, and CCI LC infill with paddy field layers to produce a seamless map; example shown for Kuala Lumpur where gaps were infilled with CCI LC data.

## Data structure
- Extent: Peninsular Malaysia.
- Format: Raster GeoTIFF.
- Coordinate reference system: WGS84.
- Pixel size: approximately 25 meters (in decimal degrees).
- Land use classes and raster values (illustrative mapping):
  - 1: Agriculture (non-paddy) – state polygon data + CCI LC
  - 2: Agriculture (paddy) – state polygon data + Begum et al./FAO maps
  - 3: Rural Residential – state polygon data + GHS UCDB
  - 4: Urban Residential – state polygon data + GHS UCDB
  - 5: Commercial and Institutional – state polygon data
  - 6: Industrial and Infrastructure – state polygon data
  - 7: Roads – state polygon data
  - 8: Others (forest, water bodies, bare land, beach) – state polygon data + CCI LC
  - 9: Urban – CCI LC
- File naming: Malaysia_land_use_map.tif

## File Name
- Malaysia_land_use_map.tif

## References
- Begum, M., et al. (2005). Weed diversity of rice fields in four districts of Muda rice granary area, North-West Peninsular Malaysia. Malaysian Applied Biology, 34(2), 31.
- ESA. Land Cover CCI Product User Guide Version 2. Technical Report (2017).
- FAO Regional Office for Asia and the Pacific; ESPIM project materials (2005).
- Florczyk, A.J., et al. (2019). GHS-UCDB R2019A – Urban Centre Database 2015. European Commission, JRC.
- Global Administrative Areas (GADM) database (2018). University of California, Berkeley.