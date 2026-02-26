# Supporting information for R Shiny demonstrator application for advancing reproducible research (https://doi.org/)

## Overview
- Purpose: Supporting information for a R Shiny demonstrator aimed at advancing reproducible research, including a live demo link.
- Author and date: Michael Tso, 2 March 2022.
- Live demonstration: Available at the provided sandbox URL.

## Data sources and datasets (Details of data structure)
- ECN precipitation chemistry data (1992-2015): ECN_PC1.csv; Environmental Information Data Centre; DOI: https://doi.org/10.5285/18b7c387-037d-4949-98bc-e8db5ef4264c
- ECN rainfall meteorology data (1991-2015): rain_hourly.feather; Environmental Information Data Centre; DOI: https://doi.org/10.5285/fc9bcd1c-e3fc-4c5a-b569-2fe62d40f2f5
- Lamb weather types data: 20CR_1871-1947_ncep_1948-2020_12hrs_UK.csv; Climate Research Unit data: https://crudata.uea.ac.uk/cru/data/lwt/ (accessed 22/9/2021)
- Reading daily Atlantic multidecadal oscillation (AMO) data: AMO_smoothed_from_the_Kaplan_SST_V2.csv; UCAR Climate Data Guide: https://climatedataguide.ucar.edu/climate-data/atlantic-multi-decadal-oscillation-amo (accessed 22/9/2021)

## Quality control and reproducibility
- Quality control note: The file session_info.txt lists the versions of R packages used to generate the app, supporting reproducibility.
- Demonstrator context: The information pertains to a demonstrator web app intended to advance reproducible research practices in GIS/data visualization.

## Data preparation workflow (Creating rain_hourly.feather)
- Data gathering: Download ECN meteorology CSV files and place them in a folder named ECNmet.
- Data processing steps (high level):
  - Run an R script that reads all CSV files in the ECNmet folder.
  - Filter records where FIELDNAME equals "RAIN".
  - Combine (bind) the filtered records into a single dataset.
  - Write the combined data to rain_hourly.feather.
  - Move/store the generated rain_hourly.feather in the data folder for use by the app.
- Tools used: R with packages dplyr, feather, and readr.
- Notes: The script generates a single hourly rainfall dataset from multiple source CSVs to be used in the Shiny demonstrator.

## Live demonstration and access
- Live demo URL: https://cptecn-sandboxdemo.datalabs.ceh.ac.uk/