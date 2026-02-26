# Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Dataset documenting grain size distributions from 459 soil samples collected across UK saltmarshes, 2018–2021.
- Funded by NERC (NE/R010846/1).
- Data resource includes detailed grain-size measurements and associated metadata suitable for cross-site, temporal, and process-based analyses of saltmarsh sediments.

## Data scope and geographic reach
- Geographic extent: United Kingdom, with observation coordinates provided in decimal degrees (WGS84).
- Site selection: Sites located in similar environmental regions and spread around the UK coastline to represent saltmarsh habitats.
- Observations describe grain size distributions spanning 0.02244 to 2000 µm.

## Data collection and processing methods
- Analytical instrument: Malvern Laser Granulometer.
- Sample preparation:
  - Air-dried samples broken up with a pestle and mortar.
  - Sieved through a 0.5 mm mesh to remove large rootlets and stones.
  - Digested with 10 ml of 30% H2O2, left for an hour; second 10 ml of 30% H2O2 added and left for another hour.
  - Heated to ~50°C on a hot plate for two hours while maintaining volume with deionised water.
  - Brief boil and cooling prior to laser granulometry.
- Calibration and quality control:
  - Granulometer calibrated using a standard of 0.152–0.422 mm sand.
  - Laboratory equipment calibrated according to University of York practices.
- Data handling: Observations are captured in CSV format with explicit grain-size bins.

## Data structure and variables
- Primary data file: C_SIDE_saltmarsh_grain_size.csv.
- Core-level metadata:
  - Core_ID (text)
  - Location (saltmarsh name, text)
  - Core_depth_cm (numeric; depth interval, cm)
  - Core_mid-depth_cm (numeric; mid-point depth, cm)
- Grain-size data:
  - Grain_size_1 to Grain_size_100 (numeric; grain size distributions)
  - Grain_size_1 corresponds to 0.02244 µm, Grain_size_2 to 0.025179 µm, continuing through Grain_size_100 to 1782.501876 µm
  - Missing data represented as NA

## Metadata, provenance, and data quality
- Locations described to support comparability across sites with similar environmental contexts.
- Documentation includes explicit grain-size bin definitions (µm) and the measurement protocol to support reproducibility and cross-study integration.
- Quality assurance steps include calibration of equipment and adherence to laboratory practices.

## Access, format, and discoverability
- File format: CSV (tabular data).
- Data resource details include core identifiers, location descriptors, depth information, and a wide panel of grain-size measurements (100 bins).
- Metadata describe sampling context and measurement procedures to aid discoverability and interpretation.

## Uses and implications for data-driven decision making
- Enables cross-site comparisons of sediment grain-size distributions in UK saltmarshes.
- Facilitates integration with other C-SIDE datasets to analyze carbon storage processes, sediment transport, and geomorphology in intertidal environments.
- Supports policy-oriented analyses by providing standardized, well-documented sediment data across multiple sites.

## Key challenges and considerations for Data Leaders
- Data discovery and standardization: Large, multi-site dataset with many grain-size bins requires consistent naming, units (µm), and depth definitions.
- Data gaps and completeness: NA values indicate missing measurements; assess impact on analyses and plan for gap-filling or metadata augmentation.
- Metadata completeness: Ensure site descriptions, coordinates, depth intervals, and grain-size mappings are maintained for future reuse and integration.
- Access and governance: Understand licensing and rights for reuse; verify any cross-institution data-use requirements.