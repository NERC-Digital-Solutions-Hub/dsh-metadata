# Plant material and RNA extraction

- Sampling and origin
  - Needles from four Pinus species collected from two-year-old seedlings grown in a glasshouse at the Centre for Ecology and Hydrology, Edinburgh, UK
  - Seed sources: 17 populations total (5 P. sylvestris, 5 P. mugo, 4 P. uncinata, 3 P. uliginosa) across Europe’s distribution and environmental gradients
  - Immediately frozen in liquid nitrogen and ground to powder

- RNA extraction and quality control
  - Total RNA extracted from 100 mg needle powder using Spectrum Plant Total RNA Kit
  - RNA concentration/quality assessed with Qubit fluorometer
  - 10 μg input RNA per sample used for cDNA library preparation

- cDNA library construction and sequencing
  - Library prepared with TruSeq RNA Sample Preparation Kit
  - Poly-A mRNA purified in two steps using oligo-attached magnetic beads
  - RNA fragmented to 120–210 bp; fragmentation at 94°C for 8 minutes
  - First-strand cDNA synthesized; second-strand synthesis with RNase H treatment
  - Cleanup with Ampure XP beads; end-repair to blunt ends; A-tailing
  - Illumina TruSeq adapters ligated; PCR enrichment to amplify libraries
  - Normalization performed to increase detection of low-expression genes
  - Quality control with Agilent 2100 Bioanalyzer
  - Sequencing on Illumina HiSeq 2000 (100 bp paired-end reads)
  - Scots pine sample (2_GT_31, Scotland, Glen Tanar) used as reference

- Reference transcriptome assembly
  - Raw reads filtered to remove adapters, contaminants, and low-quality/ambiguous sequences
  - De novo assembly with Trinity (r2012-06-08)
  - Final reference transcriptome contains 40,798 contigs

- Alignment, SNP calling and filtering
  - 40,798 transcripts used as reference for mapping the remaining 16 samples
  - Alignment with BWA (v0.6.1); duplicates marked with Picard
  - Local realignment with GATK to reduce indel misalignment
  - SNPs called per sample and species using Samtools (samtools-0.1.18)