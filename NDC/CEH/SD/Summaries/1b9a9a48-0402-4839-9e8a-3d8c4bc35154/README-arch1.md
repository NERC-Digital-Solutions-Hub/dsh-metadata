# Package overview

- Purpose: A collection of R functions to predict spatial patterns of encounter rate for the Seaquest Southwest monitoring scheme around the Cornwall coast, including data processing, environmental context, and prediction/visualization of encounter probability.

- Core capabilities (eight objectives):
  - Clean unclear site designations by linking site coordinates to the nearest major site.
  - Determine the viewable seascape from any coastal point and height.
  - Compute mean and variability of environmental conditions across the viewable seascape for a given site and time.
  - Compute the same environmental summaries at evenly spaced coastal points to support encounter-rate predictions.
  - Automatically download Modis Sea Surface Temperature (SST) data.
  - Automatically process VGPM (a productivity metric) and Modis SST to a user-defined grid.
  - Model encounter rate as a function of environmental conditions, observation conditions, space, and time using a calibrated random forest approach.
  - Predict and plot encounter rate.

- Collection and data generation context:
  - The package is designed to analyse data from the Seaquest Southwest monitoring scheme organized by the Cornwall Wildlife Trust.
  - The actual Seaquest data are not included in the package and must be requested externally (via ERCCIS).

- Data availability and scope:
  - Data are not supplied with the package; users must obtain data separately.
  - Environmental data and coastal boundaries needed for analysis are stored within the package’s data directory, while Seaquest data are external.

- Data structure and access:
  - The package is an installable R package (install.packages()).
  - Core processing and modeling functions are stored under R/.
  - Environmental data and coastal boundaries required for analysis reside in data/.
  - Documentation for each function is accessible via help(function_name) or ?function_name in R.

- Outputs and application:
  - Produces predictions and plots of encounter rate, integrating environmental, observation, space, and time factors through a calibrated random forest model.