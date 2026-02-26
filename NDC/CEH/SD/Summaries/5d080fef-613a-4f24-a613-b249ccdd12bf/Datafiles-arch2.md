# Datafiles

## Overview
- Compilation of environmental monitoring data across multiple forest and grassland sites.
- Aims to support consistent assessment of environmental health and policy performance over time.
- Data are organized to enable verification, quality assurance, cleaning, transformation, and standardised presentation.

## Data structure and contents
- Datafiles.rft: overview of the different files and the time period for which data are available.
- Study Sites.rtf: information on the three study sites.
- Methods.rtf: brief description of data collection methods and the contents of the datafiles.
- Datafiles include a range of raw and processed time-series datasets (CSV/RTF), covering multiple environmental variables and site types.

## Study sites and time periods
- Semi-mature forest site: extensive rainfall, micrometeorology, throughfall, stemflow, sapflow, soil moisture, and runoff data.
  - Examples of time frames: roughly 2014-10-2015-09 with various start dates (e.g., 03-10-2014 to 30-09-2015; 01-10-2014 to 30-09-2015; 15-10-2014 to 01-10-2015; 16-02-2015 to 30-09-2015; etc.).
- Young forest site (reforested/tree fallow): similarly varied datasets collected within 2014-2015 windows.
  - Data series include 5-minute rainfall, 10-minute micrometeorology, 5-minute throughfall (automatic/manual gauges), 5-minute stemflow, sapflow, soil moisture, and overlandflow.
- Degraded grassland site (degradedland): bounded overland flow plots data.
  - Data series include raw/processed rainfall, micrometeorology, soil moisture, daily overlandflow, soil heat flux, etc.
- Time periods demonstrate overlapping coverage primarily from late 2014 through 2015, with some datasets extending into early October 2015 depending on variable and site.

## Data types and sampling
- Rainfall: raw and processed datasets for multiple sites (Forest_Rainfall_raw/processed; ReforestedTF_Rainfall_raw/processed; Degradedland_Rainfall_raw/processed).
- Micrometeorology: site-wide weather data (Forest_micrometeorology.csv; ReforestedTF_micrometeorology.csv; Degradedland_micrometeorology.csv).
- Throughfall: automatic and manual gauges (Forest_Throughfall_automatic.csv; Forest_Throughfall_manual.csv; ReforestedTF_Throughfall_automatic.csv; ReforestedTF_Throughfall_manual.csv).
- Stemflow: raw and processed data (Forest_Stemflow_raw.csv; Forest_Stemflow_processed.csv; ReforestedTF_Stemflow_raw.csv; ReforestedTF_Stemflow_processed.csv).
- Sapflow: temperature-derived sap flux density and sap flow (Forest_Sapflow_raw.csv; Forest_Sapflow_processed.csv; ReforestedTF_Sapflow_raw.csv; ReforestedTF_Sapflow_processed.csv).
- Soil moisture: raw and processed soil moisture data (Forest_Soilmoisture_raw.csv; Forest_Soilmoisture_processed.csv; Degradedland_Soilmoisture_raw.csv; Degradedland_Soilmoisture_processed.csv; ReforestedTF_Soilmoisture_raw.csv; ReforestedTF_Soilmoisture_processed.csv).
- Overlandflow: daily runoff data (Forest_Overlandflow.csv; Degradedland_Overlandflow.csv; ReforestedTF_Overlandflow.csv).
- Boundaries and plot context: data described as being from bounded overland flow plots (particularly for young forest and degraded grassland sites); includes both automatic and manual measurement sources.

## Data management and accessibility
- Data are prepared to be verifiable and quality-assured, then stored and uploaded to appropriate data portals.
- Outputs are designed to be presented in standard formats such as reports, maps, and charts.
- Aims to increase the value of datasets by enabling combination with other relevant data beyond single-use applications.
- Emphasis on enabling others to access the underlying data used to generate final outputs.