# UK Pollinator Monitoring Scheme metadata: pan-trap survey data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview
- Metadata for version 2 of the pan-trap dataset from PoMS, covering 2017–2020 (pilot year 2017 with reduced data).
- PoMS aims to monitor insect pollinator populations across the UK and to support national pollinator strategies.
- Data provided as three CSV files: samples, insect occurrences, and flowers occurrences; designed for compatibility with standardised data workflows and portals.

## What the dataset contains
- Samples data: information at the pan-trap sampling level for 75 randomly selected 1 km squares across England, Scotland, and Wales.
- Insects data: occurrence-level data for bees and hoverflies identified to species where possible; includes taxon grouping/aggregation for non-distinguishable taxa.
- Flowers data: herbaceous flowering plant counts within 2 m of each pan-trap station.
- Data cover: 2017–2020, with 2017 being a pilot year and varying square/visit coverage by year and country.

## Study design and sampling framework
- Network: 75 randomly allocated 1 km squares across GB, spanning agricultural and semi-natural landscapes.
- Habitat stratification: all GB squares mapped to habitat categories using CEH Land Cover Map 2007; squares classified as agricultural or semi-natural based on land cover.
- Site layout: within each square, five pan-trap stations along a diagonal with minimum 100 m spacing; traps open during a 6-hour window (09:00–17:00 BST) on suitable weather days.
- Sampling schedule: up to 75 squares, four visits per summer (May–August), with at least two weeks between visits; some gaps due to access, weather, volunteers, or COVID-19 in 2020.
- Protocols: standardised, volunteer-friendly pan-trap method using three coloured bowls per station; traps placed in open, minimally disturbed areas; bees and hoverflies identified to species by specialists; other groups grouped as needed.

## Data collection and processing workflow
- Data entry: collected by PoMS staff and volunteers via iRecord/Indicia data warehouse; three-stage entry (sampling/environmental data, insect counts, taxonomic identifications).
- Laboratory work: insects sorted and counted; bees/hoverflies identified to species by taxonomists; cross-checks performed when necessary.
- QA checks: photo verification of flowering plants near traps; taxonomic cross-checks for difficult or range-outliers; random and targeted QA checks in 2019–2020.
- Taxonomic aggregation: where species-level ID is not possible, specimens are aggregated into defined species groups; original identifications retained for reference.

## Data files and attributes
- ukpoms_1kmPanTrapData_2017-2020_samples.csv
  - sample_id, country, location_code, location_name, X1km_square, sample_projection, land_cover, date, year, digitised_by, pan_trap_station, trap_active_from, trap_active_to, trap_disturbed, temperature_start, temperature_end, cloud_cover_start, cloud_cover_end, wind_speed_start, wind_speed_end, exposure_sun, cast_shadow, vegetation_height_average, habitat_main, habitat_other, moved, sample_code_bycatch, wasps_solitary, wasps_social, wasps_parasitic, sawflies, flies, moths, butterflies, beetles_pollen, beetles_other, insects_small, insects_other, spiders, all_invertebrates_excluding_bees_hoverflies, bees, hoverflies, all_invertebrates_including_bees_hoverflies
- ukpoms_1kmPanTrapData_2017-2020_insects.csv
  - sample_id, country, location_code, location_name, X1km_square, date, year, pan_trap_station, occurrence_id, specimen_code, taxon_group, taxon_source, English_name, source_taxon_version_key, taxon_standardised, taxon_aggregated, count, sex, stage, comment, Order, Family
- ukpoms_1kmPanTrapData_2017-2020_flowers.csv
  - sample_id, country, location_code, location_name, X1km_square, date, year, pan_trap_station, occurrence_id, taxon_group, taxon_source, English_name, source_taxon_version_key, Order, Family, floral_unit, total_floral_units
- Linkage: all occurrence records link to their corresponding sample via sample_id; datasets are designed to be used together for analyses of pollinator abundance, species richness, and plant-pollinator relationships.

## Quality assurance and data integrity
- Data entry via standardized online forms with QA steps to ensure consistency.
- Bees and hoverflies identified by taxonomic experts; double-checks conducted for difficult or out-of-range records (2019–2020).
- Aggregation rules documented in Annex to enable consistent analysis across data with identifications not possible to species level.
- Version 2 addresses and corrects summed totals that were incorrect in version 1.

## Coverage, context, and caveats
- Geographic coverage: England, Scotland, and Wales; GB totals reported by country and across GB.
- Yearly sampling intensity varies by country and year; not all squares were sampled every year, and some visits were missed due to weather, access, or COVID restrictions in 2020.
- Pilot year 2017 had fewer data than later years; 2018–2020 progressively expanded sampling.

## Access, provenance, and references
- Part of the UK Pollinator Monitoring Scheme (PoMS) within the Pollinator Monitoring and Research Partnership (PMRP).
- Funded by Defra, Welsh Government, DAERA, JNCC, UKCEH; UKCEH funded under NERC award NE/R016429/1 as part of UK-SCAPE.
- Acknowledges volunteers and partner organisations; dataset complements the PoMS FIT Count and 1 km square surveys.
- References include Carvell et al. (2016, 2020) and PMRP progress reports; dataset description and methods are linked to the PoMS website.

## Practical notes for analysts
- This dataset provides a standardised, quality-assured framework for monitoring pollinator abundance and composition across the UK, suitable for temporal trend analyses and policy evaluation.
- The data are designed to be combined with other PoMS datasets (e.g., FIT Count, 1 km square survey) for broader ecological inferences.
- Users should consult Annex on aggregate taxon groupings to interpret species-level vs. aggregated data; be mindful of year-to-year and country-level sampling variation.