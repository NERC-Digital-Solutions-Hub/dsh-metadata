# Plant material and RNA extraction

- Sampling design
  - Needles from four pine species: Pinus sylvestris, P. mugo, P. uncinata, and P. uliginosa.
  - Two-year-old seedlings grown in a glasshouse at the Centre for Ecology and Hydrology, Edinburgh, UK.
  - Seeds collected from 17 populations across Europe (five for P. sylvestris and P. mugo each, four for P. uncinata, three for P. uliginosa).

- RNA extraction and quality control
  - Needles frozen in liquid nitrogen and homogenized.
  - Total RNA extracted from 100 mg needle powder using Spectrum Plant Total RNA Kit.
  - RNA concentration and quality assessed with Qubit.
  - 10 μg input RNA used for normalized cDNA library preparation.

- cDNA library construction and sequencing
  - Library prepared with TruSeq RNA Sample Preparation Kit.
  - Poly-A mRNA purified in two steps using poly-T beads.
  - mRNA fragmented to 120–210 bp; first-strand cDNA synthesized with random hexamers; second-strand synthesis with RNase H treatment.
  - ds cDNA purified (Ampure XP beads), end-repaired, A-tailed, and adapters ligated.
  - PCR performed to enrich adapter-ligated fragments; cDNA library normalization applied.
  - Library quality checked with Agilent 2100 Bioanalyzer.
  - Sequencing performed on Illumina HiSeq 2000 (Edinburgh Genomics) to generate 100 bp paired-end reads.
  - Scots pine sample 2_GT_31 (Scotland, Glen Tanar) used as the reference sample.

- Reference transcriptome assembly
  - Raw reads filtered to remove adapters, contaminants, and low-quality/ambiguous sequences.
  - Reads de novo assembled into contigs using Trinity.
  - Final reference transcriptome contains 40,798 contigs.

- Alignment, SNP calling and filtering
  - A set of 40,798 transcripts used as reference for mapping reads from the remaining 16 samples.
  - Read alignment with BWA (v0.6.1); duplicates marked with Picard.
  - Indel misalignment addressed by local realignment using GATK.
  - SNPs called for each sample/species using Samtools (v0.1.18).