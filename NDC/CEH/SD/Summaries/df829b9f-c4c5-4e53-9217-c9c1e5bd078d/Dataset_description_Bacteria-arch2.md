# Experimental design/Sampling regime

## Study context
- Experimental streams originate from two habitat types: rough, sheep-grazed moorland (L6 & L7) and Sitka spruce lodgepole pine plantations (L3), with some forest-cover reductions at L3 due to normal logging.

## Sampling regime
- Sampling times: t = 0.5, 3, 15, and 24 hours.
- Epilithon collection:
  - From unglazed ceramic tiles colonised by epilithon in channels using a toothbrush method; top and bottom of each tile handled separately.
  - At 0.5 and 24 hours, additional epilithon sampled from stones on the channel bottom.
  - Additional river samples taken directly where rivers feed into the flumes (2 samples per river: one during the day, one at night).
  - All samples frozen immediately after collection.

## Fieldwork and laboratory instrumentation
- Experimental setup: Cascading recirculating flumes at three upland sites within the Llyn Brianne catchment (L3/Hanwell, L6/Carpenter, L7/Davies).
- Molecular workflow:
  - PCRs performed on a Geneamp PCR System 9700.
  - Sequencing conducted on an Illumina MiSeq v3 (2 x 300 bp) with Nextera XT chemistry by GeneTiCA (Prague, Czech Republic).

## Analytical methods
- Epilithon processing:
  - Samples stored at -70°C prior to DNA extraction.
  - DNA extraction with FastDNA SPIN Kit for soil (bead beating step included).
- DNA amplification:
  - PCR setup: 50 μl reactions with specific buffer, primers (357F and 518R; bacterial 16S primers S-D-Bact-0341-b-S-17 and S-D-Bact-0785-a-A-21), and 1 μl DNA template.
  - Triplicate PCRs per sample, pooled and sequenced on Illumina MiSeq (2 x 300 bp).
- Data analysis:
  - Software: R, QIIME, and microbial network analysis.
- Target data type:
  - Presence/absence of bacterial communities.

## Quality control and data structure
- Controls:
  - Each PCR included positive and negative controls.
  - Pooled samples screened with Agilent Bioanalyzer prior to sequencing.
  - Note: Sample 73 (L7 daytime river sample) showed low biomass and poor amplification.
- Mapping file (QIIME format) structure:
  - Includes SampleID, BarcodeSequence, LinkerPrimerSequence, FileName, tag_spacer_rev, Primer, Index, Combination_of_index, Stream, Treatment, Surface, Time, Description.
- OTU table:
  - Rows represent OTUs; columns include OTU identifiers, sample-specific counts, and taxonomic information for 99–105 additional columns.

## Extraction protocol (FastDNA SPIN Kit for Soil)
- Reagents and initial setup:
  - 100 mL ethanol added to SEWS-M bottle.
- Lysis and washing:
  - Add specific volumes of SPB, MT Buffer, and defrosted sample to LME tubes.
  - Freeze/thaw cycles and bead-beating steps followed by centrifugation.
  - Transfer supernatant and perform binding matrix processing with PPS and subsequent centrifugation.
- Purification and elution:
  - Sequential loading onto spin filter, washing with SEWS-M-EtOH, and final elution with sterile water.
  - Final preparation included an overnight storage at 4°C.
  
## Contributors
- Sample collection: Isa-Rita Russo, Hugh Feeley, Marian Pye, Norhisham Razi, Katie Sworn, Luke Chrimes, Dominic Edwards, Matthew Nicholls, Jenny Peach, Sarah Johnston, Carwyn James.
- Laboratory analysis: Isa-Rita Russo, Sarah Johnston, Angharad Williams.
- Data processing: Sarah Johnston, Isa-Rita Russo.
- Planning and management: Isabelle Durance, Andrew Weightman.