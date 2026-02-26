# TREE_Northumbria_ICPMS_Soil_DM

## Overview
- Metadata schema for soil ICP-MS data from UKCEH/Northumbria samples.
- Each record includes sample identifiers, site information, sampling date, and a broad suite of elemental concentrations measured as milligrams per kilogram of dry mass (mg/kg DM).

## Data structure and fields
- Sample and site metadata:
  - CEH_Sample_Identifier: UKCEH sample Identifier
  - CEH_Sample_Description: UKCEH sample description
  - Site: Sampling site
  - Sampling_Date: Date sample collected
- Element concentrations (all in mg/kg DM) with accompanying explanations:
  - I_mg_kg_DM
  - Li_mg_kg_DM
  - Be_mg_kg_DM
  - Na_mg_kg_DM
  - Mg_mg_kg_DM
  - Al_mg_kg_DM
  - P_mg_kg_DM
  - K_mg_kg_DM
  - Ca_mg_kg_DM
  - Ti_mg_kg_DM
  - V_mg_kg_DM
  - Cr_mg_kg_DM
  - Mn_mg_kg_DM
  - Fe_mg_kg_DM
  - Ni_mg_kg_DM
  - Cu_mg_kg_DM
  - Zn_mg_kg_DM
  - As_mg_kg_DM
  - Se_mg_kg_DM
  - Rb_mg_kg_DM
  - Sr_mg_kg_DM
  - Mo_mg_kg_DM
  - Ag_mg_kg_DM
  - Cd_mg_kg_DM
  - Cs_mg_kg_DM
  - Ba_mg_kg_DM
  - Tl_mg_kg_DM
  - Pb_mg_kg_DM
  - U_mg_kg_DM
- Notes in the source indicate that each element has an associated explanation (e.g., “Concentration of I in milligram per kilogram dry mass”); however, some lines contain transcription inconsistencies (e.g., repeated references to Co or mislabeling).

## Metadata quality and issues
- The field descriptions are intended to be consistent across elements, each with a unit and explanation.
- Some lines contain errors (e.g., incorrect element naming in explanations for Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U), indicating potential copy-paste issues that require data quality checks.
- UKCEH sample identifiers suggest cross-dataset linkage; ensure consistent mapping and provenance.

## Data governance, discoverability, and usability
- Centralized sample metadata (identifier, description, site, date) paired with a comprehensive elemental concentration suite.
- Units standardized to mg/kg DM (dry mass), facilitating cross-sample comparisons.
- Documentation should be updated to fix inconsistencies and provide robust metadata for each field to support data discovery and reuse.

## Recommendations for Data Leaders
- Standardize and verify metadata:
  - Correct any mislabeling in element explanations and ensure each element’s description uniquely corresponds to its column.
  - Confirm that all elements have consistent units (mg/kg_DM) and clear, unambiguous explanations.
- Improve data quality controls:
  - Implement validation rules for concentration ranges and detect any improbable values.
  - Establish a controlled vocabulary for element names and metadata fields.
- Enhance interoperability:
  - Map CEH_Sample_Identifier and Site to external datasets where relevant; maintain clear provenance and versioning.
- Document sampling and analysis protocols:
  - Include ICP-MS method details, sample preparation, detection limits, and quality assurance/quality control steps to aid interpretation.
- Build a data catalog entry:
  - Include data usage license, access restrictions, and links to related datasets to support broader data sharing within the data community.