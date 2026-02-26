# A land use map of Peninsular Malaysia for the year 2018 (25m grid)

- Overview
  - Gridded land use map for Peninsular Malaysia at approximately 25-meter resolution.
  - Contains nine classes: non-paddy agriculture, paddy fields, rural residential, urban residential, commercial/institutional, industrial/infrastructure, roads, urban, and others.
  - Built from state-level land use polygons (2018/19) provided by PLANMalaysia, rasterized to 25 m.
  - Gaps in polygon data (e.g., Kuala Lumpur) infilled using reclassified CCI Land Cover (ESA, 2017) rasters at 25 m.
  - Rural vs urban residential areas distinguished using the Global Human Settlement Layer Urban Centre Database (GHS-UCDB, Florczyk et al., 2019).
  - Paddy fields derived from state-level data where available; for states lacking details, paddy areas were located and vectorized from rice-cultivation maps (Begum et al., 2005; FAO, 2005) and rasterized to 25 m.

- Datasets used
  - PLANMalaysia state land use polygons for 2018/2019 (Johor, Kedah, Kelantan, Pahang, Perak, Perlis, Pulau Pinang, Negeri Sembilan, Terengganu, Selangor, Putrajaya, Melaka)
  - Climate Change Initiative Land Cover (CCI LC) raster for 2015 (300 m resolution)
  - Global Human Settlement Layer Urban Centre Database (GHS-UCDB R2019A, 2015)
  - Paddy field maps from Begum et al. (2005) and FAO (2005)

- Data processing workflow
  - State land use data
    - Reclassify polygon classes into nine target land use classes.
    - Rasterize to 25 m resolution.
    - Note gaps in coverage (e.g., Kuala Lumpur, parts of Johor, Kedah, Kelantan, Pahang).
  - Rural and urban residential areas
    - Use GHS-UCDB to identify urban extents.
    - Overlay with state polygons to label residential areas as urban or rural.
  - CCI Land Cover map
    - Reclassify into three classes: urban, agriculture, others.
    - Resample from 300 m to 25 m.
    - Use to fill data gaps in polygon-derived land use.
  - Paddy fields
    - For states with detailed paddy data, use state-level paddy information.
    - For other states, vectorize main rice cultivation areas from Begum et al. (2005) and FAO (2005) maps; rasterize to 25 m.
  - Creating the mosaic land use map
    - Merge rasterized state data, GHS residential classification, CCI Land Cover, and paddy field layers.
    - Fill gaps and produce a seamless land use map for Peninsular Malaysia.
    - Final map demonstrates Kuala Lumpur area fully infilled (where original data were missing).

- Data structure
  - Output extent: Peninsular Malaysia
  - Format: Raster GeoTIFF
  - Coordinate reference system: WGS84
  - Cell size: ~25 meters (expressed in decimal degrees)
  - Land use classes and raster values:
    - 1 = Agriculture (non-paddy) [state polygon data, CCI LC]
    - 2 = Agriculture (paddy) [state polygon data, Begum 2005, FAO 2005]
    - 3 = Rural Residential [state polygon data, GHS UCDB]
    - 4 = Urban Residential [state polygon data, GHS UCDB]
    - 5 = Commercial and Institutional [state polygon data]
    - 6 = Industrial and Infrastructure [state polygon data]
    - 7 = Roads [state polygon data]
    8 = Others (forest, lakes/reservoirs, bare land, beach) [state polygon data, CCI LC]
    9 = Urban [CCI LC]
  - File name: Malaysia_land_use_map.tif

- File name
  - Malaysia_land_use_map.tif

- Methods and tools
  - Processed and integrated in QGIS

- References (data sources)
  - Begum, M., et al. (2005). Weed diversity of rice fields in four districts of Muda rice granary area, North-West Peninsular Malaysia.
  - ESA. Land Cover CCI Product User Guide Version 2 (2017).
  - FAO Regional Office for Asia and the Pacific (2005). ESPIM rice-related studies.
  - Florczyk, A.J., et al. (2019). GHS-UCDB R2019A—Urban Centre Database 2015.
  - Global Administrative Areas (GADM) (2018). Peninsular Malaysia data.