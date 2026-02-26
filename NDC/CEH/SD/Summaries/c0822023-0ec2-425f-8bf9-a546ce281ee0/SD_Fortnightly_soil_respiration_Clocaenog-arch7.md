# Details of data structure for 'Fortnightly soil respiration_Clocaenog.csv'

## Overview
- Supplement to the supporting documentation for the data series related to Fortnightly soil respiration at Clocaenog.
- Contains a single spreadsheet with 11 columns capturing soil respiration measurements across 9 plots over time, plus metadata.

## Data structure
- 11 columns total: Date, Method, and soil respiration values for plots 1–9.
- The first row lists the plot numbers (1–9) as headers for the per-plot measurements.
- The second row encodes the climate treatment.
- The Method column contains the measurement method used for the data.

## Time period
- Data range from 30/03/1999 to 30/06/2015.

## Data content and format
- Each row represents a sampling date.
- Columns for plots 1–9 hold the soil respiration measurements for that date.
- Empty cells indicate no data for that plot on that date.
- Measurements are “fortnightly” by design, but actual date entries may vary and should be treated as missing where empty.

## GIS prep and transformation
- To use in GIS, transform wide format to long format:
  - Fields to retain: date, plot_id (1–9), soil_respiration, climate_treatment, method.
  - Join with plot coordinate data to create a spatial layer per plot.
- Attributes to preserve per record: date, climate treatment (from header row), measurement method (from Method column).

## Data quality and caveats
- Units for soil respiration are not specified in the excerpt; confirm units from the full documentation.
- Header interpretation is somewhat ambiguous (plot numbers as header, climate treatment in a header row); verify parsing to ensure correct plot-to-column mapping.
- Data gaps exist where cells are empty.

## Usage considerations
- Suitable for time-series analysis of soil respiration by plot and by climate treatment.
- Can be visualized as:
  - per-plot time series maps or charts
  - climate-treatment stratified maps or dashboards
- Ensure proper handling of missing data during analysis.

## Access and format
- Original format appears to be a spreadsheet; when integrating into GIS workflows, convert to CSV or a GIS-friendly table and link to a corresponding plot shapefile or layer.