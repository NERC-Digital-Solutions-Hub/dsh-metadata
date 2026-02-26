# Package overview

- This package provides functions to predict spatial patterns of encounter rate, i.e., the probability of encountering the species on a survey visit, around the southwest Cornwall coast.
- Core objectives:
  - Clean unclear site designations by linking site coordinates to the nearest major site.
  - Identify the viewable seascape from any point and height along the coast.
  - Calculate mean and variability of environmental conditions across the viewable seascape for a given site and time.
  - Compute these same environmental metrics at evenly spaced points around the coast to support encounter-rate predictions.
  - Automatically download Modis SST data.
  - Automatically process VGPM and Modis SST data to a user-defined grid.
  - Model encounter rate as a function of environmental conditions, observation conditions, space and time using a calibrated random forest approach.
  - Predict and plot encounter rate.

## GIS workflow relevance

- Designed to support map-based data products and spatial visualization of encounter rates.
- Integrates environmental and observational variables, enabling spatially explicit predictions and map-ready outputs.
- Produces grid-based outputs suitable for mapping and further GIS analyses.

## Data scope and collection

- Code can be used to analyse data from the Seaquest Southwest monitoring scheme organized by the Cornwall Wildlife Trust.
- The Seaquest data are not included in the package and must be requested separately.

## Nature and units of recorded values

- Data are not supplied with the package.

## Quality control

- Data are not supplied with the package.

## Data structure and usage

- The package is structured as a standard R package and can be installed with install.packages().
- Functions for processing data and building reporting-rate models for several marine mammal species are stored in the R/ directory.
- Environmental data and coastal boundaries required for analysis are stored in data/.
- Seaquest data are not included but can be requested via the data request link.
- Documentation for each function is available via help(function_name) or ?function_name in R.

## Data availability and requirements

- Requires external environmental data (e.g., VGPM, MODIS SST) and coastal boundaries not included in the package.
- Automatic data download and grid processing are supported to facilitate reproducible GIS workflows.

## Data access

- Data from Seaquest Southwest can be requested here: https://erccis.org.uk/requesting-data

## Practical notes for GIS Specialists

- Useful for creating map-based predictions of encounter rates across coastal regions.
- Supports building, validating, and visualizing spatial models that combine environmental, space, and time factors.
- Facilitates reproducible mapping workflows through automated data retrieval and grid-based outputs.