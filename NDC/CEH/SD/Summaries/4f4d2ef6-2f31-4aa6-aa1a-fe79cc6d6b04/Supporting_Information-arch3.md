# Dataset files

- Overview: A 2020 wild bee monitoring dataset collected in Leighfield Forest (Leicestershire and Rutland, UK) comprising 14 files that cover raw observations, abundance by guild, species richness, transect locations, and land use classifications. Data support analysis of pollinator abundance and guild structure across habitats and seasons.

## Data structure and contents

- SurveyData_PanTraps_raw.csv
  - Raw pan trap catches data for wild bees, per site and per species; organized at species level.
- SurveyData_Transects_raw.csv
  - Raw transect observations data for wild bees, per site and per species; organized at species level.
- BeeSpecies_to_Guild_Table.csv
  - Classifies each recorded species into one of four guilds:
    - Ground Nesting Solitary Bees (GNSB)
    - Cavity Nesting Solitary Bees (CNSB)
    - Ground Nesting Bumblebees (GNBB)
    - Tree Nesting Bumblebees (TNBB)
- Abundance_Transects_ByGuild_Spring.csv
  - Transect observations of abundance by guild for Spring; includes a total per survey grid.
- Abundance_Transects_ByGuild_Summer.csv
  - Transect observations of abundance by guild for Summer; includes a total per survey grid.
- Abundance_PanTraps_ByGuild_Spring.csv
  - Pan trap abundances by guild for Spring; includes a total per survey grid.
- Abundance_PanTraps_ByGuild_Summer.csv
  - Pan trap abundances by guild for Summer; includes a total per survey grid.
- Abundance_AllObservations_ByGuild.csv
  - Collated abundance by guild combining pan trap and transect observations across Spring, Summer, and Total.
- SpeciesRichness_AllObservations.csv
  - Species richness by site for Spring, Summer, and Total.
- Transect_Locations.shp (and associated files: .cpg, .dbf, .prj, .qpj, .shw)
  - Shapefile detailing transect locations and paths (grid, transect number, start/end coordinates).
- Leighfield_LULC_2020.tif
  - Raster land-use/land-cover map for the region at 10 m resolution with six classes; projected in British National Grid.
- Leighfield_LULC_2020_Legend.lyr and Leighfield_LULC_2020_Legend.qml
  - GIS legend files detailing land-use/land-cover classes for the 2020 map.
- Note: The column headings for each data file are described in Tables 2–8 (e.g., 36 columns in SurveyData_PanTraps_raw.csv; 57 columns in SurveyData_Transects_raw.csv; etc.). Blank cells indicate no observation.

## Methods and provenance

- Study context: Wild bee survey within Leighfield Forest during Spring/Summer 2020; methodology adapted from Carvell et al. (2016) to better capture guild-specific habitat use.
- Key methodological changes:
  - Transect length reduced to 100 m; multiple transects per 1 km2 grid (up to seven) with two visits per transect per season (Spring and Summer); aim for at least three visits for coverage.
  - No quadrat flower observations due to time constraints; extended transect visits instead.
  - Up to seven sets of pan traps; fieldwork timed to avoid peak heat; daily circuits where possible.
  - Weather data referenced from the Loddington station; weather coverage may vary by site.
- Outcomes: Ten 1 km2 survey squares were studied, with two visits per square per season; data were checked by ecologists and organized by species, guild, and season.
- Equipment: Insect nets, hand lenses, vials, transect markers, pan trap kits, camera, GPS, and field maps.

## Land use and habitat context

- Field habitats surveyed included:
  - Woodland (mature, new, edge)
  - Hedgerows (various heights)
  - Crops (various types) and margins
  - Watercourses and ditch margins (un-grazed and grazed)
  - Field margin habitats and broader farmland features
  - Roadside margins and disused railway lines
- Land use/land cover mapping:
  - Created with Google Earth Engine using Sentinel-2 imagery from Sept 2020; four primary classes (Woodland, Grassland/Pasture, Arable, Built Environment) plus manual additions for Farm vs Domestic Buildings and Field Margin Habitats.
  - Training data developed in QGIS; random forest classifier used; final map included five classes and was manually refined.
  - Accuracy assessment: 700 random points; overall accuracy 89.1%.

## Data quality, limitations, and governance

- Strengths for monitoring:
  - Standardized data structure with guild-based abundances and species richness to support policy-relevant indicators.
  - Clear documentation of data files, formats, and column descriptions to facilitate reuse.
  - Linkage between field observations and habitat/LULC context for habitat-based monitoring analyses.
- Limitations and constraints:
  - Modifications to the Carvell et al. framework (shorter transects, more frequent visits) may affect comparability with other studies.
  - Some habitats are only a sample of regional variety; not all landscape features are represented.
  - No floral quadrat observations due to time constraints; may limit certain pollinator-plant interaction inferences.
  - Weather data availability may vary by site; potential impact on comparability across grids.
  - LULC classification required manual refinement beyond the initial four classes, introducing potential subjectivity in habitat delineation.
- Data governance considerations for monitoring frameworks:
  - The dataset exemplifies the need for explicit metadata, data provenance, and clarity on data transformations.
  - Open data considerations: the dataset provides raw and derived measures that should be accompanied by metadata and versioning to enable reproducibility.

## Spatial and temporal coverage

- Temporal: Spring and Summer of 2020.
- Spatial: Leighfield Forest region; ten 1 km2 survey sites (grid-referenced); transects and pan traps distributed across habitats within the region.
- Outputs include season-specific and total abundance by guild, species richness, and transect locations mapped to British National Grid.

## Reproducibility and use

- Appendix 2 provides Google Earth Engine code used for the land-cover classification workflow (Sentinel-2 processing, cloud masking, ensemble classification, and export). The code demonstrates end-to-end workflow from image collection to classified output and export.
- The dataset structure supports reuse in policy analyses, trend monitoring, and habitat-effect evaluations by linking species/guild abundances to habitat context and land-use changes.

## Relevance for monitoring frameworks

- Demonstrates how to structure a pollinator monitoring dataset for policy-relevant evaluation:
  - Distinct raw data files (species-level observations) and derived indicators (guild abundances, species richness, total per site/season).
  - Clear mapping of species to ecological guilds to support guild-based indicators.
  - Integration of habitat and land-cover context to enable habitat-based impact assessments.
  - Documentation of field protocol adaptations and their implications for data comparability.
  - Availability of reproducible geospatial workflows (LULC classification) to support methodological transparency and governance.

## Appendix references

- Appendix 1: Location details for the ten 1 km2 survey sites (British National Grid references).
- Appendix 2: Google Earth Engine code used for the random forest-based land-cover classification (including training data handling and export).