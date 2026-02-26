# Supporting documentation for 04-Soil_Gamma_Spectrometry.csv

## Overview
- Metadata and schema for a soil gamma spectrometry dataset (04-Soil_Gamma_Spectrometry.csv).
- Samples are soil, collected from various locations, at shallow depth (Sample_Description indicates soil at 0-10 cm).
- Key measurement: activity concentrations of radionuclides in Bq per kg dry mass (Bq/kg_dm).
- Radionuclides included: Ra-226, Ra-228, K-40, Cs-137.
- For each radionuclide: activity concentration, associated uncertainty, and detection limit (ISO 11929).
- Some results are reported as “in equilibrium” with other isotopes (e.g., Pb-214, Bi-214, Ac-228).
- Blank values indicate concentrations below the detection limit.

## Data Schema and Key Fields
- Sample_Code: unique sample identifier.
- Location: name of the collection site.
- Sample_Type: Soil.
- Sample_Description: additional explanation; example indicates depth 0-10 cm.
- Collection_Date: date collected (dd-mm-yyyy).
- Sample_size: amount analyzed (Kg dry matter).
- Radionuclide fields (per isotope):
  - Ra-226_Bq/kg_dm; Unc_Ra-226_Bq/kg_dm; Detection_Limit_Ra-226_Bq/kg_dm
  - Cs-137_Bq/kg_dm; Unc_Cs-137_Bq/kg_dm; Detection_Limit_Cs-137_Bq/kg_dm
  - Ra-228_Bq/kg_dm; Unc_Ra-228_Bq/kg_dm; Detection_Limit_Ra-228_Bq/kg_dm
  - K-40_Bq/kg_dm; Unc_K-40_Bq/kg_dm; Detection_Limit_K-40_Bq/kg_dm
- Units: Bq per kg dry mass (Bq/kg_dm); Date format: dd-mm-yyyy.
- Notes per field:
  - Some entries specify “In equilibrium with” other isotopes.
  - Where blank, values are below the detection limit.

## Data Quality, Uncertainty, and Detection
- Each radionuclide includes an uncertainty term (Unc_…).
- Detection limits are provided for each radionuclide and are calculated according to ISO 11929.
- Blank values indicate non-detects (below limit).
- Equilibrium notes provide context for interpretation of related isotopes.

## GIS and Mapping Considerations
- Suitable for creating spatial maps of radionuclide concentrations at the 0-10 cm soil depth.
- Uncertainty fields enable the creation of uncertainty layers or error-aware maps.
- Detection limits can be used to classify censored data (non-detects) in maps.
- Requires linking Location names to geographic coordinates for GIS integration.
- Standardization of field names and units will streamline joins with other geospatial datasets.

## Data Gaps and Preparation Notes (for GIS specialists)
- Data may be dispersed across multiple sources; plan for data harmonization.
- Some fields include non-numeric indicators (e.g., “In equilibrium with …”) that require interpretation or separation into metadata.
- Incomplete values (blanks) must be treated as below detection or handled as missing, depending on analysis goals.
- Ensure consistent data standards for field naming (e.g., Detection_Limit_Ra-226_Bq/kg_dm) across the dataset.

## Practical Next Steps for GIS Production
- Clean and normalize field names and units; convert numeric fields to appropriate data types.
- Join Location to a spatial layer to assign coordinates and enable mapping.
- Create layers:
  - Primary concentration layers for Ra-226, Ra-228, K-40, Cs-137 (with 0-10 cm depth).
  - Uncertainty layers corresponding to each concentration.
  - Detection-limit masks to indicate censored data.
- Incorporate collection date to enable temporal analyses if multiple sampling events exist.
- Document interpretation rules for equilibrium notes and non-detect values in metadata and GIS workflows.