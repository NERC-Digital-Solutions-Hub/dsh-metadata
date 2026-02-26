# TREE_Northumbria_ICPMS_Deer_DM_Concentration

## Overview
- A dataset of ICP-MS measured concentrations of multiple elements in deer tissue, expressed as mg/kg dry mass (DM).
- Includes sample metadata (species, site, date, tissue, sample codes/descriptions, and mass ratios) to support environmental monitoring and trend analysis.
- Aims to support standardised reporting of environmental health indicators and policy performance over time.

## Data Structure and Fields
- Core identifiers and metadata:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Ratio
- Concentration measurements (mg/kg DM) for elements:
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM
  - Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM
  - V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM
  - Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM
  - Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM
  - Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Notes on data representation:
  - Some values are reported as '<' (less than) indicators for concentration.
  - Some entries include "No data for Roe deer 4 thyroid," indicating missing data for that specific tissue/species combination.
  - Several fields have accompanying explanations, many of which are not applicable (n/a).

## Key Measured Analytes
- Essential and trace elements captured across deer tissues:
  - Iodine (I), Lithium (Li), Beryllium (Be), Sodium (Na), Magnesium (Mg)
  - Aluminium (Al), Phosphorus (P), Potassium (K), Calcium (Ca), Titanium (Ti)
  - Vanadium (V), Chromium (Cr), Manganese (Mn), Iron (Fe), Cobalt (Co)
  - Nickel (Ni), Copper (Cu), Zinc (Zn), Arsenic (As), Selenium (Se)
  - Rubidium (Rb), Strontium (Sr), Molybdenum (Mo), Silver (Ag), Cadmium (Cd)
  - Cesium (Cs), Barium (Ba), Thallium (Tl), Lead (Pb), Uranium (U)
- Units consistently in mg/kg dry mass; tissue type and sample mass relationships are recorded.

## Sample and Metadata Details
- Sampling context includes species name, common name, site location, collection date, and UKCEH sample codes/descriptions.
- Tissue sampled is specified (e.g., various deer tissues).
- Fresh-to-dry mass ratio provided to enable conversion or interpretation of results.
- Data provenance linked to established monitoring processes and data portals.

## Data Quality and Gaps
- Data gaps include explicit missing data for Roe deer 4 thyroid sample.
- Some measurements are reported as less-than values, indicating detection limit constraints.
- Several fields contain generic notes (n/a) or explanatory text that may require cleaning for analysis.

## How This Supports Environmental Monitoring
- Provides a standardized, comparable set of tissue-based contaminant concentrations across deer and sites.
- Facilitates assessment of environmental health and policy performance over time when integrated with broader datasets.
- Supports data sharing and reuse by storing and referencing UKCEH sample codes and descriptions.

## Access, Reuse, and Integration
- Designed to be uploaded to appropriate data portals and linked with underlying sampling metadata.
- Should be combined with other datasets to increase analytical value (e.g., cross-site comparisons, temporal trends, or linkage with other environmental indicators).
- Highlights the need to access underlying data behind outputs for transparency and secondary analyses.

## Challenges and Opportunities
- Challenge: enhancing the value of datasets by merging with related environmental data for richer insights.
- Opportunity: improving accessibility of underlying data to enable wider scrutiny and reuse by researchers and policymakers.