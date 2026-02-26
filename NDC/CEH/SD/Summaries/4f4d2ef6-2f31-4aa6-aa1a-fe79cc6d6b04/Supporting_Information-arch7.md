# Dataset files

- Overview
  - A multi-file dataset from wild bee surveys in Leighfield Forest (Spring/Summer 2020), organized at multiple spatial scales (sites, transects, grids) and across guilds and seasons for GIS analysis and map-based visualisation.
  - Includes raw observation data, species-to-guild classification, abundance aggregates by guild, species richness, transect locations, and a high-resolution land-use/land-cover (LULC) map with associated legend.
  - Spatial data are provided in GIS-friendly formats (CSV, shapefile with associated files) and raster formats (GeoTIFF) in the British National Grid projection.

- Data files and formats (14 files)
  - SurveyData_PanTraps_raw.csv: Raw pan trap catches for wild bees, per site, per date, per grid reference, with species columns.
  - SurveyData_Transects_raw.csv: Raw transect observations for wild bees, per site, per date, per transect, with species columns.
  - BeeSpecies_to_Guild_Table.csv: Maps each bee species to one of four guilds (GNSB, CNSB, GNBB, TNBB).
  - Abundance_Transects_ByGuild_Spring.csv: Abundance of each guild from transect surveys in Spring, per survey grid.
  - Abundance_Transects_ByGuild_Summer.csv: Abundance of each guild from transect surveys in Summer, per survey grid.
  - Abundance_PanTraps_ByGuild_Spring.csv: Pan trap abundance by guild in Spring, per survey grid.
  - Abundance_PanTraps_ByGuild_Summer.csv: Pan trap abundance by guild in Summer, per survey grid.
  - Abundance_AllObservations_ByGuild.csv: Collated abundance (pan traps and transects) by guild across Spring, Summer, and total seasons.
  - SpeciesRichness_AllObservations.csv: Species richness by site across Spring, Summer, and total seasons.
  - Transect_Locations.shp (with associated cpg, dbf, prj, qpj, shw): Location and path of transects, projected in British National Grid.
  - Leighfield_LULC_2020.tif: Raster land-use/land-cover map, 10 m resolution, six classes, British National Grid.
  - Leighfield_LULC_2020_Legend.lyr and Leighfield_LULC_2020_Legend.qml: Legend files for the GIS display of the LULC map.
  - Note: The document references 14 files (Table 1) and provides more detail in accompanying Tables 2–8 for column headers and data structure.

- Data schema and key fields
  - Site, Date, Grid_Reference, and transect/site identifiers used to align observations spatially.
  - Species columns in the raw data files capture counts per species; these are subsequently linked to guilds via BeeSpecies_to_Guild_Table.
  - Abundance and species richness tables summarize counts by guild and season.
  - Transect_Locations provides coordinates for transect start/end points and transect identifiers.
  - LULC map uses defined classes (Woodland, Grassland/Pasture, Arable, Built Environment) with additional manual classes for Farm Building, Domestic Building, and Field Margin Habitats.

- Spatial references and GIS products
  - British National Grid (BNG) is the primary coordinate reference for site, grid, and transect data.
  - Transect locations are provided as a shapefile with standard GIS components.
  - Leighfield_LULC_2020 is a 10 m resolution raster in GeoTIFF format suitable for map-based visualisation and analysis.
  - Legend files accompany the LULC map for correct class interpretation in GIS.

- Methods and data collection notes (survey design and deviations)
  - Based on a modified Carvell et al. (2016) pollinator monitoring framework, conducted in Leighfield Forest (Spring/Summer 2020).
  - Key modifications:
    - Transects shortened to 100 m but increased count per 1 km^2 grid; each transect visited twice (Spring and Summer), with a preference for more visits if time allowed.
    - No quadrat flower observations were recorded due to limited field time.
    - Pan trap sets increased (up to seven sets) with color-specific pans (white, yellow, blue).
    - Fieldwork timed to avoid hottest parts of the day; circuit-based transects when possible.
    - Weather data captured from Loddington station; recognition that weather data may not be available for all sites.
  - Final products include season-specific and total guild abundances, and species richness by guild/season.

- Habitats and land-use observations
  - Surveyed habitats span woodland (mature, young, edges), hedgerows of varying heights, multiple crop types, watercourses and margins, field margins, margins and track infrastructure, disused rail lines, and roadside margins.
  - Habitats were mapped to support interpretation of pollinator guild usage across landscape types.

- Land Use / Land Cover (LULC) mapping
  - LULC map produced using Google Earth Engine from Sentinel-2 imagery (Sept 20, 2020), with a training dataset created in QGIS v3.6.1.
  - Class structure:
    - Primary classes: Woodland, Grassland/Pasture, Arable, Built Environment.
    - Added classes: Farm Building, Domestic Building, Field Margin Habitats.
  - Accuracy assessment:
    - 700 random validation points with overall accuracy 89.1%.
  - Process:
    - Random forest classifier trained on Sentinel-2 derived features, manual post-processing to refine classes, and export to GeoTIFF.

- Data integration and processing notes (GIS-focused)
  - Data from raw observations are cleaned, standardized, and transformed for guild-based aggregation.
  - Datasets across different resolutions are integrated by common spatial references (BNG) and grid references.
  - Abundance and richness metrics are organised by survey grid and season, enabling map-based visualization of spatial patterns by guilds.

- Appendix and processing details
  - Appendix 2 provides Google Earth Engine code for the random forest classification used to generate Leighfield LULC, including:
    - Sentinel-2 data preprocessing, cloud masking, compositing
    - Training data extraction and feature selection (bands with percentiles)
    - RandomForest classifier configuration (300 trees, bag fraction, etc.)
    - Training and classification steps
    - Export of the classified raster to Google Drive as a GeoTIFF
  - The document includes sample code blocks and a snippet of the GEE workflow used to reproduce the LULC map.

- References and notes
  - Primary reference: Carvell et al. (2016) for design and testing of a national pollinator monitoring framework.
  - Appendix 1 and Appendix 2 provide locations for survey sites and GEE code used in classification.

- Practical implications for GIS specialists
  - Rich, multi-resolution bee survey dataset suitable for map-based visualization of species guilds and biodiversity across landscapes.
  - Clear spatial references and GIS-friendly formats enable overlay with LULC, habitats, and other SES datasets.
  - Guild-based aggregation supports targeted spatial analyses of pollinator habitat use and landscape management.
  - Availability of LULC map with high accuracy (89.1%) facilitates integration with other GIS analyses and cartographic products.