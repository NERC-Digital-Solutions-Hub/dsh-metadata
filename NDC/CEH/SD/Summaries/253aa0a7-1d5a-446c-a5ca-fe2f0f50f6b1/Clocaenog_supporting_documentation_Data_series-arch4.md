# Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- Describes the Climoor climate change manipulation experiment at Clocaenog Forest, North East Wales, established in 1998.
- Uses automated roof technology to simulate drought and warming treatments reflecting 20–30 year climate predictions.
- Two main treatments (drought and warming) with three replicates each plus three control plots (total of 9 plots) arranged in a block design.
- Multiple data streams collected since 1998 across abiotic and biotic domains, with ongoing collection and various data processing histories.

## Data landscape and types
- AWS meteorological data: daily measurements of humidity, air temperature, rainfall, air pressure, net radiation, solar radiation, PAR, wind.
- Micro-meteorological plot data: daily soil and air temperatures, soil moisture (5, 10, 20 cm depths; later methods), hourly cadence.
- Rainfall data: site-level storage rain gauge (biweekly), rainfall chemistry from rain collectors (pH, NO3, Cl, SO4, DOC, ammonium).
- Throughfall data: plot-level rainfall (biweekly); used to derive treatment-specific rainfall changes.
- Water table depth: biweekly measurements via permeable tubes (down to bedrock).
- Soil respiration: fortnightly measurements with collars; multiple instrumentation over time (CIRAS-2, LICOR 8100, automated systems); converted to mg CO2-C m-2 h-1.
- Trace gases (CH4, N2O): measured with closed chambers and gas chromatography; sampling at multiple time points.
- Net ecosystem CO2 exchange (NEE): measured in several years with different chamber systems; includes adjustments for biomass differences.
- Photosynthesis: ambient and response-curve data (A vs PAR, A vs Ci) using CIRAS instruments; leaf-level measurements with biomass normalization.
- Vegetation survey data (plant biomass): Pin-point method in fixed quadrats; long-running biomass and cover data; annual updates with calibration from destructive sampling.
- Canopy reflectance: NDVI and PRI indices from ground-based spectrometry in select years.
- Vegetation phenology, annual growth, pathogens: shoot elongation, leaf counts, budburst, flowering status, herbivory and disease indicators.
- Vegetation chemistry: elemental analyses (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) on green and senesced material.
- Litterfall: monthly to yearly collections (1999–2002; later less frequent); conversion to g m-2 and subsequent chemical analyses.
- Root biomass: multiple cores and methods across years (2003–2013), including washing and Winrhizo analysis for biomass estimation.
- Soil microbial biomass: chloroform fumigation method (2000, 2001, 2012) with DOC-based calculations.
- Nitrogen mineralisation: periodic core sampling (1998–2004) with nitrate and ammonium analyses, enabling net mineralisation rate estimates.
- SOM, SOC and bulk density: cores analyzed for SOM and SOC with density calculations; conversions to g m-2.
- Soil solution and leachate chemistry: lysimeters and tensioned samplers; biweekly sampling; analyses for NO3, Cl, SO4, NH4, pH, DOC.

## Experimental design and data collection implications
- Treatments are scripted annually/seasonally with specific start and end dates, rain-shield mechanisms, and wind-exclusion considerations.
- Throughfall and rainfall adjustments applied to derive treatment-specific rainfall reductions.
- Equipment evolution over time (sensor types, data loggers, automation) affects data consistency and requires careful provenance tracking.
- Spatial layout and quadrat mapping documented in appendices; site and plot layout provide essential context for spatial analyses.

## Data management, storage, and accessibility
- Data are collected via on-site AWS and plot sensors, and stored in various formats and locations.
- Not all data are stored in a central repository (EIDC); contact details provided for data access and provenance: Sabine Reinsch and Bridget Emmett at CEH Bangor.
- Appendix materials detail plot and quadrat layouts, supporting spatial data integration.
- Legacy data documentation varies in completeness; explicit data processing notes exist for several datasets, including unit conversions and calibration factors.

## Data quality, processing, and limitations
- Quality control primarily through manual visual checks in Excel; recognizes limitations of automated limits for unusual conditions.
- Throughfall data handling includes exclusion criteria when measurements are compromised; occasional data infilling applied.
- Multiple measurement technologies over time require careful harmonization (e.g., Rs calculations, unit conversions).
- Some datasets are infrequent or sporadic (legacy data); best-practice documentation not consistently followed across all periods.

## Metadata, standards, and documentation
- Data descriptors include sensor types, measurement frequency, time scales, and processing notes (e.g., RS units, conversion factors, and measurement intervals).
- Specific conversion formulas are provided for key datasets (e.g., soil respiration from g CO2 m-2 h-1 and µmol m-2 s-1 to mg CO2-C m-2 h-1), facilitating re-use.
- Datasets are identified by structured file names and dataset descriptions; Appendix 1–3 provide site-level context and plotting details.

## Implications for data leadership and governance
- The Climoor dataset represents a rich, multi-decadal asset with diverse observational streams requiring strong data governance.
- Key needs include: centralized metadata cataloging, standardized data formats, explicit data lineage, and robust versioning to accommodate evolving instrumentation and methodologies.
- Given legacy data gaps and heterogeneous processing histories, implement clear data curation policy, documentation of processing steps, and data quality flags for each dataset.
- Ensure long-term preservation, interoperability, and discoverability to support cross-site analyses, meta-analyses, and policy-relevant research.

## Practical takeaways for Data Leaders
- Map the full data portfolio, including provenance, sensors, time coverage, frequency, units, and processing methods.
- Establish a central, queryable data catalog with consistent naming conventions and metadata schemas across all data types.
- Implement standardized data ingests with validation rules, unit conversion checks, and calibration traceability.
- Maintain comprehensive documentation for legacy datasets and ensure ongoing documentation for new data streams.
- Facilitate data discoverability and access by clearly publishing contact points and data-use terms; consider partnerships with CEH Bangor for data access.
- Plan for ongoing data governance, including data quality monitoring, error handling, and data revision policies to maximize data reuse and reliability.