# Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021

## Overview
- The UK Pollinator Monitoring Scheme (PoMS) is a partnership to monitor pollinator populations across the UK, producing large-scale datasets.
- The dataset described comprises Flower-Insect Timed Count (FIT Count) data from 2017–2021, including related 1 km square FIT Count data and pan-trap data published as a separate dataset.
- Data are hosted by the Environmental Information Data Centre (EIDC) within NERC Environmental Data Service and managed by UK Centre for Ecology & Hydrology (UKCEH).
- Access is under the Open Government Licence; users must cite PoMS data in publications and acknowledge PoMS and its funders/volunteers.

## Data scope and content
- Two main surveys:
  - Public FIT Count: counts insects landing on a target flower within a 50 cm × 50 cm quadrat during ten minutes, conducted by volunteers under flexible weather windows (April–September).
  - 1 km square FIT Counts: similar method, conducted in up to 95 randomly allocated 1 km squares across the UK with four visits per summer (May–Aug); co-located with PoMS pan-trap surveys and related environmental data.
- Geography and habitat:
  - Location data include 1 km resolution for FIT Counts and associated habitat classifications derived from the UKCEH Land Cover Map 2007 to stratify sampling by landscape type (AG and SN categories; includes urban and other land covers).
  - Northern Ireland data are present from a limited 2021 pilot; NI data are not uniformly complete across years.
- Data contents:
  - For each FIT Count: location, environmental variables, counts by insect taxon groups, date, and related metadata.
  - Datasets describe target flowers, floral units, counts per insect group, and contextual fields (e.g., weather, habitat, recorders).
- Data quality and curation:
  - After collection, data are quality checked (photos for target flowers, consistency checks) and cleaned using R; raw data are retrieved via SQL from Indicia/Indicia Warehouse, then harmonised for analysis and export.

## Data access, licensing and citation
- Data accessible via the Environmental Information Data Centre (EIDC), part of NERC EDS, hosted by UKCEH.
- License: Open Government Licence.
- Citation example: UK Pollinator Monitoring Scheme (2024). Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021. NERC EDS Environmental Information Data Centre.
- Acknowledgement requirements emphasize PoMS partnerships (UKCEH, JNCC, Defra and devolved governments) and volunteers.

## Data governance and provenance
- PoMS data are collected through citizen science, submitted via iRecord Indicia, and stored in Indicia data warehouses and PoMS websites.
- Data processing includes metadata capture (location, date, habitat, target flower, etc.), provenance tracking, and documentation of transformations and corrections.
- Cross-year collation is performed to enable trend analysis and consistent reporting.

## Data quality assurance and cleaning
- QA steps include:
  - Online data capture with standardized formats.
  - Photo verification of target flowers; optional photos of insect groups.
  - Post-season data cleaning with R; SQL data extraction and cleaning from Indicia.
  - Checks for duplicate sample IDs, appropriate date types, and ensuring counts fall within the FIT Count methodology.
  - Filtering out non-conforming counts (e.g., counts outside the season, night-time counts, counts misaligned with the 1 km square network).
  - Validation against 1 km spatial references and pan-trap data where applicable.
- Specific data cleaning activities include floral corrections, unit corrections for target flowers, habitat categorisation harmonisation, and non-flowering plant handling.

## Data processing and enhancements
- Floral corrections:
  - Target flower identifications and corrected targets based on submitted photos.
  - Corrections to target_other_name and corresponding family/structure data.
- Habitat information:
  - Habitat categories harmonised into four main classes (agricultural, semi-natural, garden, urban) with additional habitat details captured and later integrated.
- Floral unit handling:
  - Non-flowering plants treated by setting floral_unit_count and related fields to NA where appropriate.
  - Grasses standardised to remove unit-based inconsistencies.
- Unit count outliers:
  - Outlier floral unit counts identified and adjusted using conversion factors; some adjustments are applied at the sample_id level.
- Data integrity:
  - Consistent cross-year naming for target flowers; harmonisation of units and counts across years; checks to identify incomplete or inconsistent records.

## Datasets and export formats
- Public FIT Count data: ukpoms_publicFITCountData_2017-2021.csv
- 1 km FIT Count data: ukpoms_1kmFITCountData_2017-2021.csv
- Data fields (high-level):
  - sample_id, country, location_code, location_name, x1km_square, sample_projection, land_cover, date, year, digitised_by, recorder_type, habitat, habitat_other_detail, habitat_type, target_flower, target_flower_corrected, target_other_name, target_other_name_corrected, target_flower_family, flower_structure, flower_cover, floral_unit_count, floral_unit, flower_context, count_start_time, cloud_cover, sunshine, wind_speed, bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other, all_insects_total, etc.
- Export includes subsequent collation across years:
  - Public 4-year dataset (public counts 2017–2021)
  - 1 km 4-year dataset (1 km counts 2017–2021)
  - Combined outputs used for trend analyses and public data releases
- Additional metadata files cover file attributes, habitat transformations, and floral corrections workflows.

## Collation across years and versioning
- 4-year datasets are created by attaching 2017–2021 data and harmonising fields (target_flower names, floral units, etc.).
- Floral unit corrections and habitat categorizations are applied consistently across years to enable robust cross-year comparability.
- After manual checks, corrections are implemented and reflected in the 4-year public and 1 km datasets.

## Usage notes and limitations for data stewards
- Data come with caveats:
  - 2017 is a pilot year with fewer data; 2020 data have gaps due to Covid-19; NI data remain limited for 2021.
  - Data are collected via volunteer networks and may require ongoing QA to address misclassifications, non-standard units, or habitat descriptions.
  - Some counts may require reallocation to the correct survey type (public vs 1 km) based on timing and location.
- Ongoing governance needs:
  - Clear update workflows for annual revisions and cross-year harmonisation.
  - Documentation of all corrections for reproducibility and transparency.
  - Maintenance of licensing, attribution, and user guidance to ensure proper data use and citation.

## References
- Carvell, C., et al. (design and testing of pollinator monitoring frameworks; Defra/Scottish/Welsh Government guidance)
- PMRP and related UK pollinator monitoring reports
- PoMS project pages and methodology documentation (Fit Count guidance; habitat and floral data resources)