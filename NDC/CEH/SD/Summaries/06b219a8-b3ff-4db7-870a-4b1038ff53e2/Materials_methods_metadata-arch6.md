# Materials and methods, and metadata for Global data for soil water, groundwater and riverine freshwater DO14C data taken from 'Linking soil solution and riverine DO14C to soil carbon turnover', Adams et al, 2019 Biogeochemistry.

## Overview
- Compiles global data for dissolved organic carbon (DOC) concentration, DOC isotopic composition (δ13C), and radiocarbon content (Δ14C) in soil water, groundwater, and riverine freshwater.
- Literature data cover soil solution (1989–2015) and groundwater (1988–2008); river data built on Marwick et al. 2015 with additional records to 1962–2015.
- New UK river surface-water measurements collected 2013–2015 to extend coverage; data digitised from graphs when needed and integrated with existing datasets.
- Includes associated river discharge data for select sites and extensive metadata to support data use and cross-study comparisons.

## Data sources and coverage
- Literature sources for soil water and groundwater: DOC concentration ([DOC]), δ13C, and Δ14C data (1989–2015 for soil water; 1988–2008 for groundwater).
- River data foundation: Marwick et al. (2015) with additions to extend temporal coverage to 1962–2015; some data digitised from published figures using Engauge Digitizer.
- River discharge data included where available for single-site, multi-observation records.
- New measurements (TableS3_River_Surface_Water_New): UK rivers sampled 2013–2015 by CEH, JHI, and UEA; archived samples from Norwegian and US rivers from the 1960s–1970s also included.

## Methods and laboratory workflow
- Sample collection and processing for new river samples:
  - Use new or acid-washed equipment; samples filtered through pre-combusted or quartz-fibre filters; filtrates stored in clean bottles.
  - DOC concentrations measured with Vario EL elemental analyser and Thermo Flash 2000 at respective labs.
  - CO2 liberated from treated samples analysed for radiocarbon at SUERC (East Kilbride) after carbonate removal and purification.
- Isotopic measurements and calibrations:
  - δ13C determined by dual-inlet mass spectrometry (Thermo Fisher Delta V) with VPDB scale; precision about ±0.1 ‰.
  - Where purge incomplete (high δ13C values), re-analyses conducted purging to lower pH (to pH 2) and δ13C values sometimes adjusted or omitted if not representative.
  - Radiocarbon dating performed by AMS at SUERC; results expressed as percent modern (pMC) and converted to Δ14C values; international standards (oxalic acid) used for decay correction since AD 1950.
  - Graphite targets for 14C analysis prepared by iron/zinc reduction from recovered CO2; five samples required δ13C-derived corrections in lieu of direct 13C measurements during AMS.
  - Overall analytical precision reported as average 0.45 pMC (range 0.35–0.70).
- Data processing and quality control:
  - Results decay-corrected to account for time between sampling and analysis.
  - Process controls and standards used to verify accuracy and precision; calibration to modern standard defined as 100% modern (pMC).
  - For some samples, δ13C values obtained during AMS were used to correct Δ14C when direct δ13C measurements were not representative; these δ13C values were not considered representative of the original combusted material.

## Data structure and metadata
- Tables and associated column explanations:
  - TableS1_Soil_water_data.csv: site-level data including Location, Country, lat, long, date_yr, vegetation, Land_class, soil, depth_cm, [DOC], 13C, delta14C, Note, Reference.
  - TableS2_Groundwater_data.csv: groundwater site data including Location, Country, lat, long, Date_yr, aquifer, [DOC], 13C, delta14C, Note, Reference.
  - TableS3_River_Surface_Water_New.csv: new UK river data with Data_line, Country_or_Region, Site, year, Lat, Long, [DOC]_mg/L, delta13C_‰, delta14C_‰, Land_class, Publication_code.
  - TableS3_Marwick_River_Surface_Water.csv: river data from Marwick et al. (2015) and related sources.
  - TableS3_Extra_Published_River_Surface_Water_Data.csv: additional published river surface-water data.
- Column definitions and unit conventions are provided within the dataset documentation (including text descriptions, units such as mg/L for [DOC], ‰ for δ13C and Δ14C, and year fields).
- Land classification and site purity:
  - Pure status requires at least 90% of vegetation type (forest or wetland) in the catchment.
  - NSN category covers natural or semi-natural landscapes (e.g., mixed landscapes, ungrazed grasslands, heathlands).
  - Discharge data used to test specific hypotheses only when quantified.

## Site information and classification
- Site metadata includes location coordinates, country, vegetation type, land use classification, soil type, depth of sampling, and sample-specific notes.
- Land use and catchment characteristics (Land_class) linked to TABLES for understanding carbon sources and transport pathways.

## Statistical and data-use considerations
- Statistical analyses (t-tests and linear regressions) conducted in Excel.
- Data normality and homoscedasticity checked; transformations applied as needed.
- Data and metadata are designed to support cross-study comparisons, data discovery, and the creation of data products (e.g., self-serve dashboards, charts, and analyses) by Data Support teams.

## References and data provenance
- Core data sources and methodological references include:
  - Engauge Digitizer for digitising graphed results.
  - Radiocarbon laboratories and calibration standards (SUERC AMS facility; oxalic acid standard).
  - Foundational studies and datasets: Marwick et al. 2015; PROTOS project outputs; various riverine carbon isotopic studies cited in the references.
- Detailed references accompany Tables S1, S2, and S3 datasets, including major works by Buckingham, Mulder, Raymond, Teodoru, and many others, spanning soil to riverine carbon turnover and isotopic analyses.

## Accessibility and intended use
- Data and accompanying metadata are provided to enable re-use, re-annotation, and integration with other data products.
- The materials support exploration of soil-to-river carbon turnover through DO14C and associated isotope data across multiple reservoirs (soil water, groundwater, rivers).
- Designed to aid Data Support activities in understanding data provenance, quality, and applicability for policy, environmental monitoring, and research dissemination.