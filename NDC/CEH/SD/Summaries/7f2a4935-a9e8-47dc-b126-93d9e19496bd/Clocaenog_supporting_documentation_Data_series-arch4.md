Climoor field site in Clocaenog forest Supporting documentation for data

## Overview
- A climate change manipulation experiment at Clocaenog Forest, North East Wales, using automated roof technology to simulate drought and warming over the next 20–30 years.
- Established in 1998 on upland moorland dominated by Calluna vulgaris (heather); aims to reflect future climate predictions.
- Experiment comprises replicated drought and warming treatments plus control plots, with 9 total plots arranged in blocks.
- Data span a wide range of abiotic and biotic measurements collected over many years.

## Data streams and datasets
- AWS meteorological data (daily, 1999–present): air temperature, humidity, rainfall, solar and net radiation, PAR, wind, pressure.
- Micro-meteorological plot data (daily, 1998–present): soil/air temperature, soil moisture.
- Rainfall and rainfall chemistry (biweekly to monthly, 1998–present): site-level rainfall and chemical constituents (pH, nitrate, chloride, sulfate, DOC, ammonium).
- Throughfall data (biweekly, 1999–present): plot-level rainfall; used to derive treatment-specific rainfall changes.
- Water table depth (biweekly, 2009–present): groundwater depths in plots.
- Soil respiration (fortnightly and automated data, 1998–present): CO2 efflux from plot collars; multiple measurement systems over time.
- Trace gases (CH4 and N2O; 1999–2000, 2007–2009): fluxes using static chambers and GC analysis.
- Net ecosystem CO2 exchange (NEE; 2002–2004, 2011): chamber-based CO2 flux; includes respiration adjustments via biomass data.
- Photosynthesis (2001–2003): leaf-level measurements using CIRAS-2 and leaf spectral standardization.
- Vegetation survey data (pin-point biomass; 1998–2012, with gaps): species- and life-form-specific biomass estimates; conversion from pin hits to biomass.
- Canopy reflectance (2000–2004; 2001–2002, 2003–2004): NDVI and PRI metrics from ground-based spectroscopy.
- Vegetation phenology, annual growth and pathogen assessment (1998–present): shoot elongation, budburst, leaf counts, flowering; herbivory and disease observations.
- Vegetation chemistry (1998–present): elemental analyses (C, N, P, K, Ca, Mg, lignin, tannin, alpha-cellulose, carbohydrates) on green and senesced material.
- Litterfall (1999–2002; later years): monthly to yearly collection; biomass and C/N analyses.
- Root biomass (2003–2013): soil core extractions and WinRHIZO analysis; varying methodologies over years.
- Soil microbial biomass (2000–2001, 2012): chloroform fumigation with DOC measurement; biomass derived from fumigated vs. unfumigated samples.
- Nitrogen mineralisation (1998–2004): incubation cores with nitrate and ammonium analyses.
- SOM, SOC and bulk density (1999–2004, 2013): core-based soil carbon and density assessments; SOM/C) and conversion to g m^-2.
- Soil solution and leachate chemistry (1998–2008): lysimeter and tension lysimeters; pH, NO3, Cl, SO4, DOC, NH4 analyses.
- Appendix materials: site and plot layouts.

## Data provenance, methods and processing
- Data collected via multiple instruments and methods across time; measurement frequencies range from daily to annual.
- Unit conversions and cross-method harmonization documented (e.g., soil respiration conversions between CIRAS-2 and LI-COR outputs; NEE to mg CO2-C m^-2 h^-1).
- Legacy data include some incomplete documentation of data processing; best-practice documentation exists for many datasets, with some notes referencing older workflows.
- Data processing approaches include biomass-adjusted NEE/NEE-derived photosynthesis, pin-hit to biomass calibrations, and standard lab analyses for chemical constituents.

## Data management, quality and metadata
- On-site AWS and plot data are stored as CSVs (with separate supporting documentation in RTF/appendices); not all data are stored in a single centralized repository (some data noted as not stored in EIDC).
- Quality control reported as visual checks in Excel; explicit automated quality thresholds are not consistently applied across legacy datasets.
- Metadata cover sensor types, units, sampling frequency, time scales, and measurement locations; some datasets include detailed methodological notes (e.g., chamber dimensions, calibration, correction factors).

## Access, sharing and governance
- Datasets are available as named data files (e.g., Daily automated weather station data_1999to2015_Clocaenog.csv, Throughfall_Clocaenog.csv, etc.).
- For access or additional details, contact CEH Bangor researchers (e.g., Sabine Reinsch, Bridget Emmett); note that some data are not currently centralized in EIDC.
- Contact points and dataset-specific supporting docs provide guidance on data provenance and usage.

## Challenges and considerations for Data Leaders
- Data are highly multi-dimensional and span several decades, with evolving instrumentation and methods.
- Data are fragmented across many datasets; inconsistent or incomplete documentation for some legacy processing.
- Throughfall, soil solution, and trace gas datasets require careful reconciliation between plot-level and site-level measurements.
- Long-term data stewardship risks include gaps, changes in measurement protocols, and limited centralized metadata.

## Recommendations for data governance and exploitation
- Create a unified data catalog and metadata schema covering all datasets, with standardized units, data types, and versioning.
- Develop a central data repository (or clearly documented access layer) to enhance discoverability and discoverable lineage across datasets.
- Establish data provenance records linking datasets to measurement methods, instruments, calibrations, and processing scripts.
- Implement data quality controls, including automated validation where feasible, and document data processing steps for legacy records.
- Foster data stewardship and co-ownership: engage cross-disciplinary teams and external partners to align data products with user needs and to support broader data sharing within networks.
- Produce data products and cross-dataset analyses (e.g., climate response across soil and vegetation metrics, long-term C and N flux budgets) to maximize value for data leaders managing complex systems.