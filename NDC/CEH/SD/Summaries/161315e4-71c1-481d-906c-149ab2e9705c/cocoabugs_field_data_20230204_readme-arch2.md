# cocoabugs_field_data_20230204_readme.docx

## Overview and Context
- 123 Malaise trap samples collected Nov–Dec 2021 in the 908 km² forested “leakage belt” buffer of Gola Rainforest National Park (GRNP), eastern Sierra Leone.
- Cocoa farming is the main cash crop driving deforestation in the area.
- Study supported by Natural Environment Research Council (Grant NE/S014063/1).
- Bounding box for the Area of Study provided via UTM coordinates.

## Methods and Quality Assurance
- Arthropods collected with Malaise traps at each sampling point for 5 days using ethanol-preserved collection bottles.
- After collection, samples transferred to fresh 99% ethanol, stored at ambient temperature, then shipped to the UK for metabarcoding (NatureMetrics) using Leray2 primers.
- Quality assurance focuses on avoiding misrecording labelling errors and contamination:
  - Handwritten field sheets transcribed to a spreadsheet on the day of collection.
  - Clear, multiple labelling of samples before sequencing.
  - Bulk DNA in bulk-arthropod samples minimizes trace contamination risk.
  - Use of a commercial metabarcoding service with a tested bioinformatic pipeline to reduce error rates.

## Data Products and Structure
- CocoaBugs_field_data_20230128.csv
  - Contains environmental covariates for each sample.
  - NatureMetrics_sample_name links to the OTU table; SRA_sample_name links to NCBI BioSampleObjects and fastq files.
- Malaise_traps_ZG0001592.client.otuids.csv
  - OTU table (species X sample format; transposed).
  - NMSeqID is the OTU identifier; taxonomic fields (Kingdom, Phylum, Class, Order, Family, Genus, Species) populated by NatureMetrics.
  - Incidence (number of samples OTU detected), Similarity (taxonomy assignment confidence), Status (Target vs Unassigned), IUCN.Red.List, and other metadata (RunID, Sequence).
- BioSampleObjects_20230128.txt
  - NCBI SRA accession numbers and overall BioProject numbers for the samples.

## Metadata: Covariates and Taxonomy Details
- CocoaBugs_field_data_20230128.csv (and the corresponding readme sections)
  - Core covariates include: Section, Surveyor, Date/Time of deployment and collection, Site ID, latitude/longitude, canopy height, bare ground, grass, cocoa tree coverage, liana cover, forest cover, agricultural cover, recent burning, stump presence at various diameters, oil palm presence, notes, and instrument metadata (Audiomoth, BAR Recorder, sample tube status).
  - Sectioning reflects sampling campaigns; GRNP sites provide a contrast against agroecosystem sampling.
  - Sample naming conventions link to OTU data and SRA accessions; multiple replicates are indicated (e.g., A, B).
- Malaise_traps_ZG0001592.client.otuids.csv
  - Taxonomic assignments for OTUs (Kingdom through Species) with incidence and similarity metrics.
  - Additional fields: Comments (confidence notes), Status (Target vs Unassigned), IUCN Red List if assignable, and RunID.
  - Sequence data column contains the representative DNA barcode sequence (not all fields used in this dataset).

## Data Access, Provenance, and Context
- SRA accessions and BioProject references are provided to enable retrieval of the raw sequencing data.
- The dataset connects environmental covariates to metabarcoding outputs via the NatureMetrics pipeline.
- Context: data are generated to monitor arthropod communities in a cocoa-dominated landscape within a protected area, contributing to environmental health and policy performance assessments.

## Relevance for Environmental Monitoring
- Provides a standardized, auditable dataset linking field covariates to metabarcoding-derived arthropod community data.
- Enables tracking of biodiversity changes over time in a cocoa-agroforest interface and protected area context.
- Supports integration with other environmental datasets to strengthen monitoring and policy evaluation.

## Challenges and Opportunities for Data Use
- Increasing the value of datasets by integrating with other relevant data sources (to avoid single-use outputs).
- Ensuring broad access to underlying data for secondary analyses and transparency.