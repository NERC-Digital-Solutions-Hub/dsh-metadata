# COMPARATIVE TRANSCRIPTOMICS OF A COMPLEX OF FOUR EUROPEAN PINE SPECIES

- The manuscript presents a comparative transcriptomics study across four European pine species, anchored by a Scots pine reference transcriptome from Glen Tanar, Scotland.

## Overview

- Objective: Generate and compare transcriptomic data across multiple Pinus species to identify genetic variation and expression patterns relevant to environmental health and forest resilience.
- Reference: Reference transcriptome sequence for Scots pine (Reference_PS2_trinity.fna) from Glen Tanar, Scotland.
- Scope: Raw transcriptome data for the reference plus 16 samples spanning four species:
  - Pinus sylvestris (4 samples)
  - Pinus mugo (5 samples)
  - Pinus uncinata (4 samples)
  - Pinus uliginosa (3 samples)
- Output: A set of SNP (SNP) variant call files (VCF) documenting polymorphisms relative to the reference sequence.
- Data repository: European Nucleotide Archive (ENA), accession PRJEB6877.
- Reference composition: 40,798 contigs in the transcriptome reference.

## Data and Methods

- Reference PS2_trinity.fna:
  - Source: Scots pine samples from Glen Tanar, Scotland.
  - Library prep: TruSeq RNA Sample Preparation Kit (Illumina).
  - Sequencing: Illumina HiSeq 2000, 100 base paired-end reads.
  - Purpose: Reference transcript sequence used for SNP discovery across other samples.
- Raw data:
  - Includes the reference plus 16 samples from four species (as listed above).
- SNP datasets:
  - PS1_SNPs.vcf: Pinus sylvestris samples from Scotland (Shieldaig) vs Ref.
  - PS2_SNPs.vcf: Pinus sylvestris samples from Scotland (Glen Tanar) vs Ref.
  - PS3_SNPs.vcf: Pinus sylvestris samples from Finland (Punkaharju) vs Ref.
  - PS4_SNPs.vcf: Pinus sylvestris samples from Poland (Jarocin) vs Ref.
  - PS5_SNPs.vcf: Pinus sylvestris samples from Spain (Trevenque) vs Ref.
  - M1_SNPs.vcf to M5_SNPs.vcf: Pinus mugo samples from Romania, Bosnia and Herzegovina, Italy, Austria, Poland vs Ref.
  - UN1_SNPs.vcf to UN4_SNPs.vcf: Pinus uncinata samples from France, Spain, Andorra, Spain vs Ref.
  - UG1_SNPs.vcf to UG3_SNPs.vcf: Pinus uliginosa samples from Poland, Poland, Germany vs Ref.
- All SNP calls are relative to Reference_PS2_trinity.fna.

## Datasets and Access

- Reference transcriptome: Reference_PS2_trinity.fna (40,798 contigs).
- SNP datasets: 18 VCF files (PS1–PS5, M1–M5, UN1–UN4, UG1–UG3) capturing population-level polymorphisms relative to the Scots pine reference.
- Primary data repository: ENA, accession PRJEB6877, containing raw transcriptome data for all samples (reference plus 16 samples across four species).

## Data Quality, Metadata and Governance Considerations

- Metadata availability and standardization: Noted as general considerations for monitoring frameworks; effective use requires adequate metadata to verify data suitability for needs.
- Data sharing openness: Data are deposited in a public repository, supporting transparency but potential barriers may arise in some contexts when sharing datasets.
- Cross-site data integration: Data span multiple countries and species, highlighting the need for consistent data formats and harmonized metadata to facilitate integration into monitoring programs.

## Applications for Monitoring Environmental Health and Policy

- Baseline genetic variation: Provides a comprehensive cross-species, multi-population reference to assess genetic diversity and population structure, informing resilience assessments under environmental stress (e.g., climate change, disease).
- Comparative genomics for monitoring: SNP data across geographic ranges enable tracking of adaptive variation and gene flow, supporting monitoring frameworks that evaluate forest health, adaptability, and potential management strategies.
- Data governance alignment: The study exemplifies robust data sharing and openness, with explicit reference to data provenance and reproducibility, aligning with monitoring programs’ data quality and governance needs.

## Key Takeaways

- A high-quality Scots pine reference transcriptome (40,798 contigs) underpins broad SNP discovery across four European pine species.
- The dataset comprises 18 curated SNP VCF files representing population-level variation across diverse geographic regions.
- All raw data are publicly archived (ENA PRJEB6877), enabling reuse for monitoring, policy evaluation, and future research on environmental health and forest resilience.
- Metadata quality and data governance are critical considerations to maximize the utility of these resources for monitoring frameworks.