# Species traits, ecological preferences and distribution metrics for 48 species of ladybird considered resident in the United Kingdom

## Overview
- A comprehensive compilation of ecological traits, habitat and diet preferences, phenology, and distribution metrics for 48 UK-resident ladybird species.
- Data sources include published literature, the Field Guide to the Ladybirds of Britain and Ireland (Roy & Brown 2018), UK Ladybird Survey records, iRecord, and European records via GBIF.
- Derived variables cover occupancy trends (long-term and short-term), temperature indices, habitat associations, feeding guilds, and phenology.
- A detailed data paper will be published alongside the dataset.

## Data structure
- Four CSV files:
  - ladybird_traits.csv: 48 species, 74 variables plus header; includes traits, preferences, trends (uses NA where data are missing).
  - metadata.csv: description of variables, definitions, units, and value ranges.
  - prey_list.csv: prey species by family for calculating diet breadth across the 48 species.
  - sources.csv: list of sources (books, papers, websites) used for variable compilation.
- Key variable types include taxonomy, conspicuousness, body size, polymorphism, native status, records counts, country-level presence (England/Wales/Scotland/Northern Ireland), 10-km grid presence, vice-counties, long- and short-term occupancy trends with 95% credible intervals, feeding guilds, number of prey families, habitat associations, phenology (larval and adult first/last/peak months), voltinism, and Species Temperature Indices (UK and Europe).

## Data provenance and sources
- Primary data from:
  - UK Ladybird Survey and iRecord (via NBN Atlas) for occurrence records (1970–2023) and occupancy trends (1970–2018 for long-term; 2009–2018 for short-term).
  - Field Guide to the Ladybirds of Great Britain and Ireland (Roy & Brown 2018).
  - GBIF for European records (processed with strict cleaning).
- Methods and sources documented in the database, including DRUID-based occupancy modelling and habitat/diet classifications.
- Code and data processing workflows publicly accessible (GitHub: LadybirdTraits).

## Methods
- Trait and preference derivation:
  - Sourced from literature and Roy & Brown (2018); where data are missing, NA is used.
- Occupancy trends:
  - Bayesian occupancy models applied to day-resolution presence-only records (1970–2021), with long-term trends (1970–2018) and short-term trends (2009–2018) calculated as annual growth rate.
  - First and last years used for trend calculations; models only retained converged years (rhat ≤ 1.1).
- Diet and feeding guilds:
  - Prey species compiled from literature; prey family classification aligned with GBIF taxonomy; feeding guilds assigned as dominant, occasional, or unrecorded; confidence levels (low/medium/high) based on number of feeding records.
- Habitat associations:
  - Presence/absence within IUCN Level 1 habitats; weighted habitat counts account for primary vs. occasional presence.
- Phenology:
  - First/last/peak larval and adult months derived from larval datasets (1929–2021) and processed UK records; peaks validated against histograms; larval data may be sparse.
- Species Temperature Indices (STIs):
  - UK/STIs computed from UK records (mean across months and peak months) using WorldClim historical climate data (1970–2000); Europe/STIs derived from GBIF occurrence data after rigorous cleaning with CoordinateCleaner.
- Spatial analysis:
  - Records overlaid on 1-km grid squares for occupancy; 10-km OS grid for range extent; vice-counties used for Britain and Ireland.
- Quality control:
  - Expert validation (PMJB and HER); peaks verified against monthly histograms; GBIF processing documented; limitations acknowledged for inconspicuous species and convergence issues in trends.
  - Raw GBIF data processing script available in the repository; GBIF access requires an account.

## Spatial and temporal coverage
- Scope: 48 species considered resident in the UK.
- Temporal range: 1970–2023 for records; occupancy trends up to 2018; larval records up to 2021 (not publicly available).
- Spatial scale: UK-wide with country-level presence (England/Wales/Scotland/Northern Ireland), 1-km grid occupancy, 10-km grid occurrence counts, and vice-counties.

## Quality control and limitations
- Gaps for inconspicuous species due to data limitations or late arrival; some variables missing (NA) where data are unavailable.
- Short-term trends may be missing for some species due to non-convergence in the occupancy models.
- Larval data are sparse and not available for inconspicuous species; potential biases in prey data due to uneven research effort and reporting.
- Europe-based STI estimates rely on GBIF and rigorous data cleaning; residual spatial biases may remain.

## Access, reproducibility, and governance
- Code and data processing workflow publicly available at the referenced GitHub repository.
- GBIF-derived data require proper data access permissions; metadata documents units, definitions, and value ranges to support reuse.
- The dataset emphasizes transparency, metadata completeness, and data provenance to facilitate monitoring and policy-relevant analyses.
- A forthcoming detailed data paper will accompany the dataset.

## Implications for monitoring and policy
- Provides a standardized, multi-dimensional baseline of traits, habitat preferences, diet breadth, phenology, occupancy trends, and temperature associations for UK ladybirds.
- Enables monitoring of responses to climate change and habitat modification through occupancy trajectories, habitat usage, and STI comparisons.
- Supports cross-species comparisons and informs habitat management, conservation planning, and early-warning indicators for environmental health monitoring.