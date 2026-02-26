# Dataset files

- Overview
  - A multi-file dataset from a wild bee survey in Leighfield Forest (Leicestershire and Rutland, UK) conducted in Spring/Summer 2020. Data are organized by survey type (pan traps and transects), species guilds, seasons, and spatial units. Includes a land use/land cover (LULC) map product and GIS metadata to support spatial analyses.

- Data files (14 individual files described in the source)
  - SurveyData_PanTraps_raw.csv
    - Raw pan trap catches data for wild bees, by site, date, grid reference, pan color, and species columns (36 columns total; 342 rows in the sample).
  - SurveyData_Transects_raw.csv
    - Raw transect observations data for wild bees, by site, grid reference, date, transect details, and species columns (57 columns total; 114 rows in the sample).
  - BeeSpecies_to_Guild_Table.csv
    - Classification of each bee species into one of four guilds: Ground Nesting Solitary Bees (GNSB), Cavity Nesting Solitary Bees (CNSB), Ground Nesting Bumblebees (GNBB), Tree Nesting Bumblebees (TNBB), with a total species count per guild.
  - Abundance_Transects_ByGuild_Spring.csv
    - Abundance of bees by guild for transects in Spring; includes GNSB, CNSB, GNBB, TNBB, and TOTAL per survey grid.
  - Abundance_Transects_ByGuild_Summer.csv
    - Abundance of bees by guild for transects in Summer; same guild columns as Spring.
  - Abundance_PanTraps_ByGuild_Spring.csv
    - Pan trap abundance by guild for Spring surveys; same guild structure as transects files.
  - Abundance_PanTraps_ByGuild_Summer.csv
    - Pan trap abundance by guild for Summer surveys; same guild structure as Spring.
  - Abundance_AllObservations_ByGuild.csv
    - Collated abundance by guild across pan traps and transects, for Spring, Summer, and All Seasons; includes GNSB_Spring, CNSB_Spring, GNBB_Spring, TNBB_Spring, GNSB_Summer, CNSB_Summer, GNBB_Summer, TNBB_Summer, plus AllSeasons totals for each guild.
  - SpeciesRichness_AllObservations.csv
    - Species richness by site for Spring, Summer, and All Seasons.
  - Transect_Locations.shp (and related files: .cpg, .dbf, .prj, .qpj, .shw)
    - Shapefile with transect locations: grid, transect number, and start/end coordinates.
  - Leighfield_LULC_2020.tif
    - 10 m resolution raster land use/land cover map for the study region (four initial classes: Woodland, Grassland/Pasture, Arable, Built Environment) plus two manually added classes (Farm Building, Domestic Building) and a Field Margin Habitats class.
  - Leighfield_LULC_2020_Legend (legend files: .lyr and .qml)
    - GIS legend files detailing the land use/land cover classes.
  - Note: The document references additional appendices and notes that accompany these files (e.g., Appendix 1 and 2) and mentions a secondary item formatting duplication in the Abundance_PanTraps_ByGuild_Spring entry.

- Table-level data structure highlights
  - SurveyData_PanTraps_raw.csv
    - Columns include: Site, Date, Grid_Reference, Catch_no_catch, Start_finish_time_Total, Station_Transect_no, Pan_colour, Pan_trap_grid_ref, plus 9–36 corresponding to species names (raw counts).
  - SurveyData_Transects_raw.csv
    - Columns include: Site, Grid_Reference, Date, Transect_start_finish_time_Total, Station_Transect_no, Transect_start_and_finish_grid_ref, Pan_trap_grid_ref, plus 7–57 corresponding to species names (raw counts).
  - Abundance and richness tables
    - Structured by Survey_Grid (grid reference) with guild-specific counts and total per grid, and species richness per grid for Spring, Summer, and All Seasons.
  - Transect_Locations
    - Spatially explicit transect plots: Grid, Transect, Start Northing/Easting, End Northing/Easting.
  - LULC map and legend
    - Classified landscape map with four initial classes, expanded to include Farm Building, Domestic Building, and Field Margin Habitats; classification accuracy reported (89.1%).

- Methods and data generation notes
  - Survey approach and modifications (based on Carvell et al. 2016)
    - Original method involved five 200 m transects per km² with repeated visits and accompanying floral observations.
    - Modifications implemented to better capture habitat heterogeneity:
      - Transects shortened to 100 m, with up to seven transects per 1 km² grid; each transect visited twice (Spring and Summer); aim for at least three visits when possible.
      - No quadrat flower observations due to insufficient time; 10-minute observations removed to focus on transect and trap data.
      - Up to seven sets of pan traps used; fieldwork scheduled to avoid hottest parts of the day; transects arranged in circuits where possible.
      - Weather data (for fieldwork dates) obtained from the Loddington weather station.
  - Study extent and habitats
    - Ten 1 km² squares surveyed, with habitats including woodland (mature, young, edges), hedgerows, crops (various), watercourses, and other linear/block habitats (margins, pollen/nectar strips, margins, margins near roads, disused railways).
  - Land use/land cover mapping
    - LULC map created via Google Earth Engine from Sentinel-2 imagery (Sept 20, 2020). Training data developed in QGIS for four primary classes (Woodland, Grassland/Pasture, Arable, Built Environment), with two additional manual classes: Farm Building and Domestic Building, plus Field Margin Habitats drawn from visual interpretation.
    - Random forest classifier used in GEE; accuracy assessed with a confusion matrix across 700 random points; overall accuracy 89.1%.
  - Equipment used
    - Insect nets, hand lens, glass capture tubes, transect markers, pan trap bowls and posts, GPS, camera, and field maps.
  - Habitats documented
    - Detailed habitat types across woodland, hedgerows, crops, watercourses, field margins, and other features (e.g., pollen/nectar strips, muck heap margins, roadside margins).
  - Appendix 1 and Appendix 2
    - Appendix 1: Locations and grid references for the ten 1 km² survey sites.
    - Appendix 2: Google Earth Engine code used for random forest classification (includes Sentinel-2 data processing, cloud masking, band selection, training data import, model training, classification, and export to Google Drive).

- Data use and accessibility notes
  - The dataset combines raw observations, guild classifications, and spatially explicit outputs to support analyses of pollinator abundance, guild-specific trends, and habitat associations.
  - The LULC product provides a spatially explicit context for analyzing habitat relationships with bee communities.
  - Metadata and code (Appendix 2) support reproducibility of the land cover classification workflow.

- References
  - Carvell, C. et al. (2016) – Design and Testing of a National Pollinator and Pollination Monitoring Framework (final summary report to Defra, Scottish Government, Welsh Government).

- Endnotes
  - Blank cells in data indicate no observation recorded.
  - The document notes potential refinements for future fieldwork (e.g., more field days, better weather conditions, expanded observation times) to improve data coverage and interpretability.