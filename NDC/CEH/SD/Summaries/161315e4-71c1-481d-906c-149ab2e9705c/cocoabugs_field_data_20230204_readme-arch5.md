# cocoabugs_field_data_20230204_readme.docx

- Overview
  - Describes locations and local environmental conditions of 123 Malaise trap samples collected in Nov–Dec 2021 in the 908 km2 forested “leakage belt” buffer of the Gola Rainforest National Park, eastern Sierra Leone; cocoa farming dominates as a driver of deforestation.
  - Area defined by a UTM bounding box and bounded by cocoa/agroforest context.
  - Funded by the Natural Environment Research Council (Grant NE/S014063/1).

- Collection and generation methods
  - Arthropods collected with a single Malaise trap per sampling point, deployed for 5 days with ethanol in the collection bottle.
  - Post-collection, samples transferred to clean ethanol, stored at ambient temperature, and shipped from Sierra Leone to the UK.
  - Metabarcoding performed by NatureMetrics using Leray2 primers via their bulk invertebrate service.

- Quality control (QC) considerations
  - Primary error sources identified: misrecording of environmental covariates and sample mislabelling; DNA degradation, cross-contamination during PCR, sequencing errors, and bioinformatics errors.
  - QC actions:
    - Handwritten field sheets transcribed to a spreadsheet on the collection day.
    - Sites and samples labeled clearly and multiplicatively before sequencing.
    - Bulk DNA approach reduces detectable contamination due to high sample DNA abundance.
    - Use of NatureMetrics’ bespoke lab and validated bioinformatic pipeline to mitigate metabarcoding errors (vs. relying on a single researcher).

- Data structure and files
  - CocoaBugs_field_data_20230128.csv
    - Records environmental covariates for each sample.
    - Key linking columns:
      - NatureMetrics_sample_name connects to sample columns in Malaise_traps_ZG0001592.client.otuids.csv.
      - SRA_sample_name connects to NCBI SRA BioSampleObjects.txt (fastq accessions).
  - Malaise_traps_ZG0001592.client.otuids.csv (OTU table)
    - Species X sample table (transposed OTU table).
    - NMSeqID: unique NatureMetrics OTU representative sequence name.
    - Taxonomic fields (Kingdom, Phylum, Class, Order, Family, Genus, Species) as assigned by NatureMetrics.
    - Incidence: number of samples the OTU is detected in.
    - Similarity: sequence similarity to reference used for taxonomic assignment.
    - Status: Target ( Arthropoda) or Unassigned.
    - Additional fields: IUCN.Red.List, RunID, Sequence (DNA barcode), etc.
  - BioSampleObjects_20230128.txt
    - Provides NCBI SRA accession numbers for each sample and the overarching BioProject number.

- Data provenance, linkage, and discoverability
  - Linkages:
    - Each CocoaBugs_field_data_20230128.csv row corresponds to a sample in Malaise_traps_ZG0001592.client.otuids.csv via NatureMetrics_sample_name.
    - SRA_sample_name in covariate data links to specific SRA BioSample entries in BioSampleObjects_20230128.txt, which in turn tie to the fastq files archived in SRA.
  - Reusability and discoverability:
    - SRA accession numbers and BioProject IDs enable retrieval of raw sequencing data.
    - Taxonomic assignments, incidence, and quality notes are embedded in the OTU table.

- Data semantics and naming conventions
  - NatureMetrics_sample_name encodes sampling context (sample column in OTU table).
  - SRA_sample_name encodes project and replicate details; a trailing letter (A, B, etc.) indicates technical replicates sequenced by NatureMetrics.
  - Section, SITE_ID, date_deploy/date_collect, and latitude/longitude fields provide spatial-temporal context and allow auditing of logistics and site movements (e.g., “New” sites or moves from the original plan).

- Covariates and units (examples)
  - Spatial: Latitude, Longitude.
  - Habitat features around traps: canopyHt_m, bare_ground_pct, grass_pct, cocoa_pct, liana_pct, forest_pct, agric_pct.
  - Disturbance and structure: recent_burning_y_n, stumps_gt_10cm_y_n, stumps_gt_30cm_y_n, oil_palm_y_n.
  - Survey logistics: sections, section-specific IDs, surveyor name, sample_tube presence.
  - Temporal: date_deploy, time_deploy, datetime_deploy, date_collect, time_collect, datetime_collect.
  - Miscellaneous: notes, Audiomoth and BAR_Recorder identifiers, run metadata, and, for OTUs, taxonomic and quality attributes (incidence, similarity, status, IUCN status).

- Practical considerations for Data Stewards
  - Data governance and completeness
    - Ensure covariate fields are complete and consistently encoded for each sample.
    - Maintain robust linkage between covariates, OTU table rows, and SRA/BioSample entries to preserve traceability.
  - Metadata standards and interoperability
    - Document and preserve the relationships across files (sample-level metadata, OTU-level taxonomy, and sequence data) to support reproducibility.
    - Track changes in taxonomic assignments over time if re-analyses occur.
  - Data quality and stewardship
    - Preserve QC notes and data provenance steps (transcription on collection day, labeling practices, ethanol preservation, laboratory pipeline) to justify data quality.
  - Access, licensing, and embargo
    - Leverage public SRA/BioProject records for discoverability; monitor any embargoes or rate-limiting access in the future.
  - Maintenance and updates
    - Consider versioning for fields that may be updated (taxonomy, metadata corrections) and maintain a changelog.
  - Potential challenges to plan for
    - Alignment of user needs with dataset structure and availability (cross-portal discoverability).
    - Handling multiple data formats and systems (field sheets, CSV OTU table, BioSample text, sequence data).
    - Managing large datasets and ensuring timely delivery of data to portals and users.
  - Documentation
    - Provide clear mappings between column names, sample identifiers, and their real-world meanings to facilitate discovery and reuse by others.