# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf'

## Overview
- Describes a single spreadsheet dataset used for a data series related to Clocaenog.
- Contains measurements across multiple plots (1–9) and multiple variables over time.

## Data structure
- One spreadsheet with 38 columns.
- Columns include:
  - Date
  - Soil temperature at 5 cm depth for plots 1–9
  - Soil temperature at 20 cm depth for plots 1–9
  - Air temperature at 20 cm above the soil surface for plots 1–9
  - Soil moisture (m³/m³) for plots 1–9
- The second row contains the plot numbers.
- Empty cells indicate no data for that day.

## Data interpretation for GIS use
- Data are organized by date and by plot, enabling per-plot temporal visualization of soil temperature (at two depths), air temperature, and soil moisture.
- Suitable for creating time-series maps or per-plot heatmaps and for comparative analyses across plots and variables.

## Data quality and handling notes
- Missing data are represented by empty cells.
- Spatial granularity is at plot level (plots 1–9); appears to be non-spatially explicit beyond the plot identifiers on the second row.

## GIS workflow suggestions
- Import the spreadsheet; ensure proper parsing of date column and per-plot variable columns.
- Create a long-form dataset (Date, Plot, Variable, Value) to facilitate GIS joins and time-enabled visualizations.
- Handle missing data by filtering or imputing as appropriate for the analysis.
- Validate that plot numbers in the second row correctly align with their corresponding columns.