# Supporting documentation for 04-Soil_Gamma_Spectrometry.csv

## Overview
- Provides metadata and field definitions for a soil gamma spectrometry dataset.
- Documents sample identifiers, sampling context, and measurement results for radionuclides in soil.
- Includes concentration values, uncertainties, detection limits, and notes on equilibrium relationships.

## Key Columns and Meanings
- Sample_Code: Unique sample identifier.
- Sample_Type: Indicates the sample is soil.
- Location: Name of where the sample was collected.
- Sample_Description: Additional detail about the sample (example: soil collected at depth 0-10 cm).
- Collection_Date: Date of sample collection (format: dd-mm-yyyy).
- Sample_size: Amount of sample analyzed (units: Kg dry matter).
- Radionuclide concentrations (all in Bq/kg_dry_mass):
  - Ra-226_Bq/kg_dm: Activity of Ra-226; in equilibrium with Pb-214 and Bi-214.
  - Cs-137_Bq/kg_dm: Activity of Cs-137.
  - Ra-228_Bq/kg_dm: Activity of Ra-228; in equilibrium with Ac-228.
  - K-40_Bq/kg_dm: Activity of K-40.
- Unc_* (uncertainties): Uncertainty associated with each radionuclide concentration (same units as concentration).
- Detection_Limit_*: Detection limit for each radionuclide, calculated per ISO 11929.
- Notes fields: 
  - Indicate equilibrium relationships (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228).
  - Indicate when a value is below detection limit (blank values denote below detection limit).

## Data Quality and Interpretation
- Blank values for concentration or uncertainty indicate results below the detection limit.
- Detection limits follow ISO 11929 methodology for Ra-226, Cs-137, Ra-228, and K-40.
- Equilibrium assumptions are explicitly noted for Ra-226 (with Pb-214 and Bi-214) and Ra-228 (with Ac-228), affecting interpretation of related concentrations.
- Units are consistently in Bq per kilogram of dry matter (Bq/kg_dm).

## Practical Considerations for Analysis
- When comparing samples, account for detection limits and treat blanks as non-detects.
- Use uncertainties to quantify confidence in reported activities and to propagate errors in downstream analyses.
- Consider equilibrium relationships when inferring activities of related radionuclides.
- Ensure sample metadata (location, collection date, sample size, and depth) aligns with spatial and temporal analyses.

## Notes on Documentation Format
- The documentation provides field-level explanations, units, and notes for each relevant column, enabling consistent data usage and interpretation across analyses.