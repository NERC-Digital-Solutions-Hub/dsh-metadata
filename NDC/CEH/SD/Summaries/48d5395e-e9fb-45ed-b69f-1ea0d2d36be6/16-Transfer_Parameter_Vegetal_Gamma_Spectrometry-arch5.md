# Supporting documentation for 16-Transfer_Parameter_Vegetal_Gamma_Spectrometry.csv

## Overview
- Contains transfer parameter (Fv) values for radionuclides in plant-related samples, with associated uncertainties and detection limits.
- Focuses on Ra-226, Cs-137, Ra-228, and K-40 transfer factors, with units described as unitless or kg dry matter per liter for olive oil and wine.
- Includes metadata fields such as Sample_Code, Sample_Type, Location, Sample_Description, and Collection_Date to support dataset discovery and reuse.
- Indicates when a Fv value is below the detection limit via blank fields or notes.

## Key fields and metadata
- Sample_Code: Unique sample identifier.
- Sample_Type: Soil.
- Location: Name of the collection site.
- Sample_Description: Part of the plant analyzed (e.g., specific plant section).
- Collection_Date: Date of sample collection (formatted as dd-mm-yyyy).
- Fv fields for each radionuclide:
  - Ra-226_Fv: Transfer value.
  - Unc_Ra-226_Fv: Uncertainty of Ra-226 Fv.
  - Detection_Limit_Ra-226_Fv: Detection limit for Ra-226 Fv.
  - Cs-137_Fv, Unc_Cs-137_Fv, Detection_Limit_Cs-137_Fv: analogous fields for Cs-137.
  - Ra-228_Fv, Unc_Ra-228_Fv, Detection_Limit_Ra-228_Fv: analogous fields for Ra-228.
  - K-40_Fv, Unc_K-40_Fv, Detection_Limit_K-40_Fv: analogous fields for K-40.
- Notes:
  - Blanks for Fv or Unc fields indicate values below detection limits.
  - Detection limit fields specify the threshold below which values are not detected.
- Units note: Fv values may be unitless or expressed per kg dry matter per liter for olive oil and wine, depending on radionuclide.

## Data quality and standardization
- Dates use a consistent dd-mm-yyyy format.
- Units are specified per field; ensure consistency across the dataset.
- Nondetects are represented by blanks with accompanying notes on detection limits.
- Documentation implies a need for consistent interpretation of Fv, Unc, and Detection_Limit values across radionuclides.

## Data governance and stewardship actions
- Provenance: Capture method details (gamma spectrometry), calibration, QA/QC procedures to accompany Fv values.
- Metadata completeness: Ensure dataset-level metadata includes measurement methods, instrument types, detection limit determination, and data processing steps.
- Versioning: Track updates and new samples to maintain a clear history.
- Sharing and access: Define embargoes, licensing, and data-use guidance; specify how updates propagate to linked portals or catalogs.
- Accessibility: Use controlled vocabularies for Location and Sample_Description where possible to aid discoverability and interoperability.

## Practical implications for data users
- How to interpret results: Fv values with corresponding Unc indicate measurement precision; blanks indicate below-detection results.
- Data integration: Requires joining on Sample_Code, Collection_Date, Location, and Sample_Description to align with sample metadata and matrices (olive oil, wine context).
- Handling uncertainties: Use Unc fields in any quantitative analyses and propagate through downstream calculations.
- Temporal considerations: Collection_Date is essential for trend analyses and alignment with other environmental datasets.

## Challenges and recommendations for Data Stewards
- Challenge: Incomplete picture of user needs and prioritization.
  - Recommendation: Create dataset-level documentation outlining intended analyses and typical use cases; gather user feedback to refine metadata fields.
- Challenge: Getting data in a timely manner and ensuring metadata completeness.
  - Recommendation: Implement a data submission checklist covering Sample_Code, Location, Collection_Date, Sample_Description, and all Fv/Unc/Detection_Limit fields.
- Challenge: Harmonizing formats and dealing with multiple systems.
  - Recommendation: Adopt a common data model for transfer factors and specify field definitions, units, and allowed values; provide mapping guidance from legacy formats.
- Challenge: Handling large datasets and non-interoperable legacy data.
  - Recommendation: Encourage export in a standardized CSV/JSON with explicit schemas; maintain a data dictionary and versioned schema.
- Challenge: Updating datasets while respecting data sharing constraints.
  - Recommendation: Establish update and embargo policies, contact points, and a clear process for versioned releases.