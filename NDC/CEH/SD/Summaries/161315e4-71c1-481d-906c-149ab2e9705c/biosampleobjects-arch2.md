# SRA_sample_name mapping and SRA data release information for CocoaBugs_field_data_20230128.csv

## Overview
- Documents the link between CocoaBugs_field_data_20230128.csv and SRA sample records via the SRA_sample_name field.
- Provides SRA metadata, including accession, submission ID, release date, and access link.

## Data structure and connections
- CocoaBugs_field_data_20230128.csv contains environmental covariate data for each sample and a key to connect to the speciesXsample table (Malaise_traps_ZG0001592.client.otuids.csv).
- The second column (SRA_sample_name) maps each row in CocoaBugs_field_data_20230128.csv to a corresponding row in the SRA data table (Sample Name).
- SRA data table fields include Accession, Sample Name, SPUID, Organism, Tax ID, BioProject.

## SRA data details
- Accession/project: PRJNA898889
- Temporary Submission ID: SUB12256650
- Release date: 2024-12-31
- Public access: After release, SRA records are accessible at https://www.ncbi.nlm.nih.gov/sra/PRJNA898889

## Sample metadata snapshot
- The document lists numerous SAMN entries associated with accession 1839947, detailing:
  - Sample Name (e.g., GRNP-240_16405, outdoor, metagenome)
  - SPUID, Organism, Tax ID, BioProject
- Many entries are presented in a dense, concatenated format with inconsistent line breaks, indicating a large, composite mapping between field samples and SRA records.
- Some entries describe environmental contexts (e.g., outdoor) and data types (e.g., metagenome).

## Data quality and formatting considerations
- The long SAMN list shows formatting irregularities (mixed fields, multiple values per line, incomplete separators) that may hinder automatic parsing.
- Requires validation to ensure correct linkage between CocoaBugs_field_data_20230128.csv rows and the corresponding SAMN/SRA records.
- Recommendation to standardize Sample Name formatting and confirm alignment of SPUID, Organism, Tax ID, and BioProject across records.

## How Analysts can use and integrate
- Retrieve SRA records using PRJNA898889 and link back to field covariates in CocoaBugs_field_data_20230128.csv.
- Cross-check Sample Name mappings against Malaise_traps_ZG0001592.client.otuids.csv to maintain accurate species-by-sample associations.
- Store and publish derived datasets following standard environmental monitoring data practices (versions, provenance, and portal uploads).
- Integrate SRA-derived data with environmental covariates to enhance monitoring outputs and policy performance assessments.

## Access and provenance
- SRA data are tied to Accession PRJNA898889 with a Temporary Submission ID SUB12256650.
- Release date is 2024-12-31; post-release access via the provided SRA link.

## Key challenges
- Increasing the value of datasets by linking field environmental data with SRA-derived data and enabling broader data reuse.
- Ensuring accessible and well-documented underlying data (beyond final outputs) to support scrutiny and reproducibility.