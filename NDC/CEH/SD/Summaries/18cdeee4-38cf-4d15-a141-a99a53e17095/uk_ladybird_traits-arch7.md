# Species traits, ecological preferences and distribution metrics for 48 species of ladybird considered resident in the United Kingdom

## Summary for GIS Specialists
- A comprehensive dataset describing traits, ecological preferences, and distribution metrics for 48 UK-resident ladybird species.
- Includes both species-level attributes (morphology, habitat, diet, phenology) and distributional metrics (occurrence records, occupancy trends, spatial extents, and temperature indices).
- Data are derived from multiple sources (literature, Field Guide Roy & Brown 2018, UK Ladybird Survey, iRecord, GBIF) and prepared for map-based GIS analysis.

## Dataset scope and purpose
- Objective: enable map-based exploration of species traits, habitats, distributions, phenology, and occupancy trends for policy, conservation planning, and public communications.
- Target audiences: policymakers, consultants, researchers, and the public.
- Outputs: data ready for GIS visualisation and integration with other geospatial layers (habitat maps, climate surfaces, grid systems).

## Data structure and files
- ladybird_traits.csv
  - 74 variables across 48 species (49 rows including header).
  - Contains trait data, ecological preferences, occupancy trends, distribution metrics, and derived indicators.
  - Missing values denoted as NA where data are not available.
- metadata.csv
  - Table of variable definitions, units, and value ranges (Table 1).
- prey_list.csv
  - List of prey species and families used to calculate diet breadth (number of prey families).
- sources.csv
  - List of sources used to compile variables (books, papers, websites).

## Key variables and what they represent
- Taxonomy and identity: genus, species, common name, authority, tribe, subfamily.
- Conspicuousness: Conspicuous or Inconspicuous status.
- Body size: body_size_min and body_size_max (mm).
- Melanic and spot polymorphism: presence/absence and frequency (common/rare/not present).
- UK native status: native (1) or non-native (0).
- Records and occurrence: n_records, First_yr, Most_recent_yr; presence by country (England, Wales, Scotland, Northern Ireland); n_10k (10 km grid cells); n_vicecounties.
- Trends: Longterm_trend (occupancy change per year) with LT_trend_lower/upper and LT_first/LT_last; Shortterm_trend with ST_trend_lower/upper and ST_first/ST_last.
- Feeding guilds and diet: 11 feeding guild indicators, nfood_recs, nfamilies_diet, and Foodguild_confidence (low/medium/high).
- Habitat associations: presence in IUCN Level 1 habitats (Forest_woodland, Shrubland, Native_grassland, Wetlands_inland, Marine_intertidal, Marine_coastal_supratidal, Artificial_terrestrial, Other) and weighted/n_habitats counts.
- Phenology: Larvae_first/Last, Peak_larvae; Adult_first/Last, Peak_adult1/Peak_adult2; Max_month and Max_month_EU.
- Voltinism: Voltinism_min and Voltinism_max (generations per year).
- Species Temperature Indices (STI): UK_mean/Peak and Europe_mean/Peak (mean annual temperature across UK or Europe ranges; values rounded to two decimals).
- Data provenance and quality: nfood_recs and data confidence reflect data richness; expert validation noted.

## Spatial and temporal coverage
- Spatial scope: 48 species considered resident in the UK.
- Temporal coverage: records spanning 1970–2023 (UK records from UK Ladybird Survey and iRecord; Europe records from GBIF).
- Trend calculations: long-term trends cover 1970–2018; short-term trends cover 2009–2018 (because of potential changes in recorder effort after 2018).
- Larval data: first/last/peak larval months derived from records 1929–2021; applicability limited by data availability for some species.
- Europe STI: derived from GBIF records filtered to European countries; dataset comprises 631,289 records for the 48 species after cleaning.

## Collection, generation, and transformation methods
- Data sources: Field Guide to the Ladybirds of Britain and Ireland (Roy & Brown 2018), UK Ladybird Survey, iRecord (NBN Atlas), GBIF.
- Occupancy and trends: Bayesian occupancy modelling (DRUID framework) using day-resolution 1 km grid records; long-term and short-term trend estimates derived from occupancy trajectories.
- Spatial metrics: 10 km OS grid cells and British vice-counties used to quantify spatial extent and distributional reach.
- Diet and habitat: feeding guilds and habitat associations compiled from literature, expert input, and IUCN habitat scheme classifications.
- Phenology: first/last/peak months for larvae and adults calculated where data are sufficient; peak determinations validated by histogram checks.
- Temperature indices: UK-based indices from processed UKLadybird/iRecord data; Europe-based indices derived from filtered GBIF occurrences with CoordinateCleaner.

## Quality control and caveats
- Some inconspicuous species lack complete data; NA used where variables are not estimable.
- Short-term trend estimates may be missing if occupancy models did not converge.
- Prey and habitat data may carry biases due to uneven knowledge across species.
- Larval records are uneven across species; peaks and first/last months may be NA for some.
- All records are quality-checked (verification of dates/locations; land-based grid references) by survey organizers; expert validation performed on all variables.
- Data accessibility: code and workflow available on GitHub; GBIF usage requires a registered account.

## GIS applications and data product considerations
- Map-ready variables: occupancy trends, distribution extents (n_10k, n_vicecounties), country presence, habitat associations, and STI values.
- Visualization options: heatmaps of occupancy, choropleth maps of habitat breadth and tecnh properties, phenology by month, and temperature-index-based suitability layers.
- Data integration: align with IUCN habitat layers, 10 km grid surfaces, climate surfaces (WorldClim) for advanced analysis; cross-wertilize with other UK biodiversity datasets (e.g., pollinators, beetles).
- Uncertainty and confidence: incorporate Foodguild_confidence, data completeness (n_records, first/last year), and NA values to convey data quality in maps and summaries.

## Access and references
- Code for data processing and GBIF data handling: https://github.com/CharlieOuthwaite/LadybirdTraits
- Key sources and data providers: UK Ladybird Survey, iRecord (NBN Atlas), GBIF, Field Guide to the Ladybirds of Great Britain and Ireland (Roy & Brown 2018), and related publications (Outhwaite et al.; Powney et al.; Roy et al.).
- Notable data standards and tools referenced: CoordinateCleaner, OS British National Grids, DRUID occupancy modelling framework.