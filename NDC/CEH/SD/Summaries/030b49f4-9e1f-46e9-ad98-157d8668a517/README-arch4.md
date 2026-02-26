# Package overview

- Purpose: The speciesRecordTools R package provides functions to examine the distribution of species records, understand sampling trends and potential biases, and build correlative presence-background species distribution models (SDMs) for predicting species distribution across the landscape.
- Data source and scope: Designed to work with Environmental Record Centre for Cornwall and the Isles of Scilly's (ERCCIS) opportunistic species records (Cornwall Wildlife Trust). The package itself does not include data; data can be requested from ERCCIS.
- Data strategy implications: Enables assessment of data coverage, sampling bias, and data suitability to inform data collection priorities, model-based predictions, and decision-making. Can be applied to ERCCIS data or other species occurrence records.
- Collection/generation methods: Code can be used to analyze data held by ERCCIS; data access requires a data request via ERCCIS.
- Nature/units of recorded values: Data are not supplied with the package; units are not specified within the package.
- Quality control: No data are included within the package; quality control must be applied to user-supplied data or data obtained from ERCCIS.
- Data structure and organization: The package follows a standard R package structure. Processing and modeling functions are in the R/ directory; grids for data analysis are in the data/ directory. Species record data are not included but can be requested.
- Data access and reuse: Data can be requested from ERCCIS at https://erccis.org.uk/requesting-data or obtained from other sources.
- Documentation and support: Documentation for each function is available via help(function_name) or ?function_name in R; a vignette with usage details is provided for data analysis workflows.