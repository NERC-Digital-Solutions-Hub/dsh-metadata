# UK Pollinator Monitoring Scheme metadata: Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview
- Metadata for version 2 of the Flower-insect Timed Count (FIT Count) dataset collected under the UK Pollinator Monitoring Scheme (PoMS) for 2017–2020 (2017 is a pilot year).
- PoMS aims to monitor pollinator populations across the UK, leveraging volunteer participation and linking to national pollinator strategies.
- PoMS comprises two large-scale surveys: public FIT Counts and the 1 km square FIT Counts; a pan-trap dataset is published separately.

## Data scope and content
- Timeframe: 2017–2020 (2017 with limited data; 2018–2020 more complete).
- Data types:
  - Public FIT Counts: counts at user-chosen locations/dates (1 April–30 September).
  - 1 km square FIT Counts: counts in up to 75 randomly allocated 1 km squares during four visits per summer (May–August); co-located with PoMS pan-trap and National Plant Monitoring Scheme (NPMS) grids.
- Data include location (resolution 1 km; OSGB grid references for 1 km squares), environmental context, target flowers, and insect counts by group.
- Data underwent deduplication in version 2 (previous version contained duplicates).

## Data collection methodology
- Public FIT Count:
  - 50 cm × 50 cm quadrat, 10-minute count, recorded 1 April–30 September.
  - Weather thresholds: min 13°C with clear sky; 15°C with cloudy sky.
  - 14 target flower types; participants may substitute a different flower if needed.
- 1 km square FIT Count:
  - Similar method to public counts; conducted within selected 1 km squares.
  - Four visits per summer; timing typically May–August; some gaps possible.
- Habitat stratification:
  - Squares classified by dominant land cover (CEH Land Cover Map 2007) into agricultural (AG) or semi-natural (SN).
  - Other habitat categories provided; a small number of urban/coastal squares excluded.

## Habitat and sampling design
- Spatial design:
  - GB 1 km squares aligned with NPMS framework; 1 km squares co-located with pan-trap sampling in England/Scotland/Wales; separate coverage in some areas.
- Stratification:
  - Strata defined by habitat composition; AG vs SN designation based on >50% coverage in key land-cover classes.
- Data context:
  - For 1 km squares, habitat and broader context captured to support analyses of pollinator changes in cropped vs non-cropped landscapes.

## Quality assurance and data curation
- Data entry via online forms (iRecord/Indicia) with post-season QA.
- QA steps include:
  - Photo verification for target flowers; corrections applied if identifications are revised.
  - Taxonomic corrections to target flowers using lookup tables for family names.
  - Validation of 1 km square geolocations; ensuring counts link to correct squares.
  - Exclusion of counts outside recording period or with missing geolocation.
- Guidance and documentation available on the PoMS website for field methods, target flowers, and insect groups.

## Data files and attributes
- Data files:
  - ukpoms_1kmFITCountData_2017-2020.csv (1 km square FIT Counts)
  - ukpoms_publicFITCountData_2017-2020.csv (Public FIT Counts)
- Key attributes (selected examples):
  - sample_id, country, location_code, location_name, X1km_square, sample_projection, date, year
  - habitat, habitat_other_detail, target_flower and corrected variants, target_flower_family
  - flora-related: flower_cover, floral_unit_count, floral_unit, flower_context
  - counts by insect groups (bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other, all_insects_total)
  - weather/context: count_start_time, cloud_cover, sunshine, wind_speed
  - habitat_type, flower_structure, etc.
- Notes on data harmonisation:
  - 2017 data categories harmonised to align with 2018–2020 term sets for consistent analysis.
  - Some Northern Ireland data include NA or corrected columns to reflect local recording variations.

## Access, licensing, and citation
- Data access: https://doi.org/10.5285/13aed7ac-334f-4bb7-b476-4f1c3da45a13
- License: Open Government Licence; attribution required in publications describing research using the data.
- Citation: UK Pollinator Monitoring Scheme (2022). Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2. NERC EDS Environmental Information Data Centre. (Dataset).
- Acknowledgement: PoMS funded by Defra, Welsh Government, Scottish Government, DAERA (NI), JNCC, UKCEH; volunteers acknowledged.
- Related information: PoMS is part of PMRP; methodology and additional datasets described on PoMS/PMRP publications and websites.

## Usage notes and context
- Methodology and interpretations are supported by PoMS guidance; primary users are researchers and analysts seeking to understand pollinator trends and habitat associations.
- Data are designed to enable analyses of pollinator abundance and diversity in relation to habitat type (AG vs SN), target flowers, and environmental conditions.
- The dataset is complemented by additional PoMS datasets (e.g., pan-trap data and 1 km square data in separate files) and linked to the NPMS framework for broader ecosystem monitoring.