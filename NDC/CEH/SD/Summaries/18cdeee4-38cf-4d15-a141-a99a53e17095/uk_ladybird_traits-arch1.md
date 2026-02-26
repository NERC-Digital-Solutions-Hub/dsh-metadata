# Species traits, ecological preferences and distribution metrics for 48 species of ladybird considered resident in the United Kingdom

## Overview
- A dataset compiling traits, ecological preferences, and distribution metrics for 48 ladybird species resident in the UK.
- Includes morphology, habitat and diet preferences, phenology, occupancy trends, and species temperature indices (STI) where available.
- Data sources: published literature, the Field Guide to the Ladybirds of Great Britain and Ireland (Roy & Brown 2018), UK Ladybird Survey records, iRecord (NBN Atlas), and Europe data from GBIF.
- A detailed data paper will accompany the dataset.

## Data Structure
- four CSV files:
  - ladybird_traits.csv: 74 columns with trait, preference, and trend information for 48 species (49 rows including header; NA where missing).
  - metadata.csv: metadata table corresponding to the traits data.
  - prey_list.csv: prey species and their families used to calculate diet breadth (number of prey families).
  - sources.csv: list of sources used to compile variables (books, papers, websites).

## Variables and Metrics
- Taxonomy and identity: genus, species, common name, authority, tribe, subfamily; conspicuous vs inconspicuous; UK native status.
- Morphology and life history: body_size_min/max (mm), polymorphism_melanic, polymorphism_spot, voltinism_min/max, larval/adult phenology details.
- Occupancy and trends: n_records; first_yr, most_recent_yr; present in England/Wales/Scotland/Northern Ireland; n_10k grid cells; n_vicecounties.
- Trends: long-term (1970–2018) and short-term (2009–2018) occupancy trends with 95% credible intervals (LT_trend, LT_trend_lower, LT_trend_upper; ST_trend, ST_trend_lower, ST_trend_upper).
- Diet and feeding ecology: 11 feeding guilds (dominant, occasional, or unrecorded) across prey groups; nfamilies_diet; nfood_recs; food_guild confidence.
- Habitat associations: presence/absence or weighted presence across IUCN Level 1 habitats (Forest/woodland, Shrubland, Native grassland, Wetlands, Marine, Artificial terrestrial, Other); n_habitats_weighted; n_habitats.
- Phenology: first/last/peak monthly records for larvae and adults where data exist; maximum/peak months (with caveats for sparse data).
- Temperature indices: STI_UK_mean and STI_UK_peak (UK-based, all months vs peak month); STI_Europe_mean and STI_Europe_peak (Europe-based, GBIF-derived).
- Spatial scope: UK-focused occupancy and distribution metrics; European data used for STI_Europe analyses.

## Spatial and Temporal Coverage
- Records sources: UK Ladybird Survey, iRecord, GBIF (Europe).
- Temporal span for trait-derived data and occupancy: 1970–2023 (records); occupancy trends computed from 1970–2018 (long-term) and 2009–2018 (short-term).
- Larval data: records from 1929–2021 (not publicly available for all species).
- Europe STI calculations based on GBIF data (1970 onward) and processed to 631,289 records after cleaning.

## Collection, Processing, and Transformation Methods
- Trait and preference data: collated from literature, Roy & Brown (2018), UK Ladybird Survey, iRecord, and GBIF Europe records; body size range compiled from published sources.
- Diet breadth and prey families: prey species mapped to GBIF families; eleven feeding guilds assigned; confidence levels (low/medium/high) based on feeding records.
- Habitat associations: IUCN Habitat Classification Level 1 categories; weighted habitat count reflecting presence vs. occasional presence.
- Distribution metrics: counts of records, first/last years, country-level presence, 10-km grid cell coverage, and vice-county counts.
- Occupancy trends: Bayesian occupancy models (DRUID project) using day-resolution 1 km grid records; trends computed as annual percent change from first to last converged year; long-term uses 1970–2018, short-term uses 2009–2018.
- Phenology: larval and adult monthly records used to identify first/last/peak months; larval data limited to some species; peaks validated against histograms.
- Temperature indices: UK STI calculated from UK records (all months and peak month); Europe STI calculated from GBIF records with data cleaning (CoordinateCleaner) to ensure reliability.
- Reproducibility: code to download and process GBIF data available at GitHub (CharlieOuthwaite/LadybirdTraits); GBIF access may require account.

## Quality Control and Limitations
- Some variables missing for inconspicuous or recently arrived species; short-term trends may be incomplete due to convergence issues.
- Data gaps: sparse larval records for some species; potential biases in prey records due to uneven research effort.
- Post-2018 changes (e.g., Field Guide publication) may affect recording effort and apparent trends, especially for inconspicuous species.
- Validation: expert review by PMJB and HER; peaks checked against histograms; UK records verified by survey organizers.
- Not all species have complete data for every variable; NA used where data are unavailable.

## Reproducibility, Access, and Documentation
- four CSV files with metadata and data definitions; detailed definitions provided in the metadata.
- GitHub repository for data processing and GBIF workflow: https://github.com/CharlieOuthwaite/LadybirdTraits
- A detailed data paper will be published alongside the dataset.

## Potential Uses for Analysts
- Cross-species trait analyses and correlations with occupancy trends.
- Comparative studies of habitat use, diet breadth, and phenology across UK resident ladybirds.
- Integrating trait data with occupancy models to inform conservation or management decisions.
- Temporal analysis of range shifts and population dynamics under different environmental scenarios.
- Reproducible data pipeline for similar trait-occupancy datasets in other taxa.