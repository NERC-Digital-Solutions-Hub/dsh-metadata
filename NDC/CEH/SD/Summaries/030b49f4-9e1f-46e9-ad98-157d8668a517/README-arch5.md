# Package overview

- The speciesRecordTools R package provides functions to examine the distribution of species records, understand sampling trends and potential biases, and build correlative presence-background species distribution models (SDMs) to predict species distributions across landscapes.
- It is built to work with Environmental Record Centre for Cornwall and the Isles of Scilly's (ERCCIS) opportunistic species records.
- The package vignette contains details on how to use the functions for data analysis.

- Collection/generation methods:
  - Code can be used to analyze data held by ERCCIS (Cornwall Wildlife Trust). 
  - The data are not included in the package but can be requested at https://erccis.org.uk/requestingdata.

- Nature and units of recorded values:
  - Data are not supplied with this package.

- Quality control:
  - Data are not supplied with this package.

- Details of data structure:
  - The data are organized as a standard R package and can be downloaded and installed using the install.package() function in R.
  - Code within the package can be used to analyse data held by ERCCIS (Cornwall Wildlife Trust) and other species occurrence records.
  - All functions for processing data and building species distribution models are stored in R/.
  - Grids for data analysis are stored in data/.
  - Species record data are not included in the package, but can be requested at https://erccis.org.uk/requesting-data or obtained from other sources.
  - Documentation for each function is available and can be accessed via help(function_name) or ?function_name in the R console.