# Supporting documentation for 03-Soil_Parameters.csv

- Overview
  - Defines the metadata fields for the soil parameters dataset and clarifies the meaning, units, and notes for each field to support data governance, discoverability, and reuse.

- Dataset fields and metadata
  - Sample_Code: Unique sample identifier. Units: n/a. Notes: n/a.
  - Sample_Type: General description of the sample (soil). Units: n/a. Notes: Soil.
  - Location: Name of the collection location. Units: n/a. Notes: n/a.
  - Sample_Description: Further description of the sample. Units: n/a. Notes: Soil 0 - 10 cm.
  - Collection_Date: Date of sample collection. Units: dd-mm-yyyy. Notes: n/a.
  - pH: Soil pH in water. Units: n/a. Notes: n/a.
  - Conductivity_uS/cm: Soil conductivity. Units: μS/cm. Notes: n/a.
  - %_Clay: Percentage of clay in soil. Units: %. Notes: n/a.
  - %_Silt: Percentage of silt in soil. Units: %. Notes: n/a.
  - %_Fine_sand: Percentage of fine sand in soil. Units: %. Notes: n/a.
  - %_Coarse_sand: Percentage of coarse sand in soil. Units: %. Notes: n/a.

- Metadata and data governance implications
  - Ensures consistent terminology, units, and descriptions to support interoperability across datasets.
  - Emphasizes the importance of unique identifiers, explicit collection dates, and clear sample depth context (as indicated by the Sample_Description note “Soil 0 - 10 cm”).
  - Facilitates data reuse by clarifying what each field represents and how it should be measured (e.g., pH in water, conductivity units).

- Data quality and sharing considerations
  - Data stewards should verify accuracy and consistency of measurements (pH, conductivity, and particle percentages) and ensure alignment with the described metadata.
  - Maintain completeness of metadata fields to support user needs and discoverability.
  - Prepare for publishing or cataloging by ensuring all fields are present, correctly formatted (e.g., Collection_Date as dd-mm-yyyy), and accompanied by clear notes where applicable.

- Practical next steps for Data Stewards
  - Validate field names, definitions, and units across related datasets to support standardized ingestion.
  - Ensure the dataset is uploaded to relevant portals and properly cataloged with the defined metadata.
  - Document any data transformations or quality checks applied to the soil parameter data.