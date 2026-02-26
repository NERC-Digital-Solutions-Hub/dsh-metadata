# Details of data structure for 'Vegetation survey_Clocaenog.csv'

## Overview
- A single spreadsheet with 22 columns containing vegetation biomass data.
- Two data series: species-level biomass per plot (columns 1-12) and plot-level total biomass per unit area (columns 13-22).
- Year range: 1998 to 2012.
- Empty cells indicate missing data.

## Data structure by columns
- Columns 1-12: plot-level plant biomass data per unit area by species across time
  - Column 1: Year (1998–2012)
  - Column 2: Measured plant species
  - Column 3: Biomass type (total biomass or living biomass)
  - Columns 4-12: biomass measurements for experimental plots 1 to 9
- Columns 13-22: plot-level total biomass data per unit area over time
  - Column 13: Year (1998–2012)
  - Columns 14-22: total biomass measurements for experimental plots 1 to 9

## Temporal and spatial scope
- Years: 1998–2012
- Plots: 9 experimental plots (1–9)
- Format: CSV; suitable for GIS when linked to plot geometry

## GIS considerations and use cases
- Enables time-enabled maps of biomass by species and total biomass per plot.
- Requires integration with plot location data (coordinates or shapefile) to visualize spatially.
- Data cleaning needed for consistency in units, biomass type, and handling missing values.

## Data preparation steps (suggested)
- Reshape to long format for GIS:
  - Species-level data: Year, PlotID, Species, BiomassType, BiomassValue
  - Total biomass data: Year, PlotID, BiomassValue
- Join with plot geometries for mapping.
- Separate layers/filters for living vs total biomass and for individual species as needed.
- Validate year alignment between the two data series (1998–2012).

## Reference
- Supplement to Clocaenog supporting documentation_Data series.rtf