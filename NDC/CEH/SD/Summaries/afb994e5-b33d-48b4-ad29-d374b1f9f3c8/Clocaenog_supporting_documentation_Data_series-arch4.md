# Climoor field site in Clocaenog forest Supporting documentation for data

- A climate change manipulation experiment at Clocaenog Forest, North East Wales (established 1998) using automated roof technology to simulate drought and warming treatments over the next 20–30 years.
- Purpose: document, curate, and facilitate reuse of the diverse environmental and ecological data generated across multiple decades and measurement platforms.
- Lead authors/editors: Alwyn Sowerby (author), Sabine Reinsch (editor); CEH Bangor involvement; data may be stored in the Environmental Information Data Centre (EIDC) with some legacy datasets outside it.

## Data assets and datasets

- AWS and meteorological data
  - AWS daily meteorological data (1999–present)
  - Micro-meteorological plot data (soil and air temperature, soil moisture; daily to current day)
- Rainfall and rainfall chemistry
  - Rainfall at site (biweekly; storage gauge; 1998–present)
  - Rainfall chemistry (biweekly; pH, nitrate, chloride, sulfate, DOC, ammonium)
- Throughfall and hydrology
  - Plot-level throughfall data (fortnightly; used to compute plot rainfall reductions)
  - Water table depth data (2009–present; permeable tubes)
- Soil and ecosystem processes
  - Fortnightly soil respiration data and automated soil respiration data (1998–present; various methods)
  - Trace gas measurements (CH4 and N2O; 1999–2000, 2007–2009)
  - Net ecosystem CO2 exchange (NEE) data (2002–2004, 2009–2011)
  - Photosynthesis data (2001–2003; select species)
  - Soil solution and leachate chemistry (1998–2008)
  - Soil organic matter carbon density, SOM, SOC, and bulk density (various periods 1999–2004, 2013)
- Vegetation and aboveground measurements
  - Vegetation survey data (pin-point biomass, 1998–2012; multiple years)
  - Canopy reflectance data (2000–2001, 2003–2004)
  - Vegetation phenology, annual growth, and pathogen assessment (1998–present; annual/periodic)
  - Vegetation chemistry (green and senesced material; 1998–present)
  - Litterfall (1999–2002; later years with irregular collection)
  - Root biomass (2003–2004, 2008, 2010–2011)
- Microbial and soil biology
  - Soil microbial biomass (2000–2001, 2012)
  - Nitrogen mineralisation (1998–2004)
- Soil physical/chemical properties
  - SOM, SOC, and bulk density (as above)
- Datasets referenced by name (examples)
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
- Note: Not all data are stored in the EIDC; some smaller or post-2015 data are stored elsewhere. For access details, contact CEH Bangor collaborators.

## Data collection, processing, and quality

- Instrumentation and data capture
  - AWS meteorological station (on a secured mast; sensors for temperature, humidity, rainfall, radiation, PAR, wind)
  - Micro-met sensors for plot-level soil temp, soil moisture, etc.
  - Rain gauges and rainfall collectors for site and plot-level rainfall and chemistry
  - Lysimeters, tensioned water samplers for soil solution
  - Soil respiration and trace gas chambers (static/vented) for CO2, CH4, N2O
  - Automated systems (e.g., LI-COR 8100) in later years for respiration measurements
- Measurement frequency and scale
  - Measurements span from 1998 onward with varying frequency (daily, hourly, fortnightly, monthly, yearly)
- Data processing and unit conversions
  - Explicit conversion factors between raw instrument outputs and final units (e.g., CO2 flux units, from g CO2 m^-2 h^-1 or µmol m^-2 s^-1 to mg CO2-C m^-2 h^-1)
  - Biomass adjustments for NEE based on above-ground biomass measured in chambers
  - Pin-point vegetation data converted to biomass using species-specific calibration factors
  - Throughfall and rainfall data reconciliation: plot-level reductions derived by applying percent differences to site-level rainfall data; occasional data loss leads to plot exclusion or infill with year-averaged reductions
- Data quality and caveats
  - Data quality control relied on visual checks and basic Excel-based QC; some legacy data may not meet modern best-practice documentation
  - Treatment measurements (drought and warming) have documented variability, timing, and wind-exclusion constraints
  - Some datasets are infrequently collected or were collected using evolving methodologies; users should review dataset-specific supporting docs for methodological context
- Metadata and documentation
  - Comprehensive dataset-level documentation linked to each dataset name; contact Sabine Reinsch or Bridget Emmett for data details
  - Appendices provide site layout and quadrat layout essential for spatial context

## Data governance and access

- Storage and access
  - Primary data direction through the Environmental Information Data Centre (EIDC) for many datasets
  - Some smaller or post-2015 datasets may reside outside EIDC; contact CEH Bangor for access specifics
- Contacts for data access and queries
  - Sabine Reinsch (sabrei@ceh.ac.uk)
  - Bridget Emmett (bae@ceh.ac.uk)

## Context: site, treatments, and layout

- Location and environment
  - Clocaenog field site, upland moorland ecosystem with Calluna vulgaris-dominated vegetation; experiments reflect climate change projections
- Treatments
  - Two climate treatments: drought (roof over plot to reduce rainfall by ~20–80% depending on year and event) and warming ( retractable aluminum mesh curtains to reduce nighttime heat loss)
  - Each treatment replicated thrice across plots; controls with scaffolding to mirror shading
  - Operational details: drought typically May–Sept (varies by year), warming responds to light/dark cycles and rainfall events; wind constraints prevent curtain operation
- Experimental design and layout
  - 9 plots in total (3 warming, 3 drought, 3 control) arranged in blocks
  - Appendix materials provide the exact plot and quadrat layouts (Appendix 1–3)

## Appendix and data context

- Appendix 1: Site layout
- Appendix 2: Quadrat layout (D3, E4, E7) and plot details
- Appendix 3: Plot layout with quadrats and measurement areas
- Site-wide tables summarize climate, soil, vegetation, and measurement history to support data reuse and cross-study comparisons

- Overall, the document provides a comprehensive, multi-decadal blueprint of data streams, measurement methodologies, data processing steps, and access points essential for Data Leaders aiming to integrate, steward, and enable reuse of the Climoor field site data.