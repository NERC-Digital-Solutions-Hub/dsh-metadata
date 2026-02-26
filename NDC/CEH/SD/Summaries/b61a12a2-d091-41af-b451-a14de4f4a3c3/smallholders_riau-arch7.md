# DataLoggers_Riau.csv

- A multi-dataset data package from biodiversity surveys in Riau, Sumatra, Indonesia, designed to support map-based data products and GIS analyses of oil palm plantations and associated biodiversity.
- Primary GIS relevance:
  - Location and spatial context through PlantationCode and GPS linking codes.
  - Integration of environmental, biological, and management attributes into spatial layers.

## Datasets and GIS Context

- DataLoggers_Riau.csv
  - Hourly air temperature readings from data loggers within plots (TempHr1–TempHr25).
  - Each record ties to a plot (PlantationCode) and a logger location within the plot (SamplePoint).
  - Useful for interpolating microclimate surfaces and validating Climate/Temperature layers in GIS.

- Inflorescences_Riau.csv
  - Inflorescence-level biodiversity data from two observation days.
  - Includes Plot (PlantationCode), date, weather, pollinator counts, and ground/ vegetation context (e.g., canopy openness metrics, palm height, ground cover, and vegetation attributes).
  - Joins to spatial data via PlantationCode and GPS coordinates for inflorescence sites.

- Pitfalls_Riau.csv
  - Abundance data for arthropods captured in pitfall traps, with taxa-level counts.
  - Spatial linkage via PlantationCode and sampling point (T1–T4) for mapping trap locations.

- Transects_Riau.csv
  - Observational data for butterflies, orb-weaving spiders, and assassin bugs, including weather and air temperature.
  - Species-level observations with date, time, microhabitat, and habitat notes; suitable for point and short-interval GIS analyses.

- Traps_Riau.csv
  - Setup and collection times for pitfall traps, sticky traps, dataloggers, and bait cards.
  - Detailed time stamps and GPS-related codes that enable precise geolocation of trap activity layers in a GIS.

- StickyTraps_Riau.csv
  - Abundance data for arthropods captured by sticky traps, including counts by taxa and total specimens.
  - Spatially linked via PlantationCode and trap point field (StickyTrapSamplePoint).

- Environmental_Riau.csv
  - Vegetation, microclimate, and soil conditions across plantations.
  - Contains plantation geometry cues (plot dimensions, side lengths) and environmental variables (canopy openness, crop cover, ground cover, vegetation height, soil properties).
  - Supports creation of environmental raster/vector layers and spatial summaries per plantation.

- Social_Riau.csv
  - Plantation-level survey data covering management practices, farm demographics, economic indicators, and attitudes toward nature.
  - A rich source for thematic GIS maps (e.g., concentration of certain management practices, income proxies) and for linking socio-economic attributes to spatial units (plantations).

- Environmental_Riau.csv (second occurrence)
  - Duplicate/extended set of environment-related fields with additional canopy/soil metrics and weather descriptors.
  - Reinforces spatially explicit environmental context for mapping and analysis.

- GPS/Data linkage
  - Many datasets reference GPSCode, GPSCodeCorner, GPSCodeCentre, GPSCodeT1–T4, etc., linking to GPSDataRiau.csv (not included in this text) to obtain coordinates.
  - GIS workflow relies on joining by these GPS codes to create accurate spatial features (points, centers, corners, transects, and sample locations).

## Data Structure and Key GIS Considerations

- Common keys for integration:
  - PlantationCode (Plot ID) as a primary spatial unit.
  - GPSCode references to join to GPSDataRiau.csv for coordinates.
  - SamplePoint and T1–T4 references to locate sub-plot positions within plantations.

- Attributes and units to map:
  - Temperature, canopy openness, ground/vegetation cover, palm height/health, soil properties, and microclimate variables.
  - Species counts and pollinator observations for biodiversity layers.
  - Management practices and socio-economic indicators for thematic mapping.

- Data quality notes:
  - Field-labeled headers are long and sometimes garbled; care needed when loading (verify encoding and header parsing).
  - Some descriptions include minor inconsistencies or typos; validation required during data cleaning.
  - Resolution varies by dataset (plot-level vs. sub-plot level; hourly vs. daily).

## GIS Workflow Recommendations

- Data preparation
  - Load all CSVs and standardize field names (remove extraneous spaces and fix encoding).
  - Consolidate coordinates by joining each dataset to GPSDataRiau.csv via GPSCode or equivalent GPSCodeT1/T2/T3/T4 links.
  - Normalize units where needed (e.g., canopy openness as percent, temperature in °C, area in hectares).

- Spatial layers to create
  - Point layer: plantation sampling points (T1–T4, data loggers, transects, pitfall/sticky trap locations) with attributes from respective CSVs.
  - Polygon layer: plantation boundaries derived from SideLength and corner GPSs (where available) or from GPS-based plantation centroids to approximate extents.
  - Environmental layers: canopy openness, vegetation/ground cover, soil properties, and microclimate rasters if suitable sensor grids exist; otherwise, summarized per plantation.
  - Biodiversity layers: species/inflorescence observations, trap catches, and transect observations linked to plantation points.

- Data integration and visualization
  - Join per-plot attributes from Social_Riau.csv and Environmental_Riau.csv to plantation polygons or centroids for thematic maps (e.g., management intensity, soil health).
  - Create time-enabled maps for data with timestamps (e.g., TempHr readings, date/time of transects, trap setup/collection).
  - Use canopies/palms health scores and other ordinal metrics for classified symbology.

- Quality assurance and updates
  - Validate GPS joins with a subset of records against known coordinates.
  - Cross-check for missing GPS codes and fill gaps via alternative links or manual georeferencing if feasible.
  - Document data provenance and versioning to track updates across multiple CSVs.

## Practical Notes for GIS Specialists

- The dataset enables multi-layer GIS products: climate context, vegetation/soil environment, biodiversity observations, and plantation management characteristics.
- Strong capability for cross-dataset spatial analyses through PlantationCode and GPSCode references.
- Expect the need for data cleaning and standardization due to formatting irregularities and long descriptive headers.
- A GPSDataRiau.csv file (not shown here) is essential to fully realize spatial joins; ensure access to that file for complete georeferencing.

## Summary of Purpose and Utility

- This collection provides structured, geo-referenced biodiversity and environmental data from oil palm plantations in Riau, enabling GIS-based exploration of spatial patterns in climate, vegetation, soil conditions, and biodiversity across multiple plots and sampling points.
- Ideal for creating map-based data products that communicate spatial biodiversity patterns, environmental context, and management influences to policy colleagues, clients, and the public.