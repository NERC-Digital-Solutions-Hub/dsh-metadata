# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Climate change manipulation experiment at Clocaenog forest (upland moorland, Wales, UK) using automated roof technology to simulate drought and warming for 20–30 years ahead.
- Established 1998 with replicated drought and warming treatments (9 plots total: 3 warming, 3 drought, 3 controls).
- Powered by solar and wind; aims to reflect climate predictions and study ecosystem responses.
- Datasets cover meteorology, hydrology, soil and ecosystem processes, vegetation, chemistry, and litter dynamics collected over multiple years.

## Data holdings and datasets
- Datasets and file names include:
  - AWS meteorological data: Daily automated weather station data_1999to2015_Clocaenog.csv
  - Micro-meteorological data: Daily micromet data_1998to2015_Clocaenog.csv
  - Rainfall and rainfall chemistry: Rainfall_Clocaenog.csv
  - Throughfall (plot-level rainfall): Throughfall_Clocaenog.csv
  - Water table depth: Water table depth_Clocaenog.csv
  - Soil respiration: Fortnightly soil respiration_Clocaenog.csv; Automated soil respiration_Clocaenog.csv
  - Trace gases: Trace gases_Clocaenog.csv
  - Net ecosystem CO2 exchange: Net ecosystem exchange_Clocaenog.csv
  - Photosynthesis: Photosynthesis_Clocaenog.csv
  - Vegetation biomass/phenology/chemistry: Vegetation survey_Clocaenog.csv; Phenology Growth Pathogens_Clocaenog.csv; Vegetation chemistry_Clocaenog.csv
  - Canopy reflectance: Canopy reflectance_Clocaenog.csv
  - Litter and root dynamics: Litterfall.csv; Root biomass.csv
  - Soil microbial biomass: Soil microbial biomass.csv
  - Nitrogen mineralisation: Nitrogen mineralisation.csv
  - SOM, SOC and bulk density: Soil organic matter carbon density.csv
  - Soil solution and leachate chemistry: Water chemistry.csv
- Notes for data discovery:
  - Data exist as described above; some smaller or infrequently collected datasets may not be stored in the EIDC.
  - Since 2015, not all data have complete on-dataset documentation within the EIDC.
  - For access or details on smaller or post-June-2015 data, contact the data custodians listed below.
- Contact points for data access and details:
  - Sabine Reinsch (sabrei@ceh.ac.uk)
  - Bridget Emmett (bae@ceh.ac.uk)
  - CEH Bangor data liaison

## Data collection, processing and QA
- On-site infrastructure:
  - Automated Weather Station (AWS) for daily meteorology; sensors mounted on secured mast after 2007.
  - Micro-meteorological plots for soil/air temperature and soil moisture; daily sampling.
- Data collection cadence and processing:
  - Measurements collected at high frequency (minutes) with hourly averages logged.
  - Data quality control (QC) performed via visual inspection in Excel; acknowledges limitations of this approach.
  - Legacy data processing notes indicate that best practices for data processing documentation were not always followed; some processing steps described but not uniformly standardized.
- Key data processing details by dataset:
  - Conversions for flux datasets (e.g., soil respiration and net ecosystem exchange) to common flux units (mg CO2-C m^-2 h^-1 or mg CO2-C m^-2 h^-1, from g CO2 m^-2 h^-1 or µmol m^-2 s^-1 using provided conversion factors and the ideal gas law).
  - NEE and photosynthesis calculations require biomass adjustments; above-ground biomass measured with pin-point methods and conversions to biomass used to normalize flux data.
  - Rainfall and throughfall datasets require processing to estimate plot-level rainfall by applying percent changes from throughfall relative to site-level rainfall; data losses lead to plot exclusion or infilling with averaged reductions.
