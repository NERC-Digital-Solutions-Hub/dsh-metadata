# Dataset files

## Overview
- A multi-file dataset describing wild bee surveys in Leighfield Forest (Leicestershire and Rutland, UK) during Spring/Summer 2020.
- Contains raw observation data, species guild classifications, abundance and species richness by guild and season, transect locations, and land use/land cover (LULC) data.
- Includes methodological notes, equipment lists, habitat descriptions, and a Google Earth Engine (GEE) classification workflow with accompanying Appendix materials.

## Datasets and file formats
- SurveyData_PanTraps_raw.csv — Raw pan trap catches for wild bees, by site, date, pan, and species (36 species columns; 342 rows).
- SurveyData_Transects_raw.csv — Raw transect observations for wild bees, by site, date, transect, and species (57 species columns; 114 rows).
- BeeSpecies_to_Guild_Table.csv — Mapping of each bee species to one of four guilds (Ground Nesting Solitary Bees, Cavity Nesting Solitary Bees, Ground Nesting Bumblebees, Tree Nesting Bumblebees).
- Abundance_Transects_ByGuild_Spring.csv — Number of bees per guild along transects in Spring; includes TOTAL per site.
- Abundance_Transects_ByGuild_Summer.csv — Number of bees per guild along transects in Summer; includes TOTAL per site.
- Abundance_PanTraps_ByGuild_Spring.csv — Pan trap abundance per guild for Spring; includes TOTAL per site.
- Abundance_PanTraps_ByGuild_Summer.csv — Pan trap abundance per guild for Summer; includes TOTAL per site.
- Abundance_AllObservations_ByGuild.csv — Collated abundance by guild across Spring, Summer, and AllSeasons for pan traps and transects.
- SpeciesRichness_AllObservations.csv — Species richness per site for Spring, Summer, and AllSeasons.
- Transect_Locations.shp (plus associated files: .cpg, .dbf, .prj, .qpj, .shpw) — Shapefile of transect locations and paths.
- Leighfield_LULC_2020.tif — 10 m resolution raster land use/land cover map for the survey region (four primary classes plus two added classes during processing).
- Leighfield_LULC_2020_Legend.lyr and Leighfield_LULC_2020_Legend.qml — Legend files for GIS interpretation of LULC classes.
- Tables 2–8 (data dictionaries) accompany the data files, detailing column names, descriptions, and structure.

## Data schema and documentation
- Table 2 (PanTraps_raw) provides 36 species columns plus core fields: Site, Date, Grid_Reference, Catch_no_catch, Start_finish_time_Total, Pan_trap_grid_ref.
- Table 3 (Transects_raw) provides 57 columns including Site, Grid_Reference, Date, Transect_start_finish_time_Total, Transect_start_and_finish_grid_ref.
- Table 4 (BeeSpecies_to_Guild_Table) maps each species to its Guild_Code (GNSB, CNSB, GNBB, TNBB) with descriptive names.
- Tables 5–7 (Guild-specific abundances, AllObservations, SpeciesRichness) summarize abundance and richness by guild, season, and survey grid.
- Table 8 (Transect_Locations) provides grid, transect, and start/end coordinates (Northing/Easting) for transects.
- Data note: blank cells indicate no observation recorded.

## Methods, provenance, and processing notes
- Survey area: Leighfield Forest, UK; Spring/Summer 2020; methodology modified from Carvell et al. (2016) to better capture habitat-driven pollinator variation.
- Modifications include:
  - Transects reduced to 100 m but increased per km2 coverage (up to 7 per km2); two visits per transect per season; aim for three visits if possible.
  - Elimination of quadrat flower observations due to time constraints; emphasis on transect-based sampling and pan traps.
  - Pan traps expanded to up to seven sets; fieldwork scheduled to avoid peak heat.
  - Weather data linked to field dates via a central station (Loddington) where available.
- Field equipment list includes nets, insect vials, transect markers, pan traps, GPS, and maps.
- Habitats surveyed span woodland (various age classes), hedgerows, crops, watercourses, field margins, and roadside/railway margins.
- Land Use/LULC mapping:
  - Generated with Google Earth Engine using Sentinel-2 imagery (Sept 2020), four primary classes (Woodland, Grassland/Pasture, Arable, Built Environment) plus manually added classes for Farm/Domestic buildings and Field Margin Habitats.
  - Random forest classification; accuracy assessed with 700 random points; overall accuracy 89.1%.
  - Final map refined in QGIS with legend additions and manual class delineation.

## Quality, limitations, and governance considerations
- Data quality notes:
  - Final datasets include both raw observations and aggregated summaries by guild and season.
  - The dataset contains explicit column descriptions and data dictionaries to support interpretability and reuse.
  - Blank cells indicate no observation; treatment of non-detections is explicit in the data.
  - LULC mapping accuracy documented (89.1%), with caveats about training data and manual refinements.
- Provenance and reproducibility:
  - Appendix 2 provides Google Earth Engine code used for the random forest classification, demonstrating reproducible processing steps.
  - Appendix 1 lists locations of the ten 1 km2 survey sites.
- Potential data stewardship considerations:
  - Clear data provenance, versioning, and change-tracking are essential for updates or re-analyses.
  Data consumers should reference the BeeSpecies_to_Guild_Table for consistent guild classifications.
  Metadata should capture survey dates, site IDs, grid references, and any data gaps or exclusions.
  Ensure alignment with data standards for species nomenclature and spatial referencing (British National Grid).

## Appendices and supplementary materials
- Appendix 1: Location and grid references of the ten 1 km2 survey sites.
- Appendix 2: Google Earth Engine code used for the random forest land use classification, including data preparation, training, classifier setup, and export steps.
- References: Carvell et al. (2016) methodology and related monitoring framework context.