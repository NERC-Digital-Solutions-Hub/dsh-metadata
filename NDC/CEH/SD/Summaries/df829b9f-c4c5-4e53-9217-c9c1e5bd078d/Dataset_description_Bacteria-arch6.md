# Experimental design/Sampling regime

- Study settings and contexts
  - Experimental streams occur in rough, sheep-grazed moorland (L6 & L7) or in plantations of Sitka spruce (Picea sitchensis) with lodgepole pine (Pinus contorta) (L3).
  - Some reductions of forest cover have occurred in L3 due to normal logging operations.

- Sampling schedule and targets
  - Epilithon samples collected at time points t = 0.5, 3, 15 and 24 hours.
  - Epilithon collected from unglazed ceramic tiles colonised by epilithon in channels using the toothbrush method; top and bottom of each tile analyzed separately.
  - At 0.5 and 24 hours, additional epilithon samples taken from stones in the channel bottom.
  - Epilithon samples also collected directly from rivers at the point they feed into the flumes (2 samples per river: daytime and nighttime).
  - All samples frozen immediately after collection.

- Fieldwork and laboratory instrumentation
  - Experimental setup used cascading recirculating flumes at three upland sites for the Llyn Brianne catchment.
  - Flume identifications: L3 (Hanwell), L6 (Carpenter), L7 (Davies).
  - PCRs performed on a Geneamp PCR System 9700; sequencing on an Illumina MiSeq v3 (2 x 300 bp) with Nextera XT chemistry by GeneTiCA (Prague, Czech Republic).

- Analytical methods
  - DNA extraction from epilithon using the FastDNA SPIN Kit for soil with bead beating.
  - PCR setup: 50 μL reactions containing 10 μL PCR buffer, 0.2 μM of each primer, 1.5 U Taq polymerase, and ~50 ng/μL DNA.
  - Targeted bacterial 16S region amplified with primers 357F and 518R (Turner et al. 1999; Muyzer et al. 1993); alternative 16S primers S-D-Bact-0341-b-S-17 and S-D-Bact-0785-a-A-21 (Klindworth et al. 2013) used for sequencing.
  - Triplicate PCRs per sample pooled for sequencing on Illumina MiSeq v3.
  - Data analysis performed in R and QIIME with microbial network analysis.

- Nature and units of recorded data
  - Data represent presence/absence of bacterial communities (no quantitative abundance reported in the summary).

- Quality control
  - All PCRs included both positive and negative controls.
  - Pooled samples evaluated with an Agilent Bioanalyzer prior to sequencing.
  - Note: Sample 73 (L7 daytime river sample) had very low biomass and poor amplification.

- Data and metadata structure (mapping and OTU tables)
  - Mapping file format: tab-separated with 13 columns including
    - SampleID, BarcodeSequence, LinkerPrimerSequence, FileName, tag_spacer_rev, Primer, Index, Combination_of_index, Stream, Treatment, Surface, Time, Description.
  - OTU table: rows as OTUs; columns 2–98 correspond to sample IDs; columns 99–105 contain taxonomic information, with column 1 as OTU identifiers.

- DNA extraction protocol (FastDNA SPIN Kit for Soil)
  - Stepwise protocol (summarised)
    - Pre-extraction: add ethanol, prepare buffers and components.
    - Lysis and initial processing: add SPB and MT Buffer to samples, bead-beat, cool, and centrifuge to collect supernatant.
    - Binding and washing: mix with PPS, centrifuge, transfer to binding matrix, perform successive washes with BMS and SEWS-M-EtOH steps; centrifuge to dry the filter.
    - Final elution: add sterile water, re-suspend, incubate, centrifuge to recover DNA.
    - Storage: store DNA at 4°C overnight.

- Contributors to the dataset
  - Sample collection: Isa-Rita Russo, Hugh Feeley, Marian Pye, Norhisham Razi, Katie Sworn, Luke Chrimes, Dominic Edwards, Matthew Nicholls, Jenny Peach, Sarah Johnston, Carwyn James.
  - Laboratory analysis: Isa-Rita Russo, Sarah Johnston, Angharad Williams.
  - Data processing: Sarah Johnston, Isa-Rita Russo.
  - Planning and management: Isabelle Durance, Andrew Weightman.