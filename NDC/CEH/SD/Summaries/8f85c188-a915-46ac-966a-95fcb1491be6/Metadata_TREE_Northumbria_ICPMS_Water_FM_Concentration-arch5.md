# TREE_Northumbria_ICPMS_Water_FM_Concentration

## Overview
- Dataset likely contains ICP-MS measured concentrations of multiple elements in water samples from Northumbria, with Northumbria Environmental context (CEH references).
- Focused on concentrations of elements in milligrams per litre (mg/l) across various samples, with associated metadata to support discovery, provenance, and reuse.
- Metadata fields specify sample identifiers, descriptions, site, sampling date, and notes on preparation.

## Data Model and Schema
- Core metadata fields
  - CEH_Sample_Identifier: UKCEH sample code
  - CEH_Sample_Description: UKCEH sample description
  - Site: Sampling site
  - Sampling_Date: Date sample collected
  - Notes: Notes on preparation
- Concentration measurements (all in mg/l)
  - Al_mg_l, As_mg_l, B_mg_l, Ba_mg_l, Be_mg_l, Ca_mg_l, Cd_mg_l, Ce_mg_l, Co_mg_l, Cr_mg_l
  - Cs_mg_l, Cu_mg_l, Fe_mg_l, K_mg_l, La_mg_l, Li_mg_l, Mg_mg_l, Mn_mg_l, Mo_mg_l, Na_mg_l
  - Ni_mg_l, Pb_mg_l, Pr_mg_l, Rb_mg_l, Sb_mg_l, Se_mg_l, Si_mg_l, Sn_mg_l, Sr_mg_l, Ti_mg_l
  - U_mg_l, V_mg_l, W_mg_l, Zn_mg_l
- Data qualifiers and special cases
  - A subset of concentration columns uses a “<” marker (e.g., <Cs, Mo_mg_l, Na_mg_l, etc.) to indicate a value below the reporting/detection limit
  - Some entries include “n/a” for non-applicable fields or explanations
- Explanations for each concentration field
  - Each analyte is described as its concentration in milligram per litre (mg/l)

## Data Quality and Standardization Considerations
- Consistent units across all concentration fields (mg/l)
- Handling of quoted qualifiers:
  - “<” markers indicate censored/below-detection values; ensure these are captured as data qualifiers in the dataset and in metadata
- Metadata completeness:
  - Ensure CEH_Sample_Identifier, Site, Sampling_Date, and Notes are present for traceability
- Data provenance:
  - Link sample identifiers to the UKCEH source and maintain a clear mapping to sampling events
- Data quality checks:
  - Validate that non-applicable fields are correctly coded as n/a
  - Verify that sample descriptions align with sample identifiers and sites
- Interoperability considerations:
  - Dataset may need alignment with other CEH/Northumbria datasets and standardized vocabularies for sites and sample descriptions

## Data Management, Access, and Sharing
- Likely intended for uploading to data portals and cataloguing within data holdings
- Documentation should accompany the dataset to support discovery and reuse by data users
- Potential need for updating datasets as new samples are collected or metadata is refined

## Challenges to Address
- Incomplete or evolving user needs related to sample scope and analyte coverage
- Timely acquisition of data from multiple sources or systems
- Ensuring data creators meet standard metadata and units (mg/l) consistently
- Managing large, multi-parameter datasets and potential formatting inconsistencies
- Handling legacy or non-interoperable databases and heterogenous data formats

## Practical Next Steps for Data Stewards
- Verify and standardize core metadata fields (sample IDs, site, date, description, notes)
- Confirm all analyte columns and their units (mg/l) and apply consistent handling for < values
- Document data provenance, including data origin, processing steps, and any transformations
- Implement data quality checks and flags for below-detection values
- Prepare guidance for data users on interpreting qualifiers and non-applicable fields
- Plan for ongoing updates and versioning to reflect new data and metadata refinements