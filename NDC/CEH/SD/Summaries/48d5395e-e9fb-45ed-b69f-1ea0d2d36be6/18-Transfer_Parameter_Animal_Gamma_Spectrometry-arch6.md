# Supporting documentation for 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv

- Purpose: This document provides field-level explanations, units, and notes for the 18-Transfer_Parameter_Animal_Gamma_Spectrometry.csv dataset, enabling data discovery, validation, and self-service analysis for downstream users.

- Dataset scope:
  - Combines sample metadata (identity, description, collection details, and location) with radiological concentration ratio (CR) data for specific radionuclides.
  - Focuses on measurements related to Ra-226, Cs-137, Ra-228, and K-40, including their reported CR values, uncertainties, and detection limits.

- Key fields and their meanings:
  - Sample_Code: Unique sample identifier.
  - Sample_Type: Type of sample (e.g., Soil).
  - Location: Name of the collection site.
  - Sample_Description: Part of the organism analysed (e.g., tissue or component).
  - Collection_Date: Date of sample collection (format: dd-mm-yyyy).
  - Ra-226_CR, Cs-137_CR, Ra-228_CR, K-40_CR: CR values for each radionuclide (unitless or kg dry matter per L for milk).
  - Unc_Ra-226_CR, Unc_Cs-137_CR, Unc_Ra-228_CR, Unc_K-40_CR: Uncertainties associated with the CR values.
  - Detection_Limit_Ra-226_CR, Detection_Limit_Cs-137_CR, Detection_Limit_Ra-228_CR, Detection_Limit_K-40_CR: Detection limits for each CR value.
  - Notes (for CR fields and detection limits): If a value is blank or Not Determined, the CR value is below the detection limit.

- Units and interpretation:
  - CR values and their uncertainties use units described as Unitless or kg dry matter per L for milk.
  - Blank entries indicate values below the detection limit.
  - Corresponding detection limit fields indicate the threshold above which a value would be reported.

- Data quality considerations:
  - Some field name typos in the documentation (e.g., Ra-22 6_CR, Cs-13 7_CR) likely refer to Ra-226_CR and Cs-137_CR; alignment may be needed during data integration.
  - Sample_Type shows Soil in the documentation, which should be verified against actual samples to ensure consistency with Sample_Description and intended analysis scope.
  - Date formats, unit consistency, and handling of below-detection-limit values should be standardized when integrating with other datasets.

- How this supports data use:
  - Enables cleaning and standardization of sample metadata and CR measurements for dashboards, pivot tables, and reports.
  - Facilitates quality checks by clearly separating CR values, uncertainties, and detection limits per radionuclide.
  - Supports data discovery and reuse by providing explicit field definitions, units, and interpretation rules for missing data.

- Recommendations for data preparation and reuse:
  - Harmonize field names and correct any typographical inconsistencies before merging with other datasets.
  - Standardize date formats (dd-mm-yyyy) and verify against source records.
  - Explicitly flag and document below-detection-limit values (blank CR fields) and ensure corresponding detection limit fields are consulted.
  - Validate units across records to confirm consistency (Unitless vs. per milk dry matter) and align with analysis context.