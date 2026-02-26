# Supporting documentation for 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv

## Overview
- Provides metadata and variable definitions for the dataset 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv.
- Focuses on transfer factors (Fv) for radionuclides in plant-related contexts, reporting both values and associated uncertainties, along with detection limits.
- Describes sample identifiers, sample type, collection details, and interpretation rules for non-detects.

## Key fields and definitions
- Sample_Code: Unique sample identifier.
- Sample_Type: Soil.
- Location: Name of the location where the sample was collected.
- Sample_Description: Part of the plant analysed (e.g., portion of the whole plant analysed separately).
- Collection_Date: Date of sample collection (format: dd-mm-yyyy).
- Fv fields (transfer parameters):
  - Ra-226_Fv: Transfer value for Ra-226.
  - Cs-137_Fv: Transfer value for Cs-137.
  - Ra-228_Fv: Transfer value for Ra-228.
  - K-40_Fv: Transfer value for K-40.
- Unc_ fields: Uncertainty associated with each Fv value (e.g., Unc_Ra-226_Fv, Unc_Cs-137_Fv, Unc_Ra-228_Fv, Unc_K-40_Fv).
- Detection_Limit_ fields: Detection limits for each Fv value (e.g., Detection_Limit_Ra-226_Fv, Detection_Limit_Cs-137_Fv, Detection_Limit_Ra-228_Fv, Detection_Limit_K-40_Fv).
- Units:
  - Fv, Unc_Fv, and Detection_Limit fields: Unitless or kg dry matter per L for olive oil and wine (as specified per radionuclide).
  - Some notes reference “olive oil and wine” in the context of units.
  
## Data formatting and units
- Sample_Type and Location use non-numeric descriptive data; Collection_Date uses date format.
- Sample_Description clarifies the specific plant portion analysed.
- Fv and related fields may be blank (missing) to indicate non-detects or values below detection limits, with guidance in the notes.
- Notes indicate formatting inconsistencies in the source (e.g., minor typos in field names), but the intended meaning is that blank values correspond to below detection limits.

## Handling of detection limits and missing data
- If a Fv value (e.g., Ra-226_Fv) is blank, it indicates that the value was below the instrument’s detection limit.
- If a Detection_Limit field is blank, the note states that the Fv value was above the detection limit (i.e., not a non-detect).
- The notes accompanying fields sometimes include formatting anomalies (e.g., spaces in field names such as “Detection_Limit_Ra-226_Fv”), but the interpretation is the standard below/above detection-limit convention.

## Sample and collection details
- Sample_Type is designated as Soil.
- Location identifies where the sample was collected, aiding spatial analysis.
- Collection_Date provides temporal context for uptake analyses.
- Sample_Description indicates which plant component was analysed, enabling interpretation of transfer factors relative to plant parts.

## Data quality and interpretation considerations
- Non-detects are common and should be treated as left-censored data in analyses.
- Some field names contain typographical inconsistencies; align on the intended meaning (Fv values with corresponding Unc and Detection_Limit fields).
- Units vary slightly by radionuclide; ensure consistent unit interpretation (unitless vs. kg dry matter per L where applicable).

## Suggested uses for analysis
- Correlate soil samples with measured transfer factors for each radionuclide.
- Compare uncertainties (Unc_ fields) across radionuclides to assess measurement precision.
- Incorporate detection limits to properly handle censored data in statistical models.
- Build uptake models by relating Collection_Date and Location to Fv values, accounting for sample descriptions (plant portion).