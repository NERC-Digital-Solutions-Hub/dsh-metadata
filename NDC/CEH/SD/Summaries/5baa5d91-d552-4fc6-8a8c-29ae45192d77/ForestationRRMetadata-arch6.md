# Partial river flow recovery with forest age is rare in the decades following establishment

## What this dataset is
- A systematic review–based dataset addressing how forest age affects river flow after forestation.
- Contains annual river-flow change data, with comparisons to control (pre-forestation land cover) and metadata from primary and secondary sources.
- Data products: two CSV files
  - Forestation_RR_Bibliography.csv (bibliographic data for the studies)
  - Forestation_RR_EffectSize.csv (extracted dataset of effect sizes)
- Acknowledgement and citation: Bentley, L. & Coomes, D. (2020) Global Change Biology; DOI 10.1111/gcb.14954

## What you can download
- Forestation_RR_Bibliography.csv: bibliographic fields for each primary data source (e.g., Source_ID, Author, Title, Source, Year, Volume, Issue, DOI).
- Forestation_RR_EffectSize.csv: compiled dataset with per-catchment details and river-flow data (e.g., Catchment_ID, Catchment_Name, Area_km2, MAP, Prior_LC, Establishment, Forest_Type, Hydro_Regime, Tree_Age, Experiment_type, Graphically_Extracted, Modified_Data, C_Type, T_Type, Data_Duration, T_Duration, C_Duration, Year, P_mm, Precipitation, Q_C, Q_T, RR_mm, RR_%).

## How the dataset was created
- Literature search: Web of Science (1900 to January 4, 2018); search terms covering forestation/afforestation/reforestation and catchment/river basin.
- Screening and inclusion: relevance screening on titles/abstracts, then full text; limited to hydrologically independent catchments; excluded studies with deforestation+forestation or non-independent catchments; included 43 catchment experiments from 567 sources.
- Data extraction: from primary papers and related reviews; extracted four data categories per experiment:
  - Catchment descriptors (e.g., area, MAP, prior land cover)
  - Treatment descriptors (e.g., forest type, year of planting)
  - Experiment descriptors (e.g., treatment duration, control data method)
  - Experimental data (time since planting, forest area by year, control/treatment river flow, annual precipitation, study year)
- Forest age: calculated as an area-weighted mean; when annual forest area changes were not reported, assumed constant rate between known years.
- Data quality and calibration:
  - Control river-flow data sometimes calibrated to enable comparability with forested data using linear regression against precipitation or forested river flow (pre-forestation data).
  - Climate data: annual precipitation and other climate variables sourced from primary data or CRU TS4.3 when not reported.
  - Catchment extents digitized; where unavailable, climate data drawn from a circle of equal area or from the catchment location.
  - Graphically reported data extracted with PlotDigitizer when needed.
- Longitudinal handling: for multiple sources in the same catchment, the longest available time series was used.

## Data structure and variables (reference to Tables 1–3)
- Table 1 (Bibliography data): variables describing each primary data source (Source_ID, AU, TI, SO, PY, VL, IS, SN, DI).
- Table 2 (Effect size data): per-catchment and per-study variables, including:
  - Catchment descriptors: Catchment_ID, Catchment_Name, Area_km2, Lat, Lon, MAP, Prior_LC, Prior_LU
  - Treatment descriptors: Establishment, Forest_Type_BN, Forest_Type_ED, Hydro_Regime, Tree_Age
  - Experiment descriptors: Experiment_type, Graphically_Extracted, Modified_Data
  - Data descriptors: Year, P_mm, P_mm_Source, C_Type, T_Type, Data_Set_Duration, T_Duration, C_Duration, Historically_forested, FC_PD, FA_WM
  - River-flow data: CQ_mm (control), TQ_mm (treatment), RR_mm (river flow response), RR_PD (response in %), plus climate variables CRUTS4_PET and CRUTS4_TMP
  - Geographic and context: Country
- Table 3: Search string details (used in Web of Science) to reproduce the literature search.

## Calibration and data processing details (Table 4)
- Calibration approaches depend on study design:
  - Single catchment vs Paired catchments
  - Whether pre-forestation data are present
  - Whether calibration uses historic paired river flows or post-forestation conditions
- Calibration options involve linear regression to predict control flow using precipitation or historic control-flow relationships; multiple calibration options are compared, and the calibration with the highest adjusted R2 is chosen.
- Calibration scenarios cover:
  - No calibration (raw extraction)
  - Calibration using pre-forestation data
  - Predictions of corrected control flow for comparison with forested catchment data

## Data access and citation
- Access: dataset downloadable via the Environmental Information Data Centre (EIDC) catalogue.
- Files: Forestation_RR_Bibliography.csv and Forestation_RR_EffectSize.csv.
- Citation: Bentley, L. & Coomes, D. (2020) Partial river flow recovery with forest age is rare in the decades following establishment. Global Change Biology. DOI 10.1111/gcb.14954

## Practical notes for data users (Data Support perspective)
- Suitability: useful for meta-analyses or cross-catchment comparisons of forestation effects on river flow over time and by forest age.
- Reusability: rich metadata enables filtering by forest type, establishment method, hydro regime, catchment size, and climatic context.
- Provenance and quality: clear documentation of data sources, calibration methods, and data extraction tools; explicit handling of uncertainties and data gaps.
- Limitations to consider: reliance on published data and digitized values; potential biases despite calibration; variability in study designs and reporting across catchments.

## How this supports data-use and sharing
- Provides both bibliographic context and harmonized effect-size data for cross-study comparisons.
- Facilitates end-user exploration through structured variables (e.g., by forest age, forest type, or catchment characteristics).
- Clear citation and data-use guidance to promote reproducibility and proper attribution.