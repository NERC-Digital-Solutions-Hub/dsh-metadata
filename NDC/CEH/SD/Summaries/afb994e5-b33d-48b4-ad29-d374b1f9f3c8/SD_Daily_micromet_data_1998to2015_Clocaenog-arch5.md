# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf' Details of data structure for 'Daily micromet data_1998to2015_Clocaenog.csv'

## Overview
- Describes the data structure for a daily micrometeorological dataset from Clocaenog (1998–2015).
- Dataset is a single spreadsheet with 38 columns.
- Columns include: Date, soil temperature at 5 cm (plots 1–9), soil temperature at 20 cm (plots 1–9), air temperature at 20 cm above the soil (plots 1–9), and soil moisture (m3/m3) for plots 1–9.
- The second row contains the plot number.
- Time span: first entry 05/11/1998; last entry 30/06/2015.
- Empty cells indicate missing data.

## Dataset structure and fields
- 38 columns in total; the listed variables are present for plots 1–9 across multiple measurements.
- Key columns to identify:
  - Date
  - 9x4 measurements (soil temp 5 cm, soil temp 20 cm, air temp 20 cm above soil, soil moisture) for plots 1–9
- Note: the second row contains plot numbers, which may indicate a per-row plot identifier or require validation in the metadata.

## Time coverage
- Start date: 05 November 1998
- End date: 30 June 2015
- Data appears daily, with missing values indicated by empty cells.

## Units and variables
- Temperature: degrees Celsius
- Soil moisture: cubic meters per cubic meter (m3/m3)
- Measurements are organized per plot (1–9) and depth/measurement type as listed.

## Data quality and governance considerations
- Missing data handling: empty cells denote data gaps.
- Metadata needs: confirm exact column definitions, units, sensor types, depths, and any data processing steps.
- Provenance: ensure the supplement links clearly to the broader Clocaenog supporting documentation and maintains a traceable data lineage.

## Data handling and sharing guidance
- Prepare a clear data dictionary detailing each column, its meaning, units, valid ranges, and any transformations.
- Validate dataset for date continuity and reasonable value ranges; document any gaps or known issues.
- Ensure compatibility with data portals by including metadata about collection methods, sensors, and collection cadence.

## Recommended actions for Data Stewards
- Confirm and document the exact 38-column schema, including the meaning of the second-row plot number.
- Create and attach a metadata file with definitions, units, valid ranges, and data quality rules.
- Perform quality checks (date sequence, sensor calibration notes, missing data patterns) and document data provenance.
- Prepare the dataset and metadata for discoverability and reuse within the appropriate data governance framework.