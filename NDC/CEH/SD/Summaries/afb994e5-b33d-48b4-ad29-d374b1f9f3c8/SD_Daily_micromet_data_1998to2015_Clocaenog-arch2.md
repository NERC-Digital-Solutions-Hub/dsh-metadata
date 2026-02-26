# Daily micromet data_1998to2015_Clocaenog.csv

- Overview
  - Supplement describing the data structure for the Daily micromet dataset from Clocaenog, aligned with the broader supporting documentation for the data series.
  - Intended to aid analysts in understanding how the dataset is organized for monitoring environmental conditions over time.

- Dataset structure
  - One spreadsheet containing 38 columns.
  - Columns (examples): Date; soil temperature (°C) at 5 cm depth for plots 1–9; soil temperature (°C) at 20 cm depth for plots 1–9; air temperature (°C) at 20 cm above the soil surface for plots 1–9; soil moisture (m3/m3) for plots 1–9.
  - The second row contains plot numbers.
  - Date range from 05/11/1998 to 30/06/2015.
  - Empty cells indicate missing data for that day.

- Data details and units
  - Temporal coverage: 1998-11-05 to 2015-06-30.
  - Measurements by plot: 9 plots (1–9) across multiple variables.
  - Depths for soil temperature: 5 cm and 20 cm.
  - Units: temperatures in Celsius; soil moisture in cubic meters per cubic meter.

- Data quality and handling implications for analysts
  - Daily time series with potential gaps (missing data).
  - Requires cleaning, quality assurance, and potential standardisation for integration with other datasets.
  - The mention of a second row with plot numbers suggests careful loading/interpretation to align measurements with correct plots.

- Relevance for environmental monitoring
  - Enables monitoring of microclimate and soil moisture across plots and depths over an extended period.
  - Supports comparisons over time and across locations (plots) and depths.
  - Suitable for producing standard outputs (charts, maps) and for uploading to data portals as part of routine environmental monitoring.

- Practical considerations for use
  - This document is a supplement to the Clocaenog data series documentation, intended to be used alongside the broader supporting materials.
  - Ensure consistent handling of missing data and correct interpretation of plot-number information when loading into analysis workflows.