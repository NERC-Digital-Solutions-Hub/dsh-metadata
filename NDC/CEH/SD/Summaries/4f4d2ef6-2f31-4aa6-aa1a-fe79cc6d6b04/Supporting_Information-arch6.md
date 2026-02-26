# Dataset files

- Overview: A dataset documenting wild bee surveys in Leighfield Forest (Leicestershire and Rutland, UK) during Spring/Summer 2020. It comprises 14 files (raw data, derived abundance by guilds, species richness, and spatial data) and includes a land-use/land-cover (LULC) map produced using Google Earth Engine. Data are organized by survey location, time period, and bee guilds (Ground Nesting Solitary Bees, Cavity Nesting Solitary Bees, Ground Nesting Bumblebees, Tree Nesting Bumblebees). Blank cells indicate no observation.

## Data files and structure

- SurveyData_PanTraps_raw.csv (CSV)
  - Raw pan trap catches by site and date, organized at the species level.
  - Key columns: Site, Date, Grid_Reference, Catch/no Catch, Start_finish_time_Total, Station_Transect_no, Pan_colour, Pan_trap_grid_ref, followed by 9-36: species columns with raw counts.

- SurveyData_Transects_raw.csv (CSV)
  - Raw transect observations by site, organized at the species level.
  - Key columns: Site, Grid_Reference, Date, Transect_start_finish_time_Total, Station_Transect_no, Transect_start_and_finish_grid_ref, Pan_trap_grid_ref, followed by 7-57: species columns.

- BeeSpecies_to_Guild_Table.csv (CSV)
  - Species-to-guild mapping.
  - Columns: Species, Guild_Code (GNSB, CNSB, GNBB, TNBB) with descriptive guild names.

- Abundance_Transects_ByGuild_Spring.csv (CSV)
  - Abundance by guild for transects in Spring.
  - Columns: Survey_Grid, GNSB, CNSB, GNBB, TNBB, TOTAL.

- Abundance_Transects_ByGuild_Summer.csv (CSV)
  - Abundance by guild for transects in Summer.
  - Columns: Survey_Grid, GNSB, CNSB, GNBB, TNBB, TOTAL.

- Abundance_PanTraps_ByGuild_Spring.csv (CSV)
  - Pan trap abundance by guild for Spring.
  - Columns: Survey_Grid, GNSB, CNSB, GNBB, TNBB, TOTAL.

- Abundance_PanTraps_ByGuild_Summer.csv (CSV)
  - Pan trap abundance by guild for Summer.
  - Columns: Survey_Grid, GNSB, CNSB, GNBB, TNBB, TOTAL.

- Abundance_AllObservations_ByGuild.csv (CSV)
  - Collated abundance by guild across pan traps and transects for Spring, Summer, and AllSeasons.
  - Columns: Survey_Grid, GNSB_Spring, CNSB_Spring, GNBB_Spring, TNBB_Spring, GNSB_Summer, CNSB_Summer, GNBB_Summer, TNBB_Summer, GNSB_AllSeasons, CNSB_AllSeasons, GNBB_AllSeasons, TNBB_AllSeasons.

- SpeciesRichness_AllObservations.csv (CSV)
  - Species richness by season.
  - Columns: Survey_Grid, Species_Richness_Spring, Species_Richness_Summer.

- Transect_Locations.shp (Shapefile) and associated files (cpg, dbf, prj, qpj, shw)
  - Spatial locations and paths of transect surveys.
  - Columns: Grid, Transect, St_Northin, St_Easting, En_Northin, En_Easting.

- Leighfield_LULC_2020.tif (GeoTIFF)
  - 10 m resolution land-use/land-cover map with six classes.

- Leighfield_LULC_2020_Legend.lyr and Leighfield_LULC_2020_Legend.qml
  - GIS legend files detailing land-use/land-cover class names.

- Notes: Blank cells indicate no observation recorded.

## Data columns and content details

- Table 2 (SurveyData_PanTraps_raw.csv): 36 columns; 342 rows.
  - Example: Site, Date, Grid_Reference, Catch_no_catch, Start_finish_time_Total, Station_Transect_no, Pan_colour, Pan_trap_grid_ref, followed by species-specific columns.

