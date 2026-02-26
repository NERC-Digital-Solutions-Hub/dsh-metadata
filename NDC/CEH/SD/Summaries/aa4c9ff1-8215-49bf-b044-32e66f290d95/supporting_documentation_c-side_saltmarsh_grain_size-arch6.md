# Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Dataset describing grain size distributions from 459 soil samples collected across UK saltmarshes between 2018 and 2021.
- Part of the C-SIDE project funded by NERC (NE/R010846/1).
- Aimed at enabling comparability of granulometric data across similar environmental regions of the UK.

## Data resource and scope
- Location: United Kingdom; observations cover sites around the UK coastline to represent diverse saltmarsh habitats.
- Spatial coordinates provided in decimal degrees (WGS84) for site locations.
- Focus: grain size distribution ranging from 0.02244 to 2000 µm.

## Sampling and site details
- Sites chosen to be in similar environmental regions to allow comparability and broad UK representation.
- Data describe core samples from saltmarsh environments (saltmarsh cores).

## Methods and quality assurance
- Grain size analyses performed with a Malvern Laser Granulometer.
- Sample preparation: air-dried, broken up, sieved to remove large rootlets/stones, digested with H2O2 (30%), heated, and then analysed.
- Calibration: Malvern Laser Granulometer calibrated using standard 0.152–0.422 mm sand.
- QA: Laboratory equipment calibrated according to University of York practices; data checks reflect these quality controls.
- Statistical treatment: Not specified (NA) in this record.

## Data structure and formats
- Data resource file: C_SIDE_saltmarsh_grain_size.csv
- Core-level fields:
  - Core_ID (text)
  - Location (text)
  - Core_depth_cm (numeric): depth interval of sub-sample (cm)
  - Core_mid-depth_cm (numeric): mid-point depth (cm)
  - Grain_size_1 to Grain_size_100 (numeric): grain size distributions for 100 size classes
- Grain size classes: 100 discrete sizes from 0.02244 µm to 2000 µm (values listed in the dataset as Grain_Size(µm) equivalents)
- File format: CSV
- Data checks: Some fields may be NA (e.g., certain statistical treatments); explicit data quality notes indicate calibration and standard procedures were followed.

## Variables and measurement details
- Grain size distribution: 100 concentration values per core, corresponding to successive grain size classes (µm scale from ~0.02244 to ~2000).
- Core-related metadata: core identifier, location name (saltmarsh), and depth information (depth interval and mid-depth).

## Access, provenance, and usage
- Dataset is tied to the project data records for C-SIDE and is intended to support cross-site comparisons and integration with broader data products.
- Useful for researchers and data users aiming to analyze granulometry across UK saltmarshes, supporting carbon storage and sediment transport studies.
- Outputs can include summary statistics, comparisons across cores/sites, and integration with other C-SIDE datasets to build data products or dashboards for self-serve analysis.

## Practical notes and considerations
- Ensure correct interpretation of grain size class mapping to the 100 Grain_size_1…Grain_size_100 columns.
- Be aware of NA indicators in statistical treatment fields; check calibration and QA notes when validating analyses.
- When combining with other data, align site identifiers and depth references to ensure consistent cross-dataset analyses.