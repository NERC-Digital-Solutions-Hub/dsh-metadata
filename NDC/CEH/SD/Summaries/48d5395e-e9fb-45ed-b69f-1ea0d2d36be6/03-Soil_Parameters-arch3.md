# Supporting documentation for 03-Soil_Parameters.csv

- Overview
  - Provides a field-by-field data dictionary for the 03-Soil_Parameters.csv dataset to support monitoring framework authors in data collection, sharing, quality assurance, and governance.

- Key Fields and Descriptions
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of sample (Notes indicate Soil; some ambiguity with the example description).
  - Location: Name of the collection site.
  - Sample_Description: Additional description of the sample (explicitly notes Soil 0 - 10 cm).
  - Collection_Date: Date of sample collection; format dd-mm-yyyy.
  - pH: Soil pH measured in water.
  - Conductivity_uS/cm: Soil conductivity; units μS/cm.
  - %_Clay: Percentage of clay in soil.
  - %_Silt: Percentage of silt in soil.
  - %_Fine_sand: Percentage of fine sand in soil.
  - %_Coarse_sand: Percentage of coarse sand in soil.

- Metadata Details and Units
  - Each field includes an Explanation, Units, and Notes where applicable.
  - Units vary (e.g., μS/cm for conductivity, % for texture fractions); some fields list n/a for units.
  - Notes provide contextual information (e.g., Sample_Type notes indicate Soil, Sample_Description specifies soil depth).

- Data Quality, Sharing, and Governance Implications
  - The dictionary supports data traceability, standardised metadata, and clear field definitions to aid data governance.
  - Facilitates data sharing and reuse by clarifying data meaning, units, and collection context.
  - Highlights potential metadata gaps (e.g., some fields show n/a for Units or cross-field inconsistencies) that can affect verification and interoperability.

- Practical Use for Monitoring Frameworks
  - Enables consistent data ingestion into reports, dashboards, and indicators for soil health.
  - Supports transparency and reproducibility by documenting data provenance (collection date, location, depth) and measurement parameters (pH, conductivity, texture fractions).