# Partial river flow recovery with forest age is rare in the decades following establishment

- Purpose and scope
  - A dataset produced via systematic review to address how forestation and forest age influence river flow over time.
  - Focuses on annual river flow responses, with comparisons to control river flow and associated metadata from primary and secondary sources.
  - Aimed at enabling analysis of spatially explicit catchment responses to forestation.

- Data sources and access
  - Systematic literature search of Web of Science (1990-01-01 to 2018-01-04).
  - Identified 567 unique data sources; 43 catchment experiments met strict inclusion criteria.
  - Data downloadable from the EIDC catalogue; two associated CSV files:
    - Forestation_RR_Bibliography.csv (bibliographic data)
    - Forestation_RR_EffectSize.csv (extracted dataset)
  - Acknowledgement and citation guidance provided for use and reproduction.

- Study design and selection criteria
  - Accepted designs: single catchment experiments and paired catchment experiments.
  - Excluded: studies with deforestation plus forestation, non-hydrologically independent catchments, retrospective causes of observed declines, or overlapping data with shorter time series when longer series exist.
  - Data inclusion intended to minimize confounding variables related to climate and catchment differences.

- Data collection and processing (beginning and middle sections)
  - Four data categories extracted per experiment:
    - Catchment descriptors (e.g., area, MAP, prior land cover).
    - Treatment descriptors (forest type, year of planting).
    - Experiment descriptors (treatment duration, method to produce control data).
    - Experimental data (time since planting, forest area planted per year, control and forested river flow, annual precipitation, hydrological year).
  - Requirements:
    - Forest age known over time; percent catchment forested reported.
    - If annual change in forest area was not reported, assumed constant.
    - Forest age calculated as an area-weighted mean to reflect multi-year establishment.
  - Spatial and geographic data handling:
    - Catchment extents digitised; where insufficient data for digitisation, climate data sampled from a circle of equal area around the catchment or from the catchment location.
    - Geographic coordinates (lat, lon) recorded for forested catchments.
  - Data extraction from figures:
    - Graphical data extracted using PlotDigitizer.

- Climate and data calibration (middle section)
  - Control river flow data were sometimes calibrated to align with forested catchment conditions.
  - Calibrations used linear regressions relating control flow to precipitation or forested flow based on pre-forestation data; alternatives included using CRU TS4.3 climate data when local data were unavailable.
  - When necessary, precipitation data were derived from CRU TS4 and used to compute ancillary climate variables (PET, mean annual temperature).
  - In cases with insufficient data to digitise catchment extent, sampling strategies ensured representative climate inputs across catchments.

- Variables and data structure (Tables)
  - Table 1: Variable descriptions for Forestation_RR_Bibliography.csv (bibliographic fields: AU, TI, SO, PY, etc.).
  - Table 2: Variable descriptions for Forestation_RR_EffectSize.csv (catchment-level and experimental variables):
    - Catchment_ID, Catchment_Name, Area_km2, Lat, Lon, MAP, Prior_LC, Prior_LU, Establishment, Forest_Type_BN, Forest_Type_ED, Hydro_Regime, Tree_Age, Experiment_type, Graphically_Extracted, Modified_Data, C_Type, T_Type, Data_Set_Duration, T_Duration, C_Duration, Historically_forested, FC_PD, FA_WM, Year, P_mm, P_mm_Source, CQ_mm, TQ_mm, RR_mm, RR_PD, Country, CRUTS4_PET, CRUTS4_TMP, etc.
  - Table 3: Search string details used in Web of Science (for TS queries related to forestation and catchments).
  - Table 4: Description of control river flow calibration methods (least-squares regression options and calibration strategies across single vs paired catchments, pre-forestation data presence, and scenarios for predicting corrected control flow).

- Data contents and interpretation (end sections)
  - Data set composition:
    - Forestation_RR_Bibliography.csv contains bibliographic metadata for the primary data sources.
    - Forestation_RR_EffectSize.csv contains per-catchment, per-experiment data including spatial, climatic, land-cover, forestation, and hydrological variables.
  - Key derived metrics:
    - RR_mm: river flow response to forestation (forest flow minus control flow, in mm).
    - RR_PD: river flow response as a percentage of control flow.
    - FC_PD: percentage of catchment area forested relative to pre-forestation land cover.
    - FA_WM: forest age, area-weighted mean when age is not uniform.
  - Time coverage:
    - Includes data on years since first planting and the duration of river flow records for both treatment and control catchments.

- Practical notes for GIS and data use
  - Catchment-scale data with coordinates and extents enable spatial analyses of forestation effects on river flow.
  - Data harmonization steps (calibration, climate data sourcing, and catchment extent digitisation) are documented to support reproducibility.
  - Where data were graphically extracted, metadata indicate extraction method to inform uncertainty.

- Acknowledgement, usage, and citation
  - Users should cite Bentley, L. & Coomes, D. (2020) Partial river flow recovery with forest age is rare in the decades following establishment. Global Change Biology. DOI 10.1111/gcb.14954
  - Access via the EIDC catalogue; data intended for informing GIS-based analyses of forestation and hydrological responses.

- Related references
  - Farley, K. A., Jobbágy, E. G., & Jackson, R. B. (2005). Effects of afforestation on water yield: A global synthesis with implications for policy.
  - Harris, I. et al. (2014). CRU TS4 climate data.
  - Plot Digitizer (Huwaldt, 2015) used for graphical data extraction.