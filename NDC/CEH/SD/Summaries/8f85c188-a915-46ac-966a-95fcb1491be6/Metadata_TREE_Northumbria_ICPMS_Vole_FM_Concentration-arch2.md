# TREE_Northumbria_ICPMS_Vole_FM_Fresh_Mass_Concentration

## Overview
- A dataset of fresh mass concentrations of elements in vole tissue from Northumbria, produced using ICP-MS.
- Captures specimen and sampling metadata alongside extensive elemental concentrations for cross-site environmental monitoring.

## Data structure and fields
- Identification and sampling context
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes (UKCEH sample codes)
  - Sample_Details (sample preparation information)
  - CEH_Sample_Description (UKCEH sample description)
  - Tissue (notes on vole preparation; no separate tissues prepared)
- Sample metadata and mass
  - Fresh_Mass_Ash_Mass_Ratio
- Concentration measurements (mg/kg fresh mass, FM)
  - I_mg_kg_FM, Li_mg_kg_FM
  - Be_mg_kg_FM (with <Be indicating a censored value)
  - Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM
  - P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM
  - Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM
  - Fe_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM
  - As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM
  - Mo_mg_kg_FM, Ag_mg_kg_FM (with <Ag indicating censored value)
  - Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM
  - Tl_mg_kg_FM, Pb_mg_kg_FM
  - U_mg_kg_FM (with <U indicating censored value)
- Notes on data quality
  - Some concentrations are reported as less-than values (censored indicators) using the < symbol for specific elements (e.g., Be, Ag, U, etc.)

## Measurements and units
- All listed concentrations are in milligrams per kilogram of fresh mass (mg/kg FM).
- Some fields use asterisks or markers to denote data not applicable or censored values (e.g., <Be, <Ag, <U).

## Data quality flags
- Less-than markers indicate concentrations below detection limits (censored data), applied to specific elements in the dataset (e.g., Be, Ag, U).

## Data governance and usage
- UKCEH sample codes are included for traceability.
- Data are produced to support standardized outputs (reports, maps, charts) and stored/uploaded to appropriate portals.
- Datasets are intended to be cleaned, quality assured, and made accessible to others, enabling broader use and integration with other monitoring data.

## Relevance to environmental monitoring
- Provides a standardized, comparable set of contaminant concentrations in small mammal tissue to assess environmental health and policy performance over time.
- Facilitates cross-site comparisons and time-series analysis, helping to increase the value of monitoring data by enabling data integration with related datasets.