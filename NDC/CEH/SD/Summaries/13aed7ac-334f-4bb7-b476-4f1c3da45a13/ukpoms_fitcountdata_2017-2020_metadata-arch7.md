# UK Pollinator Monitoring Scheme metadata: Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview
- Metadata and description for version 2 of the Flower-insect Timed Count (FIT Count) dataset from PoMS (2017–2020; 2017 pilot year).
- Datasets support map-based data products and GIS analyses of pollinator activity across the UK.
- Includes both 1 km square FIT Counts and Public FIT Counts, with data quality checks and harmonised terminology across years.

## What the dataset covers
- Two data files:
  - ukpoms_1kmFITCountData_2017-2020.csv (FIT Counts in 1 km squares)
  - ukpoms_publicFITCountData_2017-2020.csv (Public FIT Counts)
- Time period: 2017–2020 (2017 is a pilot year with sparser data; 2018–2020 more complete)
- Spatial scope:
  - 1 km square FIT Counts: up to 75 randomly allocated 1 km squares in England, Scotland, Wales; co-located with pan-trap data and National Plant Monitoring Scheme squares in most cases.
  - Public FIT Counts: locations chosen by participants; 1 May–30 September weather-permitting counts in 50 cm × 50 cm quadrats.

## Spatial design and sampling
- Location data includes:
  - country, location_code, location_name
  - X1km_square (grid reference) with OSGB projection
  - sample_projection (grid reference system used)
  - land_cover: predominant land-cover in the 1 km square (agricultural vs semi-natural) based on CEH Land Cover Map 2007
  - habitat_type (semi-natural, agricultural, garden, urban)
  - habitat_other_detail for “Other” descriptions
- Habitat stratification and sampling logic:
  - Squares classified as agricultural (AG) or semi-natural (SN) based on >50% coverage in specific LC classes
  - Excluded squares: highly urbanised/coastal with large sea share
  - Aims to explore habitat- and cropped/non-cropped landscape effects on pollinator changes

## Data collection and methodology
- Public FIT Counts:
  - Conducted at dates/locations chosen by participants between 1 April and 30 September
  - Weather thresholds:
    - Clear sky: minimum 13°C
    - Cloudy sky: minimum 15°C
  - Target flowers: 14 types (participants may use others)
  - Quadrat: 50 cm × 50 cm; 10-minute count
- 1 km square FIT Counts:
  - Similar methodology to Public counts from 2018 onward
  - Four visits per summer (May–Aug), aiming for one visit per month
  - Data aligned with PoMS pan-trap and 1 km square survey framework
- Co-location:
  - 1 km squares co-located with NPMS squares in England/Scotland; Wales co-located with a wider 1 km pool
  - Habitat and land-cover mapping linked to LC Map 2007 to support stratified analyses

## Data attributes and structure
- Data file: ukpoms_1kmFITCountData_2017-2020.csv
  - sample_id, country, location_code, location_name, X1km_square, sample_projection, year, date, habitat, habitat_type, target_flower, target_flower_family, flower_cover, floral_unit_count, floral_unit, flower_context, count_start_time, cloud_cover, sunshine, wind_speed, bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other, all_insects_total, and additional corrected fields (target_flower_corrected, target_other_name_corrected, etc.)
  - Includes QA fields and corrected identifications after photo review
- Data file: ukpoms_publicFITCountData_2017-2020.csv
  - sample_id, country, X1km_square, date, year, sample_projection, digitised_by, recorder_type, habitat, habitat_other_detail, target_flower, target_flower_corrected, target_other_name, target_other_name_corrected, target_flower_family, flower_cover, floral_unit_count, floral_unit, flower_context, count_start_time, cloud_cover, sunshine, wind_speed, enjoyment, difficulty, habitat_type, flower_structure, bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other, all_insects_total, and additional corrected fields
- Common insect groups tracked: bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other, with totals

## Data quality assurance and processing
- Data entry via online forms (iRecord/Indicia) with standardised formats
- Post-season QA by PoMS staff:
  - Photo verification for target_flower and corrections if identifications were updated
  - Floral units and target flowers checked against correct targets
  - Plant family names appended from lookups
  - 1 km square geolocations validated to be within linked square
  - Transferred data where 2017 public entries were misfiled into 1 km square datasets
  - Exclusion of counts outside recording period or with missing geolocations
- Documentation links and guidance on methodology available on PoMS website

## Data access, rights, and citations
- Data is accessible under Open Government Licence
- Required: cite UK Pollinator Monitoring Scheme (PoMS) 2022 dataset in any publications
- Acknowledgement required for use:
  - PoMS funded by Defra, Welsh Government, Scottish Government, DAERA, JNCC, UKCEH (NERC funding)
  - Special thanks to volunteers and listed partner organisations
- DOIs and project reports provided for further documentation and methodology

## Relevance for GIS-based data products
- Rich spatial context for mapping pollinator activity at 1 km scales and targeted 50 cm × 50 cm plots
- Compatible with habitat mapping and land-cover layers (LCM 2007) for stratified GIS analyses
- Enables landscape-level assessments across England, Scotland, and Wales, with cross-year harmonisation and corrected identifications
- Supports integration with other PoMS datasets (e.g., pan-trap, NPMS) for comprehensive pollinator monitoring visualisations and policy-relevant outputs