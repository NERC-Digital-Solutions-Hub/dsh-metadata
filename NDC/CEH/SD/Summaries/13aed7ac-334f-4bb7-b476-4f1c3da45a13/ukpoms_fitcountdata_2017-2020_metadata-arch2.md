# UK Pollinator Monitoring Scheme metadata: Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview
- Metadata for the Flower-Insect Timed Count (FIT Count) data from PoMS, covering 2017–2020 version 2 (duplicate rows from the previous version deduplicated).
- Data accessible via DOI: https://doi.org/10.5285/13aed7ac-334f-4bb7-b476-4f1c3da45a13.
- Open Government Licence; dataset must be cited in publications describing research using the data.
- Acknowledges funding and contributions from Defra, Welsh Government, Scottish Government, DAERA NI, JNCC, UKCEH (UKCEH funded by NERC under NE/R016429/1; UK-SCAPE programme).
- PoMS is a national-scale pollinator monitoring effort, engaging volunteers and aligning with national pollinator strategies.

## Data content and scope
- Two data files included:
  - ukpoms_1kmFITCountData_2017-2020.csv: FIT Counts from the 1 km square survey.
  - ukpoms_publicFITCountData_2017-2020.csv: Public FIT Counts submitted by citizen scientists.
- Timeframe: 2017–2020 (2017 was a pilot with sparse data).
- Geography: England, Scotland, Wales (1 km square data co-located with National Plant Monitoring Scheme squares; public data includes England, Isle of Man, Northern Ireland, Scotland, Wales).
- Data collected: location (1 km square or grid reference), environmental variables, and counts of insects by broad taxon groups visiting target flowers in a 50 cm × 50 cm quadrat over a 10-minute period.
- Survey design:
  - Public FIT Counts: volunteer-chosen locations/dates, 1 April–30 September; weather thresholds: ≥13°C with clear sky or ≥15°C with cloud.
  - 1 km square FIT Counts: up to 75 randomly allocated squares; four visits per summer (May–Aug), with some months skipped.
  - Habitat stratification uses CEH Land Cover Map 2007 (LCM) to categorize squares as agricultural (AG) or semi-natural (SN); additional habitat categories recorded.
- Relationship to other PoMS data: 1 km square survey also collects pan-trap data and environmental data (published separately).

## Methodology and data collection
- Part of the UK Pollinator Monitoring and Research Partnership (PMRP) to assess long-term pollinator population changes.
- FIT Count method:
  - Target flowers: 14 predefined types; participants may select alternatives if unavailable.
  - Counting period: ten minutes; insects counted in broad taxon groups visiting the target flower within the quadrat.
  - Data capture via iRecord (Indicia warehouse) with online forms to ensure consistency.
- Data processing:
  - 1 km square: geolocations checked to ensure counts link to the correct square; counts outside the 1 April–30 September window excluded; missing geolocations excluded.
  - 2017 data translated to 2018–2020 terminology for consistency; 2017 pilot data consolidated.
- Documentation directs users to PoMS for full methodology, target flowers, insect group definitions, and field recording forms.

## Data files and key attributes
- ukpoms_1kmFITCountData_2017-2020.csv (1 km square FIT Counts)
  - Core fields: sample_id, country, location_code, location_name, X1km_square, sample_projection, date, year, land_cover, habitat, target_flower (and corrected), target_flower_family, floral_unit_count, floral_unit, flower_cover, cloud_cover, sunshine, wind_speed, habitat_type, flower_structure, insect_group counts (bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other), all_insects_total, and related metadata (recorder_type, digitised_by, etc.).
  - Taxonomic corrections: target_flower_corrected, target_other_name_corrected, etc.
  - Habitat and context descriptors: habitat, habitat_other_detail, flower_context, count_start_time, etc.
- ukpoms_publicFITCountData_2017-2020.csv (Public FIT Counts)
  - Core fields: sample_id, country, date, year, X1km_square, sample_projection, digitised_by, recorder_type, habitat, target_flower (and corrected), target_flower_corrected, target_other_name, target_other_name_corrected, target_flower_family, flower_cover, floral_unit_count, floral_unit, flower_structur e, flower_context, count_start_time, cloud_cover, sunshine, wind_speed, habitat_type, bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other, all_insects_total, enjoyment, difficulty, and related metadata.
  - Additional fields compared to the 1 km file include measures of recorder experience and participant-reported enjoyment/difficulty.

## Quality assurance and data cleaning
- Data entry via iRecord with standardised formats; end-of-season QA checks by PoMS staff.
- Photo verification: target flower identification confirmed or corrected using submitted photos; floral unit counts cross-checked against correct target flowers; plant family lookups added.
- Data integrity checks for 1 km square data: grid-reference verification, correction of miscategorized counts (public vs 1 km data), exclusion of counts outside the season, and removal of records with missing geolocations.
- Metadata harmonisation across years to ensure comparability (e.g., retrospective translation of 2017 terms to 2018–2020 terms).

## Access, citation, and use
- Data use governed by Open Government Licence; citations required in publications describing research using the data.
- Suggested citation: UK Pollinator Monitoring Scheme (2022). Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2. NERC EDS Environmental Information Data Centre. (Dataset). https://doi.org/10.5285/13aed7ac-334f-4bb7-b476-4f1c3da45a13
- Acknowledgement requirements emphasize PoMS funding sources and volunteer contributors.

## References and provenance
- Foundational design and testing of the monitoring framework (Defra/partners) and PMRP establishment; progress reports and datasets related to PoMS are cited for methodological context and sampling design.
- Key references include Carvell et al. 2016/2020 and PMRP reports, with project details available through Defra and UKPOMS channels.

## Implications for environmental monitoring and analysis
- Provides standardized, quality-assured, geo-referenced pollinator visitation data across multiple UK nations for 2017–2020.
- Enables habitat-stratified analyses (AG vs SN) and integration with habitat and land-cover data (LCM 2007).
- Supports longitudinal assessments of pollinator communities and interactions with floral resources, useful for tracking environmental health and policy performance over time.
- Data structure supports cross-dataset integration, including potential linkage with pan-trap and plant-monitoring datasets under the PMRP umbrella.