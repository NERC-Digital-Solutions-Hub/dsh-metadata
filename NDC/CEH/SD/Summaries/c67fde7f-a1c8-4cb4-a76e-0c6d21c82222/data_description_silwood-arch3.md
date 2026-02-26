# Wild rodents social networks and the microbiome

## Overview
- A multi-modal study combining trapping data, tracking data, and gut microbiome data from wild rodents at Silwood Park (2014–2015).
- Objective: understand how social contacts influence gut microbe transmission in a wild setting.
- Data types include field collection records, pheromonal/space-use logger data, genetic kinship data, and microbiome sequencing data.
- Data were collected under a structured field protocol, with extensive data processing, quality control, and documentation to enable downstream analyses and replication.

## Study design and field data collection
- Location and scale: 2.47 ha mixed woodland plot (Nash's Copse) at Imperial College Silwood Park, UK.
- Target species: several rodent species (e.g., Apodemus sylvaticus, Apodemus flavicollis, Myodes glareolus).
- Trapping: fortnightly to 2–4 weekly trapping with 122 Sherman traps; animals processed, weighed, aged, and permanently identified with PIT-tags; ear punches collected for genotyping.
- Faecal sampling: gut microbiota samples collected from traps and stored at -80°C within 8 hours.
- Social-space data: nine custom PIT-tag loggers deployed to capture fine-scale social associations; loggers rotated to cover contiguous grid territories, with random relocation within each territory to ensure even spatial coverage.
- Logging protocol: loggers rotated 3.54 times per week on average; rotations occur between 10:00–14:00; data filtering excludes nights with low sampling lift or trapping nights to maintain coverage; data cleaning removed corrupt reads.
- Result: after cleaning, 83 of 93 tagged mice remained in the logger data; spatial coverage and data integrity emphasized.

## Kinship analysis and genotyping
- Genetic data: ear tissue genotyped at 11 microsatellite loci (after failing samples, one marker discarded due to Hardy–Weinberg deviation).
- Genotyping workflow: DNA extraction, multiplex PCRs, sequencing on an ABI 3730, and genotype scoring with standard software; assessment of genotyping quality (null alleles, scoring errors) reported per locus.
- Pedigree reconstruction: COLONY used to infer parental and sibship structures, accounting for polygamy and potential inbreeding; cross-validated against trapping data to resolve impossible relationships.
- Kinship outcomes: final pedigree included multiple relationship types (e.g., 17 mother–pup pairs, 14 father–pup, 13 full-sib, 26 half-sib); created dyadic kinship distance matrices (e.g., parent-offspring and full siblings assigned 0.5; half-siblings/cousins 0.125).

## Gut microbiota characterization and sequencing
- Sample set: 239 fecal samples from 75 individual mice (covering 90% of monitored mice; mean 3.2 samples per mouse; range 1–9).
- Laboratory workflow: DNA extraction, two-step PCR to amplify ~240 bp of the V4 region of 16S rRNA using N515F/N806R primers; extensive controls included extraction and PCR blanks plus mock community standards.
- Library preparation and sequencing: indexing with dual barcodes, pooling and size-selection, and sequencing on an Illumina MiSeq (2x250 bp); four sequencing runs with randomized batch allocation.
- Quality controls: mock communities validated the pipeline; negative controls showed no contamination in initial checks.
- Data handling: sequence data processed with DADA2, trimmed for primer/adapters, dereplicated, ASVs inferred, merged, and filtered to remove chimeras and low-quality reads; taxonomy placed against GreenGenes; non-gut taxa removed; data normalized to relative abundances.
- Diversity and completeness: iNEXT used to assess sample completeness and curve stabilization (plateau around 4000 reads; diversity stabilizes around 2500–4000 reads).

## Data processing, quality control, and metadata
- Comprehensive processing pipeline: field data cleaning and filtering steps, genetic data quality checks (Heterozygosity, HWE, null alleles, scoring errors), sequence quality control, and normalization steps to enable comparability across samples.
- Metadata and documentation: detailed dataset descriptions and column definitions accompany each data file; explicit documentation of sampling dates, locations, trap IDs, logger positions, and kinship links to individuals.
- Reproducibility: explicit methodological details (lab protocols, software versions, parameter settings) provided to enable replication and reanalysis.

## Data products and datasets
- silwood_rodent_trapping_data.csv
  - Captures per trap-date combination, including trap setup/collection times, environmental conditions, species, sex, mass, age, capture status, ID, PIT-tag, and other phenotypic notes.
- silwood_rodent_capture_data.csv
  - Clean dataset of capture events; includes grid location, individual ID, PIT-tag, species, sex, age, trap-date, and spatial coordinates.
- silwood_logger_data.csv
  - Clean dataset of logger records with timestamped presence data; includes logger ID, grid location, territory area, social encounter data, and metadata on year, date, time, sex, species, and sample identifiers.

## Data governance, metadata, and sharing considerations
- Rich metadata: comprehensive definitions for each dataset and column, facilitating interpretation and reuse.
- Data quality emphasis: explicit cleaning steps, controls, and filtering described to ensure reliable downstream analyses.
- Data sharing: the documentation demonstrates a model for transparent sharing of multi-source environmental health data, including integrated field, genetic, and microbiome data, with attention to provenance and data management standards.

## Implications for environmental health monitoring and policy
- Multi-data integration: demonstrates how combining ecological, behavioral (space-use), genetic, and microbiome data can inform understanding of environmental health dynamics (microbial transmission linked to social networks).
- Data governance lessons: highlights the importance of metadata richness, data provenance, and transparent processing pipelines to enable policy-relevant monitoring and evaluation.
- Practical considerations: illustrates concrete challenges—data completeness, transformation needs, access to integrated datasets, and ensuring timeliness of data for decision-making.
- Framework guidance: provides a blueprint for monitoring frameworks that rely on diverse data streams, rigorous quality control, and stakeholder-informed metadata to support evidence-based environmental health decisions.