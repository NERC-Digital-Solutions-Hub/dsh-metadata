# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming treatments over the coming decades.
- Site characteristics: upland moorland with predominance of Calluna vulgaris (heather); diverse bryophytes and vascular plants; humo-ferric podzol soil; typically wet climate with mean annual rainfall around 1411 mm.
- Establishment and scope: established in 1998; data collection and supporting documentation updated through version 6 (dated 04/11/2016). The documentation covers site information, climate treatments, equipment, data processing, and a wide range of ecological and climatic measurements.

## Climate treatments and experimental design
- Treatments and replication: two climate treatments (drought and warming) with three replicates each, plus three control plots that mirror shading effects of the structures (total of 9 plots).
- Drought treatment: operates May–September (1999–2011) and April–October since 2012; uses retractable polyethylene roof to exclude rainfall, reducing annual rainfall by about 20% (and excluding ~80% of rainfall during drought periods).
- Warming treatment: uses retractable aluminum-curtain roofs that reflect infrared radiation, reducing nocturnal heat loss; roofs retract during rain to preserve rainfall (~14% annual rainfall reduction). Nighttime cooling mitigation achieves ~64% reduction in heat loss; operation is triggered by a night-time dark threshold and can be suspended in winds above 10 m s-1.
- Treatment timing and variability: drought and warming implementation dates and timings vary by year; wind and rainfall events influence operational details.

## Data types, collection, and processing (data inventory)
- On-site data infrastructure:
  - AWS meteorological data (daily) – temperature, humidity, rainfall, wind, radiation, etc.
  - Micro-meteorological plot data (daily) – soil/air temperature and soil moisture.
  - Rainfall data – storage rain gauge (site level) and biweekly sampling for rainfall chemistry (pH, NO3, Cl, SO4, DOC, NH4).
  - Throughfall data – plot-level rainfall collected biweekly.
  - Water table depth – fortnightly measurements via permeable tubes (installed 2009).
  - Soil respiration – fortnightly; multiple measurement systems over time (1999–2000 CIRAS-2; 2001–2008 CIRAS/LICOR; 2013–2014 automated LI-COR with ground collars).
  - Trace gases (CH4 and N2O) – measured using static chambers with headspace gas sampling.
  - Net ecosystem CO2 exchange (NEE) – measurements in 2002–2004 and 2011; two different chamber systems used.
  - Photosynthesis – ambient and response-curve measurements (2001–2003, with various years for fixed PAR/CO2 conditions).
  - Vegetation survey data (plant biomass) – pin-point method across multiple years (1998–2012); biomass calibration via destructive sampling and species-specific conversion factors.
  - Canopy reflectance – NDVI and PRI indices from ground-based spectrometry (2001–2004).
  - Vegetation phenology, annual growth, and pathogen assessment – shoot elongation, budburst, leaf emergence, and signs of herbivory or disease (1998–2009; extended in later years).
  - Vegetation chemistry – elemental analyses (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) on green and litter material.
  - Litterfall – collectors; monthly to yearly samples (1998–2002 with ongoing years not always monthly); conversion to g m-2 and subsequent chemical analyses.
  - Root biomass – multiple core-based methods across years (2003–2013) with both manual sorting and modern imaging/analysis techniques.
  - Soil microbial biomass – chloroform fumigation method (2000, 2001, 2012).
  - Nitrogen mineralisation – soil core incubations (1998–2004).
  - SOM, SOC, and bulk density – derived from paired cores and standard soil analyses.
  - Soil solution and leachate chemistry – lysimeters and tensioned samplers (biweekly sampling; pH, NO3, Cl, SO4, DOC).
- Data format and storage:
  - Summary tables and data files described (e.g., “SD_Daily automated weather station data_Clocaenog.rtf”, “SD_Soil respiration_Clocaenog.rtf”, etc.).
  - Not all data are stored in the EIDC (Energy and Information Data Centre) – smaller, infrequent, and post-2015 datasets may reside elsewhere.
  - Data processing notes: various instrument changes over time; unit conversions required for cross-method comparability (e.g., soil respiration flux conversions; NEE conversions). Legacy data may lack full processing documentation.
- Data quality and provenance:
  - Basic, visually based quality control in Excel; some older data lack modern provenance or processing details.
  - Measurements taken with multiple instruments over time; calibration and cross-instrument conversions documented where available.
  - Appendix documents site layout and quadrat plots for reference.

## Access, governance, and contact points
- Primary data custodians and contact points for further details:
  - Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor for data at the Clocaenog site.
- Data accessibility notes:
  - Not all data are stored within the EIDC; some smaller or post-2015 datasets may be managed separately.
  - Data documentation emphasizes ongoing metadata, provenance, and structure to aid discoverability and reuse; some legacy data lack complete processing documentation.

## Appendices and site layout
- Appendix 1: Site layout
- Appendix 2: Quadrat layout with experimental plots
- Appendix 3: Plot layout with quadrats and measurement areas
- Appendix 4: Historical plot design notes (including LYS lysimeters, PQ pin quadrats)

## Key considerations for Data Stewards
- Data inventory and interoperability: The project spans many data types and historical measurement methodologies; ensure consistent metadata, units, and provenance across all datasets, and document instrument changes and data conversions.
- Data completeness and discoverability: Some datasets are not stored in the central repository (EIDC); establish clear data ownership, storage locations, and access procedures; maintain a central catalog or metadata registry.
- Data quality and governance: Implement standardized quality checks beyond visual Excel QC; capture data validation rules, calibration records, and data lineage (source instruments, processing steps).
- Versioning and updates: Track versions of the documentation and data files; include revision history that notes treatment changes, equipment updates, and processing methodology updates (e.g., post-2015 data handling).
- User needs and usability: Consider publishing-minded data curation to improve usability for secondary users (datasets aligned with common ecological metadata standards, clear variable definitions, and consistent units).