- Instrument and methodological notes:
  - AWS sensors include temperature, humidity, rainfall (tipping bucket), wind, solar radiation, PAR, net radiation, barometric pressure; data sampled every minute and averaged hourly.
  - Micro-met data include soil temperature, soil moisture (varying methods over years; TDR sensors from 2008 onward; earlier methods included theta probes).
  - Soil respiration and trace gas measurements use collars and closed-chamber techniques; instrumentation evolved from CIRAS-2 to LICOR LI-8100 and automated systems; calibration and measurement timing documented, with some notes on measurement duration and handling to minimize CO2 buildup.
  - Throughfall, lysimeters, and tensioned soil water samplers used for detailed hydrology and solute chemistry.
- Documentation and provenance:
  - Data descriptions and supporting documents exist (rtf files) alongside dataset CSVs.
  - Some data processing steps and methodological details are included, but explicit, uniform data dictionaries or processing scripts are not consistently provided across all legacy datasets.

## Data quality, limitations and caveats
- Legacy data challenges:
  - Not all datasets have comprehensive, uniform documentation; some processing steps are not fully captured.
  - Changes in instrumentation and protocols over time (e.g., different soil respiration measurement systems) require careful cross-walks or conversion for comparability.
- Data gaps and reliability concerns:
  - Throughfall measurements can be compromised by equipment issues (funnel/bottle loss, overflow) leading to plot-level exclusions or infilling with averages.
  - AWS data quality control relied on manual QC; automated QC scripts are not described.
  - Some years have limited measurements (e.g., photosynthesis measurements were infrequent).
- Data availability caveats:
  - Not all data are housed in the EIDC; some smaller or post-2015 datasets may be stored elsewhere or not yet cataloged.
  - Users should contact data custodians for access to non-EIDC data and to confirm dataset completeness and metadata availability.

## Data governance, access and stewardship considerations
- Ownership and stewardship:
  - Managed by CEH Bangor with on-site collaborators; data are tied to long-term climate manipulation experiments.
- Metadata, discoverability and provenance:
  - Dataset names and supporting documents are cataloged; detailed metadata exist within the accompanying documentation.
  - There is a need for consistent, machine-readable metadata and a unified data dictionary across all datasets to improve discoverability and interoperability.
- Access and sharing considerations:
  - Data discoverability should be improved in the EIDC; ensure clear versioning and data lineage.
  - For samples not stored in EIDC or for post-2015 data, establish a formal access process and update metadata accordingly.
- Contacts and governance actions:
  - Primary contacts listed above should be engaged for data requests, missing metadata, or clarifications about data processing.
  - Consider establishing a data management plan (DMP) to standardize metadata schemas, unit conventions, data formats, versioning, and change-notification procedures.

## Recommendations for data stewards
- Standardize metadata and structure:
  - Create a consolidated data dictionary covering all datasets, variables, units, timing, and processing steps.
  - Adopt consistent units and provide explicit conversion factors in metadata for flux datasets.
- Improve data quality assurance:
  - Document QC procedures in a machine-readable format; retain data quality flags where applicable.
  - Record instrumentation changes and cross-wacdown calibrations to support long-term comparability.
- Enhance data discoverability and access:
  - Ensure all datasets (including smaller and post-2015 data) are cataloged in the EIDC with clear provenance, license, and usage notes.
  - Provide stable dataset identifiers (DOIs or persistent URLs) and version histories.
- Document data processing and lineage:
  - Capture end-to-end data processing scripts or step-by-step pipelines where possible; link to supplementary documents (rtf, PDFs) in a standardized way.
- Plan for ongoing updates and maintenance:
  - Establish a schedule for updating metadata as new data are added; implement a change notification mechanism for downstream users.
  - Align data documentation with the needs of data users, ensuring accessibility for data creators, data users, and governance teams.
- Engage stakeholders:
  - Maintain active contact points (Sabine Reinsch, Bridget Emmett) for data requests, clarifications, and governance decisions.
  - Consider a governance review to ensure compliance with data standards and repository requirements, given the legacy data and long-term nature of the experiment.