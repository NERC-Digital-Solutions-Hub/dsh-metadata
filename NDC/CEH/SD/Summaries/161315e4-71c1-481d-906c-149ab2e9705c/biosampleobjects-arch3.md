# The second column (SRA_sample_name) in CocoaBugs_field_data_20230128.csv connects each row of CocoaBugs_field_data_20230128.csv to one of the rows below (column name:  "Sample Name")

- Purpose and scope
  - Documents how the SRA_sample_name column in CocoaBugs_field_data_20230128.csv links each field data row to the corresponding sample entry in the SRA-related dataset.
  - CocoaBugs_field_data_20230128.csv contains environmental covariate data for each sample and a key to connect to the speciesXsample table (Malaise_traps_ZG0001592.client.otuids.csv).

- Accessions and release information
  - SRA accession: PRJNA898889.
  - Temporary Submission ID: SUB12256650.
  - Release date: 2024-12-31.
  - Post-release access: SRA records will be accessible at https://www.ncbi.nlm.nih.gov/sra/PRJNA898889.

- Data structure and contents
  - Core linkage: Each row in CocoaBugs_field_data_20230128.csv is connected to one or more SRA sample entries via the SRA_sample_name, which corresponds to entries in the "Sample Name" column of the SRA-related dataset.
  - SRA sample entries include:
    - SPUID and Organism (with Tax ID) per sample.
    - BioProject identifier (PRJNA898889) associated with the sample.
    - Multiple SAMN entries per sample (e.g., SAMN31634495, SAMN31634496, etc.) with descriptors such as 1 = GRNP-240_16405, 2 = GRNP-240_16405, 3 = outdoor, 4 = metagenome, etc.
  - The dataset encompasses a roster of samples across various contexts (e.g., outdoor vs metagenome vs Section-labeled samples) and a range of sample-specific designations (e.g., GRNP-..., NEW_..., Section, metagenome, outdoor).
  - Many entries include nested or repeated mappings to reflect different facets of the same sample (e.g., multiple subsamples or data types like metagenome vs environmental covariates).

- Connections to broader data assets
  - The SRA sample data links to the Malaise_traps_ZG0001592.client.otuids.csv (the species×sample linkage), enabling integration of sequencing results with species-level information.
  - The environmental covariates in CocoaBugs_field_data_20230128.csv can be analyzed alongside SRA-derived data to assess environmental health indicators and inform policy or monitoring decisions.

- Relevance for monitoring frameworks
  - Enables end-to-end traceability from field environmental covariates to sequencing-based observations (OTUs) through a common sample linkage.
  - Supports reproducible reporting and dashboards by providing explicit accession identifiers and a documented linking scheme.
  - Facilitates assessment of data provenance and quality by exposing the data's release status and the structure of sample-level metadata.

- Practical considerations for authors
  - When designing monitoring metrics, use the SRA_sample_name linkage to join CocoaBugs_field_data_20230128.csv with SRA sample metadata and downstream OTU data.
  - Plan for metadata cleaning if integrating the large, text-heavy sample entries (e.g., inconsistent naming within "Section"/"outdoor"/"metagenome" descriptors).
  - Ensure governance and data-sharing practices align with public availability at release, including proper citation of PRJNA898889 and management of underlying covariate metadata.

- Key takeaways
  - The document provides a clear mapping framework between field environmental covariates and sequencing-based sample data via SRA_sample_name, with explicit accessioning details and release timelines to enable environmental health monitoring and evidence-based decision-making.