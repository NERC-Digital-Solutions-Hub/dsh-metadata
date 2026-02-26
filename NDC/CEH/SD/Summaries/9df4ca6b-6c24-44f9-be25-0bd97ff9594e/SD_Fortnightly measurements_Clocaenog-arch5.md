# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Fortnightly measurements.rft'

## Overview
- Provides details of the data structure for two Fortnightly measurement datasets collected at Clocaenog during 2015–2016.
- Datasets were collected together and cover site-level measurements and soil respiration-related measurements.

## Datasets described

### 1) Fortnightly measurments_Clocaenog_2015-2016_site.csv
- Size: 20 columns, 32 rows
- Content: site-level measurements including rainfall, per-plot throughfall, and water table depth
- Key structure:
  - Date (Day/Month/Year)
  - Rainfall (mm)
  - Throughfall for plots: Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control (all in mm)
  - Water table depth measurements for corresponding plots (Plot1–Plot9)
- Notes on units:
  - Water table depth columns show a mix of units (e.g., one column listed as cm for Plot1 and subsequent columns listed with mm), indicating possible inconsistency and a need for standardization.
- Descriptions: Each column includes a description tying it to a specific plot and treatment.

### 2) Fortnightly measurments_Clocaenog_2015-2016_soil respiration.csv
- Size: 38 columns, 32 rows
- Content: soil respiration-related measurements aligned with plots and treatments
- Key structure:
  - Date (Day/Month/Year)
  - Soil respiration for Plots 1–9 (mg CO2-C m^-2 h^-1 or h^-1 variants)
  - Soil temperature for Plots 1–9 (°C)
  - Soil moisture for Plots 1–9 (Vol%)
  - Photosynthetic active radiation (PAR) for Plots 1–9 (µmol m^-2 s^-1)
- Units:
  - Soil respiration: mg CO2-C m^-2 h^-1 (with some formatting inconsistencies in the description)
  - Soil temperature: °C
  - Soil moisture: Vol%
  - PAR: µmol m^-2 s^-1
- Descriptions: Each column describes the plot and treatment (e.g., Plot1 - Warming, Plot2 - Warming, Plot3 - Control, etc.).

## Data structure and metadata considerations
- Both datasets use a date field as the temporal index and plot-specific columns that map to treatments (Warming, Drought, Control).
- The two datasets are linked by date and plot identifiers but capture different measurement domains (site-level metrics vs soil respiration-related metrics).

## Data governance and quality considerations for Data Stewards
- Metadata quality
  - Ensure complete, consistent variable-level metadata (units, descriptions, plot mappings, treatment designations).
- Unit standardization
  - Resolve inconsistencies in water table depth units within dataset 1 (cm vs mm) to ensure uniformity.
  - Confirm and document any remaining unit formatting inconsistencies in dataset 2 (e.g., minor pluralization/space issues in respiration units).
- Provenance and linkage
  - Document data collection context and any derivations; verify cross-dataset linkage via date and plot identifiers for integrated analyses.
- Data validation
  - Check date formats for consistency; assess missing values and outliers; validate plausible ranges for each variable.
- Sharing, discovery, and maintenance
  - Create and publish dataset-level and variable-level metadata (data dictionary) to data portals or catalogs; implement versioning and update workflows.
- Access and governance
  - Identify any embargoes or proprietary restrictions; document access conditions if present.

## Practical considerations and recommendations
- Prepare comprehensive data dictionaries that clearly define each column, units, and plot-treatment mapping.
- Establish a standard unit policy for water table depth (recommend a single unit, e.g., cm, with all relevant columns converted or clearly documented).
- Align naming conventions across datasets to facilitate integration (consistent plot identifiers and treatment labels).
- Plan for routine data quality checks during uploads and after updates to maintain interoperability between site-level and soil respiration datasets.