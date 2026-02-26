# Supporting information for R Shiny demonstrator application for advancing reproducible research (https://doi.org/10.5285/df57b002-2a42-4a7d-854f-870dd867618c)

- Collection/generation methods: N/A
- Nature and Units of recorded values: N/A

- Quality control
  - The file session_info.txt lists the versions of R packages used to generate the app.
  - A live demo of the application is available at https://cptecn-sandboxdemo.datalabs.ceh.ac.uk/.

- Details of data structure
  - Dataset used in this demonstrator web app are:
    - ECN precipitation chemistry data 1992-2015: ECN_PC1.csv (Environmental Information Data Centre; DOI provided)
    - ECN rainfall meteorology data 1991-2015: rain_hourly.feather (generated from ECN meteorology CSVs)
    - Lamb weather types data: 20CR_1871-1947_ncep_1948-2020_12hrs_UK.csv (Climate Research Unit)
    - Reading daily Atlantic multidecadal oscillation (AMO) data: AMO_smoothed_from_the_Kaplan_SST_V2.csv (UCAR Climate Data Guide)
  - Notes on data creation
    - Creating rain_hourly.feather: place downloaded ECN meteorology CSV files in a folder named ECNmet, then run the provided R script to:
      - Read all CSVs in ECNmet
      - Filter records where FIELDNAME == "RAIN"
      - Combine into a single data frame (rain_hourly)
      - Write the result to a Feather file in the data folder

- Additional context
  - The listed data sources include DOIs and institutional origins to support reproducibility and traceability.
  - The instructions emphasize assembling and sharing data inputs and derived outputs to enable transparent, repeatable analyses within the Shiny demonstrator.