# Supporting information for R Shiny demonstrator application for advancing reproducible research (https://doi.org/10.5285/df57b002-2a42-4a7d-854f-870dd867618c)

## Overview
- Describes the supporting information for an R Shiny demonstrator aimed at advancing reproducible research.
- Live demonstration of the app is available at the specified sandbox URL.
- Quality control includes a session_info.txt file listing R package versions used during generation.
- Details datasets used in the demonstrator and how a derived dataset (rain_hourly.feather) is produced.

## Datasets and provenance
- ECN precipitation chemistry data, 1992-2015 (ECN_PC1.csv)
  - Source: Environmental Information Data Centre
  - DOI: https://doi.org/10.5285/18b7c387-037d-4949-98bc-e8db5ef4264c
- ECN rainfall meteorology data, 1991-2015 (rain_hourly.feather)
  - Source: Environmental Information Data Centre
  - DOI: https://doi.org/10.5285/fc9bcd1c-e3fc-4c5a-b569-2fe62d40f2f5
  - Note: rain_hourly.feather is a derived file created from ECNmet CSV data
- Lamb weather types data
  - Source: Climate Research Unit (CRU)
  - URL: https://crudata.uea.ac.uk/cru/data/lwt/
  - Accessed: 22/09/2021
- Reading daily Atlantic multidecadal oscillation (AMO) data
  - Source: UCAR Climate Data Guide
  - File: AMO_smoothed_from_the_Kaplan_SST_V2.csv
  - URL: https://climatedataguide.ucar.edu/climate-data/atlantic-multi-decadal-oscillation-amo
  - Accessed: 22/09/2021

## Data formats and structure
- Primary datasets and formats
  - ECN_pc1.csv (CSV) for ECN precipitation chemistry data
  - rain_hourly.feather (Feather file) for ECN rainfall meteorology data
  - AMO_smoothed_from_the_Kaplan_SST_V2.csv (CSV) for AMO data
  - Lamb weather types data (CSV) from CRU
- Project organization and file creation
  - ECN meteorology CSVs are stored in a folder named ECNmet
  - The derived rainfall dataset rain_hourly.feather is placed in the data folder
- Data integration steps
  - rain_hourly.feather is created by:
    - Reading all CSVs in the ECNmet folder
    - Filtering rows where FIELDNAME equals "RAIN"
    - Binding the filtered data together
    - Writing the result to a Feather file for efficient access

## Reproducibility and quality control
- Reproducibility is supported by:
  - A session_info.txt file that records the R package versions used to generate the app outputs
  - A live demonstration URL, enabling interactive validation of results
- Documentation of data sources with DOIs/URLs aids traceability and provenance

## Data processing workflow to create derived dataset
- Steps to generate rain_hourly.feather
  - Place downloaded ECN meteorology CSV files into a folder named ECNmet
  - Run the provided R script which:
    - Lists CSV files in ECNmet
    - Reads each CSV and filters for records with FIELDNAME == "RAIN"
    - Combines the results into a single data frame
    - Writes the combined data as rain_hourly.feather into the data folder

## Access, usage, and governance considerations
- Datasets are associated with DOIs/URLs, enabling traceable citations and provenance tracking
- A live demo is available for validation and exploration
- Derived data generation is explicitly documented, supporting reproducibility and potential future updates

## Implications for Data Stewards
- Supports governance of reproducible research by documenting:
  - Data provenance and source identifiers (DOIs, URLs)
  - File formats and storage locations (CSV in ECNmet; Feather in data)
  - Transformation steps and criteria (e.g., selecting FIELDNAME == "RAIN")
  - Packaging of workflows to reproduce results (R scripts and session_info for environment)
- Encourages maintaining consistent metadata, versioning, and clear lineage for both primary and derived datasets
- Highlights the need for accessible, browsable demos to demonstrate data usability and sharing practices through an application.