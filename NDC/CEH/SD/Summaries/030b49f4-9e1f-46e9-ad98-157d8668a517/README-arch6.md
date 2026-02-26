# Package overview

- The speciesRecordTools R package provides functions to examine the distribution of species records, understand sampling trends and potential biases, and build correlative presence-background species distribution models to predict species distributions across landscapes.
- It is designed to work with ERCCIS (Environmental Record Centre for Cornwall and the Isles of Scilly) opportunistic species records.
- A vignette is available to detail how to use the functions for data analysis.

## Collection/generation methods

- The included code analyzes data held by ERCCIS (Cornwall Wildlife Trust).
- The actual data are not included in the package but can be requested via https://erccis.org.uk/requestingdata.

## Nature and Units of recorded values

- Data are not supplied with the package; no specific units are defined within the package.

## Quality control

- Data quality control is not provided within the package itself.

## Details of data structure

- The package is structured as a standard R package and can be installed with install.package().
- Code for processing data and building species distribution models is stored in R/; grids for analysis are stored in data/.
- Species record data are not included but can be requested from ERCCIS or obtained from other sources.
- Documentation for each function is available and can be accessed via help(function_name) or ?function_name in the R console.