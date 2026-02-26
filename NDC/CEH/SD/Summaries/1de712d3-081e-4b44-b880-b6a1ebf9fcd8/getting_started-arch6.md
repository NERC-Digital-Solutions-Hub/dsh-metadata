# State tagging application for environmental data quality assurance

## Overview
- An implementation of state tagging to improve quality assurance for environmental data.
- Returns state-dependent prediction intervals to contextualize observational data.
- States are determined by clustering auxiliary data (e.g., meteorological data) from the same day.
- Applicable to any point-based daily time series observations.

## How it supports data work
- Combines multiple data sources to assess data quality and provide contextual QA information.
- Produces self-serve outputs (state tagging and prediction intervals) to help end users interpret data reliability.
- Encourages broader data understanding and potential improvements in data creation and collection processes.

## How to use the app
- Upload two separate CSV files: one with state variables and one with observations.
- Data arrangements accepted:
  - One observation per line: columns DATE, FIELDNAME, VALUE (others ignored).
  - Tidy/Panel/Tabular: DATE column plus other columns as fieldnames.
- Ensure dates are in a non-trivial format (e.g., YYYY-MM-DD).
- After uploading, press Analyze to proceed to the next tab.

## Running and deploying
- Requires R and the necessary R packages.
- Run by pasting the app.R code into the R console or using RStudio's Run App.
- Shiny can be hosted online; references to Shiny deployment guides are provided.
- A deployment of the app is available at https://statetag-generic.datalabs.ceh.ac.uk/ (as of 2020).

## Data and example datasets
- Example state data: MIDAS data at Carlisle (Met Office, 2012).
- Example observation data: Data from automatic water monitoring buoy at Blelham Tarn, 2008–2011.
- Example data formats and snippets provided to illustrate usage.

## Outputs and interpretation
- Outputs include state tagging results and state-dependent prediction intervals.
- Provides contextual information to assess observational data quality.
- Includes guidance on using and interpreting the outputs, supporting iterative improvement of data products.

## Licensing and references
- Code is available under the Open Government Licence; no warranty.
- Citation: Tso, C.-H.M. (2020) State tagging application for environmental data quality assurance.
- References to underlying methods: Tso et al. (2020) Frontiers in Environmental Science.
- Data sources cited for examples: MIDAS (Met Office) and Blelham Tarn buoy datasets.