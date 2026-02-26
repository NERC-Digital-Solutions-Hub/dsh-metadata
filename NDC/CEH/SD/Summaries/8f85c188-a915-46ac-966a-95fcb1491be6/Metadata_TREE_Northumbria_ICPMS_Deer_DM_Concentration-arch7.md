# TREE_Northumbria_ICPMS_Deer_DM_Concentration

## Overview
- A data dictionary/dataset description for Northumbria-based ICP-MS concentrations in deer tissues, with both metadata fields and a comprehensive list of elemental concentration columns.
- Columns cover species identifiers, sampling details, sample codes, tissue type, and numerous element concentrations reported as mg/kg on a dry-mass basis.
- Notes indicate missing data for specific samples (e.g., “No data for Roe deer 4 thyroid”) and values reported as below detection (< markers).

## Key Fields and Structure
- Identity and taxonomy
  - Latin_Species_Name, Common_Species_Name
- Sampling context
  - Site, Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Elemental concentrations (examples of columns)
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM
  - Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM
  - Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM
  - Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM
  - Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM
  - Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM
  - Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Data quality notes within fields
  - Some entries include "<" markers indicating less-than values
  - Repeated notes such as “No data for Roe deer 4 thyroid” indicating missing tissue-specific data for particular samples

## Data Quality and Gaps
- Missing data
  - Recurrent statement: “No data for Roe deer 4 thyroid” across multiple concentration columns
- Detection limits
  - "<" markers present in several concentration fields, signifying censored values
- Consistency concerns
  - Units are specified as mg/kg DM for many elements; some fields show Units = n/a or variable formatting, suggesting need for standardization

## GIS Applications
- Spatial visualization
  - Map element concentrations by sampling Site to identify spatial patterns
- Data integration
  - Join with site coordinates, shapefiles, and other GIS layers for habitat or policy analyses
- Temporal analysis
  - Use Date_Sample_Collected to explore changes over time
- Stratification
  - Filter by Tissue type and by Species for targeted analyses (e.g., Roe deer vs other species)

## Data Preparation and Best Practices
- Normalization and cleaning
  - Standardize column names and units (dry-mass basis)
  - Harmonize handling of less-than values (assign detection limits or treat as censored data)
- Missing data handling
  - Flag samples with missing tissue or concentration data (e.g., Roe deer 4 thyroid)
- Integration steps
  - Link Site to geographic coordinates; merge with site-level GIS data
  - Preserve CEH_Sample_Codes and Descriptions for traceability
- Documentation
  - Capture limitations observed in the data (missing values, detection limits) for transparent GIS storytelling

## Context and Source
- Appears to be associated with UK Centre for Ecology & Hydrology (UKCEH) sample coding
- Northumbria ICPMS (Inductively Coupled Plasma Mass Spectrometry) deer dataset focusing on tissue-based elemental concentrations