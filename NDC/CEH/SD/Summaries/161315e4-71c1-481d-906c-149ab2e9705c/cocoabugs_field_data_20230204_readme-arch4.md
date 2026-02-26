# cocoabugs_field_data_20230204_readme.docx

## Overview
- Describes the locations and local environmental conditions of 123 Malaise trap samples collected in Nov–Dec 2021 in the 908 km2 forested buffer zone around Gola Rainforest National Park (GRNP), eastern Sierra Leone.
- Cocoa farming is the main cash crop in the area, linking to deforestation drivers.
- Data include environmental covariates and metabarcoding results (arthropod) linked to NCBI SRA accessions.
- Funded by the Natural Environment Research Council (Grant NE/S014063/1).

## Collection and provenance
- Sampling method: one Malaise trap per sampling point, deployed for 5 days with >99% ethanol in the collection bottle.
- Post-collection: trap contents transferred to fresh ethanol, stored at ambient temperature, then shipped to the UK for metabarcoding using Leray2 primers via NatureMetrics.
- Quality control (QC) highlights:
  - Primary errors: misrecorded covariates/samples, and errors from storage, amplification, sequencing, and bioinformatics.
  - Mitigations: field sheets transcribed to a spreadsheet on collection day; clear, multiple labeling; outsourcing to a commercial lab with validated pipelines to reduce technician-based errors.
- Data and collection context: supported by a cross-border workflow from field to sequencing, with attention to traceability and data integrity.

## Data structure and files
- CocoaBugs_field_data_20230128.csv: environmental covariates per sample; first column links to OTU table columns, second column links to SRA accessions.
- Malaise_traps_ZG0001592.client.otuids.csv: OTU table (species X sample). Key columns:
  - NMSeqID: unique OTU identifier (DNA barcode representative).
  - Columns for each sample (NatureMetrics_sample_name).
- BioSampleObjects_20230128.txt: maps SRA accessions to BioProject numbers.
- CocoaBugs_field_data_20230204_readme.docx: describes the OTU table columns and covariate data in CocoaBugs_field_data_20230128.csv.
- Cross-links:
  - NatureMetrics_sample_name connects covariates to OTU columns.
  - SRA_sample_name connects covariates to sequencing data (SRA entries).
  - Each NatureMetrics_sample_name corresponds to a row in CocoaBugs_field_data_20230128.csv and a column in Malaise_traps_ZG0001592.client.otuids.csv.
- Sample naming:
  - NatureMetrics_sample_name examples: ZG0001592_16425_MiSeq175.
  - SRA_sample_name examples: Section 1-1, 16425A (A/B indicate replicates).
  - Section/SITE_ID structure documents sampling logistics; not strictly needed for modelling.
- Replicates: indicated by trailing letters (A, B, etc.) in NatureMetrics sample identifiers.

## Nature and units of recorded values
- CocoaBugs_field_data_20230128.csv describes covariates, including:
  - Surveyor, deployment and collection dates/times, coordinates (Latitude/Longitude).
  - Habitat context around traps: canopy height, bare ground, grass, cocoa tree coverage, liana coverage, forest cover, agricultural land, recent burning, stumps, oil palm presence, and notes.
  - Equipment indicators: Audiomoth, BAR Recorder, sample tube presence.
- CocoaBugs_field_data_20230204_readme.docx describes the OTU table and covariate linkage in detail, including:
  - Taxonomic assignments (Kingdom to Species) and OTU metadata (incidence, similarity, status, notes, IUCN status when available).
  - Run IDs (RunID), sequences (Sequence), and field-to-lab linkage for traceability.

## Data concepts and identifiers
- OTU concept: NMSeqID is the NatureMetrics-assigned OTU representative sequence identifier.
- Taxonomy and quality: taxonomic levels (Kingdom, Phylum, Class, Order, Family, Genus, Species) with incidence and similarity metrics; Status indicates Target ( Arthropoda) or Unassigned; IUCN status included when confidently assigned.
- Metadata linkage: Field covariates (CocoaBugs_field_data_20230128.csv) anchor samples to OTUs (Malaise_traps_ZG0001592.client.otuids.csv) and sequencing data (BioSampleObjects_20230128.txt).
- Data lineage: Authenticates sample collection, lab processing, sequencing, and bioinformatic analysis through established pipelines (NatureMetrics).

## Data quality considerations
- Documented potential error sources:
  - Misrecording/mislabelling of environmental covariates and samples.
  - DNA degradation, cross-contamination during amplification, sequencing errors, and bioinformatic clustering/taxonomic assignment errors.
- Mitigations:
  - Immediate transcription of field sheets, clear and multiple labeling, and separation of duties via external sequencing service with validated workflows.
  - Use of fresh ethanol preservation to minimize degradation and a bespoke pipeline to reduce lab-borne errors.

## Governance, stewardship, and usage considerations
- The dataset is designed to support data system thinking: linking environmental covariates with molecular identifiers to enable integrative analyses across samples and OTUs.
- Discoverability and interoperability:
  - Centralized covariate CSVs and OTU tables with explicit linking keys (NatureMetrics_sample_name, SRA_sample_name, NMSeqID).
  - SRA accession data available via BioSampleObjects_20230128.txt for data access and provenance.
- Practical guidance for data leaders:
  - Maintain stable, well-documented identifiers across all linked data files.
  - Ensure metadata completeness and alignment between covariates, OTUs, and sequencing records.
  - Support reproducibility by preserving linkage maps and versioned pipelines; document updates to taxonomic assignments as reference databases evolve.
  - Facilitate cross-network collaboration by providing clear provenance, sample replication details, and field deployment context.