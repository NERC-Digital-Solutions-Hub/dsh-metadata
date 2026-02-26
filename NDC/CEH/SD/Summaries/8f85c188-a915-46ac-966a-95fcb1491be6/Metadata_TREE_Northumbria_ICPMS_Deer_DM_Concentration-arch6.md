# TREE_Northumbria_ICPMS_Deer_DM_Concentration

## Overview
- A dataset documenting concentrations of multiple elements in deer tissue, reported as milligrams per kilogram of dry mass (mg/kg DM).
- Includes sampling metadata:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration fields (example names): I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM, Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM, V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM, Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM, As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM, Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM, Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM.
- Some entries include less-than values, indicated with a preceding "<" (e.g., <Be, <Al, etc.) to denote censored concentration values.
- Notes on data completeness:
  - Repeated instances of "No data for Roe deer 4 thyroid" across several concentration columns, indicating missing measurements for that sample.
- Some fields carry Units = n/a with corresponding explanations; the structure includes a mix of metadata and element concentration data.

## Data structure and key fields
- Metadata fields:
  - Latin_Species_Name, Common_Species_Name
  - Site
  - Date_Sample_Collected
  - CEH_Sample_Codes, CEH_Sample_Description
  - Tissue
  - Fresh_Mass_Dry_Mass_Ratio
- Concentration fields (mg/kg DM):
  - I_mg_kg_DM, Li_mg_kg_DM, Be_mg_kg_DM, Na_mg_kg_DM, Mg_mg_kg_DM
  - Al_mg_kg_DM, P_mg_kg_DM, K_mg_kg_DM, Ca_mg_kg_DM, Ti_mg_kg_DM
  - V_mg_kg_DM, Cr_mg_kg_DM, Mn_mg_kg_DM, Fe_mg_kg_DM
  - Co_mg_kg_DM, Ni_mg_kg_DM, Cu_mg_kg_DM, Zn_mg_kg_DM
  - As_mg_kg_DM, Se_mg_kg_DM, Rb_mg_kg_DM, Sr_mg_kg_DM
  - Mo_mg_kg_DM, Ag_mg_kg_DM, Cd_mg_kg_DM, Cs_mg_kg_DM
  - Ba_mg_kg_DM, Tl_mg_kg_DM, Pb_mg_kg_DM, U_mg_kg_DM
- Data quality indicators:
  - Presence of "<" values for censored data
  - Missing data notes (e.g., Roe deer 4 thyroid)

## Concentration values and data caveats
- Concentrations are standardized to mg/kg DM for comparability across samples.
- Some elements use a less-than notation (e.g., <Be) to indicate censoring or detection limits.
- Specific sample gaps noted: no data for Roe deer 4 thyroid in multiple element columns.
- Formatting irregularities present in the source text (e.g., occasional truncated phrases) that may require careful interpretation during data ingestion.

## Data quality and gaps
- Patchy data for Roe deer 4 thyroid across many elements.
- Some entries labeled as “Units = n/a” with explanatory notes, requiring careful handling in data loads.
- Examples of data quality considerations:
  - Censored values requiring appropriate treatment (e.g., substitution, interval censoring).
  - Inconsistent or incomplete sample metadata due to missing or truncated fields.
  - The need for harmonization of species, site, and sample codes across records.

## How to use and potential data products
- Self-serve dashboards and pivot-table reports can be built to:
  - Compare element concentrations by species, site, tissue type, and collection date.
  - Explore patterns across multiple elements within a single tissue or site.
  - Flag censored values and missing data to maintain data quality in analyses.
- Data products should include:
  - Clear metadata about units (mg/kg DM), sample IDs, and tissue types.
  - Documentation on censored values and their handling.
  - Notes on any missing samples (e.g., Roe deer 4 thyroid) to set expectations for end users.

## Recommendations for data support and next steps
- Data cleaning and harmonization:
  - Consolidate units to mg/kg DM and ensure consistent column naming.
  - Explicitly flag censored values (e.g., create a separate indicator column or metadata note).
  - Investigate and resolve gaps, particularly Roe deer 4 thyroid measurements.
- Documentation and data governance:
  - Provide a complete data dictionary with uniform explanations for all fields (including those currently labeled n/a).
  - Add provenance information (collection methods, lab methods, detection limits).
- Productization and stakeholder engagement:
  - Develop starter dashboards for species-site-tissue combinations and a multi-element comparison view.
  - Gather user feedback to refine data dictionaries, visualizations, and data quality flags.
- Data sourcing and integration:
  - Align sample codes (CEH_Sample_Codes) with site metadata to enable join operations across datasets.
  - Ensure date formats and site identifiers are consistent to support longitudinal analyses.