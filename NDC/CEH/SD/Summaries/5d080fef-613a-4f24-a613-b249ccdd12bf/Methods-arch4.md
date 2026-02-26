# Methods

- Overview
  - Hydrological and meteorological data collected on three 50 x 50 m plots near Andasibe village in eastern Madagascar ( Corridor Ankeniheny-Zahamena, CAZ).
  - Plot types: semi-mature forest (SMF), reforested tree fallow (YSF), and degraded grassland (DL).
  - Data are organized into multiple CSV files by plot type and measurement theme; raw and processed versions exist for several datasets.
  - Column headers typically include Date and Time (DD/MM/YYYY hh:mm) and measurement-specific variables; missing data are indicated with NA.
  - several datasets include accompanying description of instruments, sampling intervals, and calibration notes; some datasets provide MATLAB code used for processing.

- File naming conventions and structure
  - Forest*: data for the semi-mature forest plot (Forest_Rainfall_raw.csv, Forest_Rainfall_processed.csv, Forest_micrometeorology.csv, Forest_Throughfall_automatic.csv, Forest_Throughfall_manual.csv, Forest_Stemflow_raw.csv, Forest_Stemflow_processed.csv, Forest_Sapflow_raw.csv, Forest_Sapflow_processed.csv, Forest_Soilmoisture_raw.csv, Forest_Soilmoisture_processed.csv, Forest_Overlandflow.csv).
  - ReforestedTF_*: data for the reforested tree fallow (YSF) plot (e.g., ReforestedTF_Rainfall_raw/processed.csv, ReforestedTF_micrometeorology.csv, ReforestedTF_Throughfall_automatic.csv, ReforestedTF_Throughfall_manual.csv, ReforestedTF_Stemflow_raw/processed.csv, ReforestedTF_Sapflow_raw/processed.csv, ReforestedTF_Soilmoisture_raw/processed.csv, ReforestedTF_Overlandflow.csv, ReforestedTF_Soilmoisture_raw.csv).
  - Degradedland_*: data for the degraded grassland plot (e.g., Degradedland_Rainfall_raw/processed.csv, Degradedland_micrometeorology.csv, Degradedland_Soilmoisture_raw/processed.csv, Degradedland_Overlandflow.csv, Degradedland_Soil_Heat_flux.csv, Degradedland_Soilmoisture_raw/processed.csv, etc.).
  - For many themes, files exist in pairs: a raw data file and a processed data file; some also include explicit methodological descriptions within the file header.

- Data themes and key measurement details
  - Rainfall
    - Raw: event-based tipping bucket gauges (different tip sizes per dataset) connected to HOBO loggers.
    - Processed: raw converted to 5-minute rainfall data via MATLAB scripts; missing data marked NA.
  - Micrometeorology
    - Measurements of air temperature, relative humidity, windspeed; mast height varies by plot (e.g., 10 m, 7 m).
    - Temporal resolution typically 5- or 10-minute intervals.
  - Throughfall
    - Automatic: three V-shaped gutters per plot with tipping buckets; volumes converted to depths (mm) after correcting for gutter geometry and inclination.
    - Manual: systematic sampling using 66 funnel gauges across subplots (5 m x 10 m), readings daily; depths converted by orifice area.
  - Stemflow
    - Raw: stemflow measured on multiple trees using spiral collars with collectors; daily readings.
    - Processed: plot-level stemflow scaled by species counts and area to yield mm per ground area.
  - Sapflow
    - Methods: Thermal Dissipation Probes (TDP); multiple trees with sapwood area and DBH recorded.
    - Raw: temperature difference data collected; processed to sap flux density (Js) and sapflow (Qt) using Granier-based equations; processed outputs include Js per tree and Qt.
    - MATLAB scripts provided to compute Js and to export results.
  - Soil moisture
    - Depths: 5, 15, 40, 75, 110, 160 cm; measurements via TDR sensors.
    - Intervals: 30-minute and 5-minute depending on period; raw to actual moisture via manufacturer equation (linear transform).
  - Runoff/Overlandflow
    - Overland runoff measured on bounded plots using gutters and drums; corrections for direct rainfall input; results reported as runoff (mm) and corrected volumes.
    - Plot area, slope, drum calibration, and related constants documented for each dataset.
  - Soil heat flux
    - Measured at 5, 15, 40, 75 cm with HFP01 sensors; data averaged to 5-minute intervals.

- Data processing and code notes
  - Several MATLAB code snippets are included to illustrate data processing steps:
    - Example: converting rainfall RAW to 5-minute rainfall (Forest_Rainfall_processed.csv; ReforestedTF_Rainfall_processed.csv; Degradedland_Rainfall_processed.csv).
    - Sapflow processing scripts to compute sap flux density (Js) and to derive sapflow (Qt) for multiple tree individuals.
    - Raw-to-processed conversions for soil moisture (using manufacturer equations).
  - Processing details typically include date-time handling, aggregation windows (e.g., 5-minute, 10-minute), and conversion from volumes to depths or fluxes.
  - Processed files consistently label columns (e.g., Date and Time, Rainfall (mm), TF mm, SF mm, Js, Qt, etc.).

- Metadata, quality and gaps
  - Missing data explicitly marked as NA in all datasets.
  - Data quality notes embedded in methods (instrument types, calibration references, sampling intervals, and data collection timing).
  - Metadata covers instrument model, height, and approach (e.g., mast height, orientation, gauge types, orifice areas), enabling reproducibility and cross-dataset comparability.
  - Some typos exist in the descriptions, but the core metadata provides structure for integration and interpretation.

- Implications for data management and reuse
  - Rich, multi-theme data across three plots enables cross-cutting analysis of hydrological and ecophysiological processes (rainfall, throughfall, stemflow, sapflow, soil moisture, heat flux, runoff).
  - Clear naming schema and documentation support programmatic loading and alignment by timestamp and plot.
  - Availability of raw and processed data, plus explicit processing scripts, facilitates reproducibility, provenance tracking, and potential reprocessing with updated methods.
  - For data leadership: consider consolidating data dictionaries across plots for uniform variable naming, documenting data provenance, and establishing a central metadata catalog to enable discoverability and cross-plot integration.