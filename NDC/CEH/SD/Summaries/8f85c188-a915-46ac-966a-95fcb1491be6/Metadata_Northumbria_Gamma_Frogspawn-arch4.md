# TREE_Northumbria_Gamma_Frogspawn

## Overview
- A radiochemical data dictionary for frogspawn samples analyzed by UKCEH radiochemistry laboratory.
- Captures species information, sampling context, sample mass, and activity concentrations for K-40 and Cs-137 in both dry mass (DM) and fresh mass (FM).
- Includes measurement uncertainties, detection limits (MDA), and derived concentration ratios between frogspawn and water samples.

## Key data elements and structure
- Identification and context
  - Latin_Species_Name, Common_Species_Name: scientific and common names of the species.
  - Site: sampling location.
  - CEH_Sample_Identifier: UKCEH unique sample identifier.
  - CEH_Sample_Description: description of the sample.
  - Sampling_Date_Used_As_Decay_Date: date used as decay date for analysis.
- Sample and measurement metadata
  - Dry_Mass_Of_Sample_Analysed_g: dry mass analyzed (grams).
  - Notes related to measurement descriptions and data relationships (implicit in field names).
- Radioisotope measurements (per DM and FM)
  - K-40_Bq_per_kg_DM / K-40_Bq_per_kg_FM: activity concentration of potassium-40 in dry/fresh mass.
  - Counting_Error_K-40_Bq_per_kg_DM / Counting_Error_K-40_Bq_per_kg_FM: two-sigma counting errors for K-40.
  - MDA_K-40_Bq_per_kg_DM / MDA_K-40_Bq_per_kg_FM: minimum detectable activity for K-40 in DM and FM.
  - K-40_< / K-40_<: '<' qualifiers indicating values below detection limit.
  - Cs-137_Bq_per_kg_DM / Cs-137_Bq_per_kg_FM: activity concentration of Cs-137 in dry/fresh mass.
  - Counting_Error_Cs-137_Bq_per_kg_DM / Counting_Error_Cs-137_Bq_per_kg_FM: two-sigma counting errors for Cs-137.
  - Cs-137_DM_< / Cs-137_FM_<: '<' qualifiers for Cs-137 below detection in DM or FM.
  - MDA_Cs-137_Bq_per_kg_DM / MDA_Cs-137_Bq_per_kg_FM: minimum detectable activity for Cs-137 in DM and FM.
- Concentration ratios (Cs-137)
  - Cs-137_Concentration_Ratio_DM_<, FM - concentration ratios given as Bq per kg of DM or FM.
  - Cs-137_Concentration_Ratio_DM, FM: concentration ratio metrics (e.g., Cs-137 in frogspawn per kg DM divided by Cs-137 in water per kg DM/FM).
  - Cs-137_Concentration_Ratio_FM_<: '<' qualifier for FM-based ratio.
  - Notes_Related_To_Cs-137_Concentration_Ratio: general notes about Cs-137 concentration ratios.

## Data quality, measurement details
- Units
  - Bq per kg DM (dry mass) and Bq per kg FM (fresh mass).
- Detection and uncertainty
  - MDA fields indicate minimum detectable activity limits.
  - Counting errors are provided as two-sigma uncertainties.
  - Several fields allow < (less-than) qualifiers to reflect values below detection.
- Data relationships
  - Derived ratios link frogspawn concentrations to water samples (Cs-137 concentration ratios), enabling cross-sample comparisons.

## Data management and governance considerations
- Metadata completeness
  - Ensure clear definitions for each field, consistent units, and documentation of the measurement method.
- Discoverability and traceability
  - CEH_Sample_Identifier and CEH_Sample_Description support sample-level traceability across datasets.
- Data quality and standardization
  - Consistent handling of "<" values and MDAs across isotopes and mass conventions.
  - Clear labeling of dry mass vs. fresh mass measurements to prevent misinterpretation.
- Data integration potential
  - Ratios between frogspawn and water enable cross-dataset analyses; consider standardizing ratio conventions across studies.
- User needs alignment
  - Provides key information for researchers and policy colleagues evaluating radiochemical exposure or environmental radioactivity trends, with explicit mass-based concentration metrics and uncertainty.

## Practical implications for Data Leaders
- Use this dataset as a model for end-to-end data stewardship: from specimen identification to lab-derived radiochemical metrics, with explicit metadata and quality markers.
- Prioritize standardization of mass conventions (DM vs FM) and consistent treatment of detection limits and uncertainties to improve comparability across projects.
- Strengthen cross-dataset interoperability by maintaining unique sample identifiers and explicit notes on concentration-ratio calculations.
- Facilitate data sharing with clear data provenance, enabling co-ownership and collaboration within the wider data community.