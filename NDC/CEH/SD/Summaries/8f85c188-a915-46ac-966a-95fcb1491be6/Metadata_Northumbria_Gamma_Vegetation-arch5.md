# TREE_Northumbria_Gamma_Vegetation

## Overview
- A dataset of gamma-emission radiometric measurements from Northumbria vegetation (TREE_Northumbria_Gamma_Vegetation), focusing on K-40 and Cs-137 activity concentrations in vegetation samples.
- Records include measurements in both dry mass (DM) and fresh mass (FM), with associated uncertainties and minimum detectable activities (MDA).
- Includes taxonomic information, sampling context, sample identifiers, and derived concentration ratios between vegetation and soil.

## Key Data Elements
- Species and classification
  - Latin_Species_Name, Common_Species_Name: scientific and common names of plant species.
- Sampling and material type
  - Plant_Part_Analysed: plant part analysed.
  - Site: sampling site.
  - CEH_Sample_Identifier, CEH_Sample_Description: UKCEH radiochemistry lab sample ID and description.
  - Sampling_Date_Used_As_Decay_Date: date of sampling used as decay date.
  - Dry_Mass_Of_Sample_Analysed_g: dry mass (grams) of analysed sample.
- Radionuclide measurements (per DM and FM)
  - K-40_Bq_per_kg_DM, K-40_Bq_per_kg_FM: K-40 activity concentration per kg dry/fresh mass.
  - Counting_Error_K-40_Bq_per_kg_DM, Counting_Error_K-40_Bq_per_kg_FM: two-sigma counting errors.
  - K-40_<, MDA_K-40_Bq_per_kg_DM, MDA_K-40_Bq_per_kg_FM: less-than marker and minimum detectable activity values.
  - Cs-137_Bq_per_kg_DM, Cs-137_Bq_per_kg_FM: Cs-137 activity concentrations (DM and FM).
  - Counting_Error_Cs-137_Bq_per_kg_DM, Counting_Error_Cs-137_Bq_per_kg_FM: two-sigma counting errors for Cs-137.
  - Cs-137_DM_<, Cs-137_FM_<, MDA_Cs-137_Bq_per_kg_DM, MDA_Cs-137_Bq_per_kg_FM: detection flags and MDAs for Cs-137 in DM and FM.
- Ratios and notes
  - Cs-137_Concentration_Ratio_DM_<, Cs-137_Concentration_Ratio_DM, Cs-137_Concentration_Ratio_FM_<, Cs-137_Concentration_Ratio_FM: concentration ratios (vegetation:soil) in DM and FM, with less-than indicators.
  - Notes_Related_to_137Cs_Concentration_Ratio: explanatory notes about Cs-137 concentration ratio.
  - General_Notes: general notes field.
  - Not applicable indicators and interpretations (e.g., “<” meaning not applicable in certain fields).

## Metadata, Standards, and Documentation
- Documented relationships between vegetation and soil activity concentrations, including explicit definitions for concentration ratios.
- Clear differentiation of units and mass basis (DM vs FM) for all radionuclide measurements.
- Includes sample-level metadata (species, site, part analysed, sampling date) to support traceability and re-use.

## Quality Assurance and Data Governance Considerations
- Data Stewardship activities to align with standards:
  - Ensure accuracy, consistency, and completeness of metadata (taxonomy, site, sample identifiers, mass, dates).
  - Validate units (DM vs FM) and correct application across all radionuclide measurements.
  - Apply and interpret MDA and "<" indicators correctly, and document any censored data.
  - Maintain provenance by capturing CEH sample identifiers and descriptions; document any data processing steps.
- Data sharing and lifecycle:
  - Upload datasets to relevant portals; catalogue data holdings.
  - Potentially document work performed on datasets to support reproducibility.
  - Monitor and record data availability, disclosure restrictions, and any embargoes as part of data availability and limitations.

## Data Availability, Limitations, and Challenges
- Availability and limitations to be identified and communicated (e.g., disclosure risks, proprietary issues, embargoes).
- Challenges typical for Data Stewards in this context:
  - Incomplete understanding of user needs for specialized radiometric data.
  - Timely reception of data from contributors or partners.
  - Variability in data creators meeting metadata and standardization requirements.
  - Integration across different systems and formats; handling large, complex datasets.
  - Managing legacy or outdated databases that may require bespoke interoperability solutions.

## Practical Actions for Data Stewards
- Enforce and document data standards:
  - Standardize taxonomy, site, sampling dates, and mass units; ensure clarity between DM and FM measurements.
  - Validate and flag MDA and "<" indicators; ensure proper interpretation in analyses.
- QA processes:
  - Perform quality assurance: verify data integrity, check for missing fields, harmonize metadata, and confirm calculation of ratios.
  - Clean and, if needed, transform data prior to sharing; maintain a record of transformations.
- Documentation and governance:
  - Capture notes and general notes to aid future users in understanding dataset nuances.
  - Maintain provenance for sample identifiers and descriptions; ensure traceability.
- Data dissemination:
  - Publish to appropriate data portals; catalog and index the dataset for discoverability.
  - Provide clear metadata to facilitate reuse by researchers, policymakers, and other data stewards.