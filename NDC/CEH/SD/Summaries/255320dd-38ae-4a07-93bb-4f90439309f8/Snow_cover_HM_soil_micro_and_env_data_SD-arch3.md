Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a snow manipulation experiment in Hohe Mut, Austria, 2017' deposited in the Environmental Information Data Centre repository

## Overview
- Describes the alpine field experiment, measurements, and data structure for environmental, biogeochemical, enzymatic, and microbial data collected in 2017.
- Aims to enable scrutiny of environmental health measures and inform future monitoring decisions.
- Located on the Hohe Mut summit (2650 m), Austria, with three snow manipulation treatments applied to replicated plots.

## Experimental design and treatments
- Field setup: 15 plots of 6 m x 15 m, randomly allocated to three treatments (n = 5 per treatment): snow removal, snow addition, and untreated control.
- Plots fenced to prevent trampling; snow manipulated three times from late March to late May 2017.
- Snow depth on removal plots reduced to <10 cm, with a thin layer left to avoid ground/vegetation disturbance.
- Snow in addition plots evenly increased; control plots left undisturbed.

## Sampling regime
- Soil sampling at six time points spanning late winter to early summer 2017:
  - Late winter (28 March)
  - Snowmelt (1 June and 8 June)
  - Spring post-snowmelt (12 June and 18 June)
  - Summer (8 July)
- Five random locations per plot; cores (diameter 2 cm, depth 7 cm) collected, pooled per plot, and homogenised.
- Vegetation and litter removed; subsamples allocated for molecular analyses and biogeochemical analyses.

## Laboratory analyses

### Biogeochemical cycling and soil properties
- Plant-available NH4+-N and NO3−-N: extracted with 1 M KCl (5 g soil, 25 mL extractant); DON: extracted with ultrapure water (35 mL).
- Mineralisation: 14-day incubation at 25°C to determine NH4+-N and NO3−-N release.
- Dissolved organic carbon (DOC): water extraction and measured with TOC analyzer.
- pH (1:2.5 soil:water), soil water content by gravimetry, total C and N by elemental analysis (105°C dried soil).

### Extracellular enzyme assays (microbial functioning)
- Eight enzymes: β-glucosidase (GLC), cellobiohydrolase (CBH), β-xylosidase (XYL), N-acetylglucosaminidase (NAG), phosphatase (PHO), urease (URE), phenol oxidase (POX), and peroxidase (PER).
- GLC, CBH, XYL, NAG, PHO measured photometrically with specific substrates; incubation times range from 0.5 to 3 hours; absorbance at 405 nm.
- POX and PER measured via L-DOPA oxidation at 450 nm; times t0, t1 (1.5 h or 20 h), with corrections for colouration and enzyme overlap.
- URE determined by ammonium production from urea; measured via Berthelot reaction after KCl extraction.
- Enzyme activities standardized relative to microbial biomass using PLFA.

### Phospholipid fatty acids (PLFA)
- PLFA profiling to estimate total microbial biomass and community composition (fungi vs. bacteria; Gram-positive vs. Gram-negative).
- Extraction, saponification, and analysis by GC; biomarker lipids used to assign fungal/bacterial groups.
- Biomass expressed as nmol g soil−1; calculations include fungal:bacterial and Gram+:/Gram− ratios.

### DNA extraction and microbial community profiling
- DNA extraction with ZR Soil Microbe DNA kit; enhanced lysis step in FastPrep.
- Sequencing targets: bacteria (16S rRNA) and fungi (ITS2).
- 2-step Illumina PCR with tagged primers; libraries quantified and pooled; MiSeq sequencing (V3 chemistry).
- Data processing with DADA2 in R: quality filtering, dereplication, ASV inference, chimera removal; taxonomic assignment against GreenGenes (16S) and UNITE (ITS).
- Sequencing depth after filtering: ~5.7 million bacterial and ~3.1 million fungal sequences; rarefaction to equal depths (10,083 for 16S; 5,349 for ITS).

## Data structure and files

### Primary data files
- Snow_cover_HM_soil_env_data.csv
  - Contains soil abiotic data, PLFA, and soil extracellular enzyme activities.
  - Columns describe: date, timepoint, season, plot, treatment, snow status, sampling metadata, and a wide array of measurements (DOC, NH4, NO3, TN, TOC, pH, soil moisture, enzyme activities, PLFA metrics, and related derivatives).

### Microbial sequence and taxonomy files
- Snow_cover_HM_seq_tab_16S.csv
  - OTU/ASV abundance table for bacteria; sample-by-feature counts.
- Snow_cover_HM_seq_tab_ITS.csv
  - OTU/ASV abundance table for fungi; sample-by-feature counts.
- Snow_cover_HM_16S_taxa.csv
  - Taxonomic assignment for 16S features.
- Snow_cover_HM_ITS_taxa.csv
  - Taxonomic assignment for ITS features.

### Raw sequence data
- Raw sequence data are undergoing deposition at the European Bioinformatics Institute (EBI).

## Data availability, provenance, and processing
- Detailed experimental protocol and data processing steps provided to enable reproducibility and auditing.
- Data linked across abiotic measurements, enzyme activities, PLFA, and microbial community profiles, enabling integrated analyses of biogeochemical cycling and microbial ecology under snow manipulation.
- Data governance considerations include metadata structure, transparent data processing pipelines, and public sharing requirements discussed in the context of monitoring frameworks.

## Relevance to monitoring frameworks
- Demonstrates end-to-end data workflow: from field manipulation and sampling through lab analyses to data structuring and sharing.
- Addresses common monitoring challenges:
  - Data gaps and standardization: comprehensive suite of abiotic, enzymatic, lipid-based, and sequence-based metrics with standardized protocols.
  - Data accessibility and transparency: multiple data files with explicit schemas; plans for public deposition of raw sequences.
  - Metadata and data quality: explicit sampling dates, treatments, sampling depth, storage conditions, and processing steps; normalization and rarefaction details for sequencing data.
  - Data governance: explicit data structure, linking of environmental variables to microbial data, and references to processing pipelines (e.g., DADA2, PLFA methods).
- Provides a model for reporting, documenting, and sharing environmental health monitoring data in a coherent, citable package suitable for policy evaluation and future decision-making.