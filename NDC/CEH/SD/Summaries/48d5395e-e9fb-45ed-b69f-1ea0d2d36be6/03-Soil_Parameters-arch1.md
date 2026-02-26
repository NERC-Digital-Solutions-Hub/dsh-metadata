# Supporting documentation for 03-Soil_Parameters.csv

## Overview
- Defines the data fields for the 03-Soil_Parameters.csv dataset.
- Represents soil measurements collected from various locations at a depth of 0–10 cm.
- Includes both descriptive metadata and quantitative soil properties.

## Data fields and metadata
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

## Data quality and interpretation
- The document provides a structured data dictionary with fields, explanations, units, and notes for traceability.
- Depth specification is embedded in the Sample_Description (0–10 cm).
- Collection dates use a consistent dd-mm-yyyy format.
- Numeric soil properties (conductivity and texture fractions) are clearly labeled with appropriate units.

## Uses and analyses for analysts
- Facilitates data cleaning, integration, and reproducible analysis.
- Useful for quality checks (e.g., percent texture components sum to ~100%; consistent collection depths).
- Enables analyses of relationships between pH, conductivity, and soil texture fractions across locations and dates.

## Governance and accessibility
- Metadata is provided for each field to ensure clear interpretation and reusability.
- The dataset is designed to be discoverable and usable in subsequent analyses and reporting.