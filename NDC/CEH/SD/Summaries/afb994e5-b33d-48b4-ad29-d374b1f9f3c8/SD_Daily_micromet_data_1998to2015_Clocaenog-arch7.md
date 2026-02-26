# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf' Details of data structure for 'Daily micromet data_1998to2015_Clocaenog.csv'

## Overview
- Describes the data structure for the Daily micromet data series at Clocaenog.
- Supplements the broader supporting documentation for the data series.

## Dataset structure
- A single spreadsheet with 38 columns.
- Columns include:
  - Date
  - Soil temperature (C) at 5 cm depth for plots 1–9
  - Soil temperature (C) at 20 cm depth for plots 1–9
  - Air temperature (C) at 20 cm above the soil surface for plots 1–9
  - Soil moisture (m3/m3) for plots 1–9
- The second row contains the plot number.
- The date range runs from 05/11/1998 to 30/06/2015.
- Empty cells denote days with no available data.

## Temporal and spatial scope
- Temporal resolution: daily observations.
- Spatial scope: nine plots (1–9) at the Clocaenog site.
- Measurements captured per plot include temperature at two depths, air temperature, and soil moisture.

## Data contents and units
- Soil temperature: Celsius (5 cm and 20 cm depths).
- Air temperature: Celsius (20 cm above soil surface).
- Soil moisture: volumetric water content (m3/m3).
- Data are organized by date and per-plot measurements, with missing values indicated by empty cells.

## GIS usage considerations
- Recommended formats: reshape to long format (date, plot, measurement type, value) for easier GIS analysis, or create per-variable time series/raster layers if needed.
- Since explicit spatial coordinates are not provided, plot locations should be derived from the Clocaenog site mapping or metadata.
- Data cleaning steps may include:
  - Verifying the alignment of measurements with the correct plot numbers (given the mention of a second row listing plot numbers).
  - Handling missing data appropriately for analyses and visualizations.
  - Confirming unit consistency across all columns before integration into GIS products.

## Metadata and provenance
- This document is a supplement to the main Clocaenog data series documentation.
- For full metadata, data definitions, and data handling procedures, refer to Clocaenog_supporting documentation_Data series.rtf.