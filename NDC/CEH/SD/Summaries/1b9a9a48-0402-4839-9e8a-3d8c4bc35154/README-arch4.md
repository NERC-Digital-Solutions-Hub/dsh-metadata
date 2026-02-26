# Package overview

- Objective: Aims to predict spatial patterns of encounter rate and the probability of encountering a species on a survey visit around the south west (Cornwall) coast under specified conditions. It includes tools to clean site designations, determine viewable seascapes, compute environmental conditions, and model encounter rates.

- Key functional steps:
  - Clean unclear site designations by associating site coordinates to the nearest major site.
  - Identify the viewable seascape from any coastal point and height.
  - Calculate mean and variability in environmental conditions across the viewable seascape for a given site/time.
  - Compute these conditions at evenly spaced coastal points to support encounter-rate predictions.
  - Automatically download MODIS Sea Surface Temperature (SST) data.
  - Process VGPM and MODIS SST data to a user-defined grid.
  - Model encounter rate as a function of environmental and observation conditions, space, and time using a calibrated random forest approach.
  - Predict and plot encounter rate.

- Data sources and access:
  - Software is designed to analyze data from the Seaquest Southwest monitoring scheme (Cornwall Wildlife Trust).
  - The Seaquest data are not included in the package and must be requested separately via ERCCIS (erccis.org.uk).

- Data handling and governance:
  - Data availability: No data are supplied with the package; users must obtain data externally.
  - Data provenance and licensing: Data are sourced from partner organizations (e.g., Cornwall Wildlife Trust) with access through ERCCIS; users should manage permissions and licensing as part of data governance.

- Collection/generation and processing flow:
  - The package provides code to analyze Seaquest Southwest data and to produce reporting-rate models for several marine mammal species.
  - Environmental data and coastal boundaries required for analysis are stored in data/.
  - The toolchain includes automatic data retrieval (MODIS SST) and processing steps to align data to a common grid.

- Data structure, installation, and documentation:
  - The package is structured as a standard R package and can be installed with install.packages().
  - Data and boundaries required for analysis reside in R/ and data/ within the package.
  - Documentation for each function is accessible via help(function_name) or ?function_name in R.
  - Seaquest data is not included and must be requested separately.

- Implications for data leaders:
  - Emphasizes data discovery, integration, and governance across external datasets (MODIS SST, VGPM, Seaquest data).
  - Highlights reliance on partner data providers and the need for offline data access permissions and collaborative agreements.
  - Underlines reproducibility and transparency through in-package documentation and standard R tooling.
  - Points to potential data quality and standardization considerations given external data sources and metadata requirements.