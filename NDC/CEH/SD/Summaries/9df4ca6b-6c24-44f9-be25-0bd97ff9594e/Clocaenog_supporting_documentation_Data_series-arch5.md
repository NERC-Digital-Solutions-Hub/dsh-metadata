# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climoor is a climate change manipulation experiment at Clocaenog forest using automated roof technology to simulate drought and warming over 20–30 years.
- Data documentation covers site information, climate treatments, equipment, data processing, and a wide range of environmental and vegetation datasets collected since 1998.

## Data holdings and data types
- On-site data categories
  - AWS meteorological data: daily measurements (relative humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind speed/direction)
  - Micro-meteorological plot data: daily soil and air temperatures, soil moisture
  - Rainfall data: site-level storage rain gauge (biweekly) with rainfall chemistry samples
  - Throughfall data: plot-level rainfall (biweekly)
  - Hydrology: water table depth (2009–present)
  - Biogeochemistry: soil respiration; trace gases (CH4, N2O); net ecosystem CO2 exchange (NEE); soil solution and leachate chemistry; soil nitrogen mineralisation; soil organic matter carbon (SOM/SOC) and bulk density
  - Vegetation and ecosystem biology: photosynthesis; vegetation survey (pin-point biomass); canopy reflectance; vegetation phenology; litterfall; root biomass; soil microbial biomass; vegetation chemistry
  - Litter and detritus: litterfall collection and analysis
- Temporal scope
  - Data series span 1998–present for many datasets; some datasets have intermittent or era-specific sampling (e.g., trace gases 1999–2000, 2007–2009; NEE 2002–2004, 2011; photosynthesis 2001–2003).
- Documentation and data design
  - Appendix: site and plot layout; detailed tables for treatment layouts and coordinates
  - Version history: document is version 6 (04/11/2016); update to version 5 previously issued

## Data collection, protocols, and processing
- Climate change treatments
  - Drought: retractable roof reduces annual rainfall by ~20% during growing season (May–Sept; later adjustments to Apr–Oct); operation limited in high winds
  - Warming: retractable aluminium curtains reflect infrared radiation; nighttime warming; rain-triggered roof retraction to preserve rainfall
  - Treatment design includes replicates and controls; some years include scaffolding to mirror shading
- Equipment and data capture
  - Automated weather station (AWS) and in-plot sensors; sensors measured frequently (minute-level data with hourly averages, later half-hour averages)
  - Data quality control primarily via manual visual checks in Excel; documented limitations of automated limits
- Data processing and unit conversions
  - NEE and soil respiration data converted to mg CO2-C m-2 h-1; explicit conversion factors and, for some methods, different instrument baselines
  - Throughfall and rainfall data harmonized to plot-level rainfall using percent-change calculations with exclusion rules when data were compromised
  - Vegetation biomass derived from Pin-point data using calibration factors (Table 6)
- Legacy data and documentation
  - Some data processing steps are not fully documented due to legacy practices; current best practices may not have been applied to earlier datasets
- Data formats and storage
  - Data stored in CEH Bangor shared file area; not all datasets stored in the EIDC
  - Ongoing updates and archival decisions may affect accessibility
- Spatial and plot context
  - Appendix 1–3 provide site layout, quadrat locations, and plot layouts essential for geospatial interpretation

## Data governance, stewardship, and versioning
- Ownership and contact
  - Data provenance and contact points: Sabine Reinsch (sabrei@ceh.ac.uk) and Bridget Emmett (bae@ceh.ac.uk) at CEH Bangor for details
- Metadata and discovery
  - Documentation includes sensor types, measurement methods, frequencies, time scales, and site coordinates (Grid Reference SJ019519; 53.055N, -3.465W)
  - Not all data are stored in EIDC; seek guidance from CEH Bangor for access to smaller or post-2015 datasets
- Versioning and updates
  - Document itself shows versioning (Version 6; update history noted), highlighting the importance of dataset versioning and change tracking
- Data sharing and accessibility
  - Acknowledges potential gaps and conditional access; recommends contacting data owners for full data holdings and current storage locations

## Data quality, limitations, and caveats
- Data gaps and reliability
  - Theft and security incidents led to re-mounted AWS at higher mast; some measurements have gaps or non-standard logging practices
  - Throughfall data can be incomplete due to equipment issues; some years require data exclusion or infilling with year-average reductions
  - Legacy data processing steps not fully documented; best practices not consistently applied across all datasets
- Treatment and measurement limitations
  - Drought and warming treatments have operational constraints (wind limits, rainfall detection limits, rain-triggered retracting mechanisms)
  - Some long-term measurements (e.g., trace gases, NEE) have limited temporal coverage or changes in instrumentation over time

## Storage, access, and data management recommendations for Data Stewards
- Data storage and cataloguing
  - Ensure all datasets are versioned and metadata-rich; clearly indicate storage location (EIDC vs CEH Bangor shared area) and access conditions
- Metadata completeness
  - Capture measurement methods, sensors, depths, calibration details, units, time scales, data gaps, and processing steps
- Data quality assurance
  - Implement standardized QA procedures beyond Excel visuals; document data quality flags, gaps, and imputation rules
- Data sharing and updates
  - Maintain up-to-date contact points and data access instructions; publish dataset inventories and update logs to reflect new data and processing changes
- Data interoperability and standards
  - Harmonize units and formats where possible (e.g., CO2 flux units, soil moisture metrics, chemical concentrations); provide conversion factors and provenance for all transformations
- Appendices and documentation
  - Preserve site layout and plot maps (Appendix 1–3) to support spatial analyses and reproducibility

## Appendices and site context
- Appendix 1: Site layout
- Appendix 2: Quadrat layout with quadrats and measurement areas
- Appendix 3: Plot layout with quadrats and measurement areas indicated
- Appendix 4: Climoor plot details (not shown in excerpt) with LYS, PQ, SS codes and additional references

## Contacts
- Alwyn Sowerby (author)
- Sabine Reinsch (sabrei@ceh.ac.uk)
- Bridget Emmett (bae@ceh.ac.uk)
- CEH Bangor data management liaison for details on data stored outside the EIDC