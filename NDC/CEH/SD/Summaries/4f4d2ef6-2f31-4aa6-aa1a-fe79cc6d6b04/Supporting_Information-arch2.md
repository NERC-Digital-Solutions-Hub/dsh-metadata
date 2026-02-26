# Dataset files

- Purpose and scope
  - Describes a wild bee survey in Leighfield Forest (Leicestershire and Rutland, UK) conducted Spring/Summer 2020.
  - Methodology is a modification of Carvell et al. (2016) designed to assess pollinator guilds across varied habitats.
  - Aimed at generating standardized data to monitor environmental health and policy performance, with outputs suitable for maps, charts, and reports; datasets are stored and uploaded to appropriate portals.

- Datasets included (14 files)
  - SurveyData_PanTraps_raw.csv: Raw pan trap catches for wild bees, organized by site and species.
  - SurveyData_Transects_raw.csv: Raw transect observations for wild bees, organized by site and species.
  - BeeSpecies_to_Guild_Table.csv: Mapping of each species to one of four guilds (GNSB, CNSB, GNBB, TNBB).
  - Abundance_Transects_ByGuild_Spring.csv: Abundance by guild for transect observations (Spring).
  - Abundance_Transects_ByGuild_Summer.csv: Abundance by guild for transect observations (Summer).
  - Abundance_PanTraps_ByGuild_Spring.csv: Pan trap abundance by guild (Spring).
  - Abundance_PanTraps_ByGuild_Summer.csv: Pan trap abundance by guild (Summer).
  - Abundance_AllObservations_ByGuild.csv: All observations by guild across Spring, Summer, and total seasons.
  - SpeciesRichness_AllObservations.csv: Species richness by season across pan traps and transects.
  - Transect_Locations.shp (and associated files): Spatial locations and paths of transects.
  - Leighfield_LULC_2020.tif: 10 m resolution land-use/land-cover map for the survey region (six classes).
  - Leighfield_LULC_2020_Legend.*: Legend files for the LULC map in GIS software.
  - (Note: Table 2–7 describe the column structures for these files; Table 8 provides the shapefile details.)

- Data structure and key variables
  - Raw data files include site, grid reference, date, survey times, transect/station numbers, pan trap details, and species-level observation columns.
  - Species columns capture raw counts; the BeeSpecies_to_Guild_Table links each species to a guild.
  - Abundance and species richness outputs are organized by survey grid (British National Grid Reference) and season (Spring, Summer, All Seasons).

- Analytical outputs and formats
  - Guild-level abundance by transect and by pan traps, by season.
  - All-observations abundance by guild across seasons.
  - Species richness per grid, by season.
  - Transect locations in a shapefile for mapping; LULC map for habitat context.

- Methods overview
  - Fieldwork modified from Carvell et al. (2016):
    - 100 m transects (in practice up to seven per km^2 grid), visited twice per season (Spring and Summer); aims for better habitat coverage.
    - No quadrat flower observations; extended time per observation was constrained by fieldwork limits.
    - Up to seven sets of pan traps; fieldwork scheduled to avoid hottest parts of the day.
  - Weather data referenced from Loddington station when available.

- Field equipment
  - Insect nets and spare nets; hand lens; glass tubes for specimen transport; transect marker canes; pan trap bowls and containers; camera; GPS; field maps.

- Habitats encountered (localized survey sites)
  - Woodland: mature, young, edges, regenerating.
  - Hedgerows: various heights and margins.
  - Crops: multiple crop types, away from margins; includes pasture and meadows.
  - Watercourses: margins, banks, ditch terminology.
  - Field margins and other linear habitats: floristic margins, pollen/nectar strips, margins along tracks.
  - Roadside margins and disused railway lines as additional habitats.

- Land use / land cover mapping
  - Created a region-wide LULC map using Google Earth Engine from Sentinel-2 imagery (Sept 20, 2020).
  - Four initial classes: Woodland, Grassland/Pasture, Arable, Built Environment; plus two manually added classes: Farm Building and Domestic Building; and Field Margin Habitats.
  - Random forest classification with 300-tree forest, trained on labeled polygons; accuracy validated with 700 random points, achieving overall accuracy of 89.1%.
  - Appendix 2 provides the Google Earth Engine code used for the classification (including SVM/random forest configuration and export to GeoTIFF).

- Appendices and data provenance
  - Appendix 1: Locations and grid references for ten 1 km^2 survey sites.
  - Appendix 2: Google Earth Engine code for the random forest classification (including preprocessing, training, classification, and export steps).

- Data governance, reuse, and access
  - Data are prepared for standard environmental monitoring outputs (maps, charts, reports) and are intended to be stored in and accessible via established data portals.
  - Emphasizes the importance of making underlying data accessible to enable broader analysis and data value beyond single-use outputs.

- Challenges and opportunities (as identified by the study)
  - Increasing the value of datasets by integrating with additional relevant data sources.
  - Ensuring access to the underlying data used to produce final outputs to enable transparency, re-use, and broader analysis.