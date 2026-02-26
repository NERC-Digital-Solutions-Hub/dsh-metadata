# UK Pollinator Monitoring Scheme metadata: pan-trap survey data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview
- Metadata for the UK Pollinator Monitoring Scheme (PoMS) pan-trap data collected during 2017–2020 (version 2; previous version withdrawn due to incorrect totals).
- PoMS aims to monitor pollinator populations across the UK, supporting national pollinator strategies.
- The dataset includes pan-trap samples and occurrences of insects (bees and hoverflies prioritized to species level when possible) and flowering plants within 2 m of each trap.
- Data are collected by volunteers and staff, with taxonomic identifications validated by specialists; aggregate taxonomic groupings are used where species-level IDs are not possible.

## Data files and structure
- ukpoms_1kmPanTrapData_2017-2020_samples.csv
  - Sample-level data: sample_id, country, location_code/name, 1 km square, land_cover, date/year, trap_station, trap_times, weather-related variables, habitat codes, vegetation, and counts by taxon groups (insects) and by trap.
- ukpoms_1kmPanTrapData_2017-2020_insects.csv
  - Occurrence-level data for bees and hoverflies: sample_id, country, location, date/year, pan_trap_station, occurrence_id, taxon_group, taxon_source, English_name, taxon_version_key, taxon_standardised/aggregated, count, sex, stage, and notes.
- ukpoms_1kmPanTrapData_2017-2020_flowers.csv
  - Occurrence-level data for forbs (flowering plants) within 2 m of traps: sample_id, country, location, date/year, pan_trap_station, occurrence_id, taxon_group (flowering plant), taxon_source, English_name, Order, Family, floral_unit, total_floral_units, and related metadata.

## Sampling design and protocol
- Geography and sampling framework
  - 75 randomly allocated 1 km squares across England, Scotland, and Wales; sampled with a mix of agricultural and semi-natural landscapes.
  - Squares stratified by country land area; habitat context derived from CEH Land Cover Map 2007 (LCM) to classify as agricultural or semi-natural.
  - Within each square, five pan-trap sampling stations placed along a diagonal with approximately 100 m spacing.
- Sampling schedule and method
  - Up to 75 squares sampled over four visits per summer (May–August); minimum two-week gap between visits to the same square.
  - Pan traps: three colored bowls per station (yellow, blue, white) filled with water and a drop of detergent; traps deployed for 6 hours (09:00–17:00 BST).
  - Weather constraints: minimum temperatures (13°C if clear; 15°C if cloudy) and wind speed ≤ Beaufort 5; weather exposure and shading recorded.
  - Traps set in open, accessible locations, avoiding heavy shade, livestock enclosures, and disruptive areas; adjustments guided by field conditions.
- Data collection and processing
  - Insects sorted in UKCEH laboratories; bees and hoverflies identified to species by taxonomic experts; other insects grouped to standard taxon levels.
  - Flower data collected via photos and field notes, with floral units counted within 2 m of traps.
  - Data entered into iRecord/Indicia; multi-stage QA checks including cross-checks by multiple taxonomists and verification against known distributions where applicable.

## Taxonomy, aggregation, and quality assurance
- Aggregation for non-distinguishable taxa
  - Annex provides detailed aggregation rules (standardised and aggregated taxa) to ensure consistent analysis when species-level IDs are not possible (e.g., various Bombus and Sphaerophoria groupings).
  - Original source-level identifications retained for reference.
- QA procedures
  - Photos of flowering plants and insect specimens reviewed; identifications cross-checked by multiple taxonomists.
  - 2019 and 2020 QA included targeted checks for difficult or out-of-range identifications; some determinations updated accordingly.
  - Data quality checks include ensuring trap counts, habitat classifications, and taxonomic groupings align across years.
- Data scope and limitations
  - 2017 is a pilot year with fewer data; not all squares have complete four visits every year.
  - 2020 sampling reduced due to COVID-19 restrictions; overall data completeness varies by country and year.
  - Some years and squares have incomplete sampling; GB totals and year-by-year sampling details are described in Carvell & PMRP (2020).

## Temporal coverage and usage notes
- Temporal coverage: 2017–2020 (pan-trap data, full dataset version 2).
- Users should account for incomplete year-to-year coverage and year-specific sampling intensity when analyzing trends.
- Data are designed to support analyses of pollinator abundance, habitat associations, and temporal trends, with links to environmental data via the 1 km square framework.

## Access, references, and acknowledgements
- Data are part of the UK Pollinator Monitoring Scheme (PoMS) and PMRP; funded by Defra, Welsh Government, DAERA, JNCC, and UKCEH (NERC funding for UKCEH contribution).
- Acknowledges volunteers and research partners; references include Carvell et al. (2016, 2020) and PoMS/PMRP progress reports.
- Primary portal for additional details: PoMS 1 km square survey page (ukpoms.org.uk).