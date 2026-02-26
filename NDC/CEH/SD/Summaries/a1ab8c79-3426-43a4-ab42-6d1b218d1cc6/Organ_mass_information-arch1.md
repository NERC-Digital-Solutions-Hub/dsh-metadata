# Biota Data Dictionary

## Overview
- Defines data fields for a dataset recording biomasses (in grams) of biota and their organs/tissues, along with identifiers and collection date.
- Enables cross-species analyses of body and organ weights, and supports correlations and predictive modeling.

## Key Fields and Descriptions
- Biota
  - Explanation: English name of biota
  - Units: n/a
  - Notes: (none)
- Latin_name
  - Explanation: Latin name of species
  - Units: n/a
  - Notes: (none)
- Collection_Date
  - Explanation: Date sample was collected
  - Units: dd month yyyy
  - Notes: (none)
- ID
  - Explanation: Identifier in the data (where applicable)
  - Units: n/a
  - Notes: (none)
- Whole_body_g
  - Explanation: Mass of whole body
  - Units: grams
  - Notes: (none)
- Gut_g
  - Explanation: Mass of gut
  - Units: grams
  - Notes: (none)
- Tissue_with_thyroid_g
  - Explanation: Mass of sample containing the thyroid (thyroid too small to separate; analysed as a whole area)
  - Units: grams
  - Notes: (see explanation)
- Thyroid_g
  - Explanation: Mass of the actual thyroid (single gland)
  - Units: grams
  - Notes: (none)
- Liver_g
  - Explanation: Mass of liver
  - Units: grams
  - Notes: (none)
- Kidney_g
  - Explanation: Mass of kidney
  - Units: grams
  - Notes: (none)
- Carcass_g
  - Explanation: Mass of carcass
  - Units: grams
  - Notes: (none)

## Data Types and Units
- Mass fields (Whole_body_g, Gut_g, Tissue_with_thyroid_g, Thyroid_g, Liver_g, Kidney_g, Carcass_g): grams
- Biota and Latin_name: not applicable (categorical names)
- Collection_Date: date formatted as dd month yyyy
- ID: identifier (not applicable as a measurement)

## Special Notes
- Tissue_with_thyroid_g captures the combined area around a non-separable thyroid rather than the isolated thyroid gland.
- Some Notes fields are empty; the primary clarifications are provided where indicated (e.g., thyroid handling).

## Potential Analyses and Use Cases for Analysts
- Compare body and organ weights across species (Biota/Latin_name) to explore allometric relationships.
- Model relationships between collection date and body/organ masses to detect temporal trends.
- Compute organ-to-body mass ratios (e.g., Liver_g / Whole_body_g) for ecological or physiological insights.
- Link demographic or taxonomic metadata with mass measurements to support targeted environmental or health assessments.

## Data Quality and Access Considerations
- Data dictionary supports standardization and reproducibility; consistent units facilitate aggregation.
- Potential gaps: missing measurements or identifiers; ensure proper handling of absent values (e.g., for Tissue_with_thyroid_g vs Thyroid_g).
- Linking to external metadata (species names, collection context) enhances interpretability and downstream analyses.