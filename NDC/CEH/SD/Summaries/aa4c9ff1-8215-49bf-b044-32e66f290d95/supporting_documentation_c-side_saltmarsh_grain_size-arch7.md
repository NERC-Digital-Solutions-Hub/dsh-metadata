# Data resource description for C_SIDE_saltmarsh_grain_size.csv

## Overview
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project.
- Funded by NERC (NE/R010846/1).
- Describes grain size distributions from 459 soil samples collected across UK saltmarshes between 2018–2021.
- Data aim to support GIS-based analysis and visualization of sediment properties relevant to saltmarsh ecosystems and carbon storage.

## Spatial and temporal scope
- Geographic extent: United Kingdom (bounding coordinates roughly between lat 49.844–60.973 and lon -8.019–2.176).
- Site selection: saltmarsh locations around the UK coastline to represent diverse habitats.
- Temporal window: samples collected during 2018–2021.

## Data content and structure
- Grain size range: 0.02244 – 2000 µm.
- File: C_SIDE_saltmarsh_grain_size.csv.
- Core-level fields:
  - Core_ID (text): core identification.
  - Location (text): saltmarsh name.
  - Core_depth_cm (numeric): depth interval of sub-sample (cm).
  - Core_mid_depth_cm (numeric): mid-point depth (cm).
- Grain size distribution fields:
  - Grain_size_1 to Grain_size_100 (numeric): grain size fractions corresponding to size classes.
  - Grain sizes mapped as a series from 0.02244 µm up to 1782.501876 µm (100 classes listed).
- Data presence: metadata indicates 1 for data present; NA indicates no data in cells.

## Observation and laboratory methods
- Measurement technique: grain size analyses using a Malvern Laser Granulometer.
- Sample preparation:
  - Air-dried, ground with pestle and mortar.
  - Sieved through a 0.5 mm sieve to remove large roots and stones.
  - Digested in 10 ml of 30% H2O2; additional 10 ml added after an hour.
  - Heated to 50°C on a hotplate for two hours with volume maintained by adding deionised water.
  - Brief boil and cool before granulometry.
- Calibration: Malvern Laser Granulometer calibrated with a standard of 0.152–0.422 mm.
- Quality control: laboratory equipment calibrated per University of York practices.
- Statistical treatment: not specified (NA).

## Data formats and access
- File format: CSV.
- Metadata note: NA indicates no data; 1 indicates data present.

## GIS considerations and potential applications
- Enables mapping of grain size distributions across UK saltmarsh cores.
- Depth information (core_depth_cm and core_mid_depth_cm) supports vertical layering analyses in maps or 3D visualizations.
- Can be integrated with other C-SIDE datasets (e.g., carbon storage metrics) using Core_ID or Location for regional analyses.
- Useful for assessing sediment properties, habitat characterization, and their relationship to intertidal carbon storage dynamics.