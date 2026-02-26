# Common juniper SNP and microsatellite genotype data from individuals samples from 18 natural UK populations in 2019

## Overview
- Genotype dataset from 18 natural UK populations of Juniperus communis collected in 2019 (16 populations of J. communis plus ssp. nana and ssp. hemisphaerica).
- DNA extracted from needle tissue; SNP and SSR data generated to characterize genetic variation.
- Two accompanying CSV files: uk_juniper_snp_data.csv and uk_juniper_ssr_data.csv, with population assignments and biallelic markers.
- SNP data via Sequenom chips (historically 74 SNP loci tested; dataset specifies 65 SNP loci included); SSR data developed de novo with 6 polymorphic loci.
- Data intended for population genetics analyses (e.g., genetic differentiation/isolation) and methodological transparency for reuse.

## Data assets and structure
- Datasets:
  - uk_juniper_snp_data.csv containing 65 SNP loci per individual.
  - uk_juniper_ssr_data.csv containing 6 SSR loci per individual.
- Columns per file:
  - Sample ID, Population assignment (abbreviations from Table 1), followed by locus genotype data (allele1, allele2 for each locus).
  - SNP encoding: 0 = misread/error, 1 = A, 2 = T, 3 = G, 4 = C.
  - SSR data represented as fragment lengths (allele sizes).
- Population names and sample counts are provided in Table 1, with geographic coordinates for each population.
- Data have not been cleaned for:
  - Call rates, null alleles (SSR), Hardy-Weinberg Equilibrium (HWE), or clonal individuals.

## Sampling and laboratory methods
- Sampling:
  - Needle samples collected in 2019; stored at -20°C before processing.
  - Populations include Gleann Dubh (Scotland), Blowick Fell (Lake District), Balnaguard Glen (Scotland), Bulford Hill (S. England), Blea Tarn (Lake District), Clashindarroch (Scotland), Danebury Hill (S. England), Fasnakyle (Scotland), Glen Artney (Scotland), Invernaver (Scotland), Lammermuir (Scotland), Morrone Birkwood (Scotland), Porton Down (S. England), Thwaites Fell (Lake District), Tynron (Scotland), Whitewell (Scotland), plus ssp. nana (Scotland) and ssp. hemisphaerica (lat/long provided).
- DNA extraction:
  - Qiagen DNeasy Plant Pro kit following manufacturer instructions.
- SNP data generation:
  - Sequenom SNP chips developed at Plant Genomic Resources Centre (CNRGV, INRAE, France); chips provided data on SNP loci.
- SSR data generation:
  - New SSR markers developed; six polymorphic loci selected after testing 48 markers from 285 identified.
  - PCR with M13-tailed primers; amplification and sizing performed on Licor 4300 DNA sequencer.
- Data formatting:
  - Two CSVs structure: samples with population assignments and allele data per locus.

## Data quality and cleaning guidance
- The accompanying CSV data have not been cleaned for:
  - Missing data (call rates), SSR null alleles, loci out of HWE, or clonal duplication.
- Cleaning recommendations:
  - Drop loci with more than 10% missing data across all individuals.
  - Screen SSR loci for null alleles using Microchecker.
  - Remove loci out of HWE in more than 50% of populations (GenAlEx can assess this).
  - In each population, retain only one representative genotype (remove clonal duplicates beyond that).
- Additional details and context available in the preprint Baker et al. 2024.

## Uses, context, and provenance
- Data aim to support analyses of genetic isolation and differentiation among historically fragmented British juniper populations.
- Suitable for population genetics workflows (e.g., structure, differentiation, gene flow) with standard tools (GenAlEx, Microchecker, etc.).
- Provisions for reuse include explicit data structure, sample/population metadata, and clear labeling of SNP vs. SSR loci.

## References and provenance
- Baker, J. P., et al. 2024. Evidence of genetic isolation and differentiation among historically fragmented British populations of common juniper, Juniperus communis L. (preprint linked in documentation).
- Software/tools referenced for quality checks: GenAlEx (genetic analysis in Excel), Microchecker (null allele detection).