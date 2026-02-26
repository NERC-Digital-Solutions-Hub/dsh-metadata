# Materials and methods, and metadata for Global data for soil water, groundwater and riverine freshwater DO14C data taken from 'Linking soil solution and riverine DO14C to soil carbon turnover', Adams et al, 2019 Biogeochemistry.

## Overview
- Compiles global data on dissolved organic carbon (DOC) concentrations and DO14C (radiocarbon content) in soil water, groundwater, and riverine freshwater.
- Data sources include literature compilations (1989–2015 for soil solution, 1988–2008 for groundwater, and river data extended to 1962–2015) with digitised graphed results where needed.
- Adds new UK river measurements (2013–2015) and details robust laboratory processing, isotopic analyses, and metadata to support cross-system carbon turnover studies.

## Data scope and content
- DOC and DO14C data by compartment:
  - Soil water DOC concentration [DOC] and DO14C
  - Groundwater [DOC], δ13C, and delta14C
  - Riverine surface water [DOC], δ13C, and delta14C
- Time coverage:
  - Soil: 1989–2015
  - Groundwater: 1988–2008
  - Rivers: 1962–2015 (with literature data and extended sampling)
- Data sources and provenance:
  - Literature data compiled from multiple studies; river data based on Marwick et al. (2015) with additional literature
  - Some river data digitised from graphs using ENGAUGE digitiser
  - River discharge data collected where available
- New measurements (TableS3_River_Surface_Water_New):
  - UK river sampling 2013–2015 by CEH, JHI, and UEA
  - Rigorous sampling and lab practices to ensure radiocarbon integrity
  - DOC concentrations measured with elemental analysers; isotopic analyses performed for 13C and 14C

## Methods and processing
- Sample collection and handling:
  - Freshwater samples collected in cleaned bottles; filtration prior to analysis
  - Filtration and sample handling performed in radiocarbon tracer–free laboratories
- Isotopic and radiocarbon analysis:
  - δ13C by dual-inlet mass spectrometry (correction using δ13C VPDB; generally precise to ±0.1‰)
  - DO14C measured by AMS after converting CO2 to graphite targets (iron/zinc reduction)
  - pMC values converted to Δ14C values; results decay-corrected to AD 1950 reference standard
  - Some samples required re-analysis with purge to lower pH to address carbonate contamination
- Quality control and calibration:
  - Standards and blanks run to ensure accuracy; use of international references
  - Calibration to ongoing radioactive decay of oxalic acid standard since AD 1950
  - Overall AMS precision around 0.45 pMC (range 0.35–0.70), with δ13C precision ~±0.1‰
- Data processing and corrections:
  - Where necessary, δ13C values obtained during AMS if mass spectrometry failed and corrected to δ13C = -25 ‰ VPDB
  - Data adjusted for carbonate purge failures; graphite targets prepared via established reduction methods
- Statistical treatment:
  - All analyses (t-tests, linear regressions) performed in Microsoft Excel
  - Normality and homoscedasticity checked; log-transform applied if needed

## Data structure and metadata
- Column heading explanations (CSV metadata):
  - TableS1_Soil_water_data.csv: Location, Country, lat/long, date, vegetation, Land_class, soil, depth_cm, [DOC], 13C, delta14C, Note, Reference
  - TableS2_Groundwater_data.csv: Location, Country, lat/long, Date_yr, aquifer, [DOC], 13C, delta14C, Note, Reference
  - TableS3_River_Surface_Water_New.csv: Data_line, Country_or_Region, Site, year, Lat, Long, [DOC]_mg/L, delta13C_‰, delta14C_‰, Land_class, Publication_code
  - TableS3_Marwick_River_Surface_Water.csv: Data_line and related river data fields
  - TableS3_Extra_Published_River_Surface_Water_Data.csv: Country_or_Region, Site, year, Site Lat, year Long, [DOC]_mg/L, delta13C_‰, delta14C_‰, Land_class, References
- Units and data types:
  - [DOC] in mg/L
  - δ13C in ‰
  - Δ14C in ‰
  - Location metadata includes site name, country, latitude/longitude, sampling date
- Land-use classifications:
  - Pure status requires at least 90% vegetation type (forest or wetland)
  - NSN category covers mixed landscapes, not fertilised
  - Land_class and discharge data used to support specific hypotheses only when quantified

## Site classification and data governance
- Land classification scheme applied to sampling sites to enable cross-site comparisons
- Discharge data linked to certain analyses; qualitative land-use categories used with caution
- Data lineage emphasizes compilation from literature and rigorous new measurements, with extensive methodological documentation for reproducibility

## Data quality, limitations, and challenges
- Heterogeneous data sources with varying completeness; digitisation required for some river data
- Carbonate contamination and purge efficiency can affect DO14C accuracy; some samples re-analyzed under stricter purge conditions
- Data integration across compartments (soil, groundwater, rivers) requires careful alignment of units, standards, and correction factors
- Access implications not explicitly discussed; data are described with comprehensive metadata to facilitate discoverability and reuse

## Access and reuse considerations for Data Leaders
- Rich, well-documented metadata supports discoverability, provenance tracking, and cross-study reuse
- Standardized units and correction protocols enable cross-compartment integration and comparative analytics
- Data lineage references a wide network of primary sources, enabling traceability and replication
- Processing details (sample handling, lab methods, calibration, and quality control) provide a strong blueprint for implementing similar end-to-end data pipelines in organizational data programs