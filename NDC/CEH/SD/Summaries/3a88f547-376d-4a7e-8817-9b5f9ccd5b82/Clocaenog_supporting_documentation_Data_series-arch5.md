# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climate change manipulation experiment using automated roof technology to simulate drought and warming for the next 20–30 years.
- Location: Clocaenog Forest, North East Wales; established in 1998; powered by solar and wind.
- Design: replicated drought and warming treatments across plots with control plots to mirror shading effects; 9 total plots per table configuration.
- Purpose for data stewards: provide a long-term, multi-parameter data suite with documentation suitable for governance, discovery, and reuse.

## Data scope and coverage
- Abiotic and biotic data collected across multiple datasets and years, including:
  - AWS meteorological data (daily; 1999–present)
  - Micro-meteorological plot data (daily; 1998–present)
  - Rainfall (site level) and rainfall chemistry (biweekly; 1998–present)
  - Throughfall (plot-level rainfall; biweekly to fortnightly; 1999–present)
  - Water table depth (biweekly; 2009–present)
  - Soil respiration (fortnightly; 1998–present)
  - Trace gases CH4 and N2O (varied periods; 1999–2000, 2007–2009)
  - Net ecosystem CO2 exchange (NEE; various years)
  - Photosynthesis (ambient and response curves; multiple years)
  - Vegetation survey data (plant biomass; pin-point method; multiple years)
  - Canopy reflectance (NDVI/PRI indices; 2000–2004)
  - Vegetation phenology, annual growth, and pathogen assessment
  - Vegetation chemistry (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates)
  - Litterfall (1998–2002; annual means)
  - Root biomass (various years; multiple methods)
  - Soil microbial biomass
  - Nitrogen mineralisation
  - SOM, SOC and bulk density
  - Soil solution and leachate chemistry
- Appendix provides site and plot layouts.

## Data structure, formats and metadata
- Data are stored in multiple formats (largely .rtf and CSV) with dataset-specific descriptions.
- Each data type has documented methods, sensors, sampling frequency, and time scales (e.g., “SD_” prefixed files).
- Detailed tables and conversion factors are provided, for example:
  - Pin-hit to biomass conversion factors for vegetation (Table 6)
  - Vegetation quadrat coding and species mapping (Table 5)
  - Unit conversions for translating field measurements to mg CO2-C m-2 h-1 or similar
- Appendix 1–3 contains site layout, quadrat locations, and plot configurations.

## Data collection, equipment and protocols
- On-site AWS met data collected with an automated weather station; sensors mounted initially at 1 m, then at 4 m after 2007 due to theft and safety concerns.
- Micro-meteorological data collected in plots with soil temperature and soil moisture measurements; sampling frequency and methods updated over time.
- Rainfall and rainfall chemistry collected biweekly; throughfall in plots collected fortnightly; water table depth measured using permeable tubes from 2009.
- Soil respiration and trace gas measurements (CH4, N2O) employed static chambers with various instrumentation across years; automated and manual methods used; data processing evolved over time.
- NEE, photosynthesis, litterfall, root biomass, soil microbial biomass, N mineralisation, SOM/SOC, and soil chemistry collected using multiple procedures and instruments; field-to-lab processing described with specific steps.
- Vegetation assessments (pin-point biomass) and canopy reflectance (ground-based spectrometer) conducted in defined windows; phenology and pathogen assessments recorded annually where applicable.

## Data quality, provenance and processing
- Data quality control primarily performed with basic visual QC in Excel; acknowledges that this is less strict than automated gatekeeping.
- Several datasets are legacy data; documentation of data processing steps not always aligned with current best practices.
- Data collected using multiple instruments and methods; unit conversions and cross-calibrations required for integration.
- Some datasets have incomplete coverage or gaps due to plot-level issues (e.g., data loss, equipment changes, or environmental conditions).
- In some cases, data not stored in a central repository (EIDC) and may require contact with data custodians for access.

## Data storage, sharing and access
- Not all data are stored within the Environmental Information Data Centre (EIDC); contact CEH Bangor for details on less-frequently collected datasets or post-2015 data.
- Primary data custodians listed: Sabine Reinsch and Bridget Emmett (CEH Bangor) for data details and access.
- Documentation and data dictionaries exist to aid reuse, but some gaps remain due to legacy data practices.

## Documentation and governance considerations for Data Stewards
- Rich, multi-disciplinary data with extensive metadata requirements; ensure consistency across years and measurement methods.
- Data dictionaries, conversion factors, and site layout maps are essential for data discovery and reuse.
- Key governance actions:
  - Ensure complete metadata capture for each dataset (sensors, time steps, units, QA methods).
  - Maintain data lineage and provenance, including instrument changes and processing steps.
  - Standardize units and provide clear documentation of any conversions between datasets.
  - Develop a centralized catalog or registry entry for each dataset to improve discoverability.
  - Manage access policies and contacts; preserve legacy documentation alongside current data.
  - Plan for long-term storage and versioning, given that some data are not in the central repository.

## Notable challenges and caveats
- Incomplete alignment between user needs and dataset offerings; data spans many years with evolving methods.
- Data gaps and inconsistencies due to plot-level issues, equipment changes, and data loss.
- Legacy data require careful interpretation and may lack comprehensive processing documentation.
- Some data and datasets are not in the central repository, potentially limiting discoverability without direct contacts.

## Contacts and references
- Primary contacts for data access and governance: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk), CEH Bangor.
- Appendix materials: site layout and quadrat layouts to assist in spatial data interpretation.