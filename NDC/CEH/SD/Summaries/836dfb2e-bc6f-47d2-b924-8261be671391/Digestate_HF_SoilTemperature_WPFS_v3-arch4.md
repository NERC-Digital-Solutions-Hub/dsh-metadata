# Digestate_HF_SoilTemperature_WFPS_v1.csv

## Overview
- Supplement to supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Dataset consists of 4 columns and 87,980 rows
- Sourced from the digestate wheat trial 2017 at Henfaes Research Center, Bangor University
- Contains soil temperature and water-filled pore space (WFPS) measurements at 2.5 cm soil depth across ten plots

## Dataset structure
- Columns: Time, Plot_numbers, Soil_temperature_degrees_celsius, WFPS_percent
- Time: Date and time of day
- Plot_numbers: 10 plots (5, 6, 8, 10, 15, 18, 24, 28, 29, 30)
- Soil_temperature_degrees_celsius: soil temperature at 2.5 cm depth
- WFPS_percent: water-filled pore space at 2.5 cm depth
- Units: Degrees Celsius for soil temperature; Percent for WFPS

## Variables and units
- Time: Date and time of measurement
- Plot_numbers: Plot identifier
- Soil_temperature_degrees_celsius: Temperature at 2.5 cm depth (°C)
- WFPS_percent: Water-filled pore space at 2.5 cm depth (%)

## Provenance and context
- Related to digestate wheat trial experiments conducted in 2017
- Location: Henfaes Research Center, Bangor University
- Part of the data series documented in the referenced supporting documentation

## Data management and governance considerations for Data Leaders
- Metadata and discoverability: ensure clear metadata, column definitions, and units; reference to v1 dataset
- Data quality: verify consistency of column names, units, and depth specification (2.5 cm)
- Versioning and access: maintain versioned dataset (v1) with traceable lineage to supporting documents
- Reusability: structure supports time-series analysis of soil temperature and WFPS across plots; facilitates integration with broader data ecosystems

## Potential usage notes
- Enables analysis of relationships between soil temperature and WFPS at shallow depth across multiple plots
- Supports temporal and spatial comparison within the 2017 digestate wheat trial context
- Useful for stakeholders seeking to understand or reuse data within the wider data community and networks involved in digestate trial research