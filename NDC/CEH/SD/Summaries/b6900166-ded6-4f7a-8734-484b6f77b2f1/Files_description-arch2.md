# COMPARATIVE TRANSCRIPTOMICS OF A COMPLEX OF FOUR EUROPEAN PINE SPECIES

- A study presenting a reference transcriptome and SNP data across four European pine species, using RNA-seq to explore comparative transcriptomics and population variation.
- Reference and sample data are deposited for cross-species comparison and geographic population analysis.

## Overview of the Dataset and Samples

- Reference transcriptome:
  - Reference_PS2_trinity.fna: Scots pine (Pinus sylvestris) reference from Glen Tanar, Scotland.
  - Sequencing: Illumina HiSeq 2000, 100 bp paired-end reads; TruSeq RNA Sample Preparation Kit.
  - Reference contains 40,798 contigs.
- Sample scope:
  - Species represented: Pinus sylvestris (P. sylvestris), Pinus mugo (P. mugo), Pinus uncinata (P. uncinata), Pinus uliginosa (P. uliginosa).
  - Number of samples per species: P. sylvestris (4), P. mugo (5), P. uncinata (4), P. uliginosa (3).
  - Geographic coverage across Europe, including Scotland (Glen Tanar, Shieldaig), Finland (Punkaharju), Poland (Jarocin, Wegliniec, Sudety), Spain (Trevenque, Pyrenees, Sierra de Gudar), France (Col de la Croix de Morand), Andorra, Romania (Southern Carpathians), Bosnia and Herzegovina, Italy (Abruzzi), Austria (Karwendel), Germany (Mittenwald).
- Data formats:
  - 18 SNP variant call format files (SNPs) corresponding to various sample sets across the four species (PS1, PS2, PS3, PS4, PS5; M1–M5; UN1–UN4; UG1–UG3).
  - Each PS/M/UN/UG file contains SNPs detected in the respective population compared to the reference transcriptome (Reference_PS2_trinity.fna).

## Data Access and Provenance

- All raw transcriptome sequence data (reference plus 16 samples) are deposited in the European Nucleotide Archive (ENA), accession PRJEB6877.
- The dataset provides a broad cross-section of geographic populations to support comparative analyses and environmental adaptation studies.

## Sequencing and Reference Details

- Reference transcriptome: Scots pine (Glen Tanar, Scotland) used as the baseline for SNP discovery.
- Sequencing technology and library prep: Illumina HiSeq 2000; TruSeq RNA Sample Preparation Kit.
- Data intended for standardized analyses to enable cross-sample and cross-site comparisons.

## Relevance for Environmental Monitoring Analysts

- Enables tracking of genetic diversity and population structure across environmental gradients and geographic regions.
- Provides a consistent, reference-based framework for identifying SNPs relative to a common transcriptome, supporting monitoring of environmental health and adaptive capacity.
- Datasets are designed for integration with other data sources and for accessibility to stakeholders, aligning with goals to store, share, and reuse monitoring datasets.

## Data Quality, Standardisation and Access Considerations

- Data are produced and structured to support standardized analysis workflows (reference-based SNP calling across multiple populations).
- A key ongoing challenge highlighted is increasing the value of the datasets by integrating them with additional relevant data and making the underlying data widely accessible to downstream users.