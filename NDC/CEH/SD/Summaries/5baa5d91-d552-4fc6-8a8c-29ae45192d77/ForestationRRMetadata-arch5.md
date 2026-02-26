# Partial river flow recovery with forest age is rare in the decades following establishment

## Overview
- Purpose: A dataset from a systematic review examining how forest age affects river flow after forestation, including annual river flow changes and accompanying metadata from primary and secondary sources.
- Scope: 43 catchment experiments identified from 567 sources; includes single and paired catchment designs; excludes studies with deforestation plus forestation and nested catchments; aims to minimize confounding factors and publication bias.
- Access: Datasets available via the EIDC catalogue; two files provided (Forestation_RR_Bibliography.csv and Forestation_RR_EffectSize.csv); citations should reference Bentley & Coomes (2020).

## Data Content and Structure
- Files and purpose:
  - Forestation_RR_Bibliography.csv: bibliographic data for the studies used (Source_ID, Author, Title, Source, Year, etc.).
  - Forestation_RR_EffectSize.csv: extracted and harmonized effect-size data with detailed catchment and study descriptors.
- Variables (Tables 1 and 2):
  - Catchment descriptors: Area_km2, MAP (mean annual precipitation), Prior_LC (land cover prior to forestation), Prior_LU (land use prior to forestation), Historic foresting status.
  - Treatment descriptors: Establishment method (Natural, Planted, Mixed), Forest_Type_BN (Broadleaf/Needleleaf), Forest_Type_ED (narrowed type), Forestation year, establishment details.
  - Experimental descriptors: Treatment duration, method for control data (C_Type), method for treatment data (T_Type), data graphically extracted, data modification flags (Modified_Data).
  - Experimental data: Time since first planting, area planted per year, control river flow (CQ_mm), forested river flow (TQ_mm), annual precipitation (P_mm), hydrological year.
  - Derived/derived-credible fields: Forest age (FA_WM) as area-weighted mean, RR_mm (river flow response: TQ - CQ), RR_PD (percentage response), FC_PD (percent catchment forested), P_mm sources (Primary or CRU TS), climate variables (PET, TMP).
- Data collection and processing details:
  - Forest age calculated as an area-weighted mean to handle non-uniform forest establishment.
  - When necessary, catchment extents and climate data (CRU TS4.x) were digitized or interpolated; where data were insufficient for digitization, alternative sampling extents were used.
  - Graphical data were digitized with PlotDigitizer; multiple calculations and calibrations were applied to align control data with forested conditions.

## Data Provenance, Calibration, and Processing
- Literature search and selection:
  - Web of Science search (1990–Jan 4, 2018) to identify catchment studies on forestation effects on river flow over time.
  - Screening by titles/abstracts, then full text; access to non-online papers via libraries.
  - Inclusion criteria ensured hydrologically independent catchments; excluded retrospective cause-of-decrease analyses and non-independent data.
- Data extraction and harmonization:
  - Four data categories extracted per experiment: catchment descriptors, treatment descriptors, experiment descriptors, and experimental data (time since planting, forest area per year, flows, precipitation, etc.).
  - When multiple sources described the same catchment, the longest time series was used.
  - Data were calibrated to account for differences in climate and catchment conditions between forested and control data where needed.
- Calibration methods:
  - Calibration of control river flow where not originally comparable, using linear regression against precipitation or forested river flow prior to forestation.
  - Multiple calibration options documented (Single vs. Paired catchments; with/without pre-forestation data); the calibration with the highest adjusted R2 was selected.
  - Described in Table 4 (calibration strategies and equations), including how predicted corrected flows were generated.
- Documentation and reproduction:
  - Detailed variable descriptions provided (Tables 1 and 2).
  - For methodological transparency, tables list the exact search strings (Tables 3) and calibration descriptions (Table 4).
  - Core dataset described and published: Bentley & Coomes (2020) Global Change Biology; dataset accessible via EIDC.

## Quality, Limitations, and Governance Implications
- Quality and bias considerations:
  - Efforts to minimize bias by excluding studies that retrospectively investigate causes of known decreases in river flow.
  - Hydrologically independent catchments ensured; nested catchments excluded.
  - Where data were incomplete, proxies (CRU climate data) or digitization techniques were used, which may introduce uncertainties.
- Limitations to governance:
  - Calibrations depend on available data; variations in data reporting across studies can affect comparability.
  - Not all catchments may have complete pre-forestation data; some adjustments rely on modeling assumptions.
  - The dataset is historical (up to studies available by 2018) and may miss newer data unless updated.
- Stewardship considerations:
  - Metadata completeness is essential (Tables 1–2 provide variable descriptions; calibration methods are explicitly documented).
  - Versioning and provenance tracking are important to maintain traceability between source studies and harmonized records.
  - Open access via EIDC supports discoverability; clear citation guidance ensures proper reuse.

## Access, Citation, and Use Guidance
- Access: Data downloadable from the EIDC catalogue; two CSV files (Forestation_RR_Bibliography.csv and Forestation_RR_EffectSize.csv).
- Documentation: Comprehensive variable dictionaries (Tables 1 and 2) and calibration explanations (Table 4) accompany the dataset.
- Recommended citation: Bentley, L. & Coomes, D. (2020). Partial river flow recovery with forest age is rare in the decades following establishment. Global Change Biology. DOI 10.1111/gcb.14954
- Intended use: Enables meta-analysis and cross-study comparisons of how forest age and extent influence river flow, with explicit attention to the timing of forestation and the corresponding hydrological response. Suitable for researchers and data stewards aiming to assess or integrate governance around long-term hydrological datasets with forestation context.