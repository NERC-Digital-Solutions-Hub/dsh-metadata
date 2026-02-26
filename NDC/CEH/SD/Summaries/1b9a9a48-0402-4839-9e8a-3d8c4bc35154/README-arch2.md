# Package overview

- Objective: Provide a set of functions to predict spatial patterns of encounter rate for a species around the south west (Cornwall) coast under specified conditions, supporting environmental monitoring and policy evaluation through consistent outputs.

- Core functionalities:
  - Clean unclear site designations by linking site coordinates to nearest major site.
  - Determine the viewable seascape from any coastal point and height.
  - Calculate mean and variability of environmental conditions across the viewable seascape for a given site and time period.
  - Compute these conditions at evenly spaced coastal points to support encounter-rate predictions.
  - Automatically download Modis SST data.
  - Process VGPM and Modis SST data to a user-defined grid.
  - Model encounter rate as a function of environmental and observation conditions, space and time using a calibrated random forest approach.
  - Predict and plot encounter rate.

- Collection/generation context:
  - Tools are designed to analyze data from the Seaquest Southwest monitoring scheme operated by the Cornwall Wildlife Trust.
  - The package does not include the Seaquest data itself; data can be requested from ERCCIS.

- Nature and units of recorded values:
  - The package itself does not include data.

- Quality control:
  - No data is bundled with the package for quality control; users must verify data provenance and quality typical of their workflow.

- Data structure and usage:
  - Distributed as a standard R package; installable via install.packages().
  - Functions for processing data and building reporting rate models for several marine mammal species are stored in R/.
  - Environmental data and coastal boundaries required for analysis are stored in data/.
  - Seaquest data are not included; can be requested via ERCCIS.
  - Documentation for each function is available in the R environment (help(function_name) or ?function_name).