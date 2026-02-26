# UK Pollinator Monitoring Scheme (PoMS) 1km square pan trap data from 2017-2021

- Purpose: A GIS-focused data product set to monitor UK insect pollinator populations using map-based data, enabling users to view and explore pollinator distributions and trends across the landscape.

## What this document covers

- Overview of PoMS and its mission to monitor pollinators across the UK, with emphasis on the 1 km square pan trap survey and associated floral data.
- Description of data access, licensing, and citation requirements (Open Government Licence; UK EIDC/NERC).
- Detailed description of the pan trap dataset (2017–2021), including sampling design, locations, protocols, attributes, QA, and data processing.
- Structure and contents of the three main data files (samples, flowers, insects) and how they are exported and compiled across years.
- Procedures for quality assurance, taxonomy standardisation, corrections, and cross-year collation.
- Annexes and references, including aggregate taxon groupings for taxa not identifiable to species level.

## Data scope and sampling design

- Geographic scope: 95 randomly selected 1 km squares across England, Scotland, Wales, and Northern Ireland (NI added from 2021; NI had a limited pilot in 2021).
- Sampling period and cadence: up to four visits per summer (May–August) per 1 km square; minimum two weeks between visits; some years had gaps due to land access, weather, volunteers, or COVID-19 (notably 2020).
- Pan trap methodology: water-filled bowls at five trap stations per square, with three bowls per station (colors: yellow/blue/white); traps active for 6 hours (09:00–17:00 BST) under specified weather conditions.
- Habitat stratification and site selection: 1 km squares stratified by agricultural vs semi-natural land cover using UKCEH Land Cover Map 2007; cores located to maximize representativeness while avoiding urban/coastal extremes.
- Data collection roles: PoMS volunteers and staff collect data; specimens are sorted in UKCEH labs with bees and hoverflies identified to species where possible; other taxa grouped to higher levels.

## Data contents and structure

- Data files provided (three main CSVs):
  - ukpoms_1kmPanTrapData_2017-2021_samples.csv: sample-level data for pan trap surveys, including location, date, trap details, weather, habitat, and processing metadata.
  - ukpoms_1kmPanTrapData_2017-2021_flowers.csv: floral occurrence data (forbs within 2 m of traps), with taxon details, floral units, and counts.
  - ukpoms_1kmPanTrapData_2017-2021_insects.csv: insect occurrence data (bees and hoverflies identified to species where possible; other groups aggregated), with taxon information, counts, sex, stage, and notes.
- Data content specifics include:
  - Sample-level attributes: sample_id, country, location_code/name, 1km square reference, grid location, habitat, date_from/date_to, weather variables, trap details, and QA-derived fields.
  - Insect occurrence attributes: occurrence_id, specimen_code, taxon_group, taxon_source, english_name, taxon_version_key, count, sex, stage, comment, order, family.
  - Floral occurrence attributes: occurrence_id, taxon_group (flowering plant), taxon_source, english_name, taxon_version_key, order, family, floral_unit, total_floral_units, year.
- Year-over-year collation: datasets for 2017–2021 are combined into 2021-ready forms; floral data edits 2017–2020 were applied for consistency with the 2017–2021 release.

## Data access, licensing, and citation

- Data access: Environmental Information Data Centre (EIDC), NERC, UK Centre for Ecology & Hydrology (UKCEH).
- Licence: Open Government Licence; users must cite the dataset when describing research that used PoMS data.
- Acknowledgement: PoMS partnership funded by UKCEH, Defra, Scottish/Welsh Governments, DAERA, and JNCC; volunteers acknowledged.

## Quality assurance and data processing

- Multi-stage QA workflow:
  - Online data entry standardized; photos of flowering plants reviewed for corrected identifications.
  - Bee/hoverfly identifications by taxonomic experts; cross-checks by a second/third taxonomist for difficult cases or out-of-range records since 2019.
  - Additional QA checks from 2021 using R scripts.
- Taxonomy and data transformations:
  - Insects: taxonomy standardised and aggregated; counts and sexes harmonised; checks to ensure unique occurrence/ specimen codes; corrections applied where needed.
  - Flora: floral unit counts corrected where necessary; plants that are not in flower or are Poaceae adjusted per methodology; 0/NA handling and outlier investigations performed with plots and summaries.
- Data integrity checks:
  - Uniqueness checks for sample IDs and bycatch/specimen codes; validation that each pan trap has a unique location/date/station combination; checks for duplicates and correct date/time formatting; validation of location references to 1 km grid squares.

## Collation across years and corrections

- Floral unit outliers (2017–2020) identified and corrected manually to align with standardized taxon expectations; corrections applied to the 4-year dataset.
- 2021 dataset combines 2017–2021 data, with standardised taxonomy and corrected floral units where needed.
- Inconsistent or missing data flagged, with files created to export problematic records for follow-up (e.g., PoMS_pan_sample_errors.csv, PoMS_pan_insect_errors.csv).

## Data export and delivery

- Post-QA export of data to align with EIDC dataset conventions:
  - pan_trap_samples: renamed and reformatted columns to match EIDC fields (country, 1km square, date, location codes, etc.), plus year and trap details.
  - species_flowers: taxon_source/taxon corrections applied; year, floral_unit, total_floral_units standardized for export.
  - species_insects: standardized taxonomy fields; year and identifiers adjusted; duplicates removed as needed.
- Final outputs (for 2017–2021) are provided as:
  - ukpoms_1kmPanTrapData_2017-2021_samples.csv
  - ukpoms_1kmPanTrapData_2017-2021_flowers.csv
  - ukpoms_1kmPanTrapData_2017-2021_insects.csv
- For broader integration, a four-year and annual aggregation workflow is described, including combining 2017–2020 data with 2021 data to create a cohesive 2017–2021 dataset.

## Data limitations and notes

- 2017: pilot year with limited data; 2020: data gaps due to COVID-19 constraints; NI data added from 2021 with a pilot year in NI.
- Some floral data corrections from 2017–2020 mean the 2017–2021 dataset is not identical to earlier published datasets for those years.
- Data were designed for single-operator, single-day sampling per square; some field constraints (land access, weather, volunteers) affect completeness per square/year.

## Acknowledgements, references, and annexes

- Acknowledges volunteers and partnering agencies; lists funders and institutional contributors.
- Annex: aggregates for taxa not distinguishable to species level, detailing standardised and aggregated taxon groupings for Hymenoptera, Diptera, and other groups to enable consistent analyses.

- References to foundational methodology and surveys (Carvell et al. 2016, 2020; PoMS/PMRP reports) and links to PoMS website for more information.