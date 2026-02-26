# TREE_Northumbria_ICPMS_Vole_AM_Concentration

## Overview
- Dataset header for Northumbria vole samples analysed by ICP-MS to determine concentrations of multiple elements in ash mass.
- Captures sample metadata (species, site, date, UKCEH codes, preparation notes) and the concentrations of numerous elements in milligrams per kilogram (mg/kg) on ash mass basis.
- Includes notes on vole preparation and the ratio of fresh mass to ash mass.

## Data fields and structure
- Taxonomy and site information
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
- Sampling metadata
  - CEH_Sample_Codes
  - Sample_Details
  - CEH_Sample_Description
  - Notes
  - Fresh_Mass_Ash_Mass_Ratio
- Measurements (elements and related values)
  - I_mg_kg_AM, Li_mg_kg_AM, Be_mg_kg_AM, Na_mg_kg_AM, Mg_mg_kg_AM, Al_mg_kg_AM, P_mg_kg_AM, K_mg_kg_AM
  - Ti_mg_kg_AM, V_mg_kg_AM, Cr_mg_kg_AM, Mn_mg_kg_AM, Fe_mg_kg_AM, Co_mg_kg_AM, Ni_mg_kg_AM, Cu_mg_kg_AM, Zn_mg_kg_AM
  - As_mg_kg_AM, Se_mg_kg_AM, Rb_mg_kg_AM, Sr_mg_kg_AM, Mo_mg_kg_AM
  - Ag_mg_kg_AM, Cd_mg_kg_AM, Cs_mg_kg_AM, Ba_mg_kg_AM, Tl_mg_kg_AM, Pb_mg_kg_AM, U_mg_kg_AM
- Note on data structure for certain columns
  - Some elements have multi-part entries (e.g., Ag_mg_kg_AM_1/Ag_mg_kg_AM_2) or “<” values indicating detection limits.
  - Some descriptive text appears misaligned (e.g., lines stating “Concentration of Ca” where Ti or other elements are intended); the underlying intent is mg/kg concentrations in ash mass.

## Measurements and units
- Primary unit: milligrams per kilogram (mg/kg) on ash mass basis.
- Fresh mass to ash mass ratio provided to contextualize normalization.
- Occasional < (less-than) values indicate concentrations below detection/quantification limits.
- Some sections include placeholder or mixed labeling (likely metadata parsing artifacts) but broadly enumerate concentrations for a wide suite of elements.

## Sample metadata and preparation
- Includes sampling site and date, species identification (Latin and common names), and CEH UKCEH sample codes.
- Sample preparation details and UKCEH sample description are documented.
- Notes specify vole preparation details (e.g., no separate tissue preparations in some cases).

## Data quality and accessibility
- Described workflow aligns with standardised data practices:
  - Verify data from established sources
  - Quality assure, clean, and transform data
  - Analyse using standardised methods
  - Present outputs in clear formats (reports, maps, charts)
  - Store and upload datasets to appropriate portals

## Challenges and considerations
- Increasing the value of the linked datasets by combining them with other relevant data beyond single-use outputs.
- Enabling access to the underlying data used to create final outputs to support transparency and reuse.

## Relevance to Analysts Monitoring the Environment
- The document embodies a standardized, verifiable data assembly for environmental monitoring, enabling assessment of contaminant levels in wildlife tissue over time and across sites.
- Aligns with the Analysts’ aims to demonstrate environmental health and policy performance by providing clean, comparable data and accessible results.