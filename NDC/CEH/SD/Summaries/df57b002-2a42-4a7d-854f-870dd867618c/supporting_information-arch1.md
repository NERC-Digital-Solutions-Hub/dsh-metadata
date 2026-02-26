# Supporting information for R Shiny demonstrator application for advancing reproducible research (https://doi.org/10.5285/df57b002-2a42-4a7d-854f-870dd867618c)

## Overview
- Provides dataset sources, data structure, and steps to reproduce the rain_hourly.feather dataset used in the demonstrator web app.
- Emphasizes reproducibility through documented data inputs and a runnable R script.

## Datasets used in the demonstrator
- ECN precipitation chemistry data 1992-2015: ECN_PC1.csv (Environmental Information Data Centre)
- ECN rainfall meteorology data 1991-2015: rain_hourly.feather (download all data files; notes referenced)
- Lamb weather types data: 20CR_1871-1947_ncep_1948-2020_12hrs_UK.csv (CRU data)
- Reading daily Atlantic multidecadal oscillation (AMO) data: AMO_smoothed_from_the_Kaplan_SST_V2.csv (UCAR Climate Data Guide)

## Data generation and structure
-rain_hourly.feather creation
- Procedure: Place downloaded ECN meteorology CSVs in a folder named ECNmet, then run the provided R script to extract rain records and compile them into rain_hourly (Feather format) placed in the data folder.
- Core steps in the script:
  - Load libraries: dplyr, feather, readr
  - List CSV files in ECNmet
  - Read each CSV and filter FIELDNAME == "RAIN"
  - Bind rows from all files into a single data frame
  - Write the result as rain_hourly.feather

## Quality control and reproducibility
- Quality control: The file session_info.txt lists the versions of R packages used during generation.
- Live demo: A running demo is available at the provided sandbox URL (cptecn-sandboxdemo.datalabs.ceh.ac.uk/).