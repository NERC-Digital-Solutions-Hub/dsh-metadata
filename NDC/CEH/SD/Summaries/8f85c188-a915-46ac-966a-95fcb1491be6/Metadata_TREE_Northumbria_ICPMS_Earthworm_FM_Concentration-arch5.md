# TREE_Northumbria_ICPMS_Earthworm_FM_Concentration

## Overview
- A dataset detailing concentrations of multiple elements in earthworms, measured by ICP-MS and expressed as mg/kg in fresh mass (FM).
- Includes taxonomic information, sampling context, UKCEH metadata, and notes on earthworm sampling.
- Aimed at enabling data discovery, reuse, and appropriate data governance for datasets with large numbers of samples and measurements.

## Dataset schema
- Core identifiers:
  - Latin_Species_Name
  - Common_Species_Name
  - Site
  - Date_Sample_Collected
- UKCEH metadata:
  - CEH_Sample_Codes
  - CEH_Sample_Description
- Notes:
  - Notes on earthworm sampling
- Measurements (concentrations in mg/kg_FM):
  - I_mg_kg_FM, Li_mg_kg_FM, Be_mg_kg_FM, Na_mg_kg_FM, Mg_mg_kg_FM, Al_mg_kg_FM, P_mg_kg_FM, K_mg_kg_FM, Ca_mg_kg_FM, Ti_mg_kg_FM, V_mg_kg_FM, Cr_mg_kg_FM, Mn_mg_kg_FM, Co_mg_kg_FM, Ni_mg_kg_FM, Cu_mg_kg_FM, Zn_mg_kg_FM, As_mg_kg_FM, Se_mg_kg_FM, Rb_mg_kg_FM, Sr_mg_kg_FM, Mo_mg_kg_FM, Ag_mg_kg_FM, Cd_mg_kg_FM, Cs_mg_kg_FM, Ba_mg_kg_FM, Tl_mg_kg_FM, Pb_mg_kg_FM, U_mg_kg_FM
- Each concentration field includes:
  - Units = mg/kg
  - Explanation = “Concentration of [element] in milligram per kilogram fresh mass” (note: the source contains some misassigned explanations (e.g., many fields incorrectly reference Fe), indicating a metadata quality issue)

## Measurements and field notes
- All concentration variables are expressed relative to fresh mass (FM) and use the mg/kg unit.
- Element list covers light to heavy metals typically analyzed by ICP-MS.
- Caution: several Explanation entries appear misassigned (e.g., repeated references to Fe for multiple elements), which should be corrected during data governance and metadata curation.

## Data quality, standards, and governance
- Standards to apply:
  - Ensure accurate correspondence between field names, units, and explanations.
  - Confirm taxonomic (Latin/ common) naming consistency.
  - Standardize site naming, collection date formats, and CEH sample codes.
- QA/QAQC steps:
  - Quality assurance, data cleaning, and transformation prior to sharing.
  - Document any data processing performed on the dataset.
- Metadata completeness:
  - Verify completeness of core descriptive metadata and measurement metadata.
  - Correct misassignments in the Explanation fields to reflect the actual element measured.
- Interoperability and publishing:
  - Align with existing data models and data portals.
  - Adopt a publishing mindset to maximize dataset usability and discoverability.
- Access and updating:
  - Identify and document sharing restrictions, disclosure considerations, and potential embargoes.
  - Establish processes for dataset updates and versioning, including provenance.

## Challenges and considerations for Data Stewards
- Incomplete view of user needs and priorities.
- Timeliness of data submission from data creators.
- Variability across systems and formats for metadata.
- Handling large datasets and potential non-interoperable legacy databases.
- Ensuring ongoing alignment of measurements, metadata, and governance policies.

## Practical recommendations
- Correct metadata quality issues: fix misassigned explanations to reflect the correct element for each concentration field.
- Implement consistent metadata templates for taxonomic names, site descriptions, sampling dates, and sample codes.
- Provide clear documentation of sampling methods and QA steps to accompany the dataset.
- Facilitate data creators with tools and guidance to meet standards (naming conventions, units, and metadata completeness).
- Ensure dataset is uploaded to relevant data portals and properly catalogued with versioning and provenance.