# Experimental design/Sampling regime

- Context and aim
  - Experimental streams rise in rough, sheep-grazed moorland (L6 & L7) or plantations of Sitka spruce with lodgepole pine (L3); some forest cover reduction has occurred in L3 with normal logging.
  - Study focuses on epilithon in river channels within three upland flumes to assess microbial communities under different environmental conditions and temporal sampling.

- Treatments and data scope
  - Treatments recorded per sample include control, sugar-amended, peat-amended channels, or the adjacent river.
  - Data outputs include presence/absence of bacterial communities and downstream taxonomic information.

## Sampling regime and collection methods

- Sampling times
  - t = 0.5, 3, 15, and 24 hours.
- Substrate and sampling surface
  - Epilithon collected from unglazed ceramic tiles (top and bottom surfaces) using a toothbrush method.
  - Additional samples (0.5 h and 24 h) taken from stones in the channel bottom.
  - River samples taken directly from the river feeding into each flume (2 samples per river: day and night).
- Sample handling
  - Samples were frozen immediately after collection.

## Fieldwork and Laboratory instrumentation

- Experimental setup
  - Cascading recirculating flumes at three upland sites within the Llyn Brianne catchment.
  - Flume mapping: L3 (Hanwell), L6 (Carpenter), L7 (Davies).
- Molecular work
  - PCRs performed on the Geneamp PCR System 9700.
  - Sequencing conducted on an Illumina MiSeq v3 (2 x 300 bp) with Nextera XT chemistry by GeneTiCA (Prague).

## Analytical methods

- DNA processing
  - Epilithon samples stored at -70°C prior to DNA extraction.
  - Extraction performed with the FastDNA SPIN Kit for soil, including bead beating.
- PCR amplification
  - Primers: 357F/518R for general bacterial 16S, plus Klindworth et al. 2013 set for Illumina-compatible amplification.
  - Reactions: triplicate PCRs per sample, pooled for sequencing.
- Sequencing and data analysis
  - Sequencing on Illumina MiSeq v3.
  - Data analysis conducted using R, QIIME, and microbial network analysis tools.

## Nature and units of recorded values

- Data type
  - Presence/absence of bacterial communities; OTU (operational taxonomic unit) based abundance data with taxonomic assignment.

## Quality control

- Controls
  - Positive and negative PCR controls included.
  - Pooled samples assessed with Agilent Bioanalyzer prior to sequencing.
- Notes
  - Sample 73 (L7 daytime river sample) showed very low biomass and did not amplify well, indicating potential low-template bias.

## Data structure and file formats

- OTU table
  - Rows: OTUs; Columns: OTU ID, then sample IDs, followed by taxonomic information.
- Mapping file
  - A single tab-separated file with 13 columns, including:
    - SampleID, BarcodeSequence, LinkerPrimerSequence, FileName, Primer, Index, Combination_of_index, Stream, Treatment, Surface, Time, Description.
- Sample metadata and traceability
  - Mapping file links samples to river source, surface sampled, time point, treatment, and descriptive identifiers.

## Extraction protocol (as per FastDNA SPIN Kit for Soil)

- Reagents and prep
  - Detailed steps outlining lysis, bead beating, centrifugation, binding, washing, and elution to yield DNA, including specific volumes and times.
- Storage
  - Extracted DNA stored under specified conditions (4°C overnight noted).

## Contributors and roles

- Sample collection: Isa-Rita Russo, Hugh Feeley, Marian Pye, Norhisham Razi, Katie Sworn, Luke Chrimes, Dominic Edwards, Matthew Nicholls, Jenny Peach, Sarah Johnston, Carwyn James.
- Laboratory analysis: Isa-Rita Russo, Sarah Johnston, Angharad Williams.
- Data processing: Sarah Johnston, Isa-Rita Russo.
- Planning and management: Isabelle Durance, Andrew Weightman.