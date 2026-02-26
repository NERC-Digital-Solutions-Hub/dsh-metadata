# Supporting documentation for 09-Animal_Foodstuff_Gamma_Spectrometry.csv

## Overview
- Data dictionary and field explanations for the gamma spectrometry dataset on animal-derived foodstuffs.
- Covers sample identifiers, sample descriptions, collection details, sample size, and activity concentrations of key radionuclides with uncertainties and detection limits.
- Notes on radionuclide equilibrium relationships and how detection limits are determined.

## Data fields (key elements)
- Sample_Code: unique sample identifier.
- Sample_Type: general description of the foodstuff group.
- Location: location where the sample was collected.
- Sample_Description: part of the organism analyzed (how the sample was prepared).
- Collection_Date: date of collection (format: dd-mm-yyyy).
- Sample_Size: amount analyzed; units are kg fresh matter or L for milk.
- Ra-226_Bq/kg_fm: activity concentration of Ra-226 on a fresh mass basis (Bq/kg_fm; or Bq/L for milk). 
  - Notes: in equilibrium with Pb-214 and Bi-214; blank indicates below detection limit.
- Unc_Ra-226_Bq/kg_fm: uncertainty of Ra-226 concentration (same units and notes as above).
- Detection_Limit_Ra-226_Bq/kg_fm: detection limit per ISO 11929 (same units and notes as above).
- Cs-137_Bq/kg_fm: activity concentration of Cs-137 (Bq/kg_fm).
- Unc_Cs-137_Bq/kg_fm: uncertainty of Cs-137 concentration.
- Detection_Limit_Cs-137_Bq/kg_fm: detection limit for Cs-137 (per ISO 11929).
- Ra-228_Bq/kg_fm: activity concentration of Ra-228 (Bq/kg_fm).
- Unc_Ra-228_Bq/kg_fm: uncertainty of Ra-228 concentration.
- Detection_Limit_Ra-228_Bq/kg_fm: detection limit for Ra-228 (ISO 11929).
  - Notes: in equilibrium with Ac-228; blank indicates below detection limit.
- K-40_Bq/kg_fm: activity concentration of K-40 (Bq/kg_fm).
- Unc_K-40_Bq/kg_fm: uncertainty of K-40 concentration.
- Detection_Limit_K-40_Bq/kg_fm: detection limit for K-40 (ISO 11929).

## Measurement details and interpretation
- Units and basis:
  - All radionuclide concentrations are on a fresh mass basis (kg_fm), with milk given as Bq/L where applicable.
- Equilibrium notes:
  - Ra-226 is in equilibrium with Pb-214 and Bi-214.
  - Ra-228 is in equilibrium with Ac-228.
- Detection limits:
  - Detection limits are calculated according to ISO 11929 for each radionuclide.
  - When concentration is below the detection limit, the field may be blank, indicating sub-detection values.
- Data quality signals:
  - Uncertainties accompany each concentration value.
  - Blank detection-limit fields indicate non-detects; explicit notes clarify equilibrium conditions and notation.
  
## Data quality, metadata and governance
- Metadata sufficiency:
  - Clear definitions for sample identifiers, sample types, locations, and collection dates enhance traceability and reproducibility.
- Data handling considerations:
  - Indicate how non-detects are represented (blanks) and ensure consistent treatment across analyses.
  - Include links between activity concentrations and their uncertainties and detection limits for transparent interpretation.
- Governance and sharing:
  - To support monitoring frameworks, datasets should be quality-assured, cleaned, and made openly accessible with provenance and versioning.
  - Address potential barriers mentioned in monitoring contexts, such as data silos, metadata gaps, and the need for standardized data formats.