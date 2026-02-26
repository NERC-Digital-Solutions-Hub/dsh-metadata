# Species traits, ecological preferences and distribution metrics for 48 species of ladybird considered resident in the United Kingdom

## Overview and aims
- Compiles trait data, ecological preferences, and distribution metrics for 48 ladybird species resident in the UK.
- Includes morphology, habitat and diet preferences, phenology, occupancy trends, and speciesTemperature Indices (STIs) where possible.
- Data drawn from published literature, the UK Ladybird Survey (via Biological Records Centre), iRecord (NBN Atlas), and the Field Guide to the Ladybirds of Britain and Ireland (Roy & Brown 2018).
- A detailed data paper will accompany the dataset.

## Dataset contents and structure
- The dataset comprises four CSV files:
  - ladybird_traits.csv: 74 fields across 48 species, detailing traits, ecological preferences, and occupancy trends; includes NA where data are missing.
  - metadata.csv: metadata for variables (Table 1 format) corresponding to the traits data.
  - prey_list.csv: list of prey species and their families used to calculate diet breadth (number of prey families) per ladybird.
  - sources.csv: list of sources (books, papers, websites) used to compile variables.
- Variables cover: taxonomy, conspicuousness, body size, polymorphism (melanic and spots), native status, record counts (1970–2023), geographic presence by country, 10-km grid occupancy, vice-counties, long-term and short-term occupancy trends with credible intervals, first/last years, feeding guilds and prey family counts, habitat associations (IUCN Level 1), habitat richness, larval/adult phenology, voltinism, and species temperature indices (UK and Europe; mean and peak).

## Data sources and data generation
- Primary sources: Field Guide to the Ladybirds of Great Britain and Ireland (Roy & Brown 2018), UK Ladybird Survey records, iRecord/NBN Atlas, GBIF Europe records.
- Occupancy trends derived from DRUID-based occupancy models using presence-only records (1970–2021 for occupancy; trends up to 2018 to avoid recorder-effort biases after 2018).
- Habitat associations mapped to IUCN Habitat Classification Scheme v3.1; habitats weighted by presence level.
- Diet data assigned to 11 feeding guilds; prey families counted to derive diet breadth; confidence levels assigned based on the number of feeding records.
- Temperature indices calculated using WorldClim data (1970–2000) for UK and Europe ranges, with UK-based STI using UK records and Europe-based STI from GBIF data after careful cleaning.

## Spatial and temporal coverage
- Scope: 48 resident UK ladybird species.
- Temporal span of records: 1970–2023 (UK data), with occupancy trends based on 1970–2018 (long-term) and 2009–2018 (short-term) where available.
- Geographic coverage: UK (England, Wales, Scotland, Northern Ireland) and Europe for STI calculations; country-level presence and 10-km grid occupancy across GB and Northern Ireland (and vice counties for GB).
- Phenology: first/last/peak months for larval and adult stages where data exist; larval data available for 1929–2021 but not for inconspicuous species; peaks validated against histograms.

## Methods and quality assurance
- Data collection and verification:
  - Records from UK Ladybird Survey and iRecord verified by survey organizers.
  - Expert validation of variables by PMJB and HER.
  - Peak month calculations visually validated against monthly histograms.
- Long-term and short-term trends:
  - Derived from occupancy models; not all species have converged estimates, leading to some missing short-term trends.
  - Long-term trend endpoints: typically 1970 to 2018; first-year adjustments if species arrived after 1970.
- Data processing and cleaning:
  - GBIF Europe records cleaned with CoordinateCleaner to remove dubious records; 1,584,603 initial records reduced to 631,289 usable records for the 48 species.
  - Records filtered to European, land-based observations; missing months removed for STI computations.
- Limitations acknowledged:
  - Inconspicuous species may have incomplete trait/occupancy data due to limited observations.
  - Some variables (especially larval metrics) may be NA for certain species.
  - Short-term trends may be incomplete due to non-convergence in model estimates or limited data.

## Accessibility and reproducibility
- Code and data processing workflow available at: https://github.com/CharlieOuthwaite/LadybirdTraits
- GBIF data usage requires a GBIF account to download; processing relies on R/R-based tools (rgbif, CoordinateCleaner, splus2R) and published methods from cited literature.

## Practical implications for environmental analysts
- A standardized, multi-dimensional dataset enabling:
  - Cross-species trait comparisons (morphology, habitat, diet, phenology).
  - Temporal monitoring of occupancy trends and responses to environmental change.
  - Habitat association analyses and assessment of habitat loss or gain for resident species.
  - Climate-related analyses via STI metrics across UK and Europe.
- Supports integration with other monitoring datasets to enhance environmental health assessments and policy performance evaluations over time.
- Provides transparent provenance and methodological notes to aid data quality checks and reproducibility.

## Notes on limitations and caveats
- Some species (especially inconspicuous ones) have partial data; several variables are NA where data are unavailable.
- Short-term trend estimates may be missing for certain species due to model convergence issues.
- Larval-stage data are less complete internationally and not publicly available in full detail.

## Key references and data provenance
- Roy, H. & Brown, P. (2018). Field Guide to the Ladybirds of Great Britain and Ireland.
- UK Ladybird Survey and iRecord data (Biological Records Centre, 2024a; 2024b).
- GBIF data and processing workflows, including RGBIF and CoordinateCleaner tools.
- Foundational methods: occupancy modeling and STI calculations as described in the cited literature.