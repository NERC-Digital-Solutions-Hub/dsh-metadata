# Plant material and RNA extraction

- Study design and sample sources:
  - Needles from four Pinus species collected from two-year-old seedlings grown in a glasshouse at the Centre for Ecology and Hydrology, Edinburgh, UK.
  - Seedlings derived from seeds collected in 17 populations across Europe (5 for P. sylvestris and P. mugo; 4 for P. uncinata; 3 for P. uliginosa), representing broad distribution and environmental gradients.
- Sample preparation and RNA extraction:
  - Needles frozen in liquid nitrogen and homogenized.
  - Total RNA extracted from 100 mg of needle powder using Spectrum Plant Total RNA Kit.
  - RNA concentration and quality assessed with Qubit Fluorometer.
  - 10 μg input RNA used for normalized cDNA library preparation.

- Data creation goal:
  - Generate transcript sequence data to support downstream transcriptome assembly and SNP discovery across species.

## cDNA library construction and sequencing

- Library preparation:
  - Template cDNA libraries prepared with TruSeq RNA Sample Preparation Kit.
  - Poly-A mRNA purified in two steps using poly-T oligo-attached magnetic beads.
  - RNA fragmented to 120–210 bp inserts (72°C step for 8 minutes) and primed for cDNA synthesis.
  - cDNA synthesis: first strand with reverse transcription; second strand synthesis with DNA Polymerase I; RNase H treatment.
  - Cleanup with Ampure XP beads; end-repair to blunt ends; A-tailing; adapters ligated.
  - PCR amplification to enrich adapter-ligated fragments.
  - cDNA normalization applied to emphasize low-expression genes.
- Quality control and sequencing:
  - Library QC with Agilent 2100 Bioanalyzer (DNA1000 chip).
  - Sequencing performed on Illumina HiSeq 2000 at Edinburgh Genomics, producing 100 bp paired-end reads.
  - All samples sequenced, with Scots pine 2_GT_31 (Scotland, Glen Tanar) used as the reference sample.

## Reference transcriptome assembly

- Read filtering for reference sample:
  - For sample 2_GT_31, reads were filtered to remove adapters, contaminants, and low-quality/ambiguous sequences ("N").
- De novo assembly:
  - Assembled reads into transcripts/contigs using Trinity (version r2012-06-08).
  - Final reference transcriptome comprised 40,798 contigs.

## Alignment, SNP calling and filtering

- Mapping reads to reference:
  - A set of 40,798 transcripts used as the reference for mapping reads from the remaining 16 samples.
  - Alignment performed with BWA (version 0.6.1).
  - PCR duplicates marked with Picard.
  - Local realignment performed with GATK to correct indel misalignments.
- SNP discovery:
  - SNPs called for each sample and species relative to the reference using Samtools (version samtools-0.1.18).