# Details of data and its generation

- Purpose and scope
  - Describes data generation and analyses for virus evolution experiments; full methods are provided to supplement the main results.
  - Focuses on DCV (Drosophila C Virus) propagation, host range experiments across 19 Drosophilidae species, sequencing of evolved viral lineages, and downstream population-genomic analyses.

- Virus production
  - DCV is a positive-sense RNA virus isolated from D. melanogaster; single infectious clones were prepared via serial dilution to minimise genetic variation.
  - Produced in Schneider's Drosophila line 2 (DL2) cells at 25°C; virus strain from Charolles, France.
  - Determined tissue culture infectious dose (TCID50) of 6.32 × 10^9 infectious particles per ml.
  - Cloned clone B6A amplified in culture; debris removed and aliquoted; stored at -80°C.

- Inoculating fly species
  - Virus passaged through 19 Drosophilidae species, aiming for 10 replicates per species.
  - Species selected across phylogeny (including closely related clades) and reared at 22°C.
  - Inoculation: 4–11 day old males infected with DCV via needle pricks; strict sterility and randomised order.
  - Each lineage injected into a mean of 11 flies per passage (range 4–18); samples snap-frozen at 3 days post-infection for RNA extraction and supernatant for subsequent infections.
  - Number of passages: 10 for most species; 8 for D. montana due to stock reproduction issues.
  - Estimated viral generations: approximately 100–200 based on observed replication dynamics; 3-day incubation chosen because viral load peaks around day 3.

- Sequencing
  - Post-passaging, evolved viral lineages sequenced with a mean of ~9 independent replicates per species.
  - cDNA synthesized with Superscript III; genome amplified in eight overlapping PCRs covering 97% of the genome (62–9050 bp; 8989 bp total).
  - Libraries prepared with Illumina Nextera XT; sequencing performed on Illumina MiSeq v3 (600 cycles; 300 bp paired-end reads).
  - Ancestral virus sequence amplified and sequenced to generate a reference.

- Bioinformatics and variant calling
  - Quality control: FastQC; trimming with Trimmomatic (MINLEN 30; TRAILING 15; SLIDINGWINDOW 4:20; adapter clipping).
  - Reference: ancestral DCV sequence generated in-house; sequences edited and checked manually.
  - Read alignment: BWA-MEM (with -M); SAM to BAM conversion and sorting with SAMtools.
  - Read groups added with Picard.
  - Variant calling: GATK UnifiedGenotyper with ploidy set to 100 (to detect low-frequency variants); minimum phred confidence 30; downsample to 1000× coverage.
  - Coverage and quality metrics indicate high-quality mappings (99.5% of reads with mapping quality >60).

- Ancestral and reference data
  - Ancestral DCV sequence used to anchor analyses; additional references compiled from direct sequencing of ancestral clones.
  - Data and scripts prepared to reproduce analyses; derived allele frequencies stored per site.

- Host phylogeny
  - Time-based ultrametric host phylogeny constructed from seven genes using BEAST; tree pruned to the 19 species used in the study.
  - Phylogeny inputs processed in R with the ape package.

- Statistical analysis of genetic variation
  - SNP filtering: include SNPs with frequency >0.05 in any viral lineage; ancestral replicates used to identify pre-existing variation or sequencing errors.
  - Focus on tri-allelic sites by including all three alleles where present.
  - Parallel evolution within species: estimated FST between virus lineages using heterozygosity (Hb and Hw) per site; assessed whether lineages from the same host species show higher FST similarity than those from different species via permutation (1000 iterations).
  - Individual SNPs checked for signatures of parallel evolution within species.
  - Parallel evolution between species: correlated pairwise viral lineage FST with genetic distance between host species; significance assessed by randomising host labels on the phylogeny (1000 permutations). SNP-specific correlations examined similarly.
  - Data and results available as derived allele frequencies and per-site statistics; support data and R scripts accompany the manuscript.

- Data availability and reproducibility
  - Sequence data available in NCBI SRA (Accession: SRP119720).
  - Processed data and analysis outputs available in the NERC data repository (BAM files, phylogeny, derived allele frequencies, allele frequency trajectories for triallelic sites).
  - Supporting R scripts provided to reproduce figures and statistics in the paper.

- Software and references
  - Tools and versions noted for quality control, alignment, and variant calling (FastQC v0.11.2, Trimmomatic v0.32, BWA-MEM, SAMtools, Picard, GATK v3.3.0).
  - Phylogenetic and statistical analysis conducted in BEAST, BEAUti, R (and packages such as Ape); cited literature and methodological references provided.