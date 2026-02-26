# Genotyping microarray performance statistics for Scots pine (Pinus sylvestris) and closely related members of the Pinus mugo complex

## Overview
- Data provide summary statistics for the performance of a genotyping microarray tested on a set of 87 samples from Scots pine and closely related Pinus mugo complex.
- The array comprises 49,829 SNPs, with additional SNPs from various sources, summarized per locus.

## Data content
- For each locus, the dataset includes:
  - State: polymorphic or monomorphic
  - Mean allele frequency (MAF)
  - Conversion rate (CR)
- Across all loci, the mean values are estimated from the 87-sample genotypes.
- Column headings:
  - SNP_ID: identifier
  - ConversionType: Poly (polymorphic) or Mono (monomorphic)
  - MAF > 0.1: indicator (Y = yes, N = no, NA = not available)
  - CR: call rate

## Data scope and SNP sources
- SNPs on the array total 49,829, sourced from:
  - Transcriptome sequencing of four pine species: Pinus sylvestris, P. mugo, P. uncinata, P. uliginosa (majority)
  - Candidate genes (578 SNPs)
  - Mitochondrial DNA SNPs (14)
  - SNPs putatively linked to susceptibility to Dothistroma needle blight (185), originally identified in Pinus radiata
- The combined set reflects a mix of common, species-fixed, and cross-species polymorphic SNPs.

## Data collection and rationale
- When: Data assembled in 2016.
- Why: For manufacture and validation of a 50K SNP Axiom genotyping array for Scots pine and its close relatives.
- Instrumentation/methods: SNP array-based genotyping; SNP selection and filtering performed by Thermo Fisher (p-convert filtering and avoidance of SNPs with polymorphisms within 35 bp).

## Responsibility and provenance
- Responsible for collection and interpretation: Stephen Cavers (scav@ceh.ac.uk)
- Data are presented as summary statistics across 87 genotypes.

## Completeness
- The document provides details on included SNP sets and the general data structure.
- Completeness status (whether any data are missing) is not explicitly stated in the provided text.