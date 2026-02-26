# Experimental design/Sampling regime

## Study context and experimental streams
- Experimental streams rise in rough, sheep-grazed moorland (L6 & L7) or plantations of Sitka spruce with lodgepole pine (L3); some reductions of forest cover occurred in L3 due to logging.
- Three upland sites host cascading recirculating flumes for the Llyn Brianne catchment: L3 Hanwell, L6 Carpenter, L7 Davies.

## Sampling timeline and surfaces
- Samples collected at t = 0.5, 3, 15, and 24 hours.
- Epilithon sampled from unglazed ceramic tiles (top and bottom surfaces) using the toothbrush method; at 0.5 and 24 hours, additional samples from stones in the channel bottom.
- River inflow samples: 2 per river (one daytime, one nighttime) where rivers feed into the flumes.
- Samples frozen immediately after collection.

## Collection methods and field procedures
- Epilithon collected from tiles in the river channels; tiles cleaned and surface treated separately (top vs bottom).
- River samples collected directly at inflows and stored for transport to the lab.

## Fieldwork and laboratory instrumentation
- Field equipment: cascading recirculating flumes at three sites (L3 Hanwell, L6 Carpenter, L7 Davies).
- Laboratory instruments: Geneamp PCR System 9700; Illumina MiSeq v3 (2 x 300 bp) with Nextera XT chemistry; sequencing performed by GeneTiCA (Prague).

## Analytical methods and data processing
- DNA extraction: FastDNA SPIN Kit for soil with bead-beating.
- Target: bacterial 16S rRNA region amplified with primers 357F and 518R (and broader Illumina-compatible primers for MiSeq).
- PCRs run in triplicate and pooled; sequencing on Illumina MiSeq v3 (2 x 300 bp).
- Data analysis: R, QIIME, and microbial network analysis.

## Nature of recorded data and data formats
- Recorded data focus on presence/absence of bacterial communities.
- OTU (Operational Taxonomic Unit) table (OUT's table): rows are OTUs; columns 2–98 correspond to sample IDs; columns 99–105 contain taxonomic information.
- Mapping file (TAB-separated, 13 columns) includes:
  - SampleID (unique)
  - BarcodeSequence
  - LinkerPrimerSequence
  - FileName
  - tag_spacer_rev
  - Primer
  - Index
  - Combination_of_index
  - Stream
  - Treatment
  - Surface
  - Time
  - Description

## Data quality control and notes
- All PCRs included positive and negative controls; pooled samples validated with Agilent Bioanalyzer.
- Sample 73 (L7 daytime river sample) had notably low biomass and failed to amplify well.

## Extraction protocol details
- DNA extraction steps provided for FastDNA SPIN Kit for soil, including lysis with bead beating, purification, binding matrix steps, ethanol washes, drying, and final elution; storage at 4°C overnight.

## GIS-ready considerations and integration
- Spatial context: three flume sites within the Llyn Brianne catchment; sample metadata links each observation to a specific stream, flume, surface, and time point, enabling spatial-temporal mapping.
- Available data to map:
  - Presence/absence of bacterial communities per sample, linked to Site (L3/L6/L7), Flume (Hanwell/Carpenter/Davies), River inflow, Surface (top/bottom tile, bottom stones), Time (hours), and Treatment (control, sugar-amended, peat-amended).
  - OTU presence across samples, enabling spatial hotspots or temporal shifts in microbial communities when joined with sample metadata.
- Recommended GIS workflow:
  - Use SampleID to join OTU presence/absence and abundance data to the 13-column mapping table.
  - Create layers for Site/Flume locations, with attributes for Stream, Surface, Time, and Treatment.
  - Visualize temporal dynamics by time-sliced maps and surface-type comparisons (tile top/bottom vs stones).
  - Integrate with broader environmental layers (upland moorland vs plantation areas) to explore correlations between land-use context and microbial metrics.

## Contributors and data stewardship
- Sample collection: Isa-Rita Russo, Hugh Feeley, Marian Pye, Norhisham Razi, Katie Sworn, Luke Chrimes, Dominic Edwards, Matthew Nicholls, Jenny Peach, Sarah Johnston, Carwyn James.
- Laboratory analysis: Isa-Rita Russo, Sarah Johnston, Angharad Williams.
- Data processing: Sarah Johnston, Isa-Rita Russo.
- Planning and management: Isabelle Durance, Andrew Weightman.