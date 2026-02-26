# Supporting information for R Shiny demonstrator application for advancing reproducible research (https://doi.org/10.5285/df57b002-2a42-4a7d-854f-870dd867618c)

## Overview
- Provides provenance, data sources, formats, and a reproducible data processing workflow underpinning the R Shiny demonstrator for advancing reproducible research.
- Includes quality control references (package versions) and a live demonstration URL.

## Data assets used in the demonstrator
- ECN precipitation chemistry data (1992-2015): ECN_PC1.csv (Environmental Information Data Centre; DOI provided).
- ECN rainfall meteorology data (1991-2015): rain_hourly.feather (Environmental Information Data Centre; created from CSVs).
- Lamb weather types data: 20CR_1871-1947_ncep_1948-2020_12hrs_UK.csv (Climate Research Unit).
- Atlantic multidecadal oscillation (AMO) data: AMO_smoothed_from_the_Kaplan_SST_V2.csv (source: UCAR Climate Data Guide).

## Data formats and structure
- mix of CSV (ECN datasets, Lamb types) and feather format (rain_hourly.feather).
- File paths and naming conventions referenced for dataset integration.

## Creation and processing pipeline
- Objective: create rain_hourly.feather from ECN meteorology CSVs.
- Procedure:
  - Place downloaded ECN meteorology CSVs in a folder named ECNmet.
  - Run the provided R script that:
    - Reads all CSV files in ECNmet.
    - Filters records where FIELDNAME == "RAIN".
    - Binds the results into a single data frame.
    - Writes the aggregated data to a feather file in the data folder.
- R libraries used: dplyr, feather, readr.
- Core operations illustrated by the script:
  - list.files to collect CSVs
  - read_csv to load each file
  - filter by FIELDNAME == "RAIN"
  - rbind across files
  - write_feather to output rain_hourly.feather

## Quality control and reproducibility
- Reproducibility evidence via session_info.txt listing the R package versions used to generate the app.
- A live demo of the demonstrator is available at the provided sandbox URL.

## Access and dissemination considerations
- Data sources are cited with DOIs/URLs, enabling traceability and reuse.
- The workflow demonstrates how event-level meteorological data can be efficiently prepared for analysis and dissemination within the Shiny app.