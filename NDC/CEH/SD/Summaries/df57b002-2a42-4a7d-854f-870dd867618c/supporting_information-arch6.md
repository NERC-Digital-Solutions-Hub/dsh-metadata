# Supporting information for R Shiny demonstrator application for advancing reproducible research (https://doi.org/10.5285/df57b002-2a42-4a7d-854f-870dd867618c)

## Overview
- Describes data sources, data structure, quality control, and steps to reproduce the R Shiny demonstrator app for reproducible research.
- Includes live demonstration access and package/version tracking for reproducibility.

## Datasets used (data structure details)
- ECN precipitation chemistry data 1992-2015: ECN_PC1.csv (Environmental Information Data Centre; DOI link provided).
- ECN rainfall meteorology data 1991-2015: rain_hourly.feather (Environmental Information Data Centre; DOI link provided).
- Lamb weather types data: 20CR_1871-1947_ncep_1948-2020_12hrs_UK.csv (CRU data).
- Atlantic multidecadal oscillation (AMO) data: AMO_smoothed_from_the_Kaplan_SST_V2.csv (Kaplan SST v2 data; URL provided).

## Data generation and processing steps
- Objective: Create rain_hourly.feather from downloaded ECN meteorology data.
- Procedure:
  - Place ECN meteorology CSV files in a folder named ECNmet.
  - Run the provided R script to extract rainfall records and assemble them into a single dataset.
  - Save the resulting data file to the data folder as rain_hourly.feather.
- R script essentials (conceptual):
  - Load libraries: dplyr, feather, readr.
  - List CSV files in ECNmet.
  - For each file, filter records where FIELDNAME == "RAIN".
  - Combine results into a single data frame and write as a feather file.

## Quality control and reproducibility
- Quality control: The file session_info.txt lists the versions of R packages used during the project, documenting the software environment for reproducibility.
- Live demonstration: A live demo is available at https://cptecn-sandboxdemo.datalabs.ceh.ac.uk/.

## Reproducibility and usage notes
- The workflow enables end-to-end data preparation for the demonstrator app, including:
  - Access to multiple data sources spanning chemistry, meteorology, climate classifications, and AMO indicators.
  - Transparency of data transformations and packaging into a self-serve data product (rain_hourly.feather).
- Users can reproduce outputs by following the data generation steps and consulting the session_info.txt for package versions.