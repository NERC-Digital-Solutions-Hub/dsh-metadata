# Climoor field site in Clocaenog forest Supporting documentation for data

- Purpose and scope
  - Climate change manipulation experiment at Clocaenog field site to reflect 20–30 year predictions for upland moorland habitats.
  - Automated roof technology creates drought and warming treatments; site established in 1998 with replicated treatments and controls.
  - Long-term, multi-parameter monitoring to inform policy and management decisions on environmental health.

- Monitoring data streams and measures (data types covered)
  - AWS meteorological data (daily): temperature, humidity, rainfall, pressure, net radiation, solar radiation, PAR, wind.
  - Micro-meteorological plot data (daily): soil/air temperature, soil moisture.
  - Rainfall and rainfall chemistry (site-level, monthly): volume, pH, NO3, Cl, SO4, DOC, ammonium.
  - Throughfall (plot-level rainfall, fortnightly): plot-specific rainfall to derive treatment effects.
  - Water table depth (bi-weekly since 2009): depth to bedrock using permeable tubes.
  - Soil respiration (fortnightly to high-resolution): CO2 flux via collars and IRGA measurements; multiple measurement technologies over time.
  - Trace gases (CH4 and N2O) flux (biweekly/monthly periods): static chamber sampling and GC analysis.
  - Net ecosystem CO2 exchange (NEE) and photosynthesis (varying frequency 2002–2011): chamber-based flux measurements; some years with PAR and temperature sensors.
  - Vegetation survey data (annually): Pin-point biomass estimates for mosses, bryophytes, shrubs (Calluna vulgaris, Vaccinium myrtillus, Empetrum nigrum) and grasses; biomass calibration.
  - Canopy reflectance (2000–2004): NDVI and PRI indices from ground-based spectrometer measurements.
  - Vegetation phenology, annual growth and pathogens (annual/seasonal observations): shoot elongation, budburst, leaf counts, and pathogen signs.
  - Vegetation chemistry (annual): elemental composition (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) from green and litter material.
  - Litterfall (1999–2002 monthly; later irregular): collection, drying, weighing, and carbon/nitrogen analysis.
  - Root biomass (2003–2013): cores and extraction with varying methods; data across years.
  - Soil microbial biomass (2000–2001, 2012): chloroform fumigation-extraction for microbial C.
  - Nitrogen mineralisation (1998–2004): ammonium/nitrate extraction from paired soil cores over time.
  - SOM, SOC and bulk density (via soil cores): fractionation of organic/inorganic layers, density measurements, and conversions to g m-2.
  - Soil solution and leachate chemistry (biweekly 1998–2008): lysimeters and tension samplers; pH, NO3, Cl, SO4, DOC, ammonium.
  - Site and plot layout data (Appendix): layout for LYS, PQ, SS, plots and quadrats.

- Data collection, processing, and metadata
  - On-site AWS and plot sensors operated with daily/minute-scale data; hourly or daily averages recorded.
  - Instrument changes over time (e.g., soil respiration systems, LICOR CIRAS, LI-COR 8100) with explicit unit conversions to harmonize datasets.
  - Processing notes include:
    - Calibration and conversion protocols for transforming raw flux measurements (g CO2 m-2 h-1 or μmol m-2 s-1) to CO2-C units.
    - Use of R/HMR package for Rs calculations; linear regression fits used for respiration estimates.
    - Documentation of methods for photosynthesis, NEE adjustments for biomass differences, and conversion factors for pin-ha biomass to g m-2.
    - Throughfall data adjustments to derive plot-level rainfall by applying percent reduction to site-level rainfall datasets; data gaps excluded from treatment means.
  - Data documentation and support:
    - Datasets named for each data stream (e.g., AWS meteorological data, Throughfall, Net ecosystem exchange, etc.) with dedicated supporting documentation.
    - Some data and metadata are legacy; not all data are stored in a central archive (EIDC); contact CEH Bangor for access to legacy and smaller datasets.
    - Appendix provides site and plot layout; 2012 Climoor plot layout referenced for broader context.

- Data governance, access, and sharing
  - Data governance and sharing are partly constrained by storage location; not all datasets are in the Environmental Information Data Centre (EIDC); access via project contacts.
  - Data are publicly shareable where possible, but historical/legacy practices and metadata gaps can hinder immediate reuse.
  - Metadata quality varies across datasets; some datasets require consultation with originators or data custodians to confirm methods and transformations.

- Quality, gaps, and challenges relevant to monitoring frameworks
  - Gaps and limitations:
    - Legacy data with incomplete or evolving processing protocols; not all data followed current best practices for data processing/documentation.
    - Some datasets have intermittent sampling frequencies or gaps (e.g., NEE measurements, high-resolution soil respiration in certain years).
    - Throughfall and rainfall data require adjustments to align with site-level rainfall and to handle data losses (e.g., funnel losses, bottle overflow, or missing weeks).
  - Metadata and standardization:
    - Inconsistent metadata across datasets; some require explicit instrument details, calibration history, and unit conversions for proper integration.
    - Data format transformations and unit harmonization are needed to enable cross-parameter analyses.
  - Access and governance barriers:
    - Not all data are centrally stored with open metadata; researchers may need to contact data custodians for complete data and documentation.
    - Data sharing requires careful governance to ensure proper data stewardship, provenance, and updates across time.

- Implications for monitoring framework design
  - A comprehensive monitoring framework should:
    - Include multi-parameter, long-term datasets (climate manipulation experiments) to evaluate policy interventions across hydrology, carbon cycling, vegetation dynamics, and soil processes.
    - Establish clear metadata standards, data provenance, and harmonized units to enable cross-domain analyses.
    - Implement robust data governance, with centralized archives (e.g., EIDC) and defined access protocols to minimize silos.
    - Provide transparent QA/QC procedures and data quality flags to support trustworthy interpretation.
  - Practical considerations:
    - Anticipate legacy data integration challenges and plan for retrospective harmonization where possible.
    - Document data processing steps comprehensively, including conversion factors and model assumptions.
    - Ensure scale alignment across datasets (plot-level vs. site-level) and adjust analyses for biomass differences when calculating fluxes like NEE.

- Datasets and contacts (for policy-oriented data use)
  - Primary datasets cover AWS and micromet data, rainfall and rainfall chemistry, throughfall, water table depth, soil respiration, trace gases, NEE, photosynthesis, vegetation biomass and chemistry, litterfall, root biomass, soil microbial biomass, nitrogen mineralisation, SOM/SOC/bulk density, and soil solution chemistry.
  - For access and detailed supporting information, contact Sabine Reinsch or Bridget Emmett at CEH Bangor; additional dataset details and availability are noted in the provided documentation.