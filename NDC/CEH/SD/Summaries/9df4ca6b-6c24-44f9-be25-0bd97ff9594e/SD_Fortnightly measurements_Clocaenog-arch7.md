# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Fortnightly measurements.rft'

## Overview
- Supplements the Clocaenog Fortnightly measurements data documentation.
- Describes two datasets collected together in 2015–2016:
  - Fortnightly measurements_Clocaenog_2015-2016_site.csv (site-level data)
  - Fortnightly measurements_Clocaenog_2015-2016_soil respiration.csv (soil-related measurements)
- Both datasets cover 32 observations (fortnightly time points) and are structured in a way suitable for GIS-like analysis when linked to plot locations.

## Datasets at a glance
- Dataset 1: Fortnightly measurements_Clocaenog_2015-2016_site.csv
  - Structure: 20 columns, 32 rows
  - Key variables:
    - Date (day/month/year)
    - Rainfall (mm) at site level
    - Throughfall measurements (Plot1–Plot9 across different treatments: Warming, Drought, Control) in mm
    - Water table depth measurements by plot (Plot1–Plot9) with per-plot column headers and indicated units
  - Notes: Columns are described with per-plot treatment labels; water table depth columns show varying units across the table (cm and mm appear in the descriptor sequence).

- Dataset 2: Fortnightly measurements_Clocaenog_2015-2016_soil respiration.csv
  - Structure: 38 columns, 32 rows
  - Key variables by plot (Plot1–Plot9) and measurement type:
    - Soil respiration (mg CO2-C m-2 h-1 or mg CO2-C m-2 hr-1)
    - Soil temperature (°C)
    - Soil moisture (Vol%)
    - Photosynthetic active radiation PAR (µmol m-2 s-1)
  - Notes: Columns are organized to cover multiple plots and measurement types, including grouped columns for respiration, temperature, moisture, and PAR across plots with treatment designations (Warming, Control, Drought).

## Data structure details (GIS-relevant)
- Both datasets are wide-format tables with per-plot measurements embedded as separate columns, enabling aggregation by plot if coordinates are attached.
- Temporal coverage is fortnights across 2015–2016, allowing time-series mapping of variables when linked to plot locations.
- Units are specified per column, but there are inconsistencies to be aware of (e.g., water table depth units across the site dataset; respiration units vary slightly in description).

## GIS implications and workflow recommendations
- Geospatial linkage:
  - To map these data, join each plot column to a geospatial point or polygon representing the plot location at Clocaenog.
  - Convert wide format to long format (plot, date, variable, value) to enable time-enabled GIS visualization.
- Visualization options:
  - Plot-level choropleth or symbol maps for variables such as rainfall, soil moisture, soil temperature, and respiration over time.
  - Time-enabled layers to animate fortnights and observe trends by treatment (Warming, Drought, Control).
- Data preparation steps:
  - Normalize and standardize units (resolve water table depth units; confirm respiration units).
  - Rename headers to GIS-friendly identifiers (e.g., Plot1_Warming_Resp, Plot1_Warming_Temp, etc.).
  - Reshape data from wide to long format for efficient GIS and time-series analysis.
  - If plot coordinates are not present, obtain plot locations or centroid coordinates and create a plot-level shapefile or feature class.

## Data quality, standards, and considerations
- Challenges to anticipate:
  - Data stored in multiple places and formats; inconsistency in units (especially water table depth).
  - Large number of plots with multiple treatment combinations; potential ambiguity in header naming.
  - Data cleaning and transformation required before GIS use (unit harmonization, header normalization, handling missing values).
- Confidence and provenance:
  - This document is a metadata supplement; verify against the primary Clocaenog Fortnightly measurements documentation for authoritative definitions and data provenance.

## Practical steps for GIS specialists
- Acquire both CSV datasets and any plot location/shapefile data for Clocaenog.
- Clean and harmonize units (especially water table depth) and standardize column names.
- Reshape to a tidy, long-form dataset suitable for GIS time-series analysis.
- Create per-plot spatial features with accurate coordinates; link to time-series measurements.
- Validate data by spot-checking known values (e.g., rainfall, soil moisture) against expected ranges.
- Document metadata and data transformations comprehensively to accompany GIS products.