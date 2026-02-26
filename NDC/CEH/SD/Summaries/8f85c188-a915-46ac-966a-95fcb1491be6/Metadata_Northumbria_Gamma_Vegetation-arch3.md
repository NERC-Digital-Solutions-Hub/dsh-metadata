# TREE_Northumbria_Gamma_Vegetation

## Overview
- A detailed data dictionary for measuring gamma-emitting radionuclides in vegetation.
- Records taxonomic information, sampling context, plant material analysed, and radiometric results.
- Supports environmental monitoring, policy scrutiny, and future decision-making through standardized data capture and metadata.

## Key Data Fields and What They Capture
- Biological identification
  - Latin_Species_Name and Common_Species_Name: scientific and common names of plant species.
  - Plant_Part_Analysed: which plant part was analysed.
- Sampling context
  - Site: sampling location.
  - CEH_Sample_Identifier: unique sample ID linked to UKCEH radiochemistry lab workflows.
  - CEH_Sample_Description: description of the sample.
  - Sampling_Date_Used_As_Decay_Date: date of sampling used for decay calculations.
- Sample mass
  - Dry_Mass_Of_Sample_Analysed_g: dry mass in grams.
- Radionuclide activity concentrations
  - K-40_Bq_per_kg_DM and K-40_Bq_per_kg_FM: activity concentration of potassium-40 per kg in dry mass and fresh mass, respectively.
  - Counting_Error_K-40_Bq_per_kg_DM and Counting_Error_K-40_Bq_per_kg_FM: two-sigma counting uncertainties for K-40.
  - MDA_K-40_Bq_per_kg_DM and MDA_K-40_Bq_per_kg_FM: minimum detectable activity concentrations for K-40 (dry and fresh mass).
  - Cs-137_Bq_per_kg_DM and Cs-137_Bq_per_kg_FM: activity concentration of cesium-137 per kg in dry mass and fresh mass, respectively.
  - Counting_Error_Cs-137_Bq_per_kg_DM and Counting_Error_Cs-137_Bq_per_kg_FM: two-sigma counting uncertainties for Cs-137.
  - MDA_Cs-137_Bq_per_kg_DM and MDA_Cs-137_Bq_per_kg_FM: minimum detectable activity concentrations for Cs-137 (dry and fresh mass).
- Concentration ratios (Cs-137)
  - Cs-137_Concentration_Ratio_DM: Cs-137 concentration ratio (vegetation/dry mass) with related fields.
  - Cs-137_Concentration_Ratio_FM: Cs-137 concentration ratio (vegetation/fresh mass) with related fields.
  - Cs-137_Concentration_Ratio_DM_<, Cs-137_Concentration_Ratio_FM_<: “less than” indicators for the respective ratios.
  - Notes_Related_to_137Cs_Concentration_Ratio: notes providing context for Cs-137 concentration ratios.
- General notes and metadata
  - General_Notes: overarching notes.
  - Not applicable indicators (e.g., where a value is not applicable) are provided in several fields.

## Measurement Details and Data Semantics
- Units and meanings are explicitly defined (Bq per kg DM or FM; g for dry mass).
- “<” markers indicate values below the detection limit (MDA).
- Two-sigma counting errors accompany concentration values to express analytical uncertainty.
- Cs-137 concentration ratios compare vegetation to dry/fresh mass, with explicit notes clarifying interpretation.

## Data Quality, Governance, and Operational Considerations
- Emphasizes clear metadata and data provenance to enable verification and reuse.
- Supports data sharing and transparency through explicit descriptions of each field.
- Highlights potential barriers relevant to monitoring frameworks:
  - Availability and completeness of metadata.
  - Variation between dry mass and fresh mass calculations requiring consistent transformation.
  - Handling of non-detects (MDA and "<" indicators) in analyses and dashboards.
  - The need to maintain data quality, standardisation, and timely updates (e.g., decay-date alignment).

## Relevance for Monitoring Frameworks and Policy Decisions
- Provides a structured, standards-based dataset for environmental radiological monitoring in vegetation.
- Enables:
  - Cross-site and temporal comparisons of K-40 and Cs-137 burdens.
  - Calculation of vegetation-to-soil or plant-to-environment transfer metrics via concentration ratios.
  - Assessment of radiological exposure pathways and potential policy implications.
  - Clear communication of results through documented uncertainty (counting errors) and detection limits.

## Implementation Considerations for Analysts
- Ensure consistent use of dry mass (DM) and fresh mass (FM) bases across all measurements.
- Properly treat MDAs and < values in statistical analyses and dashboards.
- Maintain linkage between sample identifiers, descriptions, and analytical results to support traceability.
- Leverage notes and general notes to provide context for interpretation of Cs-137 ratios and any site-specific peculiarities.