# Datafiles

## Overview
- A data inventory detailing the files and time periods available for environmental monitoring across multiple site types.
- Documents the structure, contents, and scope of data used to analyze rainfall, micrometeorology, and hydrological processes.

## Data assets and structure
- Datafiles.rft: overview of the different files and data availability period.
- Study Sites.rtf: information on the three study sites.
- Methods.rtf: description of data collection methods and datafiles contents.
- Data types (across sites):
  - Forest_Rainfall_raw.csv and Forest_Rainfall_processed.csv
  - Forest_micrometeorology.csv
  - Forest_Throughfall_automatic.csv and Forest_Throughfall_manual.csv
  - Forest_Stemflow_raw.csv and Forest_Stemflow_processed.csv
  - Forest_Sapflow_raw.csv and Forest_Sapflow_processed.csv
  - Forest_Soilmoisture_raw.csv and Forest_Soilmoisture_processed.csv
  - Forest_Overlandflow.csv
  - ReforestedTF_* (raw/processed micrometeorology, rainfall, throughfall, stemflow, sapflow, soilmoisture, overlandflow)
  - Degradedland_* (raw/processed rainfall, micrometeorology, soilmoisture, overlandflow, soil_heat_flux)
- Site categories:
  - Semi-mature forest site
  - Young forest site (reforested tree fallow)
  - Degraded grassland site

## Time periods (sample coverage)
- Forest rainfall: raw 03-10-2014 to 30-09-2015; processed 01-10-2014 to 30-09-2015.
- Micrometeorology: 15-10-2014 to 30-09-2015.
- Throughfall (automatic/manual): 01-10-2014 to 30-09-2015.
- Stemflow: raw 16-02-2015 to 30-09-2015; processed 16-02-2015 to 30-09-2015.
- Sapflow: raw 01-10-2014 to 01-10-2015; processed 01-10-2014 to 01-10-2015.
- Soil moisture: raw 15-10-2014 to 01-10-2015; processed 15-10-2014 to 01-10-2015.
- Overlandflow: 01-10-2014 to 30-09-2015.
- Reforested (young forest) site data align around 01-10-2014 to 30-09-2015, with some datasets extending to 30-09-2015.
- Degraded land site data similarly centered on 2014-2015 ranges, with accompanying soil heat flux data.

## Data provenance and quality
- Each dataset includes a descriptive note indicating contents (raw vs processed, automatic vs manual measurements, etc.).
- Metadata is embedded in file descriptions to aid verification and reuse.
- Time-aligned datasets across multiple hydrological and climatic variables enable cross-variable analyses and site comparisons.

## Relevance for monitoring frameworks
- Provides a comprehensive, multi-site data foundation for evaluating environmental health indicators such as rainfall partitioning, canopy interception, soil moisture dynamics, and runoff/evapotranspiration processes.
- Supports development of dashboards and reports through clearly defined data products (raw vs processed) and standardized time frames.
- Facilitates cross-site policy evaluation (semi-mature forest, young forest, degraded grassland) and assessment of land-use change impacts on hydrological and microclimatic responses.

## Governance and data management considerations
- Metadata and provenance are available, but attention needed to maintain metadata quality and consistency across datasets.
- Some datasets require transformation (raw to processed) for comparability; ensure clear documentation of processing steps.
- Data sharing implications are noted; ensure appropriate data governance, storage, and accessibility in line with policy requirements.