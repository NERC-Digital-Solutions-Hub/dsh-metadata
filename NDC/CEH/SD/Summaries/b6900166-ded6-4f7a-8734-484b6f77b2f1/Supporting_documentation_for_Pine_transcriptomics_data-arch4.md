# Plant material and RNA extraction

- Sampling strategy
  - Needles collected from four pine species (Pinus sylvestris, P. mugo, P. uncinata, P. uliginosa) from two-year-old seedlings grown in a glasshouse at the Centre for Ecology and Hydrology, Edinburgh, UK.
  - Seeds sourced from 17 populations across Europe (5 for P. sylvestris and P. mugo, 4 for P. uncinata, 3 for P. uliginosa) spanning distribution ranges and environmental gradients.
- RNA extraction
  - Needles frozen in liquid nitrogen, homogenized; RNA extracted from 100 mg of needle powder using Spectrum Plant Total RNA Kit.
  - RNA concentration and quality checked with Qubit fluorometer.
  - 10 μg input RNA used for normalized cDNA library preparation.

- cDNA library construction and sequencing
  - Library prep with TruSeq RNA Sample Preparation Kit; poly-A mRNA purified in two steps using poly-T beads.
  - Fragmentation to 120–210 bp inserts (94°C for 8 minutes) and priming with random hexamers.
  - First-strand cDNA synthesis, second-strand synthesis with DNA Polymerase I, RNase H treatment.
  - Cleanup with Ampure XP beads; end-repair to blunt ends; 3' adenylation; adapter ligation.
  - PCR enrichment of adapter-ligated fragments; library normalization to enhance low-expression gene discovery.
  - Quality control with Agilent 2100 Bioanalyzer (DNA1000 chip).
  - Sequencing on Illumina HiSeq 2000 (Edinburgh Genomics) to generate 100 bp paired-end reads; Scots pine sample 2_GT_31 (Scotland, Glen Tanar) used as reference.

- Reference transcriptome assembly
  - Read filtering: remove adapter contamination, potential contaminants, and low-quality/ambiguous reads ("N").
  - De novo assembly of filtered reads into contigs using Trinity (v r2012-06-08).
  - Final reference transcriptome contains 40,798 contigs.

- Alignment, SNP calling and filtering
  - Reference set: 40,798 transcripts used to map reads from the remaining 16 samples.
  - Alignment: BWA (v 0.6.1); duplicates marked with Picard.
  - Indel handling: local realignment with GATK.
  - SNP calling: Samtools (v samtools-0.1.18) for each sample/species relative to the reference.