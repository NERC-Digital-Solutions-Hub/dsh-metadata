# Methods for epilithon microbial community analysis in flume experiments

- Overview
  - Examines bacterial communities in epilithon from upland river flumes using 16S rRNA gene sequencing.
  - Three upland sites in Llyn Brianne catchment: L3 (Hanwell), L6 (Carpenter), L7 (Davies).
  - Experimental design includes different land-use contexts and treatment regimes (control, sugar-amended, peat-amended channels; adjacent rivers as references).

- Experimental design and sampling regime
  - Experimental streams rise in rough, sheep-grazed moorland or Sitka spruce plantations; some forest cover reductions observed.
  - Sampling at 0.5, 3, 15, and 24 hours.
  - Epilithon collected from unglazed ceramic tiles using a toothbrush method; tiles’ top and bottom processed separately.
  - Additional epilithon samples from stones in the channel bottom at 0.5 and 24 hours.
  - River inflows sampled at the flume entry (2 samples per river; day and night).
  - All samples frozen immediately after collection.

- Collection methods and field/lab instrumentation
  - Field site: three recirculating flumes at upland sites (L3 Hanwell, L6 Carpenter, L7 Davies).
  - Molecular workstations: PCRs on Geneamp System 9700; sequencing on Illumina MiSeq v3 (2 x 300 bp) with Nextera XT by GeneTiCA.
  - Samples stored at -70ºC on return to the laboratory.

- Analytical methods
  - DNA extraction: FastDNA Spin Kit for soil with bead beating; performed per protocol.
  - DNA quantification and quality checks (PCR controls included; positive/negative controls used).
  - 16S rRNA gene amplification: primers 357F and 518R; then primers S-D-Bact-0341-b-S-17 and S-D-Bact-0785-a-A-21 for bacteria (Klindworth et al. 2013).
  - Triplicate PCRs pooled; sequencing on Illumina MiSeq v3.
  - Bioinformatics: analyses performed in R, Qiime, and microbial network analysis tools.

- Data, metadata, and outputs
  - Mapping file (13 columns) defines sample identity and metadata:
    - SampleID, BarcodeSequence, LinkerPrimerSequence, FileName, Primer, Index, Combination_of_index, Stream, Treatment, Surface, Time, Description.
  - OTU (OTU table) structure:
    - Row per OTU; columns for each sample; taxonomic information in trailing columns.
  - Output-focused data:
    - Presence/absence of bacterial communities per sample.
    - Taxonomic assignments accompany OTU data.

- Quality control and issues
  - PCRs included positive and negative controls.
  - Pooled samples quality-checked with Agilent Bioanalyzer prior to sequencing.
  - Noted sample 73 (L7 daytime river sample) exhibited low biomass and poor amplification.
  - Detailed extraction protocol steps provided (FastDNA Spin Kit for soil), including lysis, purification, binding, washing, and elution steps.

- Data governance, management, and contributors
  - Data management and processing roles identified:
    - Sample collection: Isa-Rita Russo, Hugh Feeley, Marian Pye, Norhisham Razi, Katie Sworn, Luke Chrimes, Dominic Edwards, Matthew Nicholls, Jenny Peach, Sarah Johnston, Carwyn James.
    - Laboratory analysis: Isa-Rita Russo, Sarah Johnston, Angharad Williams.
    - Data processing: Sarah Johnston, Isa-Rita Russo.
    - Planning and management: Isabelle Durance, Andrew Weightman.
  - The document emphasizes structured metadata and clear data formats (mapping file, OTU table) to support reuse, traceability, and governance in environmental monitoring contexts.

- Relevance to monitoring frameworks authors
  - Demonstrates concrete endpoints for environmental health monitoring (presence/absence of bacterial communities in epilithon).
  - Provides a comprehensive data workflow: field sampling, sample handling, molecular analysis, and data products, suitable for informing policy and monitoring decisions.
  - Highlights the importance of rich metadata (streams, treatments, surfaces, time, river identity) to enable cross-site comparability and trend analysis.
  - Shows QA practices (controls, sequencing checks) and explicit data structures (mapping file, OTU table), addressing data quality and governance challenges.
  - Notes potential data gaps and issues (e.g., low-biomass samples) relevant to planning robust monitoring programs and data interpretation.
  - Illustrates involvement across planning, management, and technical execution, aligning with governance and stakeholder engagement aspects of monitoring frameworks.