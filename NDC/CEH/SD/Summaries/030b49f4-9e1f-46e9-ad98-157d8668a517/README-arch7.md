# Package overview

- Purpose: The speciesRecordTools R package provides functions to examine the distribution of species records, assess sampling trends and potential biases, and build correlative presence-background species distribution models (SDMs) to predict species distribution across the landscape.
- Target dataset: Designed to work with ERCCIS opportunistic species records (Cornwall and the Isles of Scilly). Data are not included in the package and must be requested.
- Data collection and generation: Code can be used to analyse data held by ERCCIS (Cornwall Wildlife Trust) and other species occurrence records.
- Data nature and units: Data are not supplied with the package.
- Quality control: No data are included with the package.
- Data structure and organization: The package follows a standard R package structure. Functions for data processing and SDM building are in the R/ directory; analysis grids are in the data/ directory. Species record data are not included within the package but can be requested or sourced elsewhere.
- Accessing data: Data from ERCCIS can be requested at https://erccis.org.uk/requesting-data; other sources may also be used.
- How to use: Documentation for each function is accessible via help(function_name) or ?function_name, and a vignette provides details on using the functions for data analysis.
- GIS relevance: Enables GIS-focused analysis and map-based visualization of species distributions, sampling biases, and SDM-driven predictions, aligning with workflows common to GIS analysts.