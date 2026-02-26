# TREE_Northumbria_ICPMS_Soil_DM

## Overview
- Dataset capturing ICP-MS–derived elemental concentrations in soil from Northumbria ( TREE_Northumbria_ICPMS_Soil_DM ).
- Key measurements are concentrations in mg/kg dry mass (DM) for a broad suite of elements (e.g., I, Li, Be, Na, Mg, Al, P, K, Ca, Ti, V, Cr, Mn, Fe, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U).
- Includes sample identifiers, sampling site, and sampling date to support contextual analyses.

## Data Structure and Key Variables
- Core identifiers and context:
  - CEH_Sample_Identifier (UKCEH sample identifier)
  - CEH_Sample_Description (UKCEH sample description)
  - Site (sampling site)
  - Sampling_Date (date sample collected)
- Elemental concentration variables (examples):
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM
  - Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Notes on metadata:
  - Units are mg/kg DM for all listed elements.
  - The dataset header includes “Units” and “Explanation” for each field; however, several explanations appear inconsistent or misassigned (e.g., repeated “Concentration of Co” or similar errors in many lines), indicating potential mapping issues between headers and descriptions.

## Data Quality and Issues
- Inconsistencies in field descriptions:
  - Multiple lines mislabel concentrations (e.g., “Concentration of Co” incorrectly applied to many elements).
  - Some header lines duplicate or confuse element meaning and units.
- Potential data quality challenges:
  - Patchy or incomplete metadata alignment with actual data columns.
  - Variability in data formats if combined from multiple sources.
- Implications:
  - Requires careful data cleaning, standardization of column names, and verification against the original source before analysis or public sharing.

## Potential Uses and Outputs for Data Support
- Self-serve exploration of elemental soil composition across sites and dates.
- Dashboards or pivot-table style summaries by site, date, or element.
- Comparative analyses against reference thresholds or historical baselines.
- Data provenance and reproducible reporting through a clean data dictionary and validated column mappings.

## Preparation and Validation Steps
- Data cleaning and standardization:
  - Align column names to a consistent schema (e.g., element names as standardized keys, all units in mg/kg_DM).
  - Correct misassigned explanations and verify against the source documentation.
- Data validation:
  - Cross-check sample identifiers, site labels, and sampling dates with the original records.
  - Validate numeric ranges and handle missing values appropriately.
- Documentation and governance:
  - Produce a clear data dictionary mapping each column to its real-world meaning.
  - Version-control cleaned datasets and preserve provenance from the original source.

## Access and Sharing Considerations
- Centralized storage with version control and clear provenance for datasets and cleaned derivatives.
- Clear guidance on acceptable uses, data licensing, and attribution for CEH/Northumbria sources.
- Encourage sharing of validated outputs (dashboards, reports) to promote data reuse and avoid duplicated effort.

## Suggested Next Steps
- Create a standardized data dictionary and a cleaned, tidy version of TREE_Northumbria_ICPMS_Soil_DM.
- Develop example analyses (e.g., site-by-site element concentration profiles, time-series by sampling date) to illustrate self-serve capabilities.
- Set up a lightweight QA checklist to routinely verify key fields (sample ID, site, date, and a subset of core elements).