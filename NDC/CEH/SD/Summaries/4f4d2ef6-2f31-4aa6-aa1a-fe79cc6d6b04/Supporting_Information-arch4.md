# Dataset files

## Overview and purpose
- A comprehensive wild bee survey dataset from Leighfield Forest (Leicestershire and Rutland, UK), collected Spring/Summer 2020.
- Aims to assess pollinator abundance and species richness across landscapes, following a modified Carvell et al. (2016) framework.
- Data are organized to support guild-based analyses, seasonal comparisons, spatial mapping, and integration with habitat/LULC data.

## Data files and formats
- Total of fourteen files, described in detail as tables 1 and 2–8.
- Key data files:
  - SurveyData_PanTraps_raw.csv: raw pan trap catches by site, date, pan color, grid reference, and per-species columns.
  - SurveyData_Transects_raw.csv: raw transect observations with site, grid reference, date, transect details, and per-species columns.
  - BeeSpecies_to_Guild_Table.csv: mapping of species to one of four guilds (GNSB, CNSB, GNBB, TNBB).
  - Abundance_Transects_ByGuild_Spring.csv; Abundance_Transects_ByGuild_Summer.csv; Abundance_PanTraps_ByGuild_Spring.csv; Abundance_PanTraps_ByGuild_Summer.csv: guild-level abundance by survey grid, for each season.
  - Abundance_AllObservations_ByGuild.csv: combined pan trap and transect abundance by guild across Spring, Summer, and total seasons.
  - SpeciesRichness_AllObservations.csv: species richness by site for Spring, Summer, and total.
  - Transect_Locations.shp (and associated files): spatial locations and paths of transects (British National Grid coordinates).
  - Leighfield_LULC_2020.tif: 10 m resolution land-use/land-cover raster (six classes).
  - Leighfield_LULC_2020_Legend.lyr / Leighfield_LULC_2020_Legend.qml: GIS legend files for the LULC map.
- Data dictionaries and schemas:
  - Table 2 provides column-level descriptions for key CSV files (e.g., Site, Date, Grid_Reference, species columns).
  - Table 5 and Table 6 describe the guild-based abundance and overall abundance structures.
- Spatial and raster data:
  - Transect_Locations.shp and related GIS files for spatial analysis.
  - Leighfield_LULC_2020.tif with a legend for map interpretation.

## Spatial data and GIS components
- Transect locations and survey grids are georeferenced in the British National Grid.
- LULC map created from Sentinel-2 imagery (Sept 20, 2020) using Google Earth Engine; classified into Woodland, Grassland/Pasture, Arable, Built Environment, plus Farm/Domestic buildings and Field Margin Habitats.
- Legend files accompany the raster for GIS interoperability.
- Appendix 1 lists ten 1 km2 survey sites with their grid references; Appendix 2 provides the Google Earth Engine code used for classification.

## Data collection methods and scope
- Field protocol is a modified version of Carvell et al. (2016) to better capture habitat variation:
  - Ten 1 km2 survey sites within Leighfield Forest.
  - Each site surveyed twice (Spring and Summer) with up to seven transects per km2, each transect ~100 m.
  - Pan traps: up to seven sets, with colored traps (blue, yellow, white) deployed for multiple hours per transect.
  - Transect observations focused on species-level identification; no separate quadrat floral observations due to limited time.
  - Weather data sourced from Loddington weather station when possible.
- Equipment list includes nets, forceps, pans, GPS, maps, and specimen containers.
- Habitats surveyed include woodland, hedgerows, various crops, watercourses, margins, and other farmland features; detailed habitat categories are enumerated.
- LULC map produced to contextualize bee assemblages within landscape types.

## Data quality, gaps, and limitations
- Blank cells in data files indicate no observations were recorded for that combination of site, date, and species.
- Field methodology changes (e.g., fewer transects per day, weather considerations) reflect trade-offs between coverage and practical field constraints.
- LULC accuracy reported at 89.1% based on a confusion matrix of 700 random points.
- Weather data coverage may be incomplete for some sites, potentially affecting seasonal comparisons.
- Habitat sampling, while broad, represents a subset of regional diversity and may limit generalization beyond studied squares.

## Data governance, metadata, and provenance
- Data are structured with explicit file naming conventions, detailed per-file descriptions, and per-column metadata (as in Tables 1–4 and Tables 5–7).
- Guild classifications rely on BeeSpecies_to_Guild_Table.csv to assign species to four functional guilds.
- Described processing steps include the creation of a regional LULC map via Google Earth Engine (Appendix 2) and subsequent GIS processing in QGIS.
- Reproducibility artifacts include:
  - Appendix 1: site locations and grid references.
  - Appendix 2: Google Earth Engine code for the random forest classification.
  - Export workflow demonstrated for generating a GeoTIFF of the classified LULC map.

## Reuse, analytics, and products
- Guild-based abundance and species richness enable analyses of habitat associations, seasonal patterns, and cross-site comparisons.
- Spatial alignment with the LULC map allows landscape-scale analyses of bee guild distributions.
- The dataset supports:
  - Temporal (Spring vs Summer) comparisons of guild abundance.
  - Species richness assessments at the grid level.
  - Linking bee assemblages to habitat types and land-use classes.
- Data products can inform pollinator management, habitat restoration, and landscape planning.

## Reproducibility and appendices
- Appendix 1: geographic locations and references for the ten survey sites.
- Appendix 2: Google Earth Engine code used for the random forest land-cover classification (with a sample script and model training/export workflow).
- The dataset includes explicit notes on data formats, column definitions, and processing steps to facilitate reuse and integration with other data.