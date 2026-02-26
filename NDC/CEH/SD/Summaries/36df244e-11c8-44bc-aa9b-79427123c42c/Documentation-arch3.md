# A land use map of Peninsular Malaysia for the year 2018 (25m grid)

- Purpose and product
  - Gridded land use map of Peninsular Malaysia at ~25 m resolution for 2018/2019.
  - Nine land use classes (non-paddy agriculture, paddy, rural/urban residential, commercial/institutional, industrial/infrastructure, roads, urban, others).
  - Raster GeoTIFF (WGS84), with each 25 m grid cell assigned a single class.
  - Created to support environmental monitoring and planning under the project “Malaysia - Flood Impact Across Scales.”

- Data sources (datasets used)
  - PLANMalaysia state land use polygons for 2018/2019 (12 states of Peninsular Malaysia).
  - Climate Change Initiative Land Cover (CCI LC) from ESA (2015; 300 m resolution) for gap filling.
  - Global Human Settlement Layer Urban Centre Database (GHS-UCDB R2019A; 2015) for distinguishing rural vs urban residential.
  - Paddy field maps: detailed state data where available plus rice-cultivation maps (Begum et al., 2005; FAO, 2005) for other areas.
  - Global Administrative Areas (GADM) for regional extent (2018).

- Processing workflow (how the map was produced)
  - Reclassified state polygon land use data into nine classes and rasterized to 25 m resolution.
  - Used GHS-UCDB to separate rural and urban residential areas by overlaying with state data.
  - Reclassified CCI LC 300 m data into three classes (urban, agriculture, others) and resampled to 25 m to fill gaps (e.g., Kuala Lumpur).
  - Split agriculture into Paddy and Non-Paddy; Paddy fields obtained from state data where available, otherwise derived from rice-cultivation maps and vectorised, then rasterised to 25 m.
  - Created mosaic by merging state rasters, GHS classifications, CCI LC, and paddy-field layers to fill data gaps.
  - Final map produced as Malaysia_land_use_map.tif.

- Paddy fields
  - Paddy data included where state polygons provided it (Kelantan, Kedah, Johor, Pahang, Perlis, Perak, Pulau Pinang).
  - For states lacking detailed paddy data (Melaka, Negeri Sembilan, Selangor, Putrajaya, Terengganu), paddy fields were located from rice cultivation maps (Begum et al., 2005; FAO, 2005) and vectorised before rasterising to 25 m.

- Data structure and delivery
  - Format: raster GeoTIFF (Malaysia_land_use_map.tif)
  - Coordinate reference system: WGS84
  - Pixel size: ~25 m
  - Nine classes mapped to raster values (integration of state data, CCI LC, GHS-UCDB, and paddy maps)
  - Class mappings include:
    1) Agriculture (non-paddy)
    2) Agriculture (paddy)
    3) Rural Residential
    4) Urban Residential
    5) Commercial and Institutional
    6) Industrial and Infrastructure
    7) Roads
    8) Others (forest, water bodies, bare land, beach)
    9) Urban

- Use and limitations (relevance to monitoring frameworks)
  - Provides a harmonised, 25 m-resolution land use map for Peninsular Malaysia suitable for monitoring land use change, urban expansion, agriculture, and infrastructure.
  - Strengths: integrates multiple data sources, attempts to fill gaps with higher-level land cover data, differentiates rural/urban residential areas.
  - Limitations and considerations for governance:
    - Data gaps in state polygon data (notably Kuala Lumpur and some states).
    - Paddy-field details incomplete for several states; reliance on external rice maps for those areas.
    - Variability in data dates across sources (2015–2019), which may affect temporal consistency.
    - Requires clear metadata and reproducible workflow (implemented in QGIS) to support ongoing monitoring and updates.
    - Data sharing and provenance considerations when updating layers or sharing derived data.

- File details and references
  - File name: Malaysia_land_use_map.tif
  - Key references: PLANMalaysia state land use data; ESA CCI Land Cover; GHS-UCDB; Begum et al. (2005); FAO (2005); GADM.