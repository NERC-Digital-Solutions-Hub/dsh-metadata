# Grain size distributions from 459 soil samples collected from across UK saltmarshes between 2018 - 2021

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Dataset focus: Grain size distributions from 459 soil samples collected across UK saltmarshes between 2018 and 2021

## Geographical scope and sampling
- Observations located in the United Kingdom; coordinates provided in decimal degrees (WGS84):
  - Examples of extents: 60.973491, -8.019200; 60.973491, 2.176113; 49.844006, -8.019200; 49.844006, 2.176113
- Site locations described as similar environmental regions to enable comparability
- Sites chosen from around the UK coastline to represent diverse saltmarsh habitats

## Variables and data collection
- Observed variable: Grain size distribution in the range 0.02244 – 2000 µm
- Analytical method:
  - Grain size analyses conducted with a Malvern Laser Granulometer
  - Sample preparation: air-dried, crushed with pestle and mortar, passed through a 0.5 mm sieve to remove large rootlets and stones
  - Digestion: treated with 30% H2O2 (initial 10 ml, then an additional 10 ml after 1 hour)
  - Pre-measurement treatment: heated to 50°C on a hot plate for two hours, adjusted with deionised water, briefly boiled, cooled
  - Measurement: ran on the Laser Granulometer
- Calibration and quality control:
  - Calibration with a standard of 0.152–0.422 mm sand
  - Data checked against university laboratory practices (University of York)
  - All laboratory equipment calibrated as part of quality control
- Data formats:
  - File format for primary data: .csv
  - Data quality note: NA indicates no data in cells for certain fields

## Data structure and contents
- Data resource designation: C_SIDE_saltmarsh_grain_size.csv
- Core information:
  - Core_ID (Text): core identification
  - Location (Text): saltmarsh name
  - Core_depth_cm (Number): depth interval of sub-sample (cm)
  - Core_mid-depth_cm (Number): depth interval mid-point (cm)
- Grain size data:
  - Grain_size_1 to Grain_size_100 (Numbers): grain size distributions, described as Grain Size (µm) values
  - Example mappings: Grain_size_1 = 0.02244 µm, Grain_size_2 = 0.025179 µm, ... up to Grain_size_100 = 1782.501876 µm
  - Note: The list provides 100 grain size bins with corresponding µm values

## Additional metadata and notes
- Data resource descriptions include core identifiers, locations, and depth information alongside the 100 grain-size measurements
- Indicates a structured, hierarchical dataset suitable for cross-site comparisons and aggregation
- Some formatting irregularities in the presented values (e.g., repeated or concatenated entries) but the intended structure is a 100-bin grain size distribution per core/depth.