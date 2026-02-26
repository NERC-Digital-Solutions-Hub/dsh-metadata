# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment in Clocaenog Forest, North East Wales, established in 1998.
- Uses automated roof technology to create drought and warming treatments to reflect predictions for the next 20–30 years.
- Site characteristics: upland moorland with Calluna vulgaris-dominated heath; humo-ferric podzol soil; mean conditions described in Tables within the document.
- Experimental design: 9 plots total comprising three warming, three drought, and three control plots arranged in blocks; drought and warming treatments have specific timings and limitations (e.g., wind restrictions on curtains; rainfall interactions with roof operation).

## Datasets and data types
- A wide range of abiotic and biotic data collected from AWS and plot-level sensors, spanning 1998–current day (and with varying end dates for older datasets).
- Data categories include:
  - AWS meteorological data (daily): temperature, humidity, rainfall, pressure, net radiation, solar radiation, PAR, wind
  - Micro-meteorological plot data (daily): soil/air temperature, soil moisture
  - Rainfall and rainfall chemistry (site-level): storage rain gauge and biweekly chemistry analyses
  - Throughfall data (plot-level rainfall; fortnightly)
  - Water table depth (biweekly; 2009–present)
  - Soil respiration (fortnightly and automated; 1998–present)
  - Trace gases CH4 and N2O (plot-level, via static chambers)
  - Net ecosystem CO2 exchange (NEE; 2002–2004, 2009–2011; multiple systems)
  - Photosynthesis (2001–2003; 2001)
  - Vegetation survey data (plant biomass; Pin-point method; multiple years: 1998–2012)
  - Canopy reflectance (NDVI and PRI indices; 2000–2004)
  - Vegetation phenology, annual growth, and pathogen assessment (1998–present for various measurements)
  - Vegetation chemistry (carbon, nitrogen, phosphorus, etc.; annually)
  - Litterfall (1999–2002; then irregular collection)
  - Root biomass (2003–2013 via multiple methods)
  - Soil microbial biomass (2000, 2001, 2012)
  - Nitrogen mineralisation (1998–2004)
  - SOM, SOC and bulk density (via soil cores; multiple years)
  - Soil solution and leachate chemistry (lysimeters; 1998–2008)
  - Appendix: Site layout and quadrat layouts

- Example dataset names:
  - Daily automated weather station data_1999to2015_Clocaenog.csv
  - Daily micromet data_1998to2015_Clocaenog.csv
  - Rainfall_Clocaenog.csv
  - Throughfall_Clocaenog.csv
  - Water table depth_Clocaenog.csv
  - Fortnightly soil respiration_Clocaenog.csv
  - Automated soil respiration_Clocaenog.csv
  - Trace gases_Clocaenog.csv
  - Net ecosystem exchange_Clocaenog.csv
  - Photosynthesis_Clocaenog.csv
  - Vegetation survey_Clocaenog.csv
  - Canopy reflectance_Clocaenog.csv
  - Phenology Growth Pathogens_Clocaenog.csv
  - Vegetation chemistry_Clocaenog.csv
  - Litterfall.csv
  - Root biomass.csv
  - Soil microbial biomass.csv
  - Nitrogen mineralisation.csv
  - Soil organic matter carbon density.csv
  - Water chemistry.csv

## Data collection, equipment, protocols and data processing
- Equipment and data streams:
  - Automated Weather Station (AWS) at 4 m height (after 2007 thefts) with sensors for temperature, humidity, rainfall, pressure, net radiation, solar radiation, PAR, wind
  - Plot-level micro-met sensors: soil/air temperature, soil moisture (varied over years)
  - Rainfall collectors (site-level and plot-level throughfall collectors)
  - Lysimeters and tensioned soil water samplers for soil solution chemistry
  - Soil respiration and trace gas measurement via static chambers and infrared gas analysers (varied instruments across years)
  - Net ecosystem CO2 exchange measurements using CIRAS-2 and later LI-COR systems
  - Vegetation surveys using pin-point methods; canopy reflectance via ground-based spectrometer
- Data timelines and treatment specifics:
  - Drought treatment: operational May–Sept (1999–2011); extended to April–October since 2012; rainfall reduction ~20% on average, with some events excluded by sensor limits
  - Warming treatment: retractable aluminum mesh curtains; night-time warming; cooling during rain events; rainfall reduction ~14% on average
  - Treatments convened in 9 plots (3 warming, 3 drought, 3 control) arranged by blocks
- Data processing notes:
  - Legacy data: multiple measurement systems used over time; unit conversions (e.g., soil respiration units CIRAS-2, LICOR 8100)
  - NEE and photosynthesis calculations adjusted for biomass (above-ground biomass measured via pin-point method; conversion factors provided)
  - Data quality control largely via manual visual checks in spreadsheet software; some documentation and processing steps are acknowledged as imperfect due to legacy data
  - Throughfall percentages used to derive plot-level rainfall from site-level rainfall; occasionally plots are excluded when data quality is compromised
  - Detailed methodological notes and calibration steps provided for several datasets (e.g., soil respiration, trace gases, canopy reflectance)

## Data governance, availability and access
- On-site data governance:
  - Data are collected across long time spans with numerous methods; some data are infrequently collected or post-June 2015; not all data are stored in a single central repository (EIDC)
- Data availability:
  - Not all data are stored within the EIDC; some smaller or newer datasets may reside elsewhere
  - Contact for access and details: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor
- Documentation and metadata:
  - Supporting documentation for datasets exists (RTF files linked to each dataset)
  - Appendix includes site and plot layouts (useful for geospatial and provenance metadata)
- Data stewardship implications:
  - There is a need to standardize metadata across datasets, capture instrumentation history, and document data processing steps for future reuse
  - Robust provenance, versioning, and data quality notes are essential to enable discovery and reuse by data stewards and data users

## Key challenges and data stewardship considerations
- Common data steward challenges reflected in the documentation:
  - Incomplete understanding of user needs due to legacy nature and broad data scope
  - Timely delivery of data given long-term, multi-year field experiments and disparate data streams
  - Ensuring data creators meet evolving metadata and standardization requirements
  - Interoperability across diverse systems and formats, including legacy methods
  - Handling large datasets and data transfer across years with changing instrumentation
  - Managing outdated databases and bespoke solutions with limited interoperability
- Governance recommendations for data stewards:
  - Consolidate and harmonize metadata across all datasets (units, sensors, time scales, methods)
  - Maintain clear data provenance, including instrumentation changes and processing steps
  - Implement data quality flags and documentation for legacy data gaps or methodological shifts
  - Establish clear data access guidelines and maintain up-to-date contact points for data requests
  - Consider creating a centralized catalog entry for Climoor with cross-references to each dataset and its supporting documentation
  - Ensure ongoing data backups and versioning, especially for long-running, multi-method studies

## Appendix and site context
- Appendix 1: Site layout and grid references
- Appendix 2: Quadrat layout and plot schematics
- Site coordinates: SJ019519; Lat 53.055°N, Lon -3.465°W
- Additional materials: plot layouts, lysimeter and sampling infrastructure mapping, and measurement areas for reproducibility and future data discovery