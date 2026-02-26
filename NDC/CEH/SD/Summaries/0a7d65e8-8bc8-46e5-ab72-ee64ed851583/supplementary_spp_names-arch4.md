# Taxonomic dataset of moth species mappings (ABH BF numbers)

## What this document is
- A large crosswalk mapping internal Lep codes to common names and external identifiers (BF_NUMBER, ABH_NUMBER) for moth species.
- Appears to be a tabular/lookup-style dataset with multiple fields per row, including scientific names, common names, and numeric/string IDs.
- Exhibits signs of extraction or parsing irregularities and inconsistent formatting.

## Data structure and content characteristics
- Rows include fields such as Lep_ codes, common names, Latin/scientific names, and numeric identifiers (BF_NUMBER, ABH_NUMBER).
- Many rows contain multiple variants, aliases, or names for the same species, with repetitive mappings.
- Data shows incomplete or truncated values, inconsistencies in punctuation/capitalization, and mixed formatting.

## Data quality and governance implications
- Quality issues: missing ABH_NUMBERs or other identifiers, inconsistent naming, duplicates, and mixed naming conventions.
- Metadata gaps: lack of explicit provenance, data dictionary, field definitions, and valid value vocabularies.
- Interoperability challenges: non-canonical keys and inconsistent schemas hinder cross-system integration and reliable lookups across networks.

## Relevance to Data Leaders
- Demonstrates the need to view data as an end-to-end system with stable identifiers and rich metadata.
- Highlights the value of mapping internal codes to user-facing names to support collaboration across partner networks.
- Underscores governance needs: data stewardship, standards, and coordination to reduce duplication and achieve consistent data quality.

## Practical recommendations (next steps)
- Establish a canonical reference model: select a primary key (BF_NUMBER or ABH_NUMBER) for unique species entries and define a unified schema.
- Standardize metadata and nomenclature: develop a formal data dictionary, normalize names, and manage synonyms via a controlled vocabulary.
- Improve data quality and validation: implement validation rules, deduplicate entries, and reconcile conflicting mappings.
- Enhance discoverability and lineage: tag data with source systems, update dates, and clear data stewardship responsibilities; document lineage.
- Enable collaborative governance: assign data owners, create communities of practice, and schedule regular data quality reviews; establish procedures for new species updates.
- Leverage for broader data products: use the standardized mapping to support policy, research, and cross-network integrations with clear stewardship and access controls.

## Key takeaway
- The dataset represents a substantial but imperfect crosswalk between internal identifiers and common names. For Data Leaders, it highlights the necessity of a well-governed, standardized data system with stable identifiers, robust metadata, and clear ownership to transform this collection into a reliable, reusable asset across the organisation and its networks.