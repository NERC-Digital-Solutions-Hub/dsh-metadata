# Supporting documentation for 03-Soil_Parameters.csv

## Purpose and scope
- Provides a structured metadata/schema for the soil parameters dataset to support data discoverability, consistency, and reuse.
- Each field includes a clear explanation, the expected units, and any notes to aid interpretation and integration across systems.

## Key fields and metadata
- Sample_Code
  - Explanation: Unique sample identifier
  - Units: n/a
  - Notes: n/a
- Sample_Type
  - Explanation: General description of sample (e.g., foodstuff group)
  - Units: n/a
  - Notes: Soil
- Location
  - Explanation: Name of the location where the sample was collected
  - Units: n/a
  - Notes: n/a
- Sample_Description
  - Explanation: Further description of the sample
  - Units: n/a
  - Notes: Soil 0 - 10 cm
- Collection_Date
  - Explanation: Date of sample collection
  - Units: dd-mm-yyyy
  - Notes: n/a
- pH
  - Explanation: Soil pH in water
  - Units: n/a
  - Notes: n/a
- Conductivity_uS/cm
  - Explanation: Soil conductivity
  - Units: μS/cm
  - Notes: n/a
- %_Clay
  - Explanation: Percentage of clay in soil
  - Units: %
  - Notes: n/a
- %_Silt
  - Explanation: Percentage of silt in soil
  - Units: %
  - Notes: n/a
- %_Fine_sand
  - Explanation: Percentage of fine sand in soil
  - Units: %
  - Notes: n/a
- %_Coarse_sand
  - Explanation: Percentage of coarse sand in soil
  - Units: %
  - Notes: n/a

## Data quality and governance implications
- Standardized field definitions with explicit explanations, units, and notes support consistent data collection and interpretation.
- Clear metadata enhances data discoverability and reusability across teams and systems.
- A well-documented schema like this reduces ambiguity and aids in data integration, validation, and reporting.

## Practical usage for data products
- Use as a reference schema to validate incoming soil data assets.
- Ensure all datasets adopt consistent field names, explanations, and units to enable cross-dataset analytics.
- Facilitate metadata-driven data catalogs and user-facing documentation for soil parameters.

## Considerations and potential enhancements
- Consider adding spatial coordinates (latitude/longitude) or geolocation metadata for location-based analysis.
- Include measurement methods or instrumentation details for pH and conductivity for reproducibility.
- Include data quality indicators (e.g., QA/QC status, calibration information) and a schema versioning mechanism.
- Consider adding data owner or steward information and dataset-level metadata (collection campaign, protocol version).