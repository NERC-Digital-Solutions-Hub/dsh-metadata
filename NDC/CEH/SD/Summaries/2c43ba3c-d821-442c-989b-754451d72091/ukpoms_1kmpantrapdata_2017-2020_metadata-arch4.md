# UK Pollinator Monitoring Scheme metadata: pan-trap survey data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview
- Provides metadata and description for the Pan-trap data from PoMS covering 2017–2020 (version 2; fixes to earlier version).
- PoMS is part of a UK-wide effort to monitor insect pollinator populations and support national pollinator strategies.
- Data are gathered via a network of 75 randomly selected 1 km squares across England, Scotland, and Wales, using pan traps and habitat/flower observations, with additional Flower-Insect Timed Count data published separately.
- Data contributors include multiple UK research and conservation organisations; funding and collaboration details are acknowledged.

## Data scope and structure
- Spatial and temporal coverage
  - 75 randomly allocated 1 km squares across GB (England, Scotland, Wales).
  - Years: 2017 (pilot year) through 2020.
  - Sampling typically across four visits per summer (May–August), weather permitting; some squares/years have incomplete data due to access, weather, volunteers, or covid-related restrictions in 2020.
- Datasets provided
  - ukpoms_1kmPanTrapData_2017-2020_samples.csv – sample-level data for each pan-trap site within a 1 km square.
  - ukpoms_1kmPanTrapData_2017-2020_insects.csv – occurrence-level data for bees and hoverflies at each sample.
  - ukpoms_1kmPanTrapData_2017-2020_flowers.csv – occurrence-level data for forbs (flowers) within 2 m of each pan-trap station.
- Data content
  - Insects: counts by taxon group; species-level identifications where possible (bees and hoverflies), with aggregations when species-level ID is not possible.
  - Flowers: counts of flowering plants within 2 m of each trap.
  - Samples: trap location, year, land cover, weather, habitat context, trap details (station, timing, movement, etc.).

## Sampling design and protocol
- Survey layout
  - 75 pan-trap stations per square distributed along a diagonal transect within each 1 km square (five stations per square, spaced evenly, minimum 100 m apart).
  - Habitat stratification linked to CEH Land Cover Map 2007 (agricultural vs semi-natural) to ensure balanced sampling across landscapes.
- Pan-trap protocol
  - Three colored bowls per trap station (yellow, blue, white) filled with water and a drop of washing-up liquid; positioned on stakes or ground in suitable open areas.
  - Sampling duration: 6 hours per visit, typically 09:00–17:00 BST, with weather thresholds for temperature, cloud cover, and wind.
  - Visits: up to four per summer per square; data collected by volunteers and staff; traps sometimes moved if disturbed.
- Sample collection and processing
  - Specimens sent to UKCEH for sorting; bees and hoverflies identified to species where possible; other taxa identified to appropriate group level.
  - Flower observations associated with trap locations documented via photos and QA processes.

## Data quality, QA, and taxonomy
- Quality assurance
  - Data entered via iRecord/Indicia in three stages: sampling/environmental data; insect counts by taxon group; species identifications by taxonomists.
  - QA checks include photo verification of flowering plants, taxonomic cross-checks, and use of lookup tables for floral associations.
  - For bees/hoverflies, identifications verified by multiple taxonomists; 2019 and 2020 included additional cross-checks for random samples and outliers.
- Taxonomic aggregation
  - Where species-level identification is not possible (e.g., cryptic groups or sex-based ID limitations), specimens are aggregated into defined species groups for analysis, while original identifications remain in records.
  - Annex of the metadata provides detailed aggregation rules for representative groups (e.g., Bombus lucorum complex, Sphaerophoria species complex, etc.).
- Data integrity notes
  - The 2017 dataset included as a pilot with fewer data than later years; 2020 data affected by covid restrictions.
  - Species-level data may include notes about sex-based identification limitations and taxonomic updates over time.

## Data fields and file-level details
- Data file: ukpoms_1kmPanTrapData_2017-2020_samples.csv
  - Contains sample identifiers, geographic context (country, location code/name, 1 km square), land cover, date/year, who digitised, trap station, timing, weather, habitat notes, movement, and trap counts by taxon groups (e.g., bees, hoverflies, various insect groups, and flowers).
- Data file: ukpoms_1kmPanTrapData_2017-2020_insects.csv
  - Contains occurrence-level data for bee and hoverfly specimens linked to sample_id, with taxon_group, taxon_source, English_name, taxon_version_key, counts, sex, stage, and aggregation fields.
- Data file: ukpoms_1kmPanTrapData_2017-2020_flowers.csv
  - Contains occurrence-level data for forbs near traps, linked to sample_id, with taxon_group (flowering plant), family, order, floral_unit, and counts.
- Cross-linking
  - Sample records link to occurrence records for insects and flowers via sample_id.
  - Geographic and temporal metadata align across files to enable integrative analyses.

## Coverage and scale (highlights)
- GB-wide network: 75 pan-trap squares across England, Scotland, and Wales.
- Yearly sampling activity (illustrative totals)
  - England, Scotland, and Wales together contributed to GB totals with varying counts per year due to field conditions and logistics.
  - GB totals (selected indicators): samples (6-hour pan-trap counts) numbered in the hundreds per year (e.g., 2017: 635; 2018: 731; 2019: 1180; 2020: 455); squares surveyed per year ranged broadly (e.g., 62–74 across years).
- Mean surveys per square varied by year and country, reflecting field realities (weather, access, volunteers).

## References and provenance
- Core design and testing references outlining the monitoring framework and PMRP integration:
  - Carvell et al. 2016; Carvell et al. 2020; PMRP progress and related reports.
- PoMS site for additional methodological detail and data pages: https://ukpoms.org.uk/

## Access, attribution, and funding
- Acknowledgements required for dataset use: PoMS collaboration, volunteer networks, and funders.
- Funded by Defra, Welsh Government, DAERA, JNCC, and UKCEH; UKCEH contribution funded by NERC award NE/R016429/1 as part of UK-SCAPE National Capability.
- Data citation: UK Pollinator Monitoring Scheme. 2022. Pan-trap survey data from the UK Pollinator Monitoring Scheme, 2017-2020 (version 2 metadata).

## Practical notes for data use
- This metadata supports data discovery, governance, and reuse by researchers and policy teams looking to analyze pollinator trends, habitat associations, and plant–pollinator interactions at a UK scale.
- When using the data, account for potential year-to-year and square-by-square gaps; apply aggregation rules for taxa not identifiable to species level; reference QA and taxonomic notes for identification caveats.
- Consider linking these data with Flower-Insect Timed Counts (FIT Count) data published separately for a more complete view of pollinator activity and plant–pollinator interactions.