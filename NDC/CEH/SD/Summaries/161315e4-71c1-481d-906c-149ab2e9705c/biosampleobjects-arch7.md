The second column (SRA_sample_name) in CocoaBugs_field_data_20230128.csv connects each row of CocoaBugs_field_data_20230128.csv to one of the rows below (column name:  "Sample Name") CocoaBugs_field_data_20230128.csv contains both the environmental covariate data for each sample and the key to connect to the speciesXsample table (Malaise_traps_ZG0001592.client.otuids.csv)

- Accession to cite for these SRA data: PRJNA898889
- Temporary Submission ID: SUB12256650
- Release date: 2024-12-31
- SRA records will be accessible with the following link after the indicated release date:
  - https://www.ncbi.nlm.nih.gov/sra/PRJNA898889

Overview
- Purpose: Describes how environmental covariate data (in CocoaBugs_field_data_20230128.csv) can be linked to SRA sequencing data for Malaise trap samples via the Sample Name key.
- End product use: Facilitates integration of field covariates with sequencing/metagenome data for mapping and spatial analysis.

Data linkage and structure
- Linking key:
  - CocoaBugs_field_data_20230128.csv SRA_sample_name column links to "Sample Name" in the SRA/Malaise data.
- Data contained per sample:
  - Environmental covariates (from the CocoaBugs_field_data_20230128.csv)
  - Connection to the speciesXsample table (via Malaise_traps_ZG0001592.client.otuids.csv)
- SRA metadata (example entries shown in the document):
  - Accession entries such as SAMN31634495, SAMN31634496, SAMN31634497, etc.
  - Each entry includes:
    - SPUID, Organism, Tax ID, BioProject
    - Descriptors such as outdoor, metagenome, and section identifiers (e.g., Section 1-0, Section 1-1, etc.)
- Project context:
  - PRJNA898889 is the BioProject for these SRA records

GIS-relevant implications
- What you can create:
  - Map-based visualizations pairing sampling sites (via sample names) with environmental covariates and sequencing type (e.g., metagenome vs. organismal data)
  - Spatial layers showing sampling locations overlaid with covariates and taxonomic/metagenomic context
- Required data handling:
  - Join CocoaBugs_field_data_20230128.csv with the SRA/Malaise sample metadata using the SRA_sample_name/Sample Name key
  - If coordinates are not in the covariate file, geolocate sites from associated metadata or an adjacent dataset
- Output opportunities:
  - Spatial distributions of samples by environmental drivers
  - Comparisons of environmental covariates across outdoor vs metagenome samples
  - Integrated map products for policy, clients, or public-facing dashboards

Quality, standards and challenges
- Challenges highlighted:
  - Data held in many places and lack of consistent data standards
  - Large or complex datasets not packaged into manageable chunks
  - Cleaning and transforming data is required to enable reliable joins
- Data quality considerations for GIS:
  - Ensure consistent sample naming conventions across datasets
  - Validate that SRA_sample_name properly aligns with Sample Name in the Malaise data
  - Normalize and standardize environmental covariates before mapping
- Data availability and lifecycle:
  - SRA data will be accessible post-release date (2024-12-31)
  - Accession PRJNA898889 should be cited in any data product

Practical workflow for GIS data products
- Step 1: Import CocoaBugs_field_data_20230128.csv and extract the SRA_sample_name column
- Step 2: Obtain SRA/malaise metadata (Sample Name, SPUID, Organism, Tax ID, BioProject) from the provided dataset
- Step 3: Left-join environmental covariates to SRA metadata via the SRA_sample_name / Sample Name key
- Step 4: Geolocate sampling sites or attach existing coordinates from a companion dataset
- Step 5: Create map layers:
  - Sampling sites with covariates
  - Sampling type (outdoor vs metagenome) and section identifiers
  - Taxonomic/metagenomic context as an attribute layer or separate thematic maps
- Step 6: Validate joins and perform quality checks; resolve any inconsistencies or missing values
- Step 7: Produce final GIS data products and provide provenance (cite PRJNA898889)

Key terms and references
- SRA_sample_name: the linking key in CocoaBugs_field_data_20230128.csv
- Sample Name: the corresponding key in Malaise_traps_ZG0001592.client.otuids.csv and SRA metadata
- PRJNA898889: SRA BioProject accession for these data
- SUB12256650: Temporary Submission ID
- Release date: 2024-12-31 (date when SRA records become publicly accessible)
- Data types noted: outdoor samples, metagenome samples, and various Section identifiers (e.g., Section 1-0, Section 1-1)

End note
- This linkage enables GIS specialists to build integrated map-based data products that visualize how environmental covariates relate to sequencing and metagenomic data across sampling sites, while acknowledging the need for data cleaning and standardization to unlock reliable, scalable GIS outputs.