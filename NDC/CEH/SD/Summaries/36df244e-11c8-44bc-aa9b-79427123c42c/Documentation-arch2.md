# A land use map of Peninsular Malaysia for the year 2018 (25m grid)

- Purpose and scope
  - Produces a 25-meter resolution gridded land use map for Peninsular Malaysia (2018/2019 base data).
  - Contains nine classes: non-paddy agriculture, paddy fields, rural residential, urban residential, commercial/institutional, industrial/infrastructure, roads, urban, and others.
  - Designed to support environmental monitoring and policy assessment by providing a consistent, harmonised land use layer.

- Data sources used
  - PLANMalaysia: detailed state-level land use polygons for 2018/2019 across 12 states.
  - Climate Change Initiative Land Cover (CCI LC, ESA): global 300 m raster used to fill data gaps.
  - Global Human Settlement Layer Urban Centre Database (GHS-UCDB R2019A): identifies urban vs. rural residential areas.
  - Paddy field maps: Begum et al. (2005) and FAO (2005) for rice cultivation areas; vectorised where needed.

- Data processing and methodology (in QGIS)
  - State polygon data: reclassified into nine land use classes; rasterized to 25 m grid.
  - Rural vs. urban residential: overlaid PLANMalaysia polygons with GHS-UCDB to differentiate rural and urban residential areas.
  - CCI LC 2015: reclassified into three broad classes (urban, agriculture, others) and resampled to 25 m to fill gaps.
  - Paddy fields: where state data lacked detail, rice maps were georeferenced and vectorised, then rasterised to 25 m; integrated with state data.
  - Mosaic/merging: gaps from state data filled with CCI LC; paddy fields merged with other classes to form final map.
  - Final product created as a single mosaic land use layer.

- Data structure and deliverable
  - Extent: Peninsular Malaysia.
  - Format: raster GeoTIFF; Coordinate Reference System: WGS84; cell size ~25 meters.
  - Land use class values mapped to nine categories with documentation of the contributing datasets per class.
  - File name: Malaysia_land_use_map.tif.

- Challenges and data gaps
  - Gaps in the state polygon data (e.g., Kuala Lumpur and areas in Johor, Kedah, Kelantan, Pahang) requiring infilling with CCI LC data.
  - Paddy field details not uniformly available across all states; supplemented with external rice maps where needed.
  - Integration relies on multiple sources with varying update cycles and resolutions.

- Relevance for environmental monitoring
  - Provides a standardised, multi-source land use layer suitable for tracking environmental health indicators and policy performance over time.
  - Facilitates data integration with other environmental datasets (e.g., hazard zoning, urban growth, agriculture extent) for monitoring at regional scales.
  - Clear provenance and methodology enable reproducibility and transparency in environmental assessments.

- Funding and acknowledgments
  - Project: Malaysia - Flood Impact Across Scales.
  - Funded under the Newton-Ungku Omar Fund, with joint support from NERC and MYPAIR Scheme (Malaysia).

- Reference context
  - Data processing and methodology summarized, including use of PLANMalaysia polygons, ESA CCI LC, GHS-UCDB, and historical rice maps to construct a comprehensive 25 m land use raster.