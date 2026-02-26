# Supporting documentation for 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv

- This document describes the fields and metadata for the dataset 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv, clarifying what each column represents, units, and handling of non-detections.

## Data fields and schema

- Sample_Code
  - Explanation: Unique sample identifier.
  - Units: n/a
  - Notes: n/a
- Sample_Type
  - Explanation: Type of sample (e.g., Soil).
  - Units: n/a
  - Notes: n/a
- Location
  - Explanation: Location name where the sample was collected.
  - Units: n/a
  - Notes: n/a
- Sample_Description
  - Explanation: Part of the organism analysed (e.g., where the whole organism was divided and analysed separately).
  - Units: n/a
  - Notes: n/a
- Collection_Date
  - Explanation: Date of sample collection.
  - Units: dd-mm-yyyy
  - Notes: n/a

## Radionuclide transfer (CR) columns

For each radionuclide (Ra-226, Cs-137, Ra-228, K-40), the dataset includes the following triplets:

- [Radionuclide]_CR
  - Explanation: Concentration or transfer parameter (CR value) for the radionuclide.
  - Units: Unitless or kg dry matter per L for milk (as stated in the documentation).
  - Notes: If blank or Not Determined, the CR value is below the detection limit.
- Unc_[Radionuclide]_CR
  - Explanation: Uncertainty of the CR value for the radionuclide.
  - Units: Unitless or kg dry matter per L for milk
  - Notes: Blank if not provided or applicable.
- Detection_Limit_[Radionuclide]_CR
  - Explanation: Detection limit of the CR value for the radionuclide.
  - Units: Unitless or kg dry matter per L for milk
  - Notes: Blank if the CR value is above the detection limit.

Specific triplets present:
- Ra-226_CR, Unc_Ra-226_CR, Detection_Limit_Ra-226_CR
- Cs-137_CR, Unc_Cs-137_CR, Detection_Limit_Cs-137_CR
- Ra-228_CR, Unc_Ra-228_CR, Detection_Limit_Ra-228_CR
- K-40_CR, Unc_K-40_CR, Detection_Limit_K-40_CR

## Data quality and handling notes

- Non-detections are indicated by blanks in the CR and/or Unc fields, with notes specifying that the value is below the detection limit.
- Detection limits are provided per radionuclide to aid in interpreting non-detected values.
- Units are described per field, though there is a potential inconsistency in the documentation text (units listed as unitless or kg dry matter per L for milk); analysts should verify units when integrating with other datasets.
- The dataset is structured to support data cleaning, uncertainty assessment, and downstream analyses of radiological transfer parameters across samples.