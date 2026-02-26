# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years.
- Powered by solar and wind; aims to reflect upland moorland responses under future climate scenarios.
- Site characteristics: upland west-atlantic moorland dominated by Calluna vulgaris (heather); diverse shrub, moss, bryophyte and moss communities; soil is humo-ferric podzol; typical growing season June–August; winter dormancy.

## Experimental design and climate treatments
- Treatments: drought, warming, with three replicates each, plus three control plots; total of nine plots arranged in blocks.
- Drought treatment: reduced site rainfall via retractable polyethylene roof during the growing season; originally May–Sept (1999–2011), extended to April–October since 2012; annual rainfall reduction ~20%, with substantial attenuation of medium-to-small rain events.
- Warming treatment: retractable aluminum mesh curtains that reduce infrared radiation at night; curtains retract when rain is detected to protect rainfall interception; typical annual rainfall reduction ~14%; curtains disabled in high winds (>10 m/s).
- Experimental layout includes block design and plot allocations; details provided in site documentation (Tables 1–2 and Appendix 1–3).

## Data architecture: datasets and data types
- Vertical integration of meteorological, micrometeorological, hydrological, biogeochemical and vegetation datasets. Major data streams include:
  - AWS meteorological data: daily measurements (air temp, RH, rainfall, pressure, net/radiation, PAR, wind); dataset: daily automated weather station data_1999to2015_Clocaenog.csv.
  - Micro-meteorological data: plot-level soil/air temperature and soil moisture; dataset: daily micromet data_1998to2015_Clocaenog.csv.
  - Rainfall and rainfall chemistry: storage rain gauge (biweekly) and chemical analyses (pH, NO3, Cl, SO4, DOC, NH4); dataset: Rainfall_Clocaenog.csv.
  - Throughfall data: plot-level rainfall; dataset: Throughfall_Clocaenog.csv (biweekly; used to derive treatment-specific rainfall reductions).
  - Hydrology: water table depth via permeable tubes; dataset: Water table depth_Clocaenog.csv.
  - Soil respiration: fortnightly and automated measurements; datasets: Fortnightly soil respiration_Clocaenog.csv and Automated soil respiration_Clocaenog.csv.
  - Trace gases: CH4 and N2O fluxes using static chambers; dataset: Trace gases_Clocaenog.csv.
  - Net ecosystem CO2 exchange (NEE): occasional measurements with different systems (2002–2004, 2011); dataset: Net ecosystem exchange_Clocaenog.csv.
  - Photosynthesis: infrequent measurements with CIRAS-2; dataset: Photosynthesis_Clocaenog.csv.
  - Vegetation biomass: pin-point vegetation surveys (1998–2012, 201? onward); dataset: Vegetation survey_Clocaenog.csv.
  - Canopy reflectance: ground-based spectrometry (NDVI and PRI indices); dataset: Canopy reflectance_Clocaenog.csv.
  - Vegetation phenology, growth and pathogens: shoot elongation, budburst, phenophases; dataset: Phenology Growth Pathogens_Clocaenog.csv.
  - Vegetation chemistry: elemental composition of green/senesced material; dataset: Vegetation chemistry_Clocaenog.csv.
  - Litterfall: collectors; dataset: Litterfall.csv.
  - Root and soil biology: root biomass (multiple methods 2003–2013), soil microbial biomass (chloroform fumigation), nitrogen mineralisation; datasets: Root biomass.csv, Soil microbial biomass_Clocaenog.csv, Nitrogen mineralisation.csv.
  - SOM, SOC and bulk density: soil carbon and density metrics; dataset: Soil organic matter carbon density.csv.
  - Soil solution and leachate chemistry: lysimeters and tension samplers; dataset: Water chemistry.csv.
- Note: Some data are not stored in the central repository (EIDC) or are infrequently collected; contact CEH Bangor for details (Sabine Reinsch, Bridget Emmett).

## Data collection, processing and quality control
- Instruments and methods:
  - AWS and micro-meteorological sensors with frequent firmware/tech changes; measurements logged as hourly averages from minute data; quality checks mainly visual in Excel; some legacy data processing not aligned with current best practices.
  - Soil respiration and trace gas measurements transitioned between CIRAS-2, LICOR 8100, LI-COR automated systems; conversions between units provided (e.g., g CO2 m-2 h-1 to mg C m-2 h-1, and µmol m-2 s-1 to mg CO2-C m-2 h-1) using ideal gas law-based conversions.
  - Throughfall data requires adjustments to align plot-level rainfall with site-level rainfall; data losses due to equipment issues may lead to plot exclusion or infilling with year-wide averages.
- Data processing notes:
  - 3 datasets explicitly note legacy data handling; current best practices may not have been applied consistently.
  - Pin-point vegetation data include conversion factors from pin hits to biomass (calibrated per species); quality checks include cross-year consistency and transcription verification.
- Data handling caveats:
  - Some data are missing or infrequently collected; not all data are maintained in the central data portal; data user should contact project contacts for access and metadata.

## Data provenance, access, and governance
- Data provenance:
  - Datasets are described with instrumentation, sampling frequency, time span, and processing steps; dataset-level notes include unit conversions and methodological caveats.
  - Appendix materials provide site and quadrat layouts for context and reproducibility.
- Access and contact points:
  - Not all data are stored in the EIDC; for access and details, contact Sabine Reinsch (sabrei@ceh.ac.uk) or Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor.
- Documentation and metadata:
  - Each dataset is linked to supporting documentation (rtf files) that describe sensors, methods, QA, and processing.
  - The documentation emphasizes data lineage, collection periods, and instrument configurations, essential for reuse and reanalysis.

## Appendices and site context
- Appendix 1: Site layout for Climoor; plot-level metadata.
- Appendix 2: Quadrat layout and pin-quadrat scheme; mapping to biomass calibration.
- Appendix 3: Plot layout with quadrats and measurement areas.

## Data Stewardship considerations and recommendations
- Ensure metadata completeness:
  - For each dataset, capture: data title, collection period, location (plot, quadrat), treatment, instrument/method, data cadence, units, QA steps, known limitations, data owner, and access constraints.
- Standardize data formats and units:
  - Maintain consistent units across years and instruments; preserve historical conversions and provide clear mapping when instrument changes occur.
- Improve data provenance and lineage:
  - Document processing steps, calibrations, and any infilling or exclusion criteria; link to supporting method documents.
- Accessibility and governance:
  - Ensure long-term storage in a centralized, queryable data portal (EIDC or successor) with clear data access routes; maintain contact points for data requests.
- Quality assurance:
  - Consider systematic QC checks beyond visual Excel reviews (range checks, timestamp validation, cross-dataset consistency) and maintain a change-log for instrumentation transitions.
- Data retention and update policy:
  - Establish an update cadence for the central repository; capture post-2015 data and any re-processed legacy data with versioning.
- Legal and licensing:
  - Attach licensing and usage rights to datasets to enable reuse while protecting sensitive or embargoed data.

Appendix: This document enumerates specific data products, methodologies, and historical instrumentation used in the Climoor field site, providing a comprehensive evidence base for data users and a governance framework for ongoing data stewardship.