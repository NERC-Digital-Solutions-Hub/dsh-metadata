# UK Pollinator Monitoring Scheme metadata: pan-trap survey data from the UK Pollinator Monitoring Scheme, 2017-2020.

## Overview
- Metadata for version 2 of the Pan-trap survey dataset (UK Pollinator Monitoring Scheme, PoMS) covering 2017–2020.
- 2017 was a pilot year; version 2 corrects incorrect summed totals from the previous version.
- Dataset documents samples and occurrences of insects and flowers from the PoMS 1 km square pan-trap survey.
- PoMS is part of PMRP and aims to monitor UK pollinator populations and inform national pollinator strategies.

## Copyright, acknowledgement and funding
- © multiple organisations (listed in the document).
- Required acknowledgement: PoMS is funded by Defra, devolved administrations, JNCC, and UKCEH, with UKCEH funding from NERC for the PMRP component.
- Acknowledges volunteers for surveys and data contributions.

## PoMS background and context
- PoMS is a partnership aimed at understanding changes in insect pollinator populations across the UK.
- Two main surveys:
  - The Flower-Insect Time Count (FIT Count) dataset (separate publication).
  - The 1 km square pan-trap survey (the dataset described here) plus associated environmental data; active in England, Scotland, and Wales during 2017–2020.
- Sampling designed to be volunteer-friendly and executable by non-experts; bees and hoverflies identified to species where possible.

## Survey design and site selection
- 75 randomly allocated 1 km squares across GB; stratified by agricultural vs semi-natural landscapes using CEH Land Cover Map 2007.
- Habitat stratification and site selection aim to detect pollinator trends over a 10-year period with adequate statistical power.
- 1 km squares are co-located with other biodiversity monitoring schemes (e.g., NPMS in England/Scotland; similar schemes in Wales).
- Spatial layout: within each square, a diagonal transect with five pan-trap stations spaced evenly and at least 100 m apart.
- Trap placement guidelines emphasize open, stable environments and minimal disturbance; avoid sampling in heavily shaded areas, enclosed livestock fields, or during known agricultural operations.

## Sampling protocol and data collection
- Four visits per summer (May–August), weather permitting; minimum two-week interval between visits for a given square.
- Pan traps: three bowls per station (one of each colour: yellow, blue, white), filled with water and a drop of dish soap to reduce surface tension.
- Traps left out 6 hours (09:00–17:00 BST); weather thresholds enforced at start and during collection (temperature, cloud cover, wind, sunshine/shade).
- Insects sorted at UKCEH laboratories; bees and hoverflies identified to species level where possible; other taxa grouped as appropriate.
- Data entry via iRecord/Indicia workflow; three-stage data entry and QA process (sampling data, counts by taxon per trap, species identifications).

## Data attributes and structure
- Data files (three CSVs) are linkable via sample_id:
  - ukpoms_1kmPanTrapData_2017-2020_samples.csv
    - Core sample-level attributes: country, location_code/name, 1 km square reference, land_cover, date/year, trap station, start/end times, weather metrics, habitat, movement, and counts by taxon groups.
  - ukpoms_1kmPanTrapData_2017-2020_insects.csv
    - Occurrence-level data for bees and hoverflies: sample_id, country, location, date, pan_trap_station, taxon_group, taxonomy fields (taxon_source, English_name, source_taxon_version_key, taxon_standardised, taxon_aggregated), count, sex, stage, and quality/notes.
  - ukpoms_1kmPanTrapData_2017-2020_flowers.csv
    - Occurrence-level data for flowering plants within 2 m of each trap: sample_id, country, location, date, pan_trap_station, taxon_group (flowering plant), taxonomy fields, floral_unit and total_floral_units.
- Taxonomic data includes both source identifications and standardized/aggregated groupings to support analysis across incomplete identifications.
- Notes on identification: some groups require male specimens for species-level IDs; aggregated taxa are used to maintain consistency where species-level IDs are not possible.

## Quality assurance and data integrity
- Data entered through standardized online forms; three-stage QA process:
  - Initial data entry by volunteers/staff.
  - Laboratory sorting and counting of specimens.
  - Taxonomic identifications by specialists; secondary checks for difficult or out-of-range records.
- Cross-checks conducted in 2019 and 2020 by additional taxonomists; a subset of occurrences re-checked.
- Photos of flowering plants QA-validated; floral units cross-checked against relevant taxon records.
- All source-level identifications retained; aggregated/standardised taxa provided for analysis.
- Specimens selected for QA based on random sampling, taxonomist requests, and potential outliers; changes to determinations documented (some reclassifications between years).

## Data completeness, availability and limitations
- 2017–2020 data cover 75 GB-scale sampling efforts across GB; not all squares sampled every year, and not all visits completed in every year.
- 2020 sampling constrained by COVID-19 restrictions.
- Tables in the document summarise counts of squares, visits, and pan-trap samples by country and year, illustrating variable effort and mean surveys per square.
- Data are subject to site access limitations, weather, and volunteer availability, which impacts completeness and comparability across years.

## Annex: Taxonomic aggregation guidance
- Provides mapping from recorded taxa to standardised and aggregated taxa for groups not distinguishable to species level.
- Examples include Bombus species complexes in Hymenoptera and various Diptera species complexes.
- Notes explain when species-level IDs rely on male specimens, or when certain genera require specific identifications; retains source-level identifications for reference.

## References and further information
- Cited methodological and progress reports from Carvell et al., PMRP/Defra, and PoMS project documentation.
- Additional information available via the PoMS website (one-km square survey page) and related PMRP reports.