# Supporting documentation for 04-Soil_Gamma_Spectrometry.csv

## Overview
- Documents the metadata and measurements for soil gamma spectrometry analysis.
- Key measurements: activity concentrations of Ra-226, Cs-137, Ra-228, and K-40 on a dry-mass basis (Bq/kg_dm).
- Includes uncertainties and detection limits (per ISO 11929) for each radionuclide.
- Sample metadata:
  - Sample_Code: unique identifier
  - Sample_Type: Soil
  - Location: name of collection site
  - Sample_Description: additional context (e.g., soil at 0–10 cm depth)
  - Collection_Date: dd-mm-yyyy
  - Sample_size: Kg dry matter
- Notes on interpretation:
  - Some isotopes are reported in equilibrium with progeny (e.g., Ra-226 with Pb-214/Bi-214; Ra-228 with Ac-228).
  - Blank values indicate concentrations below the detection limit.

## Dataset Schema and Key Fields
- Sample_Code
  - Type: Identifier
  - Purpose: uniquely identifies each sample
- Sample_Type
  - Type: Categorical (Soil)
  - Purpose: dataset-level context for the sample medium
- Location
  - Type: Text
  - Purpose: location name where the sample was collected
- Sample_Description
  - Type: Text
  - Purpose: provides detail on the sample (e.g., depth, characteristics)
- Collection_Date
  - Type: Date (dd-mm-yyyy)
  - Purpose: record of when the sample was collected
- Sample_size
  - Type: Numeric (Kg dry matter)
  - Purpose: amount of material analyzed
- Ra-226_Bq/kg_dm
  - Type: Numeric
  - Purpose: activity concentration of Ra-226 on dry mass
  - Notes: in equilibrium with Pb-214 and Bi-214
  - Interpretation: blank = below detection limit
- Unc_Ra-226_Bq/kg_dm
  - Type: Numeric
  - Purpose: uncertainty of Ra-226 concentration
- Detection_Limit_Ra-226_Bq/kg_dm
  - Type: Numeric
  - Purpose: ISO 11929-determined detection limit for Ra-226
  - Notes: in equilibrium with Pb-214 and Bi-214
- Cs-137_Bq/kg_dm
  - Type: Numeric
  - Purpose: activity concentration of Cs-137 on dry mass
  - Notes: blank = below detection limit
- Unc_Cs-137_Bq/kg_dm
  - Type: Numeric
  - Purpose: uncertainty of Cs-137 concentration
- Detection_Limit_Cs-137_Bq/kg_dm
  - Type: Numeric
  - Purpose: detection limit for Cs-137 (ISO 11929)
- Ra-228_Bq/kg_dm
  - Type: Numeric
  - Purpose: activity concentration of Ra-228 on dry mass
  - Notes: in equilibrium with Ac-228
  - Interpretation: blank = below detection limit
- Unc_Ra-228_Bq/kg_dm
  - Type: Numeric
  - Purpose: uncertainty of Ra-228 concentration
  - Notes: includes reference to equilibrium context
- Detection_Limit_Ra-228_Bq/kg_dm
  - Type: Numeric
  - Purpose: detection limit for Ra-228 (ISO 11929)
- K-40_Bq/kg_dm
  - Type: Numeric
  - Purpose: activity concentration of K-40 on dry mass
  - Notes: blank = below detection limit
- Unc_K-40_Bq/kg_dm
  - Type: Numeric
  - Purpose: uncertainty of K-40 concentration
- Detection_Limit_K-40_Bq/kg_dm
  - Type: Numeric
  - Purpose: detection limit for K-40 (ISO 11929)

## Measurement Details, Uncertainty, and Interpretation
- Units: Bq per kg dry mass (Bq/kg_dm)
- Detection limits:
  - Calculated according to ISO 11929 for relevant isotopes
  - Blank values indicate concentrations below the detection limit
- Uncertainty fields accompany each activity concentration
- Equilibrium notes:
  - Ra-226 is reported in equilibrium with Pb-214 and Bi-214
  - Ra-228 is reported in equilibrium with Ac-228
- Depth/context:
  - Sample descriptions may indicate soil depth (e.g., 0–10 cm)
- Data completeness:
  - Some fields may be blank when the concentration is below detection limits

## Provenance, Versioning, and Metadata
- The document is a supporting data dictionary/documentation for the dataset 04-Soil_Gamma_Spectrometry.csv.
- It defines field meanings, units, and interpretation rules to ensure consistent data capture and reuse.
- Important for reproducibility, data lineage, and proper downstream analysis.

## Data Governance, Sharing, and Use
- Data Stewardship considerations:
  - Ensure consistent field naming and units across the dataset (prefer to standardize on Ra-226_Bq/kg_dm, Cs-137_Bq/kg_dm, Ra-228_Bq/kg_dm, K-40_Bq/kg_dm, etc.).
  - Maintain clear documentation of detection limits and the rule that blanks indicate non-detects.
  - Preserve equilibrium notes as metadata to support interpretation of radionuclide activities.
- Data sharing and publication:
  - Upload to appropriate portals with a dataset-level description, including purpose, sampling context, isotopes measured, and interpretation guidance.
  - Catalogue data holdings with access rights, license, and version information.
  - Include a data dictionary and any domain-specific notes (e.g., how equilibrium was assessed).
- Useful metadata to add if not present:
  - Geographic coordinates or spatial system for locations
  - Measurement methods and instrument details
  - Quality flags, data qualifiers, and data provenance stamps
  - Data version, update cadence, and embargo status (if applicable)

## Challenges and Considerations for Data Stewards
- Incomplete user needs and context may require additional metadata to support discovery and reuse.
- Timely acquisition and submission of data from multiple sources or systems.
- Harmonizing data from different formats or legacy databases; ensuring interoperability.
- Handling large datasets and potential non-interoperable legacy schemas.
- Managing outdated databases and ensuring consistent interpretation of detection limits and equilibria.

## Recommendations for Data Stewards
- Enforce a standardized data dictionary with uniform field names, units, and allowed values.
- Include a dataset-level metadata record detailing sampling design, methodologies, and interpretation guidelines.
- Implement data quality checks to flag non-detects, inconsistent equilibrium notes, and missing critical metadata.
- Document measurement procedures, instrument calibration, and uncertainty estimation methods.
- Establish clear governance for updates, versioning, and provenance to support traceability and reproducibility.
- Ensure accessibility of the data through a catalogue entry with links to the data dictionary, methodological notes, and any related datasets.