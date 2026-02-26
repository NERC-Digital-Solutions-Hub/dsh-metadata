# Experimental design/Sampling regime

- Experimental streams and setting
  - Streams arise from rough, sheep-grazed moorland (L6 & L7) or Sitka spruce with lodgepole pine plantations (L3); some forest cover reductions occurred in L3 due to logging.

- Sampling regime and collection methods
  - Time points: t = 0.5, 3, 15, 24 hours.
  - Epilithon sampling from unglazed ceramic tiles colonised in channels using a toothbrush method; top and bottom tile surfaces processed separately.
  - At 0.5 and 24 hours, additional epilithon from stones in the channel bottom.
  - River inlet samples collected (2 samples per river; one during the day, one at night).
  - All samples frozen immediately after collection.

- Fieldwork and instrumentation
  - Cascading recirculating flumes at three upland sites in the Llyn Brianne catchment.
  - Flume names: Hanwell (L3), Carpenter (L6), Davies (L7).
  - PCRs on a Geneamp 9700; sequencing on Illumina MiSeq v3 (2 × 300 bp) with Nextera XT, conducted via GeneTiCA (Prague).

- Analytical workflow
  - DNA extraction: FastDNA SPIN Kit for soil with bead beating.
  - 16S rRNA amplification with primers 357F and 518R; triplicate PCRs pooled.
  - Sequencing: Illumina MiSeq v3; data analyzed using R, QIIME, and microbial network analysis.

- Data type and outcomes
  - Presence/absence data of bacterial communities.
  - OTU table structure: rows are OTUs; columns include sample IDs and taxonomic information (taxa in the latter columns).

- Quality control
  - Positive and negative PCR controls; pooled samples checked with Agilent Bioanalyzer.
  - Note: Sample 73 (L7 daytime river) had very low biomass and poor amplification.

- Metadata and data structure
  - QIIME mapping file: 13 columns including SampleID, BarcodeSequence, LinkerPrimerSequence, FileName, Primer, Index, Combination_of_index, Stream, Treatment, Surface, Time, Description.
  - OTU table: columns 2–98 for sample data; columns 99–105 for taxonomic information.

- Extraction protocol (FastDNA SPIN Kit for Soil)
  - Stepwise lysis, purification, binding, washing, drying, elution; final elution in sterile water; storage at 4°C overnight.

- Contributors
  - Sample collection: Isa-Rita Russo, Hugh Feeley, Marian Pye, Norhisham Razi, Katie Sworn, Luke Chrimes, Dominic Edwards, Matthew Nicholls, Jenny Peach, Sarah Johnston, Carwyn James.
  - Laboratory analysis: Isa-Rita Russo, Sarah Johnston, Angharad Williams.
  - Data processing: Sarah Johnston, Isa-Rita Russo.
  - Planning and management: Isabelle Durance, Andrew Weightman.