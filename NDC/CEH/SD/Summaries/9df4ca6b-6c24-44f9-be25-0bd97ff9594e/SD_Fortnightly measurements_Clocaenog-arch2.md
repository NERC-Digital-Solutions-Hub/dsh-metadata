# Details of data structure for the two datasets

## Overview
- This document supplements the supporting documentation for the Clocaenog Fortnightly measurements data series (2015–2016).
- It describes the data structure for two datasets collected together: site-level measurements and soil respiration measurements.

## Dataset 1: Fortnightly measurements_Clocaenog_2015-2016_site.csv
- Structure: 20 columns, 32 rows.
- Key variables:
  - Date (day/month/year).
  - Rainfall (mm) – site level.
  - Throughfall (mm) for multiple plots:
    - Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control.
  - Water table depth for plots:
    - Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control.
  - Note: Units are indicated per column (e.g., cm, mm) as described in the header details.

## Dataset 2: Fortnightly measurements_Clocaenog_2015-2016_soil respiration.csv
- Structure: 38 columns, 32 rows.
- Key variables:
  - Date (day/month/year).
  - Soil respiration (mg CO2-C m-2 h-1) for plots:
    - Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control.
  - Soil temperature (°C) for plots:
    - Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control.
  - Soil moisture (Vol%) for plots:
    - Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control.
  - Photosynthetic active radiation (µmol m-2 s-1) for plots:
    - Plot1 - Warming, Plot2 - Warming, Plot3 - Control, Plot4 - Drought, Plot5 - Drought, Plot6 - Control, Plot7 - Warming, Plot8 - Drought, Plot9 - Control.
- Context: All measurements are fortnightly across the 2015–2016 period, with measurements spanning multiple environmental response variables per plot and treatment combination.

## Data context and intended use
- The two datasets capture environmental conditions and soil-level responses across plots subjected to different treatments (Warming, Drought, Control).
- Site-level data (Dataset 1) provides broad environmental inputs (e.g., rainfall, throughfall, and water table depth) for each fortnight.
- Soil-level data (Dataset 2) provides plant-soil interaction indicators (soil respiration) along with related abiotic factors (soil temperature, soil moisture, and PAR) for each plot and treatment.

## Data management and quality
- The datasets are presented as a paired set, with Dataset 1 focusing on site-scale measurements and Dataset 2 on soil- and plot-scale responses.
- Data handling involves verification, quality assurance, cleaning, and transformation to support standardized outputs and reporting formats (e.g., maps, charts, and tables).

## Challenges and considerations for analysts
- Integrating these datasets with other environmental data to maximize dataset value beyond single-use analyses.
- Providing access to the underlying data used to generate final outputs, to support transparency and reproducibility.