# Package overview

- Purpose
  - R package for examining the distribution of species records, understanding sampling trends and potential biases, and building correlative presence-background species distribution models to predict species distribution across the landscape.
  - Designed to work with Environmental Record Centre for Cornwall and the Isles of Scilly's (ERCCIS) opportunistic species records.

- Data requirements and access
  - Data are not included in the package.
  - Data can be requested from ERCCIS (Cornwall Wildlife Trust) at https://erccis.org.uk/requestingdata.
  - The package can also be applied to other species occurrence records.

- Data structure and installation
  - The package is organized as a standard R package.
  - Functions for data processing and building species distribution models are stored in the R/ directory.
  - Grids used for data analysis are stored in the data/ directory.
  - The data file (species records) is not included and must be obtained separately.
  - Documentation for each function is available via help(function_name) or ?function_name in R.

- How to use
  - Install and load the package in R, then access documented functions to process data and build SDMs.
  - Use the provided workflows to examine record distribution, assess sampling trends, and identify biases.
  - Build correlative presence-background SDMs to predict distribution across landscapes using the available data.

- Outputs and capabilities
  - Analyze distribution patterns of records.
  - Assess sampling effort and potential biases.
  - Develop and evaluate presence-background species distribution models.
  - Produce outputs suitable for informing landscape-level predictions and analyses.

- Documentation and support
  - Vignettes and function-level documentation describe usage and examples.
  - Help pages available for individual functions via the R help system.

- Quality control and limitations
  - Data quality control is not included within the package.
  - The package relies on external data (ERCCIS or other sources) and requires careful data access and provenance management.