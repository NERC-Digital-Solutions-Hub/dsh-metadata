# Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021

## Overview
- The UK Pollinator Monitoring Scheme (PoMS) runs two large-scale surveys: Flower-Insect Timed Count (FIT Count) and the 1 km square survey, with data collection supported by volunteers.
- PoMS aims to monitor insect pollinator populations across the UK and provide evidence for national pollinator strategies, while engaging communities in data collection.
- This document describes the Flickr Count dataset (FIT Count) from 2017–2021, including data collection, cleaning, transformation, and product creation for exploration and analysis.

## Data Access and Citation
- Data are accessible from the Environmental Information Data Centre (EIDC), part of NERC Environmental Data Service, hosted by UKCEH.
- License: Open Government Licence. Users must cite: UK Pollinator Monitoring Scheme (2024). Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021. NERC EDS Environmental Information Data Centre.
- Acknowledgement required for PoMS partnership and volunteer contributors.

## Datasets Included
- Flower-Insect Timed Count (FIT Count) dataset (2017–2021), including location, environmental variables, and counts by insect groups.
- 1 km square FIT Count data (subset of 1 km squares with co-located pan-trap data; separate dataset for pan-trap data).
- Public FIT Count data (volunteer-driven, 50 cm x 50 cm quadrats; 10-minute counts; weather thresholds apply).
- Data were harmonised across years; 2017 contains pilot data; 2020 had COVID-related gaps; Northern Ireland data from 2021 pilot.
- Datasets were reformatted and merged for longitudinal analysis; 2017–2021 data are consolidated with subsequent year updates.

## Data Collection and Quality Assurance
- Data capture: FIT Counts submitted via the app or the PoMS/indicia websites; records entered into Indicia data warehouse; 2017–2020 via iRecord; 2021 via UK PoMS site.
- Quality assurance:
  - Visual verification of target flower identifications from photos; corrections applied when needed.
  - Data cleaned with R; raw data retrieved via SQL; various joins to assemble full datasets.
  - Spatial checks and habitat/land-cover mapping integrated (LCM 2007 used for habitat stratification).
- Data provenance and collaboration:
  - PoMS partnered with UKCEH, JNCC, Defra family partners; volunteers and staff contributions acknowledged.

## Data Cleaning and Corrections (Key Steps)
- Floral corrections:
  - Correct target flower identifications based on photo reviews; corrections stored and applied to the main dataset.
- Floral unit corrections:
  - Adjust floral unit counts when units were counted inconsistently (e.g., converting between units like flowers vs. heads, etc.); conversion logic stored and applied.
- Non-flowering plants:
  - For non-flowering plants, floral units may be set to NA or standardized; grasses standardized to non-flowering conventions.
- Target flower family and structure:
  - Added corrected family and structure information for main target flowers; manual checks for other target flowers with free-text names.
- Habitat information:
  - Habitat categories harmonized into four main groups (Agricultural, Garden, Semi-natural, Urban); new habitats added and codified; later manual checks for completeness.
- Night counts and date handling:
  - Adjustments to start times when counts appear to be recorded at night; counts outside daylight hours removed if not verifiable.
- Data integrity checks:
  - Duplicate sample IDs identified and flagged; 1 km square grid references checked for containment within the 1 km square network; date consistency checks; cross-checks for pan-trap alignment.

## Collation Across Years
- FIT Count data (public and 1 km) were combined with prior years to form a four-year dataset.
- Floral name standardisation and outlier detection were performed to harmonise across years.
- Floral unit corrections were reapplied where needed across the multi-year dataset.
- Exported final annual product files:
  - ukpoms_publicFITCountData_2017-2021.csv
  - ukpoms_1kmFITCountData_2017-2021.csv
- Datasets were merged to form a consistent public data product and a 1 km data product for cross-year analyses.

## Data Attributes and File Structure
- Core columns across datasets include:
  - sample_id, country, location_code, location_name, x1km_square, sample_projection, land_cover, date, year, digitised_by, recorder_type, habitat, habitat_other_detail, habitat_type, target_flower_corrected, target_other_name, target_other_name_corrected, target_flower_family, flower_structure, flower_cover, floral_unit_count, floral_unit, flower_context, count_start_time, cloud_cover, sunshine, wind_speed, bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other, all_insects_total, etc.
- The dataset includes both public (non-1km) FIT Counts and 1 km FIT Counts, with harmonised fields for cross-year analysis.
- Dataset description and file attributes provide guidance on column meanings, measurement units, and the provenance of each field.

## Outputs and Usage
- The cleaned, harmonised FIT Count data support trend analysis and national pollinator monitoring under PoMS.
- The public data product is suitable for public-facing dashboards and analyses; the 1 km dataset supports broader ecological analyses with co-located pan-trap data in a separate dataset.
- Outputs are formatted for export and reuse in analysis pipelines, with explicit guidance on date handling, habitat classification, and floral corrections.

## Acknowledgements and References
- PoMS acknowledges volunteers, UKCEH, Defra and partner governments, and JNCC for funding and support.
- References include Carvell et al. (multiple works) on design, monitoring framework, and PMRP collaborations.