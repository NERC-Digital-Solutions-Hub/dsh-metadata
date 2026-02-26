# Details of data structure for 'Daily micromet data_1998to2015_Clocaenog.csv'

## Overview
- Supplement describing the data structure of the daily micrometeorological dataset for Clocaenog.
- Time span: 05/11/1998 to 30/06/2015 (daily observations).
- Stored in a single spreadsheet with 38 columns.
- Missing data represented by empty cells.

## Data structure
- 38 columns in total, including an identifier for the plot.
- Columns cover:
  - Date
  - For plots 1–9:
    - Soil temperature at 5 cm depth (°C)
    - Soil temperature at 20 cm depth (°C)
    - Air temperature at 20 cm above soil surface (°C)
    - Soil moisture (m3/m3)
- The second row contains the plot number (plot identifier).

## Columns and measurements
- Date column provides the daily timestamp.
- Per-plot measurements for each of the four variables:
  - Soil temperature (5 cm)
  - Soil temperature (20 cm)
  - Air temperature (20 cm above soil)
  - Soil moisture
- Plot numbers help differentiate measurements across plots 1–9.

## Data quality and formatting notes
- Data may contain gaps where cells are empty (no data for that day/plot).
- Units are specified as:
  - Temperature: degrees Celsius
  - Soil moisture: m3/m3
- Consistency checks may be needed when aggregating across plots or aligning dates.

## Intended use and data support considerations
- Suitable for time-series analyses, cross-plot comparisons, and deriving daily environmental summaries.
- Useful for climate, soil moisture, and plant-soil interaction studies in the Clocaenog area.
- Data support tasks:
  - Validate row/column structure and plot identifiers.
  - Identify and impute missing values where appropriate.
  - Clean and format data for self-serve exploration (e.g., dashboards, pivot-like views).
  - Cross-reference with the supporting documentation and ensure units align across analyses.