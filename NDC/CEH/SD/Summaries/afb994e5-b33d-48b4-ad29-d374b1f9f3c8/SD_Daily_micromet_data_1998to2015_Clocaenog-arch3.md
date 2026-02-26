# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf' Details of data structure for 'Daily micromet data_1998to2015_Clocaenog.csv'

## Overview
- Supplements the supporting documentation for daily micrometeorological data from Clocaenog.
- Covers the data structure of the file 'Daily micromet data_1998to2015_Clocaenog.csv'.
- Temporal coverage runs from 05/11/1998 to 30/06/2015 (daily records).

## Dataset structure
- One spreadsheet with 38 columns.
- Columns include:
  - Date
  - For plots 1–9: soil temperature at 5 cm depth, soil temperature at 20 cm depth, air temperature at 20 cm above the soil surface, and soil moisture (m3/m3).
- The second row contains the plot numbers.
- The dataset is organized per plot across the listed variables.

## Data contents and handling
- Date is continuous across the time span; missing data are represented by empty cells.
- 38-column structure suggests a combination of multiple variables and plots; exact column count may include an index or metadata-related column beyond the per-plot measurements.
- Likely requires careful handling of missing values and alignment of data across plots for analysis.

## Relevance to monitoring frameworks
- Provides multi-variable, per-plot daily environmental measurements suitable for monitoring soil temperature, air temperature, and soil moisture.
- Demonstrates a structured time-series data format that can feed dashboards, reports, or policy-informed assessments.
- Highlights common data governance considerations for monitoring data, including metadata quality, data completeness, and provenance documentation.

## Data quality and governance considerations for authors of monitoring frameworks
- Metadata needs: definitions of variables, units, measurement methods, and plot naming conventions.
- Missing data handling: strategies for imputation or exclusion in analyses.
- Data standards: consistency in column naming, plotting scheme, and date formats to facilitate data sharing and interoperability.
- Data provenance: clear documentation linking the CSV to its supporting documentation and the data collection context.

## Availability and provenance
- Part of the Clocaenog supporting documentation set; reference to the underlying RTF documentation and the CSV file discussed.