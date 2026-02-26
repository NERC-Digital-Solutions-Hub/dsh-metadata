# Partial river flow recovery with forest age is rare in the decades following establishment

## Overview
- A dataset from a systematic review addressing how forest age influences river flow response after forestation.
- Contains annual river flow changes following forestation, with control river flow data and associated metadata from primary and secondary sources.
- Aims to inform policy and monitoring by evaluating temporal dynamics of water yield after forest establishment.

## Dataset contents and access
- Two associated files available from the EIDC catalogue:
  - Forestation_RR_Bibliography.csv (bibliographic data for included studies)
  - Forestation_RR_EffectSize.csv (extracted dataset with effect sizes)
- Variables described in Tables 1 and 2 of the description.
- Acknowledgement: cite Bentley & Coomes (2020) in Global Change Biology.

## Methods and data collection
- Literature search: Web of Science, 1900 to 4 January 2018; search strings provided; focus on forestation effects on river flow over time.
- Screening: relevance by titles/abstracts, then full text; sources without online access requested from libraries.
- Study selection: 567 unique sources identified; 43 unique catchment experiments meeting strict criteria; designs included single and paired catchments; hydrologically independent catchments required; mixed treatments (deforestation + forestation) excluded.
- Data extraction: four data categories per experiment:
  - Catchment descriptors (e.g., area, MAP, prior land cover)
  - Treatment descriptors (forest type, year of planting)
  - Experiment descriptors (treatment duration, control data method)
  - Experimental data (time since planting, forest area planted per year, river flows, precipitation, hydrological year)
- Forest age: calculated as an area-weighted mean; where data were graphically reported, data were digitized with PlotDigitizer.
- Climate data: precipitation and related variables sourced from primary data or CRU TS4.3 when necessary; catchment extents digitized or approximated as needed.

## Data structure and variables
- Table 2 describes key variables in Forestation_RR_EffectSize.csv, including:
  - Catchment attributes: area_km2, lat, lon, MAP
  - Land cover history: Prior_LC; Prior_LU
  - Forest establishment and type: Establishment, Forest_Type_BN, Forest_Type_ED
  - Hydro/climate context: Hydro_Regime, CRUTS4_PET, CRUTS4_TMP
  - Forest age and extent: FA_WM, FC_PD
  - Experimental design and data handling: Experiment_type, Graphically_Extracted, Modified_Data
  - Data duration fields: Data_Set_Duration, T_Duration, C_Duration
  - River flow data: CQ_mm (control), TQ_mm (treatment), RR_mm (response)
  - Additional contextual data: P_mm, P_mm_Source, Country
- Table 4 describes calibration methods used to adjust control river flow when needed (e.g., regression-based calibrations using precipitation or historic relationships).

## Calibration and data quality considerations
- Control flow data often calibrated to account for climate differences between forested and control catchments.
- Calibration options include single catchment or paired catchments designs, with or without pre-forestation data.
- The calibration approach chosen (e.g., regression between flow and precipitation) is selected based on data availability and model fit (adjusted R2).
- Some data were not calibrated; explanations and calibration options are documented to aid interpretation.

## Relevance for monitoring and policy
- Provides a harmonized, multi-study dataset enabling assessment of how forest age affects river flow over time after forestation.
- Highlights that partial river flow recovery with forest age is not universally observed, informing expectations for water yield changes following forestation.
- Demonstrates practical data integration steps (data extraction, calibration, metadata augmentation) that can guide monitoring frameworks dealing with heterogeneous data sources.
- Identifies data gaps and barriers common to environmental monitoring (metadata completeness, data sharing, cross-catchment comparability, and up-to-date datasets).

## Practical considerations and limitations
- Only 43 eligible catchment experiments among 567 sources; potential publication and selection biases exist.
- Data extraction from figures introduces potential uncertainties.
- Calibration relies on available precipitation data; some missing data required use of external climate datasets (CRU TS).
- Variability across catchments (historical forestry, land use, climate, hydro regime) limits generalizability; careful interpretation required when applying to policy contexts.

## How to use for decision-making
- Use to benchmark and monitor river flow responses to forestation across time since establishment.
- Supports design of monitoring programs by identifying essential metadata, data quality checks, and standardization needs.
- Informs policy discussions on anticipated water yield changes with forest age, highlighting that substantial recovery is not universal and is context-dependent.