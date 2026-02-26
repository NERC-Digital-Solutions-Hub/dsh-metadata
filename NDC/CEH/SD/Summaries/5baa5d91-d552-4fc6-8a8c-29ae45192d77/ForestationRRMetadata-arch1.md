# Partial river flow recovery with forest age is rare in the decades following establishment

- Purpose and scope
  - A dataset produced from a systematic literature review to assess how forest age after forestation influences river flow.
  - Focuses on annual river flow responses, with comparisons to control river flow and accompanying metadata from primary and secondary sources.
  - Produced by Laura Bentley and David A. Coomes (January 2018–October 2019).

- Data sources and study selection
  - Systematic search of the Web of Science (1990–4 January 2018) to identify catchment studies of forestation and river flow over time.
  - Initial set: 567 unique data sources; final inclusion: 43 unique catchment experiments (21 single catchment; 22 paired catchments).
  - Exclusion criteria: studies with deforestation+forestation treatments or hydrologically dependent catchments (nested within a study).
  - Effort to reduce publication bias: data from multiple sources per catchment chosen as the longest time series when available.

- Data collection and processing
  - Four data categories extracted per experiment:
    - Catchment descriptors (e.g., area, MAP, prior land cover).
    - Treatment descriptors (forest type, year of planting).
    - Experimental descriptors (treatment duration, method to construct the control dataset).
    - Experimental data (time since planting, annual forested area, control and forested river flow, precipitation, hydrological year).
  - Forest age
    - Calculated as an area-weighted mean to account for forests established over multiple years.
  - Forestry area changes
    - If year-to-year forest area change was not reported, assumed constant rate between known years.
  - Climate and catchment data
    - Precipitation data if not reported: extracted from CRU TS4.3 for the catchment location.
    - Catchment extents digitised; when insufficient data existed, climate data drawn from a circle of equal area or, for a single catchment, from the catchment location.
  - Data extraction methods
    - River flow data extracted from primary sources or digitised from graphs using PlotDigitizer.

- Data formats and variables
  - Bibliographic data sheet (Forestation_RR_Bibliography.csv): unique Source_ID, authors, title, source, year, volumes, DOI, etc.
  - Effect size data sheet (Forestation_RR_EffectSize.csv): detailed catchment-level variables including:
    - Catchment_ID, name, area (km2), geographic coordinates, MAP, Prior_LC, Prior_LU, Establishment method, Forest_Type, Hydro_Regime, Tree_Age, Experiment_type, Graphically_Extracted, Modified_Data, C_Type, T_Type, Data_Set_Duration, T_Duration, C_Duration, Historically_forested, FC_PD, FA_WM, Year, P_mm, P_mm_Source, CQ_mm, TQ_mm, RR_mm, RR_PD, Country, CRUTS4_PET, CRUTS4_TMP, etc.
  - Forest age (FA_WM) is an area-weighted mean; forestation extent (FC_PD) reported as a percentage of catchment forested.

- Calibration and analysis methods
  - Control river flow calibration to account for climate and catchment differences:
    - Linear regressions between control flow and precipitation or forested catchment flow prior to forestation.
    - Calibration approaches vary by study design (single vs. paired catchments) and data availability.
  - Calibration diagrams and options
    - Multiple calibration options described (observed vs predicted control data; with or without pre-forestation data; different regression specifications).
    - Calibration aims to align control data with forested catchment conditions for valid comparisons.
  - Data transformation for analysis
    - Where necessary, control data were recalibrated to reflect climatic conditions relevant to the forested catchment’s post-forestation period.

- Outputs and accessibility
  - Data produced to support analysis of how forest age affects river flow response after forestation.
  - Available via the EIDC catalogue with two files:
    - Forestation_RR_Bibliography.csv (study bibliographic metadata).
    - Forestation_RR_EffectSize.csv (catchment- and experiment-level data for river flow response).
  - Associated paper for detailed methodology and interpretation:
    - Bentley, L. & Coomes, D. (2020) Partial river flow recovery with forest age is rare in the decades following establishment. Global Change Biology. DOI 10.1111/gcb.14954.

- What this dataset enables for analysts
  - Assess correlations between forest age and river flow recovery across multiple catchments and forest types.
  - Compare treatment effects (forested vs. control) while controlling for precipitation and other climate variables.
  - Explore how study design (single vs paired catchments) and data calibration influence reported river flow responses.
  - Support predictive insights on whether older forests yield greater, lesser, or negligible changes in river flow over time. 

- Usage notes and citations
  - Use and cite Bentley, L. & Coomes, D. (2020) when referencing the dataset or analyses derived from it.
  - Data include potential limitations related to calibration choices, data availability, and catchment heterogeneity across studies.