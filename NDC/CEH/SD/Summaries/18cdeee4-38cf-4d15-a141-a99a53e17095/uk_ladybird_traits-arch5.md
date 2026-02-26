# Species traits, ecological preferences and distribution metrics for 48 species of ladybird considered resident in the United Kingdom

- A dataset compiling traits, ecological preferences and distribution metrics for 48 UK-resident ladybird species.
- Data sources include published literature, the Field Guide to the Ladybirds of Britain and Ireland (Roy & Brown, 2018), UK Ladybird Survey records, iRecord (NBN Atlas), and GBIF European records.
- Aims to support data governance, discoverability, and reuse by documenting variables, provenance, and processing steps; a detailed data paper will accompany the dataset.

## Data structure and files

- ladybird_traits.csv
  - 49 rows (header + 48 species) and 74 columns.
  - Contains species-level information on traits, ecological preferences, occupancy trends, and related metrics.
  - Missing values are indicated as NA; variables are described in Table 1 and in metadata.csv.
- metadata.csv
  - CSV representation of Table 1 with definitions, units, and value ranges for the traits dataset.
- prey_list.csv
  - List of prey species by family for calculation of diet breadth (number of prey families) per ladybird species.
- sources.csv
  - List of sources used to compile information (books, papers, websites).

## Variables and content overview

- Taxonomy and nomenclature
  - Scientific name, genus, common name, authority, tribe, subfamily.
- Morphology and variation
  - Body size (min/max in mm), presence of melanic and spot polymorphisms, native status in the UK.
- Population and occupancy metrics
  - Records counts, first/most recent year, presence by country (England, Wales, Scotland, Northern Ireland), 10-km grid occupancy, and number of vice-counties.
  - Long-term and short-term occupancy trends with 95% credible intervals.
  - First/last/peak months for larval and adult records (with caveats for data-sparse species).
- Diet and feeding guilds
  - Diet breadth including eleven feeding guilds; number of prey families; feeding-records-based confidence (low/medium/high).
- Habitat associations
  - Presence in Level 1 IUCN habitats (weighted and total habitat counts).
- Phenology and voltinism
  - Larval and adult record months, peak months, maximum months, and voltinism (minimum/maximum number of generations per year).
- Temperature indices
  - Species Temperature Index (STI) UK mean and peak, Europe mean and peak (based on GBIF data for Europe).
- Data scope indicators
  - n_records, first/most recent year, country-level presence flags, 10-km grid cells, vice-counties, etc.

## Temporal and spatial coverage

- Focus: 48 species considered resident in the UK.
- Temporal scope for records: 1970–2023 (UK records from UK Ladybird Survey and iRecord; GBIF Europe data used for European STI calculations).
- Trends:
  - Long-term trends: 1970–2018 (subject to data convergence and availability; first year may vary by species).
  - Short-term trends: 2009–2018 (where convergent occupancy estimates exist; some species lack short-term trends due to non-convergence).
- Spatial resolution:
  - UK-wide occupancy estimates; country-level presence (England, Wales, Scotland, Northern Ireland); 10-km OS grid cells; British vice-counties.
- Data sources for trends and records:
  - UK Ladybird Survey, iRecord (NBN Atlas), GBIF (for Europe data), Field Guide (Roy & Brown, 2018).

## Methods and processing

- Data derivation and sources
  - Traits/traits-derived metrics compiled from published literature, Field Guide (2018), UK Ladybird Survey, iRecord, and GBIF Europe records.
- Record-derived variables
  - Date- and location-derived metrics: counts of records, first/last year, presence by country, 10-km grid occupancy, and vice-counties.
  - Occupancy trends: derived using Bayesian occupancy modelling (DRUID project approach) with presence-only records reformatted to 1 km grid scale; model convergence governs usable years.
- Trend calculations
  - Long-term trends: occupancy growth rate (percent change per year) from first converged year (often 1970 or later) to 2018.
  - Short-term trends: occupancy growth rate from 2009 to 2018; upper/lower 95% credible intervals provided.
  - Some species missing trends due to non-convergence; first/last years documented for reference.
- Diet and feeding guilds
  - Literature review to identify prey items; prey family assignment via GBIF taxonomy; eleven feeding guilds; confidence levels assigned by number of feeding records.
- Habitat associations
  - Presence/absence or occasional presence across IUCN Level 1 habitats; weighted and total habitat counts computed.
- Phenology and records
  - Larval and adult first/last/peak months derived from available records; larval data limited in inconspicuous species.
  - Peak months assessed via histogram analysis; NA when data are insufficient.
- Temperature indices
  - STI UK mean/peak: derived from UK records and WorldClim data (1970–2000 baseline).
  - STI Europe mean/peak: derived from GBIF European records; cleaned with CoordinateCleaner to maximize reliability.
- Data quality and validation
  - All records from UK Ladybird Survey and iRecord undergo organizer verification.
  - Variables undergo expert validation (PMJB and HER); peaks validated visually against histograms.
  - Some data gaps and NA values acknowledged for inconspicuous species or poorly converged trends.
- Reproducibility
  - Code and data processing workflow available at: https://github.com/CharlieOuthwaite/LadybirdTraits
  - GBIF-derived data require a GBIF account; data processing includes filtering steps to ensure reliability.

## Quality, limitations and governance considerations

- Data completeness
  - Not all variables could be determined for inconspicuous species due to data limitations or recent arrivals.
  - Short-term trends may be missing for some species where model convergence failed.
- Data provenance and transparency
  - Provenance is documented (literature, field guides, citizen science records, GBIF Europe).
  - Metadata provides definitions, units, and value ranges for variables.
- Interpretation considerations
  - Biases in prey-data collection may affect diet breadth; confidence levels are provided.
  - Larval data are incomplete for some species; first/last months may be NA where data are sparse.
- Governance and reuse
  - A separate data paper will accompany the dataset, outlining methods and caveats in more detail.
  - The dataset is designed to be reusable for biodiversity monitoring, trait analyses, and conservation planning, with standardized variables and documented processing steps.

## Access, licensing and reuse guidance

- Primary data and metadata are housed in four CSV files (ladybird_traits.csv, metadata.csv, prey_list.csv, sources.csv) with clear variable definitions and units.
- Methods and code are available via the stated GitHub repository; GBIF data usage follows GBIF data access policies.
- Users should note data limitations related to inconspicuous species and potential non-convergence in trend estimates when applying analyses.

## References and data sources

- Roy, H. & Brown, P. (2018) Field Guide to the Ladybirds of Great Britain and Ireland.
- UK Ladybird Survey data (Biological Records Centre, 2024a).
- iRecord (Biological Records Centre, 2024a).
- GBIF.org (2024) GBIF Occurrence Download.
- WorldClim 2 climate surfaces (Fick & Hijmans, 2017) for STI computations.
- DRUID project methodology for occupancy trends (Outhwaite et al., 2019; Powney et al., 2019).
- CoordinateCleaner (Zizka et al., 2019) for data cleaning of GBIF records.
- Additional methodological references and data sources listed in metadata.