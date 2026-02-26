# TREE_Northumbria_Animal_Tissue_Mass

## Overview
- Dataset describing tissue masses collected from Northumbria samples.
- Captures taxonomic, sample, tissue, and mass measurements to support analysis of tissue composition.
- Includes notes on data availability and special cases (e.g., when masses are not obtained or not applicable for certain estimates).

## Key Fields and Data Types

- Latin_Species_Name
  - Description: Latin name of species
  - Units: n/a

- CEH_Sample_Code
  - Description: CEH sample codes associated with animal or sample
  - Units: n/a
  - Special: Not applicable for estimates of total muscle and total bone

- CEH_Sample_Description
  - Description: CEH sample description
  - Units: n/a

- Tissue
  - Description: Tissue type
  - Units: n/a

- Tissue_Fresh_Mass_kg
  - Description: Tissue fresh mass
  - Units: kg
  - Special: Not available when mass was not obtained

- Tissue_Freeze_Dried _Mass_kg
  - Description: Tissue freeze dried mass
  - Units: kg
  - Special: Not available when mass was not obtained

- Fresh_Mass_Dry _Mass_Ratio
  - Description: Fresh mass to freeze dry mass ratio of tissue
  - Units: kg - kilograms
  - Special: Not available when a ratio cannot be calculated

- General_Notes
  - Description: General notes
  - Units: n/a

## Data Quality and Metadata Considerations
- Ensure consistent taxonomic naming via Latin_Species_Name.
- Maintain clear mapping for CEH_Sample_Code and CEH_Sample_Description to support traceability.
- Standardize tissue naming (Tissue) and ensure mass fields use the specified units (kg).
- Explicitly record missing values with clear indicators (e.g., "Not available").
- Capture method of mass measurement and any data transformations applied (e.g., from fresh to dry mass).
- Track any applicability constraints (e.g., CEH_Sample_Code not used for certain estimates).

## Data Sharing and Governance Considerations
- Store in a catalog or data portal with fields aligned to the dataset schema for discoverability.
- Provide documentation that explains field definitions, units, and missing-value conventions.
- Include update and provenance information to support reproducibility and data versioning.

## Challenges and Considerations for Data Stewards
- Aligning user needs with dataset schema, especially for deriving muscle/bone estimates where CEH_Sample_Code usage differs.
- Obtaining timely and complete mass measurements (fresh and freeze-dried) across samples.
- Achieving cross-system/interoperability given potential naming inconsistencies (e.g., spaces in field names like "Tissue_Freeze_Dried _Mass_kg" and "Fresh_Mass_Dry _Mass_Ratio").
- Handling datasets with incomplete data and ensuring clear notation for missing values.
- Managing updates while preserving historical data and metadata context.