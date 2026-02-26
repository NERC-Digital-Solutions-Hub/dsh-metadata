# Package overview

- Purpose: A set of functions to predict spatial encounter rates for a species along the Cornwall coast, enabling clean alignment of site designations, seascape assessment, environmental condition calculations, and predictive modelling and plotting.

- Core objectives:
  - Clean unclear site designations by linking site coordinates to the nearest major site.
  - Identify the viewable seascape from any point and height on the coast.
  - Calculate mean and variability of environmental conditions across the viewable seascape for a given site and time.
  - Compute conditions at evenly spaced coastal points to support encounter-rate predictions.
  - Automatically download Modis SST data.
  - Automatically process VGPM and Modis SST data to a user-defined grid.
  - Model encounter rate as a function of environmental conditions, observation conditions, space, and time using a calibrated random forest.
  - Predict and plot encounter rate.

- Collection/generation methods:
  - Intended for data from the Seaquest Southwest monitoring scheme (Cornwall Wildlife Trust).
  - Data themselves are not included in the package and can be requested.

- Nature and units of recorded values:
  - Data are not supplied with the package.

- Quality control:
  - No data are supplied with the package; external data quality control is not described within.

- Details of data structure:
  - Implemented as a standard R package, installable via install.packages().
  - Functions for processing data and building reporting-rate models (for several marine mammal species) are in the R/ directory.
  - Environmental data and coastal boundaries required for analysis are in the data/ directory.
  - Seaquest data are not included; can be requested from ERCCIS/Cornwall Wildlife Trust.
  - Documentation for each function is available via help(function_name) or ?function_name in R.