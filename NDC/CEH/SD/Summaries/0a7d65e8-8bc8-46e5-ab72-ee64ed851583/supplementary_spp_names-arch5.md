# Lepidoptera species data dump with ABH_COMMON_NAME, BF_NUMBER, and identifiers

## Overview
- Large export of Lepidoptera species data intended for data discovery and sharing across a network of datasets.
- Each record appears to connect internal identifiers (e.g., Lep_XXXX) with scientific names, common names, and numeric codes (e.g., BF_NUMBER, ABH_NUMBER, SPECIES_ID).
- The dataset combines multiple variants per taxon (synonyms, historical mappings, and alternative naming), suggesting a raw extract rather than a publish-ready dataset.

## Data structure and content (observed patterns)
- Records typically begin with an internal Lepidoptera ID (e.g., Lep_7792) followed by several fields containing scientific names, common names, and numeric identifiers.
- Entries often present multiple variants for the same taxon (synonyms or alternate spellings) across different fields.
- Frequent use of inconsistent formatting, quotes, line breaks, and mixed punctuation, indicating parsing/export issues.
- A wide range of taxa represented, including several species with corresponding common names (e.g., Brown-spot, Chestnut, Emperor Moth, etc.).

## Data quality and completeness issues
- Incomplete fields: many rows have missing ABH_NUMBER, SPECIES_ID, or other identifiers.
- Duplicates and conflicting mappings: same taxa appear multiple times with slightly different mappings between scientific names, common names, and codes.
- Formatting/encoding problems: irregular quotation marks, broken fields, inconsistent capitalization, and stray phrases (e.g., "Oak." or "Chinese. Character") suggesting extraction errors.
- Taxonomic inconsistencies: multiple variants or synonyms per taxon require reconciliation against a canonical backbone.

## Governance and stewardship considerations
- Provenance and versioning are not explicit; metadata on source, licensing, and update history is missing.
- Interoperability requires a canonical schema to enable cross-dataset linking (stable taxon IDs, standardized common names, unique internal identifiers).
- Metadata and discoverability need enrichment (source, retrieval date, license, contact for stewardship).
- Taxonomic updates and nomenclatural changes imply a need for an update mechanism and change log.

## Recommendations and actions for Data Stewards
- Data cleansing and normalization
  - Normalize to a canonical schema with defined data types for each field.
  - Resolve duplicates by identifying unique keys (e.g., stable_id, BF_NUMBER, ABH_NUMBER) and de-duplicate or flag ambiguities.
  - Remove or flag clearly corrupted records.
- Taxonomic alignment
  - Map SPECIES_ID and ABH_COMMON_NAME to a taxonomic backbone and assign stable internal IDs.
  - Consolidate synonyms and maintain a single preferred name per taxon.
- Metadata enrichment
  - Add source, version, retrieval date, license, and contact fields.
  - Record provenance for each record (originating source and last update).
- Data quality checks and governance
  - Implement validation rules for non-null ABH_NUMBER where applicable, consistent BF_NUMBER mappings, and valid species identifiers.
  - Establish a data steward review workflow for ambiguous records.
- Publication and accessibility
  - Publish a cleaned, schema-compliant version to the data portal with documentation and usage guidance.
  - Provide a data dictionary detailing field meanings, accepted values, and aliases.

## Practical next steps
- Ingest the export into a staging area and run schema validation to identify missing fields and formatting issues.
- Develop a canonical schema (e.g., LepidopteraTaxon with stable_id, taxon_rank, scientific_name, common_name, bf_number, source_id, ab_h_number, etc.).
- Create a mapping process to align SPECIES_ID and ABH_NUMBER to a taxonomic backbone and deduplicate synonymous records.
- Compile and attach comprehensive metadata (source, license, version, retrieval date) to each record.
- Produce a cleaned dataset ready for cataloging and sharing, accompanied by a data quality report detailing remaining gaps and decisions.