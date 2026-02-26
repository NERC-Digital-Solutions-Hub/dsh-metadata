# Materials and methods, and metadata for Global data for soil water, groundwater and riverine freshwater DO14C data taken from 'Linking soil solution and riverine DO14C to soil carbon turnover', Adams et al, 2019 Biogeochemistry.

## Overview
- Compiles global data on dissolved organic carbon (DOC) concentration and DO14C in soil water, groundwater, and riverine freshwater.
- Builds on Adams et al. 2019 Biogeochemistry; combines literature data with new UK river water measurements (2013–2015).
- Provides accompanying metadata and column definitions to enable standardized use and cross-study comparisons.
- Aims to create reusable datasets suitable for environmental monitoring and policy-relevant analyses, with data storage and portal deposition.

## Data Coverage
- Soil water: DOC concentration [DOC] and DO14C data from 1989–2015.
- Groundwater: [DOC], 13C, and delta14C data from 1988–2008.
- Rivers: DO14C data extended to 1962–2015; builds on Marwick et al. (2015) with additional pre/post-2015 data.
- New river surface-water measurements (UK): 2013–2015.
- River data sources include archived Norwegian and US river samples from the 1960s–1970s.
- Land classifications and site discharge data used to interpret results where available.

## Data Creation and Sources
- Literature data
  - Compiled DOC concentration and DO14C for soil solutions (1989–2015) and groundwater (1988–2008).
  - For rivers, based on Marwick et al. (2015) and expanded with additional data to 2015.
  - Data extraction often required digitising graphed results (ENGAUGE).
  - River discharge data collected where available.
- New measurements (TableS3_River_Surface_Water_New)
  - UK sampling by CEH, JHI, and UEA (2013–2015) with strict contamination controls.
  - Protocols for sampling bottles, filtration, and laboratory processing are described in detail.
  - Radiocarbon analyses performed at the SUERC AMS facility; CO2 recovered and converted to graphite targets for AMS.
  - 13C corrections and calibrations performed; δ13C values used to correct DO14C where applicable.
  - Some samples required re-analysis to ensure purge of inorganic carbon (adjusted pH as needed).
- Site information and land classification
  - Sites categorized by land_class (e.g., pure forests, wetlands, NSN natural or semi-natural landscapes) using a consistent scheme.
  - 90% vegetation criterion used for pure status; NSN covers mixed landscapes without fertilisation.
  - Discharge data used to test hypotheses only when quantified.

## Analytical Methods and Quality Assurance
- Statistical analyses
  - Performed in Microsoft Excel.
  - T-tests and linear regressions; tests for normality and equal variances; log-transformations applied when needed.
- Radiocarbon and isotope analyses
  - DO14C data converted from pMC to Δ14C values; corrections applied for radioactive decay since AD 1950.
  - 13C corrections performed using dual-inlet mass spectrometry for most samples; when 13C results were problematic, alternative corrections were used, with notes on representativeness.
  - Analytical precision summarized: ~0.45 pMC (range 0.35–0.70) per sample, reflecting AMS statistics and lab processing uncertainties.
  - Purging and acid fumigation steps used to remove inorganic carbon; strict laboratory contamination controls (radiocarbon-tracer free labs).
- Data handling
  - All data undergo quality assurance and standardised transformations before inclusion in the respective CSV tables.
  - Metadata and column definitions standardized to facilitate cross-study integration.

## Datasets and Metadata Files
- TableS1_Soil_water_data.csv
  - Columns include: Location, Country, lat, long, date_yr, vegetation, Land_class, soil, depth_cm, [DOC], 13C, delta14C, Note, Reference.
  - Column heading explanations provided (Location, Country, lat, long, date_yr, vegetation, Land_class, soil, depth_cm, [DOC], 13C, delta14C, Note, Reference).
- TableS2_Groundwater_data.csv
  - Columns include: Location, Country, lat, long, Date_yr, aquifer, [DOC], 13C, delta14C, Note, Reference.
  - Column heading explanations provided (Location, Country, lat, long, Date_yr, aquifer, [DOC], 13C, delta14C, Note, Reference).
- TableS3_River_Surface_Water_New.csv
  - Columns include: Data_line, Country_or_Region, Site, year, Lat, Long, [DOC]_mg/L, delta13C_‰, delta14C_‰, Land_class, Publication_code.
  - Column heading explanations provided (Data_line, Country_or_Region, Site, year, Lat, Long, [DOC]_mg/L, delta13C_‰, delta14C_‰, Land_class, Publication_code).
- TableS3_Marwick_River_Surface_Water.csv
  - Data_line and related River surface-water DO14C data with publication lineage; column explanations provided.
- TableS3_Extra_Published_River_Surface_Water_Data.csv
  - Additional published river surface-water DO14C and related data; column explanations provided.
- References
  - Comprehensive citation list for table-specific data sources (Marwick et al. 2015; various radiocarbon/isotope studies; archival data).

## Data Integration, Access, and Reuse
- Standardized data formats and metadata enable cross-dataset integration for environmental monitoring and policy performance assessments.
- Datasets are prepared with clear provenance (original publications, theses, and new UK measurements) to support traceability.
- Aims to enhance reuse by enabling access to underlying data and enabling combination with other environmental datasets; data are intended for upload to appropriate data portals.

## Notes and caveats
- For five river samples, δ13C values indicated residual inorganic carbon; δ13C corrections were not considered representative for those cases.
- pMC values were converted to Δ14C with standard decay corrections; where data limitations existed, authors provide details on adjustments and uncertainties.