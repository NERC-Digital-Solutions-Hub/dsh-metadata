# TREE_Northumbria_ICPMS_Frog_mg_per_tissue_FM_Concentration

## Overview
- Dataset detailing concentrations of multiple elements in frog tissue, measured by ICP-MS.
- Concentrations are given as milligrams per total frog tissue in fresh mass (FM).
- Includes accompanying sample metadata to enable traceability and cross-analysis.

## Key Variables (Columns)
- Taxonomy and sampling metadata
  - Latin_Species_Name, Common_Species_Name: scientific and common names.
  - Site: sampling location.
  - Date_Sample_Collected: date of collection.
  - CEH_Sample_Code, CEH_Sample_Description: UKCEH sample identifiers and descriptions.
  - Tissue: frog tissue sampled.
- Concentration measurements
  - I_mg_tissue_FM, Li_mg_tissue_FM, Be_mg_tissue_FM, Na_mg_tissue_FM, Mg_mg_tissue_FM, Al_mg_tissue_FM, P_mg_tissue_FM, K_mg_tissue_FM
  - Ti_mg_tissue_FM, V_mg_tissue_FM, Cr_mg_tissue_FM, Mn_mg_tissue_FM, Fe_mg_tissue_FM, Co_mg_tissue_FM, Ni_mg_tissue_FM, Cu_mg_tissue_FM, Zn_mg_tissue_FM
  - As_mg_tissue_FM, Se_mg_tissue_FM, Rb_mg_tissue_FM, Mo_mg_tissue_FM, Ag_mg_tissue_FM, Cd_mg_tissue_FM, Cs_mg_tissue_FM, Ba_mg_tissue_FM
  - Tl_mg_tissue_FM, Pb_mg_tissue_FM, U_mg_tissue_FM
- Formatting notes
  - Some rows include a "<" prefix (e.g., <Be_mg_tissue_FM) indicating a "<" value (below a threshold or detection limit) for that concentration.
  - A few entries have "<" markers embedded in the column name to indicate such values.
- Data quality notes
  - Some explanations are inconsistent (e.g., multiple elements labeled with “Concentration of Ca” in their description, suggesting clerical/typographical errors).
  - “No data” indicates missing tissue data for certain measurements.
  - Units are typically mg per total frog tissue (fresh mass), with some entries explicitly stating the unit as mg.

## Data Quality & Notes
- Presence of potential metadata inconsistencies (typographical errors in explanations) that may require expert verification.
- Missing data indicated for some tissues or measurements; plan for handling blanks or nulls in analyses.
- Less-than values require special treatment in analyses (e.g., censored data handling).
- The dataset is structured to enable self-serve exploration but may need harmonization with other datasets or metadata for integration.

## How Data Supports End Users
- Enables creation of dashboards or pivot tables to compare element concentrations across species, sites, tissues, and sampling dates.
- Facilitates data quality checks by inspecting metadata alignment (species, site, tissue) with concentration measurements.
- Supports transparent documentation of measurement context (sample codes, descriptions) to aid reproducibility and data sharing.
- Provides clear indicators for data gaps and detection-limit issues via less-than markers.

## Practical Considerations for Use
- Treat "<" values as censored data; decide on an appropriate handling method (e.g., imputation, substitution, or specialized statistical models).
- Validate and, if needed, correct inconsistent explanations (e.g., check for erroneous “Concentration of Ca” notes across multiple elements).
- Cross-check tissue and site consistency when merging with other datasets (e.g., ecological or environmental data).
- When communicating results, clearly reference the sampling metadata (species, site, date, tissue) to avoid misinterpretation of concentration comparisons.

## Suggested Data Preparation Steps
- Standardize column explanations and verify unit consistency (mg_tissue_FM vs. other formats).
- Flag and address inconsistent descriptions; collaborate with domain experts to confirm element-specific context.
- Mark and document missing data points; decide on a consistent strategy for downstream analyses.
- Create derived variables as needed (e.g., element concentration ranges by site or tissue, detection-limit indicators).
- Prepare a data dictionary and a ready-to-use schema to support self-serve analyses.