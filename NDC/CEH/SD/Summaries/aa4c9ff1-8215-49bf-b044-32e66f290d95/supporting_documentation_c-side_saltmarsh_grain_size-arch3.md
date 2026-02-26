# Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE) 
- Funding: NERC (NE/R010846/1)
- Data focus: Grain size distributions from saltmarsh soils to support environmental health monitoring, policy scrutiny, and decision-making.

## Dataset scope and location
- Sample count and period: 459 soil samples collected across UK saltmarshes between 2018 and 2021.
- Geographic extent: United Kingdom saltmarsh sites; coordinates provided in decimal degrees (WGS84). Site selection aimed to represent the diverse range of UK saltmarsh habitats.
- Data resource description: Grain size distributions from 0.02244 to 2000 µm.

## Methods and data processing
- Sample preparation: Air-dried samples broken with pestle and mortar; sieved at 0.5 mm; digested with 10 ml of 30% H2O2 (twice), with heating to 50°C, then final dilution before analysis.
- Measurement instrument: Malvern Laser Granulometer.
- Calibration and QA: Calibrated with a standard of 0.152–0.422 mm; laboratory equipment calibrated per University of York practices; data quality checks performed.
- Metadata and data management: NA indicates no data in cells; underlying data shared and governed per stated data governance practices (public sharing can be a barrier in some cases).

## Data structure and contents
- File formats: CSV
- Core and grain size data (as described in C_SIDE_saltmarsh_grain_size.csv):
  - Core_ID: Core identification (Text)
  - Location: Saltmarsh name (Text)
  - Core_depth_cm: Depth interval of sub-sample (Numeric)
  - Core_mid-depth_cm: Mid-point depth (Numeric)
  - Grain_size_1 … Grain_size_100: Grain size distributions (Numeric)
  - Grain size mapping: Grain_size_1 corresponds to 0.02244 µm; Grain_size_100 corresponds to 1782.501876 µm; the table provides the full set of grain size classes (up to 100 entries) with detailed µm values.
- Data provenance: Lab work performed at the University of York; dataset maintained with quality checks and calibration records.

## Data governance and sharing
- Data sharing: The dataset notes that publicly sharing datasets can be a barrier in some contexts; appropriate data governance processes are expected to ensure datasets meet standards, are stored securely, and shared appropriately.

## Relevance for monitoring frameworks
- Provides high-resolution grain size distributions across multiple UK saltmarsh cores, enabling analyses of sediment characteristics, carbon storage potential, and habitat dynamics.
- Supports development of environmental health indicators, dashboards, and policy evaluations by supplying detailed PSD (particle size distribution) data.
- The rich metadata and QA steps facilitate integration into broader monitoring frameworks, subject to data governance and sharing constraints.

## Considerations for addressing common monitoring-framework challenges
- Data availability and quality: This dataset demonstrates robust QA and comprehensive metadata, but general monitoring programs should strive for complete metadata and transparent data provenance.
- Data accessibility: Be mindful of potential barriers to public data sharing; establish clear governance to balance openness with stewardship.
- Metadata completeness: Ensure consistent definitions (e.g., depth intervals, grain-size mappings) to enable easy integration with other datasets.
- Interoperability: Align with open data standards to reduce the effort required for data transformation and to minimize silos across laboratories and projects.