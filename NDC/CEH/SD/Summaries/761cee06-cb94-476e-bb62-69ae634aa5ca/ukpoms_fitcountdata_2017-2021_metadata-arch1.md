# Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021

## Overview
- The UK Pollinator Monitoring Scheme (PoMS) tracks changes in insect pollinator populations across the UK.
- Two large-scale surveys: Flower-Insect Timed Count (FIT Count) and a 1 km square survey.
- Years covered: 2017–2021 (pilot year 2017; Covid-related gaps in 2020; Northern Ireland data limited in 2021).
- Data are contributed by volunteers and staff to inform national pollinator strategies; datasets are co-managed by UKCEH and JNCC with Defra and partners.

## Data access and citation
- Data are accessible via the Environmental Information Data Centre (EIDC), NERC.
- License: Open Government Licence.
- Citation: UK Pollinator Monitoring Scheme (2024). Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021. NERC EDS Environmental Information Data Centre.
- Acknowledgement required: PoMS partnership and volunteer network.

## The PoMS and surveys
- PoMS aims to establish how insect pollinator populations are changing across the UK; runs two large-scale surveys with volunteer support.
- Public FIT Counts: volunteers count insects visiting target flowers within a 50 cm × 50 cm quadrat for 10 minutes, weather permitting.
- 1 km square FIT Counts: similar method in up to 95 randomly allocated 1 km squares; also collects pan-trap data (published in a separate dataset).
- Sampling sites are stratified by landscape type using UKCEH Land Cover Map 2007; additional co-location with NPMS squares in England/Scotland/Wales; NI pilot included from 2021.

## Description of the FIT Count dataset
- Records include location (1 km resolution), environmental variables, and counts by broad insect groups for 2017–2021.
- 2017 is a pilot year with sparser data; 2020 data have gaps due to the pandemic; NI data in 2021 are limited.
- Public FIT Count: 10-minute count on flowering plants; weather thresholds: clear sky with at least 13°C or cloudy sky with at least 15°C.
- 1 km square FIT Counts: follow the public method; include up to 95 1 km squares; four visits per summer (May–August).

## Data quality assurance and processing
- Data entry via iRecord (2017–2020) and PoMS website (2021); stored in Indicia data warehouse.
- Post-season checks include photo verification of target flowers; optional insect group photos; data cleaned in R.
- Raw data extraction via SQL from Indicia; multiple data joins to assemble complete datasets; extensive quality checks and corrections described below.

## Data cleaning and corrections (key steps)
- Data are filtered to retain only FIT Count records; exclude non-FIT or training records; ensure counts are within the UK and within survey years.
- Data harmonisation across years, including standardising target flowers and taxon groupings.
- Floral corrections: adjust target flower identifications based on submitted photos; record changes in a corrections dataset.
- Floral unit corrections: adjust unit counts when units were misrecorded (e.g., Hawthorn units vs. umbels, or other mis-specifications); flag corrections for verification.
- Other floral information: add family and structure data for target flowers; manage “Other” target flowers through manual cross-year checks and updated reference datasets.
- Habitat data: translate 2017 terms to 2018–2021 equivalents; categorise habitats into four main classes (Agricultural, Garden, Semi-natural, Urban); manual checks for “Other” habitat details.
- Night counts: adjust times when counts appear to be night-time; remove dubious counts if not verifiable.
- Location validation: fix mistyped or out-of-square grid references; retain some counts if count location strays slightly from the requested 1 km square.
- Non-flowering plants: for non-flowering taxa (often grasses), set floral unit data to NA and standardise units.
- Unit count outliers: identify unusually high counts; apply conversion factors to correct unit counts; flag edited records.
- Checks and exports: combine checks into a single Plant_Check/Time_Check/ habitat/plant quality flag; export final cleaned datasets.

## Export and data structure
- Two primary export datasets (for PoMS trend analyses and EIDC):
  - ukpoms_publicFITCountData_2017-2021.csv
  - ukpoms_1kmFITCountData_2017-2021.csv
- Collation across years: harmonised four-year dataset to enable trend analyses and cross-year comparisons; 2017–2021 alignment of taxa names and floral units.
- Dataset description and file attributes describe the columns (sample_id, country, location, date, year, habitat, target_flower, floral_unit_count, floral_unit, insect groups, environmental covariates, etc.).

## Datasets and metadata details
- Public dataset fields include: sample_id, country, x1km_square, location_code/name, date, year, digitised_by, recorder_type, habitat, habitat_other_detail, target_flower, target_flower_corrected, target_other_name, target_other_name_corrected, target_flower_family, flower_structure, flower_cover, floral_unit_count, floral_unit, flower_context, count_start_time, cloud_cover, sunshine, wind_speed, insect groups, all_insects_total.
- 1 km dataset fields include similar structure with location_name_1km and location_code; additional habitat/land_cover and pan-trap references where applicable.
- The datasets are designed for trend analysis and are discoverable via the PoMS/UKCEH data portals.

## Collation and trend reporting
- After year-by-year processing, data are appended to form a four-year public and a four-year 1 km dataset.
- Summary metrics describe the number of recorders, counts submitted, and squares covered across 2017–2021:
  - Recorders (public and 1 km combined): ~1,066 total; year-by-year increases, with peaks in 2021.
  - FIT Counts submitted to PoMS: ~8,400 total across 2017–2021.
  - 1 km squares with counts: ~1,765 total across 2017–2021.
  - Public vs. 1 km square contributions: substantial public participation; 1 km square data supplement.
- The procedures ensure consistent cross-year comparisons by standardising taxa names, units, and habitat/flower metadata.

## Dataset usage for analysts
- Provides a rich, geo-referenced, temporally resolved dataset linking pollinator counts to target flowers, habitats, and environmental conditions.
- Facilitates correlations between insect groups and floral resources, habitat types, and weather variables.
- Supports predictive modeling of pollinator activity and the impact of habitat or climate variables on counts.
- Enables data provenance tracking: documented quality checks, corrections, and versioned exports.

## References
- Carvell et al. (2020, 2016) on pollinator monitoring frameworks and PMRP progress; foundational methodology for PoMS.
- PoMS reports and integration with NPMS and Defra-led initiatives.