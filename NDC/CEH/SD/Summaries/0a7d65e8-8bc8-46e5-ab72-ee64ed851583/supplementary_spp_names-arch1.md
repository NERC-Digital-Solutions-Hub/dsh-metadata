# Lepidoptera Species Cross-Reference Dataset

## Overview
- A large cross-reference dataset mapping Lepidoptera (moths) across multiple naming and coding schemes.
- Each entry appears as a multi-field row that includes:
  - A Lepidoptera-specific identifier (e.g., Lep_7792)
  - Scientific names (genus and species), sometimes combined with common names
  - Cross-reference numbers or codes (e.g., 73.190, 73.192)
  - A canonical / full taxon entry (e.g., Agrochola macilenta)
- The text contains numerous rows for many taxa, with both scientific and common names and various cross-reference identifiers, illustrating a crosswalk between systems.

## Data Structure and Content
- Entries follow a six-field pattern, though formatting is inconsistent and sometimes corrupted:
  - Field 1: Lep_ identifier (e.g., 576, 1 = "Lep_7792")
  - Field 2–3: partial genus/species or common-name fragments (e.g., "Agrochola", "macilenta")
  - Field 4–5: cross-reference codes or numbers (e.g., "73.190")
  - Field 6: full taxon entry (e.g., "Agrochola macilenta")
- Examples of observed patterns:
  - Lep_7792 linked to Agrochola macilenta with cross-code 73.190
  - Lep_7786 linked to Yellow-line / Brick variants and circellaris with cross-code 73.192
  - Entries include many synonyms or subspecies references (e.g., helvola, litura, centrago)
- Some rows contain partial, repeated, or corrupted data:
  - Missing values denoted by periods (.)
  - Inconsistent punctuation and quoting
  - Duplicates and interleaved text resulting in misaligned fields
- The dataset covers a wide range of taxa with both scientific and common names (e.g., Emperors, Prominents, Sallows, Copper Underwings, etc.)

## Data Quality and Challenges
- Key issues:
  - Inconsistent formatting, punctuation, and quotation marks complicate parsing
  - Missing data across several fields (represented by . or blank values)
  - Duplicates and near-duplicate rows for the same taxon with different cross-references
  - Truncated or interleaved text suggesting export or OCR artifacts
  - Taxonomic updates not reconciled; multiple names/synonyms coexist
  - Some rows appear to mix identifiers from multiple schemes, making crosswalks hard to interpret without cleaning
- Implications:
  - Requires careful data cleaning and normalization before reliable cross-database lookups
  - Needs authoritative taxonomic references to validate current vs. historical names

## Potential Analyses and Use Cases
- Build a robust crosswalk:
  - Map between Lep_IDs, cross-reference codes (e.g., 73.190, 73.192), and canonical scientific names
  - Create BF_NUMBER ↔ ABH_NUMBER mappings (or equivalent scheme mappings) for cross-database lookups
- Taxonomic normalization:
  - Resolve duplicates, consolidate synonyms, and align to current accepted nomenclature
  - Flag outdated or ambiguous names and track synonym relationships
- Descriptive analytics:
  - Identify most-referenced taxa, distribution of cross-reference codes, and coverage across naming schemes
  - Group taxa by family or higher-level taxonomy to summarize cross-reference distribution
- Data enrichment opportunities:
  - Add distribution, habitat, and conservation status to support decision-making in policy or research contexts

## Data Processing Plan (Recommended)
- Ingest into a structured data store:
  - Define a schema such as: Lep_ID, Genus, Species, FullName, CommonName, CrossCode1, CrossCode2, CrossCode3, SourceInfo
- Normalize and parse:
  - Develop a parser to extract six fields per entry, handle quotes, whitespace, and missing values
  - Normalize taxon names and split combined fields into canonical components
- Deduplicate and reconcile:
  - Detect and merge duplicates; unify synonyms under canonical records
  - Reconcile cross-reference codes across entries and resolve conflicts
- Build crosswalks:
  - Create explicit mappings between cross-reference codes and canonical taxon entries
  - Produce audit trails for conflicting or missing cross-references
- Validation and documentation:
  - Implement data quality rules (mandatory fields, allowed formats)
  - Generate a data dictionary detailing field meanings, crosswalk logic, and quality notes
  - Validate against authoritative taxonomic references and document assumptions

## Deliverables and Next Steps
- Deliver a clean, queryable cross-reference dataset
- Provide a data dictionary and data quality report
- Produce crosswalk tables (e.g., BF_NUMBER ↔ ABH_NUMBER) with provenance
- Deliver a reproducible ingestion/cleaning pipeline and notes on any remaining ambiguities

## Caveats
- The dataset as presented contains substantial formatting and data quality issues likely due to export/OCR artifacts.
- Analyses should be conducted with rigorous cleaning and validation against authoritative taxonomic references.
- Many fields are incomplete or ambiguous, requiring careful interpretation during any downstream use.