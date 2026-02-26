# Package overview

- Purpose: A set of functions to predict spatial patterns of encounter rate for a species along the south west coast (Cornwall), under specified conditions.
- Key objectives (capabilities):
  - Clean up unclear site designations by associating site coordinates to the nearest major site.
  - Identify the viewable seascape from any point and height on the coast.
  - Calculate mean and variability in environmental conditions across the viewable seascape for a given site and time period.
  - Compute these conditions at evenly spaced points around the coast to predict encounter rates.
  - Automatically download Modis sea surface temperature (SST) data.
  - Automatically process VGPM and Modis SST data to a user-defined grid.
  - Model encounter rate as a function of environmental conditions, observation conditions, space and time using a calibrated random forest.
  - Predict and plot encounter rate.

- Collection/generation method:
  - Code is designed to analyse data from the Seaquest Southwest monitoring scheme run by the Cornwall Wildlife Trust.
  - Data are not included in the package but can be requested via https://erccis.org.uk/requesting-data

- Nature and units of recorded values:
  - Data are not supplied with this package.

- Quality control:
  - Data are not supplied with this package.

- Details of data structure:
  - The package is structured as a standard R package and can be installed with install.packages().
  - Functions for processing data and building reporting rate models for several marine mammal species are stored in R/.
  - Environmental data and coastal boundaries required for analysis are stored in data/.
  - Seaquest data are not included in the package but can be requested from ERCCIS at the provided URL.
  - Documentation for each function is available via help(function_name) or ?function_name in the R console.