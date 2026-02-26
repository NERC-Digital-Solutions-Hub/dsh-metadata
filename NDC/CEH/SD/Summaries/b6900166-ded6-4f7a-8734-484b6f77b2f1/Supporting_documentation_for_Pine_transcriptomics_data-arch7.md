# Plant material and RNA extraction

- Samples and origin
  - Needles from four pine species collected from two-year-old seedlings grown in a glasshouse in Edinburgh, UK.
  - Seed sources: seeds from 17 populations across Europe (5 each for Pinus sylvestris and P. mugo, 4 for P. uncinata, 3 for P. uliginosa).

- RNA extraction and quality control
  - Needles frozen in liquid nitrogen, homogenized; RNA extracted from 100 mg needle powder using Spectrum Plant Total RNA Kit.
  - RNA concentration and integrity assessed with Qubit Fluorometer.
  - 10 μg input RNA used for cDNA library preparation.

- cDNA library construction and sequencing
  - Poly-A mRNA purified in two steps using poly-T oligo-attached magnetic beads.
  - RNA fragmented to 120–210 bp inserts; cDNA synthesis initiated with random hexamers.
  - Second-strand synthesis, RNase H treatment, and dsDNA cleanup with Ampure XP beads.
  - End-repair, A-tailing, and Illumina paired-end adapter ligation.
  - PCR enrichment to amplify adapters; normalization to enhance detection of low-expression genes.
  - Quality control by Agilent 2100 Bioanalyzer (DNA1000 chip).
  - Sequencing on Illumina HiSeq 2000 platform; 100 bp paired-end reads for all samples, including Scots pine 2_GT_31 (Scotland, Glen Tanar) used as reference.

- Reference transcriptome assembly
  - Pre-assembly filtering of raw reads for the reference sample 2_GT_31 (adapter contamination, contaminants, poor-quality reads, ambiguous Ns removed).
  - De novo assembly of reads into contigs using Trinity (v r2012-06-08).
  - Final reference transcriptome contains 40,798 contigs.

- Alignment, SNP calling and filtering
  - A set of 40,798 transcripts used as reference for mapping reads from the remaining 16 samples.
  - Reads aligned with BWA (v0.6.1); duplicates marked with Picard.
  - Indel misalignment mitigated by local realignment using GATK.
  - SNPs called for each sample/species relative to the reference using Samtools (v0.1.18).