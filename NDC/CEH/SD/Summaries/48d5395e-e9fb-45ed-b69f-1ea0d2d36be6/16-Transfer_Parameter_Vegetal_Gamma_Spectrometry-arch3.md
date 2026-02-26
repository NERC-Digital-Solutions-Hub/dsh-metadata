# Supporting documentation for 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv

## Purpose
- Provides structured metadata and parameter definitions for the Vegetal Gamma Spectrometry transfer parameters dataset.
- Documents sample identifiers, sample types, locations, descriptions, collection dates, and radionuclide transfer values (Fv) along with uncertainties and detection limits.

## Data Structure and Key Fields
- Sample_Code: Unique sample identifier.
- Sample_Type: Indicates the sample is soil.
- Location: Name of the location where the sample was collected.
- Sample_Description: Specifies the part of the plant analyzed (e.g., whole plant vs. separated parts).
- Collection_Date: Date of collection, format: dd-mm-yyyy.
- Radionuclide transfer parameters (Fv) and related fields for each radionuclide:
  - Ra-226_Fv, Cs-137_Fv, Ra-228_Fv, K-40_Fv: Fv values (unitless or kg dry matter per L for olive oil and wine).
  - Unc_Ra-226_Fv, Unc_Cs-137_Fv, Unc_Ra-228_Fv, Unc_K-40_Fv: Uncertainties of the Fv values (same units as Fv).
  - Detection_Limit_Ra-226_Fv, Detection_Limit_Cs-137_Fv, Detection_Limit_Ra-228_Fv, Detection_Limit_K-40_Fv: Detection limits for the corresponding Fv values.
- Each radionuclide parameter also includes:
  - Explanation: Clarifies what the Fv value represents.
  - Notes: Indicates if a blank value means the Fv was below the detection limit.

## Radionuclide Parameters (Fv, Uncertainties, and Detection Limits)
- Ra-226_Fv: Fv value for Ra-226; units: unitless or kg dry matter per L.
  - Unc_Ra-226_Fv: Uncertainty of Ra-226 Fv.
  - Detection_Limit_Ra-226_Fv: Detection limit for Ra-226 Fv.
  - Notes specify that blanks indicate values below detection limit.
- Cs-137_Fv: Fv value for Cs-137; units: unitless or kg dry matter per L.
  - Unc_Cs-137_Fv: Uncertainty of Cs-137 Fv.
  - Detection_Limit_Cs-137_Fv: Detection limit for Cs-137 Fv.
  - Notes specify that blanks indicate values below detection limit.
- Ra-228_Fv: Fv value for Ra-228; units: unitless or kg dry matter per L.
  - Unc_Ra-228_Fv: Uncertainty of Ra-228 Fv.
  - Detection_Limit_Ra-228_Fv: Detection limit for Ra-228 Fv.
  - Notes specify that blanks indicate values below detection limit.
- K-40_Fv: Fv value for K-40; units: unitless or kg dry matter per L.
  - Unc_K-40_Fv: Uncertainty of K-40 Fv.
  - Detection_Limit_K-40_Fv: Detection limit for K-40 Fv.
  - Notes specify that blanks indicate values below detection limit.

## Sample Metadata
- Sample_Type consistently indicates Soil.
- Location records the sampling site name.
- Sample_Description details which part of the plant was analyzed.
- Collection_Date provides temporal context in a standardized date format.

## Data Quality, Accessibility, and Governance Considerations
- Metadata fields (Explanation, Units, Notes) accompany each data element to aid understanding and reuse.
- Incomplete or blank Fv fields are used to denote below-detection-limit values, which impacts interpretation and comparability.
- The dataset includes explicit detection limits and uncertainties to support quality assurance and transparent reporting.
- The accompanying structure highlights the need for data governance practices (e.g., ensuring metadata completeness, openness of data, and clear data provenance) to avoid silos and support reuse in environmental monitoring frameworks.