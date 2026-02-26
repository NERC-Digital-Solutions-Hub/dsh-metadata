# UK Pollinator Monitoring Scheme metadata: pan-trap survey data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview
- Metadata for version 2 of the pan-trap dataset; previous version withdrawn due to incorrect totals
- Describes pan-trap samples and occurrences from the UK Pollinator Monitoring Scheme (PoMS) 1 km square survey (2017–2020)
- PoMS aims to monitor pollinator populations across the UK and support national pollinator strategies; dataset is community-driven with volunteer involvement

## Data scope and content
- Geographic scope: 75 randomly allocated 1 km squares across England, Scotland and Wales; GB totals provided
- Time span: 2017–2020 (2017 was a pilot year with less data)
- Data files (three CSVs):
  - ukpoms_1kmPanTrapData_2017-2020_samples.csv (sample-level metadata)
  - ukpoms_1kmPanTrapData_2017-2020_insects.csv (occurrence-level data for bees and hoverflies)
  - ukpoms_1kmPanTrapData_2017-2020_flowers.csv (occurrence-level data for forbs near traps)
- Data include samples, environmental context, insect occurrences, and nearby flower counts
- Taxonomic identifications: bees and hoverflies identified to species where possible; some groups aggregated when indistinguishable or male-only IDs; full source taxa retained

## Sampling design and locations
- Network of 75 1 km squares with stratification by land-cover (agricultural vs semi-natural) and proportional to country land area
- Each square features a diagonal transect with five pan-trap stations, spaced to minimize disturbance and ensure open habitats
- Pan traps: three bowls per station (one of each colour), deployed for 6 hours during visits
- Sampling window: four visits per summer (May–August), with minimum two weeks between visits; weather and access can create gaps
- Trap setup and movement rules detail practical considerations (e.g., tramlines in arable fields, avoiding operations like spraying/harvest when possible)

## Sampling protocol and data collection
- Data collection conducted by PoMS volunteers and staff; initial data entered into iRecord/Indicia; specimens sent to UKCEH for sorting and taxonomic identification
- Standardized QA checks at multiple stages, including photo verification of flowering plants and cross-checks by taxonomic experts
- Bee and hoverfly identifications undergo verification by taxonomists; some taxa are aggregated when precise species-level ID is not feasible
- Flower and floral-unit data linked to trap locations through taxon-specific attributes

## Data quality assurance (QA) and taxonomy
- Multi-stage QA: field data entry, lab counting/identification, and taxonomic verification
- Cross-checking of rare or out-of-range identifications by a second taxonomist; additional random and targeted checks in 2019–2020
- Aggregation rules (Annex) standardize non-identifiable taxa while preserving as much taxonomic detail as possible; original identifications retained for reference
- Notes explain limitations, including male-only identifications in some groups and changes to determinations after QA

## Data files and attributes
- Samples file: sample_id, country, location_code/name, 1 km square reference, land_cover, date/year, trap details, weather/meteorological variables, habitat category, movement, and counts by taxon groups
- Insects file: occurrence-level data for bees and hoverflies linked to sample_id; includes pan_trap_station, taxon information (group, name, source key, standardised/aggregated taxon), count, sex, life stage, and identification notes
- Flowers file: occurrence-level data for forbs within 2 m of traps; includes taxon information, floral unit counts, and spatial context
- Attribute details cover sampling conditions (temperature, cloud cover, wind), habitat context, trap location, and data provenance (digitised_by, lab/identity info)

## Coverage and statistics
- Separate tallies are provided for England, Scotland, Wales, and GB totals across 2017–2020 (including number of squares surveyed, total visits, and pan-trap samples)
- 2017 data are partial due to pilot status; 2018–2020 progressively fuller
- Data availability notes reflect incomplete sampling in some squares/years due to access, weather, volunteer availability, and pandemic restrictions (2020)

## Usage notes and interpretation
- Incomplete per-square sampling in some years; results should consider sampling effort differences
- Taxonomic aggregation means some analyses require using aggregated taxa while preserving detailed source identifications
- QA results indicate occasional identification revisions; the dataset documents these changes and retains original source taxa

## References and supplementary information
- Key publications detailing the design, testing, and ongoing PMRP/PoMS work (Carvell et al. 2016; Carvell et al. 2020; PMRP progress reports)
- Annex with detailed explanations of aggregate species groupings and notes on taxonomy, including male-only identification constraints

## Access and related resources
- PoMS 1 km square survey overview: https://ukpoms.org.uk/one-km-square-survey
- Related datasets and publications (FIT Count, PMRP reports) provide broader context and methodology
- Dataset designed to support data exploration and the creation of data products; outputs are intended for public use within Defra and partner ecosystems