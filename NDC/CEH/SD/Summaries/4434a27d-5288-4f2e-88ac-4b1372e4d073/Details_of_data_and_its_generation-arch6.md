# Details of data and its generation

- Objective and scope
  - Document describes the generation, processing, and analysis of data from an experimental evolution study of Drosophila C Virus (DCV) across 19 Drosophilidae host species.
  - Aim is to minimise genetic variation in the DCV stock and to track viral evolution across hosts and over multiple passages.

- Virus production and initial preparation
  - DCV is a positive-sense RNA virus isolated from D. melanogaster.
  - A single infectious clone (B6A) was amplified from a serial dilution to minimise genetic variation.
  - Virus produced in Schneider's Drosophila line 2 (DL2) cells; TCID50 of 6.32 x 10^9 infectious particles per ml.
  - Inoculum prepared in complete Schneider's media; 96-well plates used to identify infectious dilutions.
  - Virus stored at -80°C after amplification.

- Inoculation and experimental evolution design
  - Virus passaged through 19 fly species across up to 10 passages (8 passages for D. montana due to stock issues).
  - Each lineage injected into a mean of 11 flies per passage (range 4–18) using a sterile needle, in randomized order.
  - Post-infection sampling occurred 3 days later: flies frozen, homogenised, and aliquots used for infection of subsequent passages; remaining material stored for RNA extraction.
  - Time course indicated viral load peaks around day 3; total estimated generations across experiments ~100–200.
  - For each species, 10 replicate passages were intended; replication and randomization designed to assess parallel evolution.

- Sequencing strategy and data generation
  - Sequencing of evolved viral lineages across 19 host species with ~9 independent replicates per species (range 6–10).
  - Ancestral DCV sequence amplified and used as reference; multiple PCR amplicons covered positions 62–9050 bp (8989 bp, ~97% genome).
  - Libraries prepared with Nextera XT; 173 pooled amplicon libraries sequenced on Illumina MiSeq (600 cycles; 300 bp paired-end reads).
  - Additional ancestral sequence obtained via Sanger sequencing (ABI 3730).

- Bioinformatics and variant calling workflow
  - Quality control: FastQC; trimming with Trimmomatic (MINLEN=30, TRAILING=15, SLIDINGWINDOW=4:20, ILLUMINACLIP settings).
  - Read alignment: reads aligned to ancestral DCV reference with BWA-MEM (option -M); SAM/BAM processing with SAMtools; read groups added with Picard.
  - Variant calling: GATK UnifiedGenotyper (sample_ploidy=100; stand_call_conf=30; downsample_to_coverage=1000) to detect low-frequency variants.
  - Ancestral sequence produced via PCR and Sanger sequencing; reference re-used for aligning evolved lineages.
  - Coverage and quality metrics indicate high-quality data (99.5% of reads with mapping phred >60).

- Host phylogeny
  - A trimmed ultrametric host phylogeny (time-based) built from seven genes with BEAST; pruned to the 19 host species used.

- Data outputs and accessible formats
  - Outputs include: BAM files, phylogeny, derived allele frequencies at biallelic sites, first and second derived allele frequencies at triallelic sites.
  - Raw sequencing data available in NCBI SRA (Accession: SRP119720).
  - Supporting datasets and analyses accessible via the NERC data repository.
  - Reproducibility: R scripts provided to reproduce all figures and statistics from the study.

- Data analysis and statistical methods
  - SNP filtering: included variants with frequency > 0.05 in any viral lineage; ancestral replicates used to identify pre-existing variation or sequencing errors.
  - Parallel evolution within species: FST calculated between lineages using Hb and Hw; permutation tests (1000 iterations) to compare same-species vs different-species lineage pairs; per-SNP analyses for signatures of parallel evolution.
  - Parallel evolution between species: correlation between pairwise FST (across lineages from different hosts) and host genetic distance; permutation tests (1000 iterations) to assess significance; per-SNP correlations also evaluated.
  - All analyses account for tri-allelic sites by treating three alleles separately.

- Data accessibility and reproducibility
  - Data and code are organized for replication:
    - FASTQ data in NCBI SRA (SRP119720).
    - BAM files, phylogeny, and derived allele frequencies accessible through the NERC data repository.
    - First/second derived allele frequencies for triallelic sites provided.
    - Supporting R scripts allow reproduction of all figures and statistics reported.