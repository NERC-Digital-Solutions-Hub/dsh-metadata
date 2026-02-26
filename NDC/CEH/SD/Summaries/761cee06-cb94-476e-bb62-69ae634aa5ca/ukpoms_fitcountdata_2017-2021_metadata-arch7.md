# Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021

## Overview
- UK Pollinator Monitoring Scheme (PoMS) produces national-scale, map-enabled data on insect pollinators to support policy and public engagement.
- This document describes the Flower-Insect Timed Count (FIT Count) dataset for 2017–2021, including data collection, QA, collation across years, and data attributes.
- Data are hosted by the Environmental Information Data Centre (EIDC) under the Open Government Licence.

## Datasets Included and Scope
- FIT Count data from two PoMS surveys:
  - Public FIT Counts: counts of insects visiting a target flower within a 50 cm x 50 cm quadrat for 10 minutes, submitted by volunteers (April 1 – September 30 each year; weather thresholds applied).
  - 1 km square FIT Counts: similar methodology in up to 95 randomly allocated 1 km squares; four visits per summer (May–August), co-located with PoMS pan-trap surveys (public 2017–2021; 2021 NI pilot data limited).
- Years covered: 2017–2021 (note: 2017 was a pilot year with less data; 2020 had covid-related gaps; NI data limited in 2021).
- Additional context: data are used with other PoMS datasets (e.g., pan traps) and national habitat/land-cover stratification (LCM 2007).

## Spatial and Temporal Coverage
- Spatial:
  - 1 km square grid references (grid_1km) and location information for each count.
  - Location references include location_code, location_name_1km, and location_square (centroid in grid reference system).
  - Habitat classification and land-cover context mapped to squares; sampling stratified by habitat types (AG = agricultural, SN = semi-natural).
- Temporal:
  - Counts occur annually within the growing season (April–September), with specific visit months per survey type.
  - Data include date_start/date_from and year extracted from counts.

## Data Collection Methods (GIS-friendly context)
- Public FIT Counts:
  - Volunteers choose locations and dates with weather conditions (min temps: 13°C if clear sky, 15°C if cloudy).
  - Target flowers (14 suggested) or user-provided flowers; quadrat 50 cm x 50 cm; 10-minute observation; insect groups tallied.
- 1 km Square FIT Counts:
  - Similar methodology to public counts, performed in up to 95 randomly allocated squares; four visits per year (May–August).
  - Co-located with pan-trap surveys; data also linked to National Plant Monitoring Scheme (NPMS) squares where applicable.
- Spatial data for mapping:
  - Sample projections include OSGB36 (27700) and WGS84 (4326); original precision tracked.
  - Location-specific attributes (land_cover, habitat_type, etc.) appended for GIS analyses.

## Data Quality Assurance and Cleaning
- Data entry via iRecord (2017–2020) and PoMS website (2021); checks implemented in R.
- Photo verification:
  - Target flowers identified from photos; corrected names updated if misidentifications found.
- Data cleaning steps:
  - Removal of counts not following FIT Count methodology; initial filtering excludes night-time or non-standard counts.
  - Cross-year collation fixes: floral data edits in 2017–2020; standardization of flower names and units.
  - Floral corrections and unit corrections:
    - Correct floral_unit_count conversions (e.g., grasses treated with NA for units).
    - Target_flower corrections and target_other_name corrections.
  - Habitat, plant family/structure, and habitat_detail corrections to ensure consistency across years.
  - Night counts resolved by adjusting times or removing ambiguous entries.
  - Duplicate sample IDs flagged and reconciled.
- Data export:
  - Public FIT Counts: ukpoms_publicFITCountData_2017-2021.csv
  - 1 km FIT Counts: ukpoms_1kmFITCountData_2017-2021.csv
  - Datasets prepared for trend analyses and EIDC publication.

## Data Structure and Key Attributes (GIS-relevant)
- Core columns (examples):
  - sample_id, country, location_code, location_name_1km, location_square
  - grid_1km (1 km square reference), sample_projection, public_spatial_ref, entered_spatial_ref
  - date_from, date_to, year, habitat, habitat_type, habitat_other_detail
  - target_flower, target_flower_corrected, target_flower_family, target_other_name, target_other_name_corrected
  - flower_structure, flower_cover, floral_unit_count, floral_unit, flower_context
  - counts for insect groups (bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other, all_insects_total)
  - cloud_cover, sunshine, wind_speed, count_start_time
- GIS outputs and ready-for-map formats:
  - 1 km square geometries linked to habitat and land-cover classifications
  - Public and 1 km datasets with consistent fields for map layers
  - Exported datasets designed for trend analysis and public data portals

## Data Access, Citation, and Usage
- Data access: Environmental Information Data Centre (EIDC), NERC EDS, hosted by UKCEH.
- Licence: Open Government Licence. Data must be cited in publications describing research using the data.
- Citation example:
  UK Pollinator Monitoring Scheme (2024). Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021. NERC EDS Environmental Information Data Centre.
- Acknowledgement: PoMS partnership (UKCEH, JNCC, Defra and devolved administrations); volunteers acknowledged.

## Data Processing and Collation Across Years
- Raw data extraction and cleaning performed per year, then combined across years.
- Effort and metadata checks include:
  - Counting recorder activity (Indicia/recorders) and yearly totals
  - Collation of 4-year datasets to assess trend consistency
  - Standardization of flower names, habitat categories, and floral units
- Flora-related corrections and habitat harmonization applied to ensure cross-year comparability.
- Final exports enable longitudinal analysis and cross-year GIS interpretation.

## Limitations and Known Issues
- 2017 pilot has lower data density; 2020 COVID-19 constraints reduced data in some years.
- Northern Ireland data limited to a 2021 pilot in NI; 1 km sampling patterns may differ by country.
- Some counts may be outside designated 1 km squares or have minor spatial misalignments; corrections implemented where identifiable, but some residual uncertainty remains.
- Data derive from volunteer-based observations; variability in effort and reporting may affect fine-grained spatial analyses.

## How This Supports GIS Specialists
- Provides standardized, map-ready FIT Count data across the UK for visualization and spatial analysis.
- Rich spatial metadata: 1 km squares, centroids, land-cover, habitat_type, and plant-insect interaction data.
- Consistent taxonomic and habitat corrections across years improves comparability for choropleth and hotspot analyses.
- Clear data provenance and licensing facilitate integration into GIS workflows and public-facing map portals.

## References
- Carvell, C. et al. (2016, 2020). Design and testing of a national pollinator monitoring framework; PMRP progress reports. Defra/Scottish/ Welsh Government/JNCC guidance and datasets.
- UK Pollinator Monitoring Scheme (PoMS) project pages and PoMS FIT Count methodology documentation.