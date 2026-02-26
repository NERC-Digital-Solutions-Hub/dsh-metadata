# The second column (SRA_sample_name) in CocoaBugs_field_data_20230128.csv connects each row of CocoaBugs_field_data_20230128.csv to one of the rows below (column name: "Sample Name")

## Overview
- Purpose: Link environmental covariate data in CocoaBugs_field_data_20230128.csv to SRA/malaise-trap sample records via the SRA_sample_name mapping to "Sample Name".
- Data identifiers:
  - SRA accession: PRJNA898889 (BioProject)
  - Temporary Submission ID: SUB12256650
  - Release date: 2024-12-31
  - SRA access link after release: https://www.ncbi.nlm.nih.gov/sra/PRJNA898889

## Data structure and key mappings
- CocoaBugs_field_data_20230128.csv contains:
  - Environmental covariates for each sample
  - A key to connect to the speciesXsample table (Malaise_traps_ZG0001592.client.otuids.csv) via the SRA_sample_name column
- The mapping table shows:
  - Columns such as Sample Name, SPUID, Organism, Tax ID, BioProject
  - Many SAMN entries (e.g., SAMN31634495, SAMN31634496, etc.) linked to specific Sample Names (e.g., GRNP-240_16405; GRNP-273_16398A; etc.)
  - For each SAMN, a corresponding assignment of Organism, Tax ID, and BioProject (PRJNA898889)

## Access and provenance
- Primary project accession: PRJNA898889
- Individual records: SAMN entries associated with various samples and environment descriptors (e.g., outdoor, metagenome)
- Release date indicates when SRA data become publicly accessible via the provided link

## Data governance and stewardship considerations
- Metadata completeness and consistency:
  - Ensure each SRA_sample_name correctly maps to the corresponding Sample Name in the mapping table
  - Verify SPUID, Organism, Tax ID, and BioProject fields are accurate and consistently formatted
- Interoperability and standards:
  - Maintain consistent sample naming conventions across CocoaBugs_field_data_20230128.csv and the SRA-linked tables
  - Align metadata schema with repository standards to support discovery and reuse
- Access and update management:
  - Track SRA status changes (embargoes, release dates) and update links/records accordingly
  - Document any corrections or re-mappings when SRA records are updated
- Provenance and discoverability:
  - Keep a changelog for updates to mappings between SRA_sample_name and Sample Name
  - Ensure the linkage remains traceable from field data to the SRA records (PRJNA898889 and SAMN IDs)

## Recommendations for Data Stewards
- Implement validation checks to confirm SRA_sample_name → Sample Name mappings are complete and unambiguous
- Version control the mapping and maintain an audit trail for updates to SPUID, Organism, Tax ID, and BioProject fields
- Provide clear documentation on how to interpret the Sample Name field and its relationship to the SRA records
- Establish a process to refresh metadata when new SAMN records are added or existing records are updated in PRJNA898889
- Monitor access status and ensure links remain valid post-release, updating stakeholders as needed