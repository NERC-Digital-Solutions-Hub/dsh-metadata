# The UK Pollinator Monitoring Scheme

- A dataset describing the UK Pollinator Monitoring Scheme (PoMS) 1 km square pan trap survey data collected from 2017 to 2021, including insect (bees and hoverflies) and floral (forbs) occurrences and associated environmental context.
- Data are intended to support analyses of pollinator abundance, community composition, and plant-pollinator relationships across the UK, contributing to national pollinator strategies.

## Data coverage and sampling design

- 95 randomly allocated 1 km squares across England, Scotland, Wales, and Northern Ireland (NI added in 2021).
- Stratified sampling by land-cover type to capture agricultural vs. semi-natural landscapes; squares matched to habitat cover from the UKCEH Land Cover Map 2007.
- Squares co-located with National Plant Monitoring Scheme (NPMS) sites in England, Scotland, and Wales; NI sampling added in 2021.
- Sampling plan aimed to detect trends over a 10-year period; initial power calculations supported a network of 75 sites with additional NI squares for broader coverage.
- Within each square: a diagonal transect with five pan trap stations, spaced to minimize disturbance and avoid shading; traps placed in open areas and collected after a 6-hour exposure.

## Sampling protocol

- Conducted by PoMS volunteers and staff; four visits per summer (May–August), with at least two weeks between visits to a given square.
- Pan traps: three bowls per station (one of each colour: yellow, blue, white) filled with water and a drop of detergent to reduce surface tension.
- Weather thresholds for sampling: temperature minimums vary with cloud cover; wind speed ≤ 5 on Beaufort scale; sampling only during suitable weather.
- Insects trapped are returned to UKCEH for sorting and identification; bees and hoverflies identified to species level; other groups identified to taxon group.
- Floral data consist of flowering herbaceous species counts in a 2 m radius around each pan trap station.

## Data files and structure

- Three main data files (pan-trap based 1 km square survey data):
  - Samples: sample-level data for each 1 km square and survey visit (sample_id, location, date, trap_station, environmental variables, etc.).
  - Insects: occurrence-level data for bees and hoverflies (occurrence_id, specimen_code, taxon_group, taxon_source, English name, taxonomy, count, sex, stage, etc.).
  - Flowers: occurrence-level data for forbs in flower within 2 m of traps (occurrence_id, taxon_group, taxon_source, English name, taxon_version_key, floral_unit_count, total_floral_units, year, etc.).
- Years covered: 2017–2021 (2017 pilot year with partial data; 2020 had covid-related gaps; NI data largely pilot in 2021).
- Data files provided (examples):
  - ukpoms_1kmPanTrapData_2017-2021_samples.csv
  - ukpoms_1kmPanTrapData_2017-2021_flowers.csv
  - ukpoms_1kmPanTrapData_2017-2021_insects.csv
- Attributes for each file are described in detail, including field definitions, units, and linkages between samples, occurrences, and year.

## Data quality and QA processes

- Data entry originally via iRecord/Indicia; later 2021 processes moved to PoMS site with the same data structure.
- Multi-stage QA:
  - Consistency checks on environmental and trap data; cross-checks between sample and occurrence data.
  - Taxonomic identifications checked by multiple taxonomists; cross-checks introduced since 2019 for a random subset and for unusual records.
  - Quality checks on photos of flowering plants near traps; corrections applied where needed.
  - Specimen codes and bycatch codes validated for uniqueness and proper linkage to samples.
  - Additional QA in 2021 using R for data integrity and consistency.
- Corrections and standardisations:
  - Taxonomy transformations saved in TRANSFORM_insect_taxonomy_all_species_to_2021.csv and updated subsequently to ensure consistent species standardisation and aggregation across years.
  - Floral unit data corrections, including handling of miscounted units and to account for Poaceae (not counted as floral units in some cases).
  - Welsh-language notes translated and standardised; format inconsistencies cleaned (e.g., date/time fields).
- Combined and exported data:
  - After corrections, data from 2017–2020 were aligned with 2021 data to form a 4-year and a 5-year dataset, with outlier handling (notably floral unit counts) documented and applied for cross-year consistency.

## Data corrections and transformations

- Floral data corrections:
  - Corrected floral unit counts when inappropriate units were used; maintained a record of corrections and applied them to the 2017–2020 data before combining with 2021 data.
  - Poaceae counts adjusted to reflect the methodological decision to exclude these from total floral units.
  - Outlier detection and correction performed for floral unit counts; boxplots generated to inspect outliers by plant family and floral unit type.
- Taxonomic standardisation:
  - Taxon names harmonised across years using a saved transformation file; updated annually to reflect new identifications while preserving historical compatibility.
- Data integrity checks:
  - Ensured unique sample_id, specimen_code, and bycatch codes; verified that traps were not duplicated and that sampling dates/locations were correctly aligned to 1 km grid squares.

## Collation across years

- The dataset was collated by combining 2017–2020 data with 2021 data:
  - 2017: pilot year with partial data; 2018–2019 more complete; 2020 had substantial gaps due to covid.
  - 2021: expanded geographic coverage to include NI and added QA enhancements.
- After applying floral unit corrections to 2017–2020 data, the four-year flowers dataset was reconciled with the 2021 data to create a cohesive five-year dataset.
- In many steps, redundant columns were removed and numbers reformatted for consistency (e.g., date/time fields, location references).

## Data export and usage

- Data are available via the Environmental Information Data Centre (EIDC), part of NERC, with Open Government Licence terms.
- Citations required when using the dataset (UK Pollinator Monitoring Scheme, 2024; EIDC reference).
- Exported data columns are aligned to the EIDC dataset structure, enabling direct integration into analyses and data portals.
- The dataset enables analyses of:
  - Temporal trends in pollinator abundances and community composition.
  - Relationships between pollinator counts and habitat/land-cover variables.
  - Plant-pollinator interactions via linked floral and insect occurrence data.

## Data access, licensing, and acknowledgments

- Access: EIDC (UKCEH) under Open Government Licence; dataset cited in publications describing research using PoMS data.
- Acknowledgments: PoMS is a partnership funded by UKCEH, JNCC, and government bodies across the four nations, with substantial volunteer contributions.
- References: Key Carvell et al. design and testing references; PMRP progress and PoMS-related publications.

## Annex and taxonomy grouping

- Annex: Aggregate species groupings for taxa not distinguishable to species level, detailing standardised vs. aggregated taxon concepts across Hymenoptera and Diptera (e.g., Bombus lucorum/terrestris/cryptarum complexes; Dasysyrphus venustus/neovenustus as a species complex; Poaceae adjustments, etc.).
- Purpose: supports consistent aggregation in analyses where species-level resolution is not possible or not necessary.

- Note: The document includes extensive methodological and data-structure details aimed at analysts seeking to perform robust, cross-year analyses of pollinator populations and their floral associations using standardized, quality-assured PoMS pan trap data.