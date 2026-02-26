# cocoabugs_field_data_20230204_readme.docx

- Overview
  - 123 Malaise trap samples collected in November–December 2021 in the 908 km² forested buffer zone (“leakage belt”) of Gola Rainforest National Park (GRNP), eastern Sierra Leone.
  - Cocoa farming is the main cash crop driving deforestation in the area.
  - Study area bounding box provided with UTM coordinates; area and location details included.
  - Research supported by Natural Environment Research Council (Grant NE/S014063/1).

- Study context and sampling design
  - Each sampling point used a single Malaise trap deployed for 5 days with >99% ethanol in the collection bottle.
  - Traps' contents were transferred promptly to clean tubes with fresh 99% ethanol, then transported to the UK for metabarcoding.

- Collection and metabarcoding methods
  - Metabarcoding performed on bulk invertebrate samples using Leray2 PCR primers.
  - Sequencing and analysis conducted by NatureMetrics (commercial service) with their eDNA lab and bioinformatic pipeline.

- Quality control and data integrity
  - Key error sources: misrecording environmental covariates, mislabelling samples, DNA degradation, cross-contamination, sequencing errors, and bioinformatics clustering/taxonomic assignment errors.
  - Mitigation steps: transcription of handwritten field sheets to a spreadsheet on collection day; careful, multiresample labelling; immediate transfer to fresh ethanol; reliance on NatureMetrics’ trained laboratory and pipeline to reduce metabarcoding errors.
  - Bulk eDNA competition reduces trace contamination risk due to high sample DNA abundance.

- Data structure and files
  1) CocoaBugs_field_data_20230128.csv
     - Contains environmental covariate values for each sample.
     - First column NatureMetrics_sample_name links to sample columns in Malaise_traps_ZG0001592.client.otuids.csv.
     - Second column SRA_sample_name links to samples in NCBI SRA (BioSampleObjects.txt).
  2) Malaise_traps_ZG0001592.client.otuids.csv
     - Species x sample (transposed OTU table).
     - NMSeqID: unique OTU identifier (DNA barcode sequence representative).
     - Taxonomic fields (Kingdom, Phylum, Class, Order, Family, Genus, Species) and incidence per sample.
     - Sequence: representative DNA barcode sequence (not all fields populated in this dataset).
     - Similarity: sequence similarity to GenBank reference.
     - Status: Target ( Arthropoda) or Unassigned; IUCN.Red.List and other metadata fields included.
     - RunID, Sequence, and sample-name mappings explained within.
  3) BioSampleObjects_20230128.txt
     - Provides the SRA accession numbers for each sample and the overall BioProject identifier.

- Nature and units of recorded values (CocoaBugs_field_data_20230128.csv)
  - NatureMetrics_sample_name: maps to a specific sample column in the OTU table.
  - SRA_sample_name: maps to the corresponding SRA BioSample entry; indicates fastq files for that sample.
  - Sample naming conventions indicate sample replication (e.g., A, B) and project-specific naming.
  - Section and SITE_ID describe the sampling logistics; notes on site movement (New) or origin (from orig plan).
  - Temporal and location data: date_deploy, time_deploy, datetime_deploy; date_collect, time_collect, datetime_collect; latitude and longitude.
  - Environmental covariates describing habitat around the trap within 30–50 m: canopyHt_m, bare_ground_pct, grass_pct, cocoa_pct, liana_pct, forest_pct, agric_pct, recent_burning_y_n, stumps_gt_10cm_y_n, stumps_gt_30cm_y_n, oil_palm_y_n; notes on site context.
  - Equipment and sampling details: Audiomoth, BAR_Recorder, sample_tube.
  - The dataset structure supports auditing and cross-referencing environmental context with arthropod metabarcoding data.

- OTU data and taxonomy (Malaise_traps_ZG0001592.client.otuids.csv)
  - NMSeqID: OTU’s unique NatureMetrics sequence identifier (DNA barcode).
  - Taxonomic fields (Kingdom to Species) assigned by NatureMetrics.
  - incidence: number of samples in which the OTU is detected.
  - Similarity: percent similarity to the reference sequence used for taxonomy.
  - Comments: notes on taxonomic confidence.
  - Status: Target (within the PCR-targeted group) or Unassigned.
  - IUCN.Red.List: conservation status where assigned.
  - RunID: sequencing run designation (MiSeq run, etc.).
  - Sequence: the actual barcode sequence (where present).
  - NatureMetrics_sample_name: links to the corresponding environmental covariate data in CocoaBugs_field_data_20230128.csv.

- Linkages and how to use the data
  - Each NatureMetrics_sample_name in CocoaBugs_field_data_20230128.csv corresponds to a column in Malaise_traps_ZG0001592.client.otuids.csv, enabling sample-level ecological and taxonomic analyses.
  - Each NatureMetrics_sample_name also connects to SRA_sample_name in BioSampleObjects_20230128.txt, tying environmental covariates to sequencing data.
  - The combined dataset allows exploration of relationships between habitat variables (e.g., cocoa plantation coverage, canopy height, ground cover) and arthropod community composition and diversity (OTU incidence, taxonomic composition, and potential functional groups).

- Potential analytical applications
  - Assess correlations between environmental covariates and arthropod OTU richness, incidence, and taxonomic composition.
  - Compare Arthropoda community structure across sites with varying cocoa crop presence, canopy cover, and disturbance (e.g., recent burning, stumps, oil palm proximity).
  - Identify taxa with indicators of cocoa-forest edge effects or habitat degradation.
  - Integrate geographic and temporal data to examine spatial or seasonal patterns within the 5-day trap intervals.

- Limitations and considerations for analysts
  - Sample scale and coverage: 123 samples over a defined 908 km² buffer zone; 5-day trap periods per site.
  - Covariate completeness and consistency: potential gaps or variation in covariate recording across sites.
  - Data provenance: reliance on a commercial metabarcoding service with a standardized pipeline; some fields may be sparse or not fully populated.
  - Replication and comparability: certain variables may have replicates or site-specific nuances requiring careful handling in comparative analyses.
  - Data integration: some fields (e.g., Sequence) may be not populated for all OTUs; cross-check with SRA records for sequencing details.

- Funding and access
  - Data generated under the Natural Environment Research Council grant NE/S014063/1.
  - Data is organized to be discoverable via linked covariates, OTU tables, and sequencing metadata to support reproducible analyses.