# Please note that the units used in the data base are as listed below.

## Overview
- Defines the mapping of database column names (Column 1) to the units used for stored values (Column 2).
- Notes that database units may differ from units quoted by chemical analysts, as referenced by the external metadata file: Metadata_Analytical methods_conwy catchment spatial water chemistry.xlsx.

## Data Structure and Units
- Variables cover site identifiers and sampling details:
  - Master_Site, Site_Code, Date, Rep
- Chemical measurements and related qualifiers (examples):
  - CaQual, Ca (units: ueq/l)
  - MgQual, Mg (units: ueq/l)
  - NaQual, Na (units: ueq/l)
  - ClQual, Cl (units: ueq/l)
  - NO3Qual, NO3 (units: ueq/l)
  - NH4Qual, NH4 (units: ueq/l)
  - NO2Qual, NO2 (units: ueq/l)
  - DOCQual, DOC (units not explicitly stated; context implies common water chemistry units)
  - pHQual, pH (pH)
  - AlkalinityQual, Alkalinity (units: ueq/l)
  - AlQual, Al (units: ug/l)
  - Total_NQual, Total_N (units not specified)
  - PO4_P, PO4_PQual (units: mg/l)
  - TON, TONQual (units: mg/l)
  - ConductivityQual, Conductivity (units: us/cm)
  - SiQual, Si (units: mg/l)
  - FeQual, Fe (units: ug/l)
  - POMQual (units: mg/l)
  - POCQual (units: mg/l)
  - SalinityQual (units: mg/l)
  - FQual (units: mg/l)
  - BrQual (units: unspecified)
  - TDPQual (units: mg/l)
  - LiQual (units: mg/l)
  - BeQual (units: ug/l)
  - Al27Qual (units: ug/l)
  - ScQual (units: ug/l)
  - VQual (units: ug/l)
  - CrQual (units: ug/l)
  - MnQual (units: ug/l)
  - Fe57Qual, Ni58Qual, Ni60Qual (units: ug/l)
  - CoQual, Ni (units: ug/l)
  - CuQual, ZnQual (units: ug/l)
  - AsQual, SeQual, RbQual, SrQual, MoQual, CdQual, SbQual, CsQual, BaQual, PbQual, UQual, BQual, SQual, LaQual, CeQual, PrQual, WQual, TiQual, SnQual (units: ug/l)
- Some entries show mixed or ambiguous formatting (e.g., multiple qualifiers per parameter, or parameters with both a measurement unit and a separate qualifier column). The pattern indicates a predominant use of:
  - ug/l for many trace/major metals and isotopes
  - mg/l for some nutrients and particulate matter
  - us/cm for conductivity
  - pH as a unitless scale
- Qualifier fields (e.g., CaQual, NO3Qual, etc.) accompany primary measurements to indicate data quality.

## Data Quality and Metadata
- Primary emphasis on verifying, quality assuring, cleaning, and transforming data prior to analysis.
- Units may require cross-checking against the external metadata file to ensure consistency across datasets and over time.
- Presence of quality-flag fields (Qual) suggests outputs should consider data quality before interpretation or publication.

## Relevance to Monitoring Analysts
- Provides a standardized, query-friendly structure to monitor environmental chemistry over time.
- Facilitates producing outputs such as reports, maps, and charts with consistent units.
- Supports storage and portal uploading of cleaned, transformed datasets for transparency and policy evaluation.

## Practical Considerations
- When integrating with other datasets, verify and, if necessary, convert units to maintain comparability.
- Pay attention to Qual fields to assess data reliability before use in analyses or dashboards.
- Use the documented unit mappings as a reference to ensure consistency in reporting and downstream analyses.