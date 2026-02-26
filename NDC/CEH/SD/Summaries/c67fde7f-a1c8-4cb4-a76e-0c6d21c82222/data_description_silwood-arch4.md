# Wild rodents social networks and the microbiome

## Overview
- A dataset combining trapping data, tracking data, and microbiome composition from wild rodents at Silwood Park (2014-2015).
- Aim: study how social contacts influence gut microbe transmission in a wild setting.
- Data collected across three linked components: field/behavioral data, kinship/genetics, and gut microbiome sequencing.
- Data processing and quality control applied at multiple stages (field protocols, lab workflows, sequencing, and bioinformatics).

## Data Types and Collection

- Field data collection
  - Wild rodent population in a 2.47 ha woodland plot (Nash's Copse) at Imperial College Silwood Park.
  - Species included Apodemus sylvaticus, Apodemus flavicollis, Myodes glareolus; trapping every 2-4 weeks over 2014-2015.
  - 122 Sherman traps used; traps baited and cleaned between sessions; animals processed, sampled, and released within their grid cell.
  - Each animal identified by PIT-tag; ear punches collected for host genotyping; faecal samples collected for microbiome analysis; traps and loggers cleaned between sessions.
  - Live-tracker design: nine custom PIT-tag loggers distributed across the grid to record visitor presence every 0.3 seconds; loggers rotated to ensure even spatial coverage; rotation times and locations randomized within defined territories.
  - Data cleaning steps include removal of corrupt logger reads and selective data from trapping nights to maintain even spatial coverage.
  - Outcome: after cleaning, 83 of 93 tagged mice were represented in the logger data.

- Kinship and genotyping
  - Ear tissue genotyped at eleven microsatellite loci (initially twelve; one discarded due to deviation from Hardy-Weinberg Equilibrium).
  - DNA extraction and PCR performed with specified protocols; genotyping quality checked with COLONY and other tools; impossible mother-pup and father-pup relationships removed after cross-validation with trapping data.
  - Final pedigree: 17 mother-pup, 14 father-pup, 13 full-sibling, and 26 half-sibling relationships.
  - Pedigree used to create dyadic kinship matrices, with kinship values translated into numeric distances (e.g., parent-offspring and full-siblings = 0.5; half-siblings/cousins = 0.125).

- Gut microbiota profiling
  - 239 faecal samples from 75 mice (covering 90% of monitored mice; mean 3.2 samples per mouse; range 1-9).
  - DNA extraction, PCR amplification of the V4 region of the 16S rRNA gene, and high-throughput sequencing.
  - Rigorous controls: extraction and PCR controls, plus mock community standards to assess accuracy.
  - Sequencing: Illumina MiSeq 2x250 bp runs; samples randomized across extraction batches; libraries prepared with dual indexing; size-selected and pooled for sequencing.
  - Bioinformatics: DADA2 pipeline for amplicon sequence variants (ASVs); trimming based on quality; taxonomic assignment via GreenGenes; removal of non-gut bacteria (e.g., Cyanobacteria, mitochondria) and singletons; data normalized to relative abundances.
  - Diversity assessment and sample completeness checked with iNEXT; rarefaction plateau observed around 2500-4000 reads per sample.

## Datasets Included

- silwood_rodent_trapping_data.csv
  - Captures per trap-date; includes trap setup/collection details, site, grid location, PIT-tags, species, sex, body metrics, age, capture type (new or recapture), and trap-specific timing data.

- silwood_rodent_capture_data.csv
  - Cleaned per-capture event data; includes grid location, rodent ID, PIT-tag, species, sex, age, trap date, and capture coordinates (X/Y meters).

- silwood_logger_data.csv
  - Logger records per second; includes datetime, lognight, rodent ID and PIT-tag, logger ID, grid location, territory, coordinates, year/day/hour/minute/second, sex, species, sample identifiers, and sequencing-related fields (read depth, diversity metrics, extraction details, DNA concentration, band strength).

## Data Processing and Quality Control

- Field and lab workflow
  - Randomization of samples across batches to prevent confounding effects.
  - Inclusion of multiple controls (extraction and PCR blanks, mock communities) to monitor accuracy.
  - Regular rotation and cleaning of loggers to maintain data quality and coverage.

- Genotyping and pedigree
  - Genotyping conducted with multiple microsatellite loci; data checked for Hardy-Weinberg deviations and null alleles.
  - Pedigree inferred with COLONY, accounting for polygamy and potential inbreeding; cross-validated against trapping data to resolve impossible relationships.
  - Resulting pedigree used to compute dyadic kinship distances for downstream analyses.

- Microbiome data processing
  - Sequence data processed with DADA2 to infer ASVs; trimming to remove adapters and low-quality tails; merging paired reads; filtering chimeras and abnormally long/short sequences.
  - Taxonomy assigned with GreenGenes; non-gut taxa removed; singleton ASVs filtered; counts converted to proportional abundances.
  - Diversity and completeness analyses performed to determine appropriate sequencing depth and sampling effort.

## Data Governance and Reuse

- Data are prepared with explicit metadata and method details for reproducibility.
- Cross-linking across data types achieved via consistent identifiers (IDs for individuals, PIT-tags, loggers, and trap/capture metadata).
- Data collection and processing protocols documented to support auditability, reproducibility, and potential reuse by other researchers.

## Key Challenges and Considerations

- Fragmented access to and integration of field and lab data across multiple linked datasets.
- Data gaps due to logger issues (e.g., a period with one logger broken) and partial sampling coverage.
- Variability in data quality and genotyping success across loci; handling of missing or conflicting kinship information.
- Ensuring accurate representation of social networks and microbial transmission given spatial rotation of loggers and sampling cadence.

## Implications for Data Leaders

- Demonstrates end-to-end data stewardship: from field collection and tracking to genetic pedigree reconstruction and microbiome sequencing, with comprehensive quality control and metadata.
- Highlights the importance of linking diverse data modalities (behavioral ecology, genetics, microbiome) through unique identifiers and harmonized metadata.
- Emphasizes robust data processing pipelines, randomization, and controls to support reliable downstream analyses and reproducibility.