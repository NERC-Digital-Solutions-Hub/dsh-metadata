# Biota Data Dictionary

- Purpose
  - Defines field descriptions, units, and notes for a dataset of biota specimens including mass measurements of various body parts.

- Dataset structure
  - Includes taxonomic identifiers (Biota English name, Latin_name), sample metadata (Collection_Date, ID), and multiple mass measurements (Whole_body_g, Gut_g, Tissue_with_thyroid_g, Thyroid_g, Liver_g, Kidney_g, Carcass_g).

- Key fields and definitions
  - Biota: English name of the biota; explanation provided; no unit; note field empty.
  - Latin_name: Latin name of the species; no unit; note field empty.
  - Collection_Date: Date when the sample was collected (where known); format is dd month yyyy.
  - ID: Identifier for the data record (where applicable); no unit; note field empty.
  - Whole_body_g: Mass of the whole body; units: grams.
  - Gut_g: Mass of the gut; units: grams.
  - Tissue_with_thyroid_g: Mass of the sample containing the thyroid; notes explain that the thyroid was too small to separate, so an area around it was analysed as a whole; units: grams.
  - Thyroid_g: Mass of the actual thyroid (single gland); units: grams.
  - Liver_g: Mass of the liver; units: grams.
  - Kidney_g: Mass of the kidney; units: grams.
  - Carcass_g: Mass of the carcass; units: grams.

- Notes and conventions
  - Some Notes fields are empty.
  - Tissue_with_thyroid_g includes a specific sampling rationale for small thyroids.

- Practical use and data quality considerations
  - Enables self-contained understanding of specimen-level body mass composition for analysis and cross-dataset merging.
  - Watch for incomplete fields and missing notes; ensure date format consistency (dd month yyyy) and gram units across records.