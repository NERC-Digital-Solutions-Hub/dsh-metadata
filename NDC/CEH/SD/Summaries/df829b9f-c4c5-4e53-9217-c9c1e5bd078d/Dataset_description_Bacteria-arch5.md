# Experimental design/Sampling regime

## Overview
- Describes experimental streams in upland moorland and Sitka spruce plantation environments, with some forest cover reductions due to logging.
- Data collection focused on epilithon from river channels and associated flumes across three sites, aiming to study microbial communities via 16S rRNA sequencing.

## Sampling and collection methods
- Sampling times: 0.5, 3, 15, and 24 hours.
- Epilithon collected from unglazed ceramic tiles using a toothbrush method; top and bottom tile surfaces sampled separately.
- Additional samples: epilithon from stones in the channel bottom (at 0.5 and 24 hours) and two river-fed samples per river (day and night).
- All samples frozen immediately after collection.

## Fieldwork and laboratory instrumentation
- Experimental setup: cascading recirculating flumes at three upland sites in the Llyn Brianne catchment (L3 Hanwell, L6 Carpenter, L7 Davies).
- PCR and sequencing: Illumina MiSeq v3 (2 x 300 bp) with Nextera XT chemistry, performed by GeneTiCA (Prague).
- PCR controls included positive and negative controls; some samples (e.g., sample 73) exhibited low biomass and poor amplification.

## Analytical methods and data types
- DNA extraction: FastDNA SPIN Kit for soil with bead beating; samples stored at -70°C prior to extraction.
- Amplification: 50 μl reactions with specified primers (357F and 518R; broader bacterial 16S primers S-D-Bact-0341-b-S-17 and S-D-Bact-0785-a-A-21 for Illumina), triplicate PCRs pooled for sequencing.
- Sequencing: Illumina MiSeq v3 (2 x 300 bp).
- Data analysis: R, QIIME, and microbial network analysis.
- Data products include presence/absence of bacterial communities and OTU tables with taxonomic information.

## Data files, formats, and metadata schema
- Mapping file: single tab-separated file with 13 columns, including:
  - SampleID, BarcodeSequence, LinkerPrimerSequence, FileName, tag_spacer_rev, Primer, Index, Combination_of_index, Stream, Treatment, Surface, Time, Description.
- OTU table (OUT's table): rows for OTUs; columns labeled by sample IDs and including taxonomic information.
- Reference metadata provide a detailed schema to link samples to rivers, treatment types, sampling surfaces, and times.
- Sequencing and primer details (forward/reverse primers, primer overhangs) included to support reproducibility.

## Extraction and lab protocol details
- Detailed FastDNA SPIN Kit for soil protocol provided, including:
  - Lysis, bead beating, centrifugation, binding and washing steps.
  - Specific reagent volumes and timings for multiple steps.
  - Conditions for elution and storage of DNA (4°C overnight).
- Storage and handling notes emphasize consistent cold-chain management and careful handling of low-biomass samples.

## Quality control and limitations
- Positive and negative PCR controls used; samples screened for quality with Agilent Bioanalyzer prior to sequencing.
- Some samples (notably sample 73) showed low biomass and suboptimal amplification, highlighting potential biases with low-input DNA.
- No explicit data access controls or embargo notes are stated; however, the inclusion of controls and combined metadata supports data reliability and reuse.

## Metadata, provenance, and contributors
- Comprehensive attribution of roles:
  - Sample collection contributors.
  - Laboratory analysis team.
  - Data processing team.
  - Planning and management leads.
- Provenance links between sample IDs, rivers, treatments, surfaces, and observation times enable traceability of data from collection through processing to analysis.

## Data management implications for data stewards
- Strengths:
  - Rich, structured metadata enabling discoverability and reuse across datasets.
  - Clear mapping between sample identifiers, sequencing data, and experimental conditions.
  - Detailed documentation of extraction and amplification protocols enhances reproducibility.
- Considerations for governance and interoperability:
  - Ensure long-term storage of raw FASTQ data, OTU tables, and processed taxonomic assignments with versioning.
  - Maintain the integrity of the 13-column mapping file and OTU table schema; consider standardizing to widely adopted metadata schemas.
  - Provide clear access points and licensing for data and any derived analyses.
  - Monitor and document any data quality flags (e.g., low biomass samples) and associated caveats for reuse.
  - Ensure ongoing data updates or corrections are tracked and reflected in the catalogue.