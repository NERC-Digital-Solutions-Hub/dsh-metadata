# Wild rodents social networks and the microbiome

## Overview
- A multi-part data assembly from Silwood Park (UK) 2014–2015 combining trapping, tracking, kinship/genotype, and gut microbiome data to study gut microbe transmission via social contacts in wild wood mice.
- Includes data on non-target species, with the field study spanning ~Nov 2014–Dec 2015 in a 2.47 ha woodland plot.
- Data collection was led by field researchers; laboratory analyses conducted for microbial profiling and genotyping; sequencing performed by Liverpool Centre for Genomics Research.

## Datasets and data types
- Field and capture data
  - silwood_rodent_trapping_data.csv: trap-date level data (trap setup/collection, site, weather, trap details, rodent status, PIT-tag, sex, mass, age, etc.).
  - silwood_rodent_capture_data.csv: per-capture event data (ID, trap/date, grid coordinates, species, sex, age, trap details, etc.).
- Social sampling and movement data
  - silwood_logger_data.csv: time-stamped logger records linking individuals (PIT-tag/ID) to logger IDs and grid locations; includes spatial territories and rotation details.
- Genetic relatedness and pedigree
  - Kinship analysis based on 11 microsatellite loci; pedigree reconstruction via COLONY; resulting kinship matrices (dyadic distances) and related statistics.
- Microbiome data
  - Gut microbiota profiles from 239 faecal samples from 75 mice; V4 region 16S rRNA sequencing (Illumina MiSeq).
  - Processed data include ASVs (via DADA2), taxonomy (GreenGenes), diversity metrics (iNEXT), and proportional abundance normalisation; QA with mock communities and controls; removal of low-count samples and non-gut taxa.
- Documentation and protocols
  - Lab protocols described (microbiome profiling methods in Raulo et al., 2021); PCR, sequencing, and data processing steps detailed; sampling and logger methods are described with figures and tables.

## Data collection, standards, and provenance
- Field collection and processing
  - Trapping: fortnightly to 2–4 weekly sessions; 122 Sherman traps; PIT-tags for permanent identification; ear punches for host genotyping; faecal samples collected promptly and stored for microbiome analysis.
  - Social tracking: 9 custom PIT-tag loggers (some rotations during the study; one logger failed temporarily); loggers rotated to ensure even spatial coverage; careful cleaning and handling between rotations.
  - Spatial design: 2.47 ha plot (Nash’s Copse) with a fixed grid; logger territories define consistent sampling areas; precise logger positions randomized within grid cells.
- Genetic data and pedigree
  - Genotyping at 11 microsatellite loci from ear tissue; PCR and sequencing performed; quality checks and marker filtering (one marker discarded due to deviation from HWE).
  - Pedigree reconstruction accounts for polygamy and potential inbreeding; cross-validated against trapping data to resolve impossible relationships.
- Microbiome sequencing and analysis
  - DNA extraction with standardized kits; two-step dual indexing for 16S rRNA V4 region; sequencing controls included (extraction controls, PCR controls, mock communities).
  - Data processing with DADA2 (v1.6.0): primer trimming, read merging, chimera removal; taxonomic assignment with GreenGenes; diversity estimation with iNEXT; singleton filtering; removal of non-gut taxa.
- Sample and data scope
  - 239 faecal samples from 75 individuals (90% coverage of monitored wood mice); mean 3.2 samples per mouse (range 1–9).
  - After QC, 83 of 93 tagged mice contributed logger data; pedigree and kinship generated for 70 individuals due to sample limitations.

## Metadata, provenance, and documentation
- Authorship and roles
  - Field data collection: Sarah Knowles; data cleaning and processing: Bryony Allen, Sarah Knowles, Aura Raulo; microbiome processing by Aura Raulo.
  - Microbiome lab work and sequencing coordinated with Liverpool Genomics; full lab protocol references provided (Raulo et al., 2021).
- Data structure and IDs
  - Linked identifiers across datasets: trapdate, trap_num, PIT_tag/ID, species, grid_square, logger.id, logger.area, etc.
  - Location and temporal details captured at fine granularity (date, time, Julian date) for logger data; trap and capture events include coordinates and environmental context.
- Documentation includes
  - Tables describing loci, primer details, allele counts, and quality metrics (Table 1 and Table 2).
  - Data dictionaries embedded within the CSVs (column names and value semantics) and figure explanations (Figure 1–3) referenced in the text.

## Data quality, processing, and lineage
- Quality assurance
  - Inclusion of negative controls and mock communities in sequencing runs; assessment of mock community composition to verify pipeline accuracy.
  - Data cleaning steps documented: removal of corrupt logger reads, filtering of nights with irregular logging, and exclusion of nights with trapping bias to preserve even spatial coverage.
- Genotyping and pedigree
  - COLONY used for sibship/parentage inference; cross-checks with trap data to resolve conflicts; final pedigree includes mother-pup, father-pup, full-sibling, and half-sibling relationships; kinship values translated into dyadic distance measures (e.g., 0.5 for parent-offspring/full sib, 0.125 for half-sibs/cousins).
- Microbiome data
  - DADA2 pipeline used for ASV inference; trimming based on quality, merging, and chimera removal; taxonomic assignment with GreenGenes; rarefaction and diversity estimates stabilising around 2500–4000 reads; singleton removal to reduce bias.
- Data completeness
  - After processing, 83/93 mice remained represented in logger data; 239 samples across 75 individuals used for microbiome analyses; one sequencing sample excluded due to low read depth.

## Data structure, linkage, and reuse potential
- Interoperability and linking
  - Datasets are designed to be cross-referenced via IDs: trap data to captures, captures to logger records, logger data to spatial territories, genotypes to pedigree, and microbiome samples to individual mice.
  - Kinship matrices provide dyadic relatedness suitable for social network and transmission analyses in conjunction with logger-based social association data.
- Reuse potential for data stewards
  - Enables studies of social networks, host genetics, and microbiome dynamics in wild populations.
  - Potential workflows: network construction from logger data; integration of kinship with social associations; correlation of social proximity with microbiome composition and diversity metrics.

## Access, sharing, and governance considerations
- Data availability
  - The dataset is described as including all collected data (field, genetic, microbiome, and logger data) with detailed documentation and column-level metadata.
- Documentation and reproducibility
  - Explicit protocols and parameter settings (e.g., PCR conditions, sequencing methods, DADA2 processing steps, iNEXT analyses) support reproducibility.
  - Availability of code or pipelines is not specified; governance would benefit from supplying processing scripts, versioned pipelines, and a data access policy or licensing statement.
- Updates and maintenance
  - Data originate from a defined study period; future updates would require clear versioning and provenance tracking to maintain traceability between raw data, processed outputs, and derived analyses.

## Challenges for Data Stewards and recommendations
- Heterogeneous data and formats
  - Multiple data types (field observations, movement data, genetic data, sequencing data) across several CSVs and processing steps require consistent metadata schemas and controlled vocabularies.
- Data completeness and quality
  - Some markers were discarded due to deviations; kinship had incomplete coverage (genotyped for 70 of 83 individuals; 83 mice in logger data); plan for documenting and communicating data gaps.
- Provenance and reproducibility
  - Ensure availability of data processing scripts (COLONY, DADA2, iNEXT) and versioning; preserve lab protocols and environment details (software versions, parameter settings).
- Data governance actions
  - Develop a data dictionary and data model mapping across datasets; implement stable identifiers across all components; provide licensing and access terms; document data quality checks and filtering steps; establish a data update and errata process if new data become available.