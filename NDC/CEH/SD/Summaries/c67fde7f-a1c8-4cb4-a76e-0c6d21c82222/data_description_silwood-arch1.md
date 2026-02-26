# Wild rodents social networks and the microbiome

## Overview
- A field study examining how social contacts influence transmission of gut microbes among wild wood mice.
- Conducted at Silwood Park, Imperial College, UK, in Nash's Copse (2.47 ha) over Nov 2014–Dec 2015.
- Integrates trapping and tracking data with host genetics and gut microbiome profiling.

## Study System and Data Types
- Species: Apodemus sylvaticus (wood mouse), plus other small mammals captured during the study.
- Data types:
  - Trapping data (capture events, dates, locations, morphology, sex, age, etc.).
  - Tracking data via custom PIT-tag loggers to record social associations and space use.
  - Host genetics: kinship inferred from microsatellite genotypes.
  - Gut microbiome: 16S rRNA gene sequencing (V4 region) from faecal samples.

## Field Data Collection and Sampling Design
- Trapping and processing
  - 122 Sherman traps arranged in a grid; traps checked every 2–4 weeks.
  - Rodents identified to species, sexed, weighed, aged; PIT-tags implanted; ear punches for genotyping; faecal samples collected and frozen promptly.
  - Traps and traps’ gear sterilized between uses; live traps cleaned with bleach.
- Social space and movement data
  - Nine custom PIT-tag loggers distributed across the plot; loggers rotated to cover contiguous grid cell territories.
  - Logger rotation: approximately 3.5 times per week; rotations conducted 10:00–14:00 to minimize nocturnal activity interference.
  - Data collection: logger reads every 0.3 seconds; logging effort mapped across grid cells.
  - Data cleaning: nights without even sampling or with trapping bias removed; erroneous reads filtered.
  - Outcome: after cleaning, 83 of 93 tagged mice remained in the logger dataset.

## Kinship, Genotyping, and Pedigree Reconstruction
- Genotyping
  - Ear tissue genotyped at 11 microsatellite loci (initially 12; one locus excluded due to deviation from Hardy–Weinberg equilibrium).
  - Genotyping success: usable data for 70 of 83 monitored wood mice.
- Pedigree reconstruction
  - COLONY software used to infer parental and sibship relationships, accounting for polygamy and potential inbreeding.
  - Conflicts resolved by cross-checking trapping data; impossible mother-pup and father-pup pairs were excluded.
  - Resulting pedigree: 17 mother–pup pairs, 14 father–pup pairs, 13 full-sib pairs, 26 half-sib pairs.
  - Dyadic kinship matrices generated; kinship values transformed into numeric distances (e.g., parent–offspring and full-siblings = 0.5; half-siblings/cousins = 0.125).

## Gut Microbiota Characterisation and Sequencing
- Sample set
  - 239 faecal samples from 75 individual wood mice (roughly 90% of monitored individuals); mean 3.2 samples per mouse; range 1–9.
- Laboratory workflow
  - DNA extraction with Zymo Quick-DNATM kits.
  - Two-step PCR to amplify ~240 bp V4 region of 16S rRNA using N515F/N806R primers with dual indexing.
  - Controls: extraction controls, PCR controls, and mock community standards.
  - Library preparation, pooling, size selection, and sequencing on Illumina MiSeq (2x250 bp).
- Quality controls
  - Mock community profiling to validate lab and bioinformatic pipeline accuracy.
  - Randomized sample processing across extraction batches and plates to minimize batch effects.

## Bioinformatics and Data Processing
- Sequence processing
  - DADA2 (v1.6.0) used to infer Amplicon Sequence Variants (ASVs) after primer/adaptor trimming and quality filtering.
  - Read merging, chimera removal, and length filtering (238–245 bp range retained).
  - Taxonomy assigned with GreenGenes database via phyloseq.
  - Filtering: remove ASVs not associated with gut bacteria (e.g., Cyanobacteria, Mitochondria); remove singletons; normalize to relative abundance.
- Diversity and completeness
  - iNEXT used to assess sample completeness and diversity; plateau around 4000 reads; stable diversity estimates around 2500–4000 reads.
- Data filtering and quality
  - One sample with very low read count removed (n=300 reads).
  - Figure 3 demonstrates mock community validation; Figure 4 shows iNEXT results.

## Datasets and Metadata
- silwood_rodent_trapping_data.csv
  - Trap-level data per trapping event and date; includes site, trap number, weather, timing, rodent captures, species, sex, mass, condition, reproductive status, ectoparasites, and trap outcomes.
- silwood_rodent_capture_data.csv
  - Capture-event data per animal; includes grid location, animal ID, PIT tag, species, sex, age, trapdate, and coordinates.
- silwood_logger_data.csv
  - Logger-record data per rodent per logger per second; includes datetime, logger ID, grid location, logger territory, sex, species, and extensive timing metadata.

## Key Considerations for Analysis and Interpretation
- Integration potential
  - Combine social network data from logger records with microbiome composition to assess correlations between contact patterns and microbial transmission.
  - Leverage kinship data to separate social contact effects from genetic relatedness in microbiome similarity.
- Scale and data quality
  - Field-scale data are rich but can be sparse for some dyads; kinship and logger-derived networks support robust correlation analyses.
  - Spatial coverage and rotation design help control for habitat structure in social interaction inferences.
- Limitations and considerations
  - Potential sampling biases due to trapping frequency, logger activity, and batch effects in sequencing.
  - Data cleaning steps and filtering thresholds (e.g., read counts, non-gut taxa removal) influence diversity estimates and downstream analyses.

## Figures and Visual Aids
- Figure 1: Logging area, logger territories, and logging effort across the study plot.
- Figure 2: Data filtering steps and data loss through processing.
- Figure 3: Mock community profiles validating sequencing and bioinformatics pipeline.
- Figure 4: iNEXT-based assessments of sample completeness and diversity plateau.