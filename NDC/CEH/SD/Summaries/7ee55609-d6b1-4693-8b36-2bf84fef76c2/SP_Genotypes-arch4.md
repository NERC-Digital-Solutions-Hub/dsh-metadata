# Genotypes for samples used to validate a 50K single nucleotide polymorphism (SNP, DNA mutation) Axiom array for Scots pine (Pinus sylvestris) and closely related members of the Pinus mugo complex.

## Overview
- Dataset documenting genotypes used to validate a 50K SNP Axiom array for Scots pine and related Pinus mugo complex species.
- Data assembled in 2016.
- High-quality subset used to establish allele-call thresholds; additional analyses use progressively larger subsets.

## Data Content
- Genotype calls for samples from Scots pine and related species (Pinus sylvestris, P. mugo, P. uncinata, P. uliginosa).
- Includes quality metrics and grouping by call rate (CR) and dish QC (DQC).
- Sample sets:
  - High-quality group used to set allele-call thresholds: N = 529.
  - Analysis group 2 (posterior calls used as priors): N = 753.
  - Analysis group 3 (posterior calls used as priors): N = 251.
- Data format: Genotypes generated with Affymetrix Axiom-based array; genotyping performed in 384-well format on a GeneTitan; calls made with Axiom Analysis Suite.

## Methods (How the data were collected)
- Sample collection and preparation:
  - DNA extraction from needles using Qiagen DNeasy 96 kit.
  - Needles dried on silica gel prior to extraction.
  - DNA quantified with Qubit; minimum concentration standardized to 35 ng/µl.
  - DNA quality checked visually on 1% agarose gel.
- Genotyping:
  - Performed at Edinburgh Genomics following Affymetrix Axiom protocol (chip hybridisation, single-base extension, signal amplification).
  - Genotype calls assigned using Axiom Analysis Suite.
  - Samples grouped by performance: DQC and CR used to assess quality.
- Quality thresholds:
  - DQC: high ≥ 0.82; low < 0.82.
  - CR: high ≥ 96%; low < 96.
  - Analysis groupings:
    - Group 1: DQC high + CR high.
    - Group 2: DQC high + CR low.
    - Group 3: DQC low + CR low.
- Analytical approach:
  - High-quality samples (N=529) used to set thresholds for allele calls.
  - Posteriors for allele calls used as priors for analyses 2 (N=753) and 3 (N=251).

## Purpose
- To validate a newly manufactured genotyping array for Scots pine and closely related members of the Pinus mugo complex.

## Responsibility
- Data collection and interpretation led by Stephen Cavers (scav@ceh.ac.uk).

## Completeness
- The provided extract includes data types, collection methods, quality metrics, and sample sizes, but the completeness field is not explicitly filled; no explicit statement on missing data is provided.