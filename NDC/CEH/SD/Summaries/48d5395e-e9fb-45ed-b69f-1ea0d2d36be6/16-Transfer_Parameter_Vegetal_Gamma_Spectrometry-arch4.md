# Supporting documentation for 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv

## Overview
- Provides metadata and explanations for a dataset of transfer parameters (Fv) for radionuclides in plant/soil contexts.
- Focuses on samples related to edible products (e.g., olive oil and wine) with units described as unitless or kg dry matter per liter.
- Includes sample identifiers, location, collection date, sample description, and radionuclide-specific Fv values, uncertainties, and detection limits.

## Key fields and meanings
- Sample_Code: Unique sample identifier (no units).
- Sample_Type: E.g., Soil (no units).
- Location: Name of the collection site.
- Sample_Description: Part of the plant analysed (e.g., division of whole plant analyzed separately).
- Collection_Date: Date of sample collection (dd-mm-yyyy).
- Fv columns:
  - Ra-226_Fv: Fv value for Ra-226 (transfer parameter); units: unitless or kg dry matter per L (olive oil and wine).
  - Cs-137_Fv: Fv value for Cs-137; same units.
  - Ra-228_Fv: Fv value for Ra-228; same units.
  - K-40_Fv: Fv value for K-40; same units.
- Unc_*_Fv: Uncertainty of the corresponding Fv value (same units).
- Detection_Limit_*_Fv: Detection limit of the corresponding Fv (same units).
- Notes: Indicate special considerations; blanks often denote non-detect or detection-related notes (text shows some inconsistencies).

## Data quality and standardization notes
- The documentation contains typos and spacing inconsistencies (e.g., "Detection_Limit_Ra-226_F v"), indicating a need for standardization.
- Some fields use ambiguous wording about blank values (e.g., whether blank means below or above detection limit); standardizing these rules is important for reliable analysis.

## Data provenance and intended use
- Documents the meaning and interpretation of each column to enable analyses of radionuclide transfer to edible plant-derived products via Fv values.
- Supports traceability of sample metadata alongside measured transfer parameters.

## Implications for Data Leaders
- Establish and enforce consistent metadata standards, including:
  - Uniform column names and definitions.
  - Clear, unambiguous rules for non-detect values and detection limits.
  - Consistent units across all Fv-related fields.
- Implement data quality checks to catch typos and formatting inconsistencies.
- Enhance discoverability and interoperability through standardized documentation and version control.
- Ensure appropriate governance around radiological data, with clear provenance, auditability, and cross-dataset linkage for broader data ecosystems.