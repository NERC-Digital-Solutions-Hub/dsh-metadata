# Supporting documentation for 13-Animal_Feeding.csv

## Overview
- Metadata for a CSV dataset describing animal feeding data.
- Fields include Animal, Location, Feeding, Daily_Ingestion, and Composition_Animal_Feed.
- Each field has Explanation, Units, and Notes to guide interpretation and use.
- Abbreviations used are based on Sample Codes.

## Data fields and definitions
- Animal
  - Explanation: General type of animal
  - Units: n/a
  - Notes: n/a
- Location
  - Explanation: Name of the location where the sample was collected
  - Units: n/a
  - Notes: n/a
- Feeding
  - Explanation: Description of the feeding regime
  - Units: n/a
  - Notes: n/a
- Daily_Ingestion
  - Explanation: Amount of dry matter ingested by an animal per day
  - Units: kg dry matter per day
  - Notes: n/a
- Composition_Animal_Feed
  - Explanation: Equation for the weighted composition of the total diet
  - Units: n/a
  - Notes: Information about animal feed composition provided by producers
- Abbreviations
  - Note: Abbreviations are based on Sample Codes

## Data governance and quality considerations
- The document provides field-level definitions, units, and provenance notes, supporting consistent interpretation across users.
- Absent or limited notes for most fields indicate potential areas for enriching metadata (e.g., data provenance, collection methods, date of sampling).

## Access, discoverability, and usage guidance
- Use field explanations to interpret values consistently across datasets.
- Refer to Units to ensure correct calculations and aggregations (notably Daily_Ingestion in kg/day).
- Abbreviations mapping (based on Sample Codes) should be maintained to avoid misinterpretation.

## Gaps and improvement opportunities for Data Leaders
- Consider adding dataset-level metadata (source, collection date, sampling methodology, data steward, versioning).
- Expand Notes fields with provenance, data quality flags, and constraints if applicable.
- Ensure consistent metadata across related datasets to improve interoperability and discoverability.

## Next steps for institutional use
- Integrate this metadata schema into the data catalog and governance processes.
- Standardize field naming and documentation across datasets to support scalable data sharing and reuse.
- Establish a process to update and validate metadata as the dataset evolves.