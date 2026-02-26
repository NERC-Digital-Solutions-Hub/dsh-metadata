# Genotyping microarray performance statistics for Scots pine (Pinus sylvestris) and closely related members of the Pinus mugo complex

## Overview
- Dataset contains summary statistics for the performance of a genotyping microarray tested on 87 Scots pine and related samples.
- About 50,000 SNPs (specifically 49,829 SNPs) on the array.
- For each locus, metrics include conversion rate, mean allelic frequency (MAF), and call rate (CR), with values averaged across the 87 samples.

## Data content and structure
- SNP set composition (49,829 total):
  - 49,052 SNPs from transcriptome sequencing of four pine species: Pinus sylvestris, P. mugo, P. uncinata, P. uliginosa; includes both cross-species common SNPs and species-fixed SNPs polymorphic in others.
  - 578 SNPs from candidate genes (279 genes) previously resequenced in population studies.
  - 14 mitochondrial DNA (mtDNA) SNPs targeting mtDNA variation.
  - 185 SNPs putatively associated with susceptibility to Dothistroma needle blight (source: Pinus radiata; ERS accession ERS1034542-53).
- For each locus, the dataset records:
  - SNP_ID (identifier)
  - ConversionType (Poly = polymorphic, Mono = monomorphic)
  - MAF (mean allelic frequency; with Y/N/NA indicating whether MAF > 0.1, not available, etc.)
  - CR (call rate)
- The summary statistics are calculated as means across the 87 sampled genotypes.

## Collection details
- Data were assembled in 2016.
- Array composition and SNP selection:
  - Thermo Fisher provided the array; SNPs were filtered based on p-convert scores and a recommended/non-recommended probe list (avoiding SNPs with polymorphisms within 35 bp).
  - The SNP set integrates data from transcriptome-derived SNPs, candidate gene resequencing, mtDNA SNPs, and disease-associated SNPs.

## Purpose
- Data were collected for the manufacture of a genotyping array for Scots pine and closely related taxa in the Pinus mugo complex.

## Responsibility
- Data collection and interpretation led by Stephen Cavers (scav@ceh.ac.uk).

## Completeness
- TheCompleteness section is present but not filled in; no explicit details on missing data beyond the described categories.