# Data Support

## Overview
- Helps others explore data, combine datasets, analyze patterns, and create data products for self-service access.
- Combines data across topics, with emphasis on data use in policy work and public-facing insights.
- Typical environments include organisations with broad remits (e.g., local councils, private companies).

## How Data Support Meets Its Aims
- Understand the ask: clarify needs, determine the best approach, and justify data requirements.
- Data preparation: locate, verify, clean, transform, and harmonize data; join datasets to reveal patterns.
- Product delivery: create end-user tools (dashboards, pivot tables) and provide usage guidance.
- Adoption and iteration: promote outputs, gather user feedback, and iterate; advocate for better data creation.

## Dataset Snapshot (Moth/Butterfly Mappings)
- Example data type: mappings between identifiers, scientific names, common names, and numeric codes (e.g., BF_NUMBER, ABH_NUMBER, 73.xx codes).
- Typical fields observed (with variations and garbling): species IDs, H_SPECIES_NAME, ABH_COMMON_NAME, BF_NUMBER, ABH_NUMBER, scientific vs. common names.
- Data pattern: repeated mappings linking codes to names, occasional synonyms, and mixed formatting.

## Data Quality Challenges Illustrated
- Patchy data density and inconsistency across entries.
- Duplicates, missing values (e.g., ABH_NUMBER), and irregular or garbled formatting.
- Mixed use of scientific names, common names, and numeric codes without a single schema.
- Data likely exported from larger systems or parsed inconsistently.

## How This Dataset Informs Data Support Practice
- Demonstrates turning raw, messy mappings into usable tools (e.g., lookups, dashboards) for end users.
- Supports self-service exploration by linking codes with names and vice versa.
- Highlights the need for governance to reduce duplication, fill gaps, and standardize formats.

## Next Steps for Users (Dataset-Oriented)
- Clean and standardize:
  - Unify field names and schema (consistent ABH_NUMBER and BF_NUMBER).
  - Resolve duplicates; fill missing ABH_NUMBER values where possible.
  - Normalize naming conventions (scientific vs. common names) and fix garbled entries.
- Create self-serve data products:
  - Build a searchable species lookup dashboard (by BF_NUMBER, ABH_NUMBER, or common name).
  - Develop cross-reference tables linking ABH/Common Name/BF Number with scientific names.
- Strengthen data governance:
  - Establish a canonical schema and data dictionary for mappings.
  - Implement validation rules to catch missing or inconsistent fields at entry time.
- Engage topic experts:
  - Validate mappings against taxonomic references.
  - Gather user feedback to refine dashboard features and data fields.

## Key Challenges to Expect
- Time spent clarifying the ask due to limited upfront data consideration.
- Working with patchy data across multiple formats and systems.
- Communicating complex taxonomic mappings clearly.
- Efforts to promote outputs for wider sharing and reuse.