# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Coarse Grain (VC)

- The text provides extensive code lists used in VC data: Species codes (with numerous mappings to Latin names and synonyms) and Quality Codes (standard ECN quality codes plus a 999 category for unusual events).
- These codes underpin data standardization, interoperability, and metadata fidelity across VC site tables and datasets.

## Key data standards and codes

- Species codes
  - Each numeric code (e.g., 2741, 2631, 1171, etc.) maps to one or more scientific names and synonyms (e.g., Salix aurita, Salix caprea, Salix cinerea, Sambucus nigra, etc.).
  - Entries frequently show equivalence between multiple accepted names or synonyms and, in some cases, cross-references to broader taxon concepts (e.g., Salix species, Solanum dulcamara, Sorbus aucuparia, etc.).
  - Many lines also include cross-references to Vas_ identifiers, indicating external taxonomic or database mappings.
  - Practical implication for Data Stewards: maintain a comprehensive crosswalk table, support multiple-name lookups, and ensure site records consistently use canonical codes while preserving synonym mappings for discovery and interoperability.

- Quality Codes
  - A standard ECN quality code set is used (e.g., 100, 101, 102, …, 999).
  - Codes cover data collection conditions and issues such as equipment problems, sample integrity, environmental disturbances, laboratory issues, and data validation status.
  - Code 999 indicates an unusual event with accompanying textual explanation in the dataset’s quality information.
  - Practical implication for Data Stewards: ensure quality codes are attached to data records, provide access to any accompanying quality text for code 999 events, and incorporate these into data quality assessments and provenance documentation.

## Data quality and metadata implications

- The presence of detailed species-code mappings requires standardized metadata to describe how codes map to taxa, including any accepted synonyms and cross-references to external taxonomic databases.
- Quality codes necessitate attached explanatory notes (especially for 999) to preserve data context and enable proper interpretation during analysis.
- Consistency across D1VC/D2VC/D3VC structures hinges on harmonized code usage, accurate mappings, and up-to-date crosswalks.

## Data governance and stewardship considerations

- Code management
  - Maintain and version control the species-code crosswalk, including all synonym mappings and external references (Vas_ identifiers).
  - Establish procedures for adding new taxa and updating existing mappings without breaking downstream datasets.
- Metadata completeness
  - Ensure each dataset record includes valid species and quality codes with references to readable names and descriptions.
  - Document provenance of codes and the date of the mapping revision.
- Interoperability and discoverability
  - Provide tooling or views to translate codes to human-readable names and vice versa.
  - Align code usage across all VC site tables to support cross-site queries and integrations.
- Data quality practices
  - Enforce validation rules to prevent invalid or orphaned codes.
  - Ensure that 999 quality entries include accompanying explanatory text as mandated by the quality information.

## Practical takeaways for Data Stewards

- Implement robust code validation and crosswalk maintenance for both species and quality codes.
- Ensure accessibility of mappings by users, including clear mappings to Latin names and synonyms.
- Maintain and expose quality metadata, including textual explanations for unusual events (code 999).
- Integrate code documentation with overall ECN metadata and protocol references to support accurate data curation, updates, and user support.