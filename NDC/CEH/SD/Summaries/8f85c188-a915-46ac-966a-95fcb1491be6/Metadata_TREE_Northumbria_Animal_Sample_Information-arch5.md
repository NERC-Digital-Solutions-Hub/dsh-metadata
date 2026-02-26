# TREE_Northumbria_Animal_Sample_information

## Overview
- Dataset detailing animal sample information collected in Northumbria.
- Captures taxonomy (Latin and common names), sampling context, physical measurements, biomass, counts, sex, notes, and analyses.
- Special case: frogspawn are bulk samples of multiple eggs.
- Uses “Not recorded” for missing measurements and “Unknown” for unknown sex.
- Metadata-focused schema intended to support data governance, interoperability, and reuse.

## Key fields and purposes
- Latin_Species_Name: Scientific name of species.
- Common_Species_Name: Common name of species.
- Site: Sampling site identifier.
- Date_Sample_Collected: Date when the sample was collected.
- Sampling_Location_Or_National_Grid_Reference: Geographic reference for sampling location.
- CEH_Sample_Codes_Associated_with_Animal_Or_Sample: CEH-related codes linked to the animal or sample.
- CEH_Sample_Description: Description of the CEH sample.
- Length_mm: Length of the organism in millimetres.
- Width_mm: Width of the organism in millimetres.
- Depth_mm: Depth of the organism in millimetres.
- Wholebody_Fresh_Mass_kg: Fresh mass of the organism in kilograms.
- Wholebody_Freeze_Dried_Mass_kg: Freeze-dried mass in kilograms.
- Wholebody_Ash_Mass_kg: Ash mass in kilograms.
- n: Number of animals or samples.
- Sex: Sex of the animal (male/female); may be Not Recorded or Unknown as appropriate.
- General_Notes: General notes about the sample or dataset.
- Sample_Preparation_And_Analysis_Performed: Details of sample preparation and analyses conducted.

## Measurements and units
- Length_mm, Width_mm, Depth_mm: millimetres (mm).
- Wholebody_Fresh_Mass_kg, Wholebody_Freeze_Dried_Mass_kg, Wholebody_Ash_Mass_kg: kilograms (kg).
- n: count of items or samples.
- Explanations accompanying each field clarify purpose and interpretation.

## Data quality, missing data, and special cases
- Not recorded: indicates measurement was not obtained.
- Unknown: used for unknown sex.
- Frogspawn: noted as bulk samples comprising multiple eggs; treatment as a single record with aggregated considerations.
- Clear linkage between codes, descriptions, and measurements to support traceability.

## Data governance and stewardship considerations
- Ensure consistency of field names, units, and definitions across datasets.
- Maintain comprehensive metadata for discoverability and reuse (data creator, collection date range, methods).
- Align with data sharing standards to facilitate interoperability across portals and catalogs.
- Track data provenance, including sample preparation and analyses performed.
- Establish workflows to minimize delays in data receipt from creators and to enforce metadata completeness.

## Implications for data sharing and discovery
- Datasets should be uploaded to appropriate portals and cataloged with standardized metadata.
- Link CEH sample codes to corresponding animal/sample records for traceability.
- Document any non-interoperable legacy formats and provide transformation guidance where needed.
- Clearly state any limitations or embargoes affecting data availability.