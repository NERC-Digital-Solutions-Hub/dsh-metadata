# Details of data and its generation

- Purpose and scope
  - Describes data generation, sequencing, and analyses for virus evolution (DCV) across 19 Drosophilidae host species.
  - Data underpin analyses of parallel evolution within and between host species; outputs include genome sequences, SNP frequencies, and associated phylogenetic relationships.
  - Data and methods are presented in line with policy requirements; supplementary materials contain additional details.

- Virus production and initial material
  - Virus: DCV, a positive-sense RNA virus; isolate from D. melanogaster; clone B6A used to minimize genetic variation.
  - Production: DCV grown in Schneider's Drosophila line 2 (DL2) cells; TCID50 of 6.32 x 10^9 infectious particles per mL.
  - Inoculation preparation: serial 1:1 dilutions of DCV; 7-day incubation; eight replicates per dilution; selection of clone for amplification.

- Inoculating fly species and experimental evolution
  - Infected 19 Drosophilidae species, with 10 replicate passages per species (except D. montana, which had 8).
  - Sampling: 3 days post-infection; flies snap-frozen, homogenized, and processed for RNA extraction and for infectious material in subsequent passages.
  - Experimental design: mean of ~11 flies per lineage per passage (range 4–18); incubation at 22°C and controlled humidity; replication and randomization across species.
  - Number of generations: estimated ~100–200 generations (based on observed viral load dynamics).

- Sequencing and genome coverage
  - RNA processing: cDNA synthesis with random hexamers; eight overlapping PCRs covering ~8989 bp of the DCV genome (97% coverage).
  - Library preparation: Nextera XT libraries; 173 pooled libraries sequenced on Illumina MiSeq (v3, 600 cycles; 300 bp paired-end reads).
  - Ancestral reference: ancestral DCV sequence amplified, sequenced, and used as reference for mapping.

- Bioinformatics workflow
  - Quality control: FastQC; trimming with Trimmomatic (MINLEN 30, TRAILING 15, SLIDINGWINDOW 4:20, ILLUMINACLIP).
  - Alignment: reads aligned to reference with BWA-MEM (-M option); SAM/BAM handling with SAMtools; read group metadata added with Picard.
  - Variant calling: GATK UnifiedGenotyper with ploidy set to 100 to capture low-frequency variants; stand_call_conf 30; downsampling to 1000x coverage.
  - Ancestral sequence data and genome assembly steps documented; high read quality (mapping phred >60 for 99.5% of reads).

- Host phylogeny
  - A trimmed ultrametric phylogeny for the 19 host species derived from seven genes with a relaxed clock (BEAST); pruned to the study species for analyses.

- Statistical analysis and SNP filtering
  - SNP filtering: baseline frequencies in ancestral replicates (mean ~0.00092; max ~0.043); include SNPs with frequency >0.05 in any viral lineage; include all alleles at triallelic sites.
  - Parallel evolution within species: compute FST between lineages using per-site heterozygosity; permutation tests to assess whether lineages evolved in the same host show more similarity than those evolved in different hosts.
  - Parallel evolution between species: correlate pairwise FST with host genetic distance; permutation tests by recoding host labels on the phylogeny.
  - SNP-level analyses: repeat parallel evolution tests for individual SNPs.

- Data output and availability
  - Raw data: sequencing reads available in NCBI SRA (Accession: SRP119720).
  - Processed data and resources: BAM files, phylogeny, derived allele frequencies (biallelic), first and second derived allele frequencies at triallelic sites, and related data files.
  - Reproducibility resources: R scripts and supporting materials available in the NERC data repository to reproduce figures and statistics from the study.

- Tools and software cited
  - Quality control and preprocessing: FastQC, Trimmomatic.
  - Alignment and processing: BWA-MEM, SAMtools, Picard.
  - Variant calling and data handling: GATK UnifiedGenotyper.
  - Phylogeny: BEAST; phylogenetic analyses via R packages (e.g., Ape).
  - Statistical computing: R.

- Notes on data structure and accessibility
  - Data are organized to support cross-species comparisons of viral evolution, including genome-level sequences, allele frequencies, and host phylogeny.
  - The combination of viral genomic data with host phylogenetic context enables investigation of parallel evolution patterns and their relationship to host relatedness.