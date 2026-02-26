# Biota Data Dictionary

- Purpose
  - Defines and standardizes specimen-related measurements for GIS-related data products.
  - Provides both common (English) and scientific (Latin) names to support cross-referencing across datasets.
  - Documents temporal information (collection date) and quantitative body measurements for each specimen.

- Key fields and definitions
  - Biota
    - Explanation: English name of the biota
    - Units: n/a
    - Notes: (empty)
  - Latin_name
    - Explanation: Latin name of the species
    - Units: n/a
    - Notes: (empty)
  - Collection_Date
    - Explanation: Date the sample was collected (where known)
    - Units: dd month yyyy
    - Notes: (empty)
  - ID
    - Explanation: Identifier in the data (where applicable)
    - Units: n/a
    - Notes: (empty)
  - Whole_body_g
    - Explanation: Mass of whole body
    - Units: grams
    - Notes: (empty)
  - Gut_g
    - Explanation: Mass of gut
    - Units: grams
    - Notes: (empty)
  - Tissue_with_thyroid_g
    - Explanation: Mass of sample containing the thyroid (the thyroid was too small to easily separate; an area around it was selected and analysed as a whole)
    - Units: grams
    - Notes: (empty)
  - Thyroid_g
    - Explanation: Mass of the actual thyroid (single gland)
    - Units: grams
    - Notes: (empty)
  - Liver_g
    - Explanation: Mass of liver
    - Units: grams
    - Notes: (empty)
  - Kidney_g
    - Explanation: Mass of kidney
    - Units: grams
    - Notes: (empty)
  - Carcass_g
    - Explanation: Mass of carcass
    - Units: grams
    - Notes: (empty)

- Data types, formats, and units
  - Mass fields are numeric and measured in grams
  - Date field follows the format day-month-year written as dd month yyyy
  - Identifiers (ID) are non-numeric or numeric as applicable; exact format not specified

- Data quality and standardization considerations
  - Some fields have empty notes, indicating incomplete metadata in places
  - Potential variation in data sources and collection practices across records
  - Requires data cleaning and harmonization when combining datasets (e.g., aligning units and date formats)

- GIS relevance and usage
  - Can be joined with spatial data (locations of sampling) to analyze spatial patterns in body composition across taxa
  - Useful for temporal analyses by linking Collection_Date with geographic context
  - Supports filtering by Biota/Latin_name for species-specific mapping and visualization
  - Enables creation of map-based data products showing body part mass distributions by species and location

- Practical considerations for GIS specialists
  - Ensure consistent taxonomic naming (Biota and Latin_name) across layers
  - Normalize and validate mass fields to handle missing values
  - Integrate with geospatial coordinates or place-based metadata to enable mapping
  - Be mindful of potential data sparsity at high resolutions and plan aggregations accordingly

- Related challenges (in the broader GIS workflow)
  - Data resides in multiple sources and may lack consistent standards
  - Gaps in data availability, especially for certain species or organs
  - Large or complex datasets require effective packaging and summarization for mapping
  - Ongoing data cleaning and transformation to support reliable visualizations and analyses