- Table 3 (SurveyData_Transects_raw.csv): 57 columns; 114 rows.
  - Example: Site, Grid_Reference, Date, Transect_start_finish_time_Total, Station_Transect_no, Transect_start_and_finish_grid_ref, Pan_trap_grid_ref, followed by species-specific columns.

- Table 4 (BeeSpecies_to_Guild_Table.csv): 2 columns; 49 rows.
  - Species → Guild_Code (GNSB, CNSB, GNBB, TNBB).

- Table 5 (Abundance_Transects_ByGuild_Spring/Summer.csv and Abundance_PanTraps_ByGuild_Spring/Summer.csv): 6 columns; 10 rows.
  - Columns: Survey_Grid, GNSB, CNSB, GNBB, TNBB, TOTAL.

- Table 6 (Abundance_AllObservations_ByGuild.csv): 13 columns; 10 rows.
  - Columns include per-season and all-season totals for each guild.

- Table 7 (SpeciesRichness_AllObservations.csv): 4 columns; 10 rows.
  - Survey_Grid, Species_Richness_Spring, Species_Richness_Summer.

- Table 8 (Transect_Locations.shp): 6 columns; 60 rows.
  - Grid, Transect, St_Northin, St_Easting, En_Northin, En_Easting.

- Table 9 (not listed as such) and related files: Geospatial layers and legends for LULC.

## Data processing, guild classification, and products

- Bee guilds: Species are classified into four guilds via BeeSpecies_to_Guild_Table, enabling aggregation of abundance by guild across transects and pan traps.
- Derived products: Abundances per guild by site/grid and season; species richness per site by season; combined/all-observations abundance by guild; a consolidated AllSeasons/seasonal breakdown.
- Data allow self-serve exploration of pollinator community structure, guild-level trends, and cross-tabulation with spatial location.

## Spatial data and land-use mapping

- Land-use/land-cover mapping: Created for the study region using Google Earth Engine (Sentinel-2, 20 Sep 2020 image, cloud masking, median composite).
- Class scheme: Initially four classes (Woodland, Grassland/Pasture, Arable, Built Environment), expanded to include Farm Building, Domestic Building, and Field Margin Habitats.
- Classification method: Random forest (300 trees) trained on a visual/ground-truth-like training dataset in QGIS; classification performed in GEE and exported as GeoTIFF.
- Validation: Confusion matrix using 700 random points; overall accuracy 89.1%.
- Appendix 2 provides the GEE code used for the random forest classification.

## Methods and fieldwork notes

- Survey framework: Based on Carvell et al. (2016) with modifications to better capture habitat exploitation by pollinator guilds.
- Key modifications:
  - Transects reduced to 100 m, with up to seven transects per 1 km2 grid; each transect visited twice (Spring and Summer); ideally three visits recommended.
  - Habitat sites chosen to span identifiable habitat types and micro-habitats.
  - No quadrat flower observations were recorded due to time constraints; increased transect/visits were prioritized.
  - Pan-trap sets increased to up to seven sets; field times adjusted to avoid peak heat; circuit-based transects when possible.
  - Weather data from Loddington station used when available to contextualize fieldwork.
- Scope: Ten 1 km2 squares surveyed; results were checked by an ecologist and compiled by guild for abundance and by season for species richness.

## Habitats and study context

- Habitats surveyed included: woodland (mature, young, edges), hedgerows (various heights), crops (multiple types), watercourse margins, ditch habitats, field margins, and roadsides.
- Land cover mapping complemented field observations to contextualize pollinator habitat availability.

## Data quality, usage, and access

- Data quality considerations: Patchy, multi-format data sources; need for data integration across transects, pan traps, and guild classifications.
- Use cases: Facilitates cross-site comparisons, guild-level abundance analyses, species richness assessments, and spatial analyses with the LULC map.
- Notes for users: Blank cells indicate no observation; ensure alignment between raw data and guild classifications when aggregating.

## Appendices and code

- Appendix 1: Location and grid references for the ten 1 km2 survey sites.
- Appendix 2: Google Earth Engine code used for the random forest classification (example snippets showing data preparation, training, classifier creation, and export to GeoTIFF).

## References

- Carvell, C. et al. (2016) Design and Testing of a National Pollinator and Pollination Monitoring Framework. Final report to Defra, Scottish Government, and Welsh Government.