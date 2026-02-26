# UK Pollinator Monitoring Scheme (PoMS) 1km Square Pan Trap Data from 2017-2021

- Purpose and scope
  - PoMS aims to monitor insect pollinator populations across the UK using a standardized 1 km square pan-trap survey, with volunteers and staff contributing data.
  - The dataset covers four main components: sample-level data, insect occurrences, and floral occurrences within 2 m of pan-trap stations.
  - Years included: 2017–2021 (2017 as a pilot; 2020 with covid-related gaps; 2021 includes Northern Ireland data from a limited pilot).

- Data access, licensing, and attribution
  - Data are accessible via the Environmental Information Data Centre (EIDC), part of NERC/UKCEH.
  - Open Government Licence; dataset must be cited in publications.
  - Acknowledgement required for PoMS partnership and funders; credits to participating organisations and volunteers.

- Data structure and files
  - Three core data files (2017–2021 pan-trap data):
    - ukpoms_1kmPanTrapData_2017-2021_samples.csv (sample-level data)
    - ukpoms_1kmPanTrapData_2017-2021_flowers.csv (floral occurrences within 2 m of traps)
    - ukpoms_1kmPanTrapData_2017-2021_insects.csv (insect occurrences, including bees and hoverflies)
  - Each file links via sample_id; flowers use a 2 m radius around each trap station; insects are occurrence-level with specimen codes and taxonomic details.
  - Taxonomy handling and aggregation
    - Insects include taxon_group, taxon_source, taxon_standardised, taxon_aggregated, and other attributes.
    - Annex provides aggregate groupings for taxa not distinguishable to species level.
  - Data collation across years
    - 2017–2020 floral data were corrected/edited in the combined 2017–2021 dataset.
    - Outlier corrections for floral unit counts applied when combining 2017–2020 with 2021 data.
    - Final 5-year dataset combines flows from all years with standardized formats and corrected fields.

- Sampling design and protocol
  - 95 randomly allocated 1 km squares across England, Scotland, Wales, and Northern Ireland (NI added from 2021).
  - Stratified by land-use cover (agricultural vs semi-natural) using UKCEH Land Cover Map 2007.
  - Within each square: diagonal transect with five pan-trap stations; minimum 100 m between stations.
  - Traps deployed for four visits per summer (May–August) with a minimum two-week gap between visits for a square.
  - Pan traps: three colored bowls per station (black bowls with UV-reactive paint), filled with water and a drop of detergent; traps active for 6 hours (09:00–17:00 BST).
  - Weather thresholds for sampling: minimum temperatures and wind conditions to ensure good conditions.
  - Post-collection processing: insects sorted/identified at UKCEH; bees/hoverflies identified to species where possible; other taxa aggregated as appropriate.
  - Data submission and QA are integrated with Indicia/iRecord systems (2017–2020) and a PoMS-specific system (2021 onwards).

- Data quality assurance and corrections
  - Multi-stage QA: data entry consistency checks, cross-checks by taxonomists, and random sampling QA.
  - From 2019, sections of QA are performed by multiple taxonomists; second opinions are sought for difficult identifications; cross-checks extended to random samples.
  - Data cleaning and transformation implemented in R and SQL workflows; checks for unique specimen identifiers, bycatch IDs, and trap-level duplicates.
  - Corrections and standardization
    - Taxonomic standardisation and aggregation rules are stored and updated (TRANSFORM_insect_taxonomy files) to ensure consistency year-to-year.
    - Floral unit corrections: a standardized floral unit conversion process applied; Poaceae handling: floral_unit_count adjustments (and NA assignment for uncertain zero counts).
    - Distinct checks to prevent duplicate sample IDs, ensure correct trap_station assignments, and verify location-square consistency.
  - Export preparation
    - Final export maps PoMS data columns to the Environmental Information Data Centre (EIDC) schema for public release.

- Data attributes and content highlights
  - Sample data: includes sample_id, country, location_code/name, 1km square, grid reference, land cover, trap details, weather and habitat variables, and counts.
  - Insect data: occurrence-level records with sample_id, occurrence_id, specimen_code, taxon_group, taxon_source, english_name, taxon_version_key, counts, sex, stage, determination details, order, family.
  - Floral data: occurrence-level floral counts with taxon_group (flowering plant), taxon_source, english_name, taxon_version_key, order, family, floral_unit, total_floral_units, year.
  - Data coverage and gaps: not all squares were sampled every year; 2020 had reduced sampling due to Covid; 2021 NI sampling was limited to a pilot.

- Projects, collaboration, and governance
  - PoMS is a partnership supported by UKCEH and JNCC, with Defra and other governments contributing; volunteers are essential to data collection.
  - Data management and curation involve UKCEH Indicia warehouse, iRecord data entry, laboratory identifications, and cross-year taxonomy standardisation.

- Data access notes and cautions
  - The dataset is designed for use in policy, monitoring trends, and ecological analysis; some years show gaps due to external factors (weather, land access, volunteers, Covid-19).
  - Floral data corrections and taxonomic aggregation should be considered when performing cross-year analyses.
  - Annexed aggregation schemes should be consulted when working with taxa not identified to species level.

- How to use and cite
  - Access the three main data files via EIDC; cite the PoMS dataset with the 2024 UK Pollinator Monitoring Scheme publication details.
  - Acknowledge PoMS partnership and funding sources; credit volunteers who contributed data.