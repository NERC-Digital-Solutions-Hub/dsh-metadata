# Summary statistics for performance of a genotyping microarray for Scots pine (Pinus sylvestris) and closely related members of the Pinus mugo complex

## Overview
- Data type: summary statistics for performance of a genotyping microarray
- Scope: test set of 87 samples from Scots pine and closely related Pinus mugo complex
- SNPs: ~50,000 SNPs (49,829) on a 50K SNP Axiom array
- Key metrics: conversion rate, mean allelic frequency (MAF), call rate
- Purpose: support manufacture of a genotyping array for Scots pine and relatives

## Data composition
- SNP sources and construction:
  - Majority (49,052) from transcriptome sequencing across four pine species (P. sylvestris, P. mugo, P. uncinata, P. uliginosa)
  - SNPs filtered by array manufacturer (Thermo Fisher) using p-convert quality metrics; exclusion of probes with polymorphisms within 35 bp
  - Additional SNPs from candidate genes (578 SNPs across 279 genes), previously resequenced
  - mtDNA-targeted SNPs (14)
  - SNPs potentially associated with Dothistroma needle blight susceptibility (185; derived from Pinus radiata)
- Dataset outputs per locus (mean across 87 genotypes):
  - State: polymorphic or monomorphic
  - Mean allele frequency (MAF)
  - Conversion rate (CR)
- Column headings:
  - SNP_ID: identifier
  - ConversionType: Poly or Mono
  - MAF > 0.1: indicator (Y, N, or NA)
  - CR: call rate

## Data collection timeline
- Data assembled during 2016

## Data provenance and responsibility
- Responsible for collection and interpretation: Stephen Cavers (scav@ceh.ac.uk)

## Completeness
- The completeness section is not provided in the excerpt; no explicit details on data absence/presence beyond the described SNP sets and filtering approach

## Relevance to environmental monitoring
- Provides standardized, QA-filtered genetic performance metrics suitable for integration into environmental monitoring datasets
- Facilitates monitoring of genetic variation and potential disease-related susceptibility in Scots pine and related species
- Data standardization (state, MAF, CR) aids cross-study comparisons and long-term policy-relevant reporting
- Emphasizes data provenance and reproducibility, with explicit data sources and assembly methods
- Highlights ongoing opportunities to enhance dataset value by combining with additional data sources and improving data accessibility