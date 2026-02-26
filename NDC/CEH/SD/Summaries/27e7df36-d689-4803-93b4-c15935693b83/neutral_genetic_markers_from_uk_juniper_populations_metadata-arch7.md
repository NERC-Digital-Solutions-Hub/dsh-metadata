# Common juniper single nucleotide polymorphism (SNP) and microsatellite (SSR) genotype data from individuals samples from 18 natural UK populations in 2019

## Overview
- Dataset of genetic data (SNP and SSR) from Juniperus communis across 18 natural UK populations sampled in 2019 (16 J. communis populations plus ssp. nana and ssp. hemisphaerica).
- Aimed at enabling spatial visualization and analysis of genetic variation using map-based data products.
- Includes geographic context (lat/long) for each population and region classifications (Scotland, Lake District, Southern England).

## Sampling and genotyping
- Sample collection: Needle samples collected in 2019 and stored at -20°C prior to processing.
- DNA extraction: Qiagen DNeasy Plant Pro kit.
- SNP data: Identified and sequenced via Plant Genomic Resources Centre; sub-sample used to develop Sequenom SNP chips with data on 74 SNP loci (dataset contains 65 SNP loci in the accompanying files).
- SSR data: New set of six nuclear microsatellite (SSR) markers developed; six loci consistently amplified and scored.
- Processing details provided for PCR and sequencing (including batch primer design and detection methods).

## Population and location details
- Populations include Gleann Dubh (AR), Blowick Fell (BF), Balnaguard Glen (BG), Bulford Hill (BH), Blea Tarn (BT), Clashindarroch (CD), Danebury Hill (DH), Fasnakyle (FK), Glen Artney (GA), Invernaver (IN), Lammermuir (LM), Morrone Birkwood (MB), Porton Down (PD), Thwaites Fell (TF), Tynron (TY), Whitewell (WW), plus ssp. nana (Nana) and ssp. hemisphaerica (Hemi).
- For each population: region (Scotland, Lake District, Southern England), latitude, longitude, and sample sizes for SNP and SSR data (N for SNP; N for SSR).
- Geographic map (Figure 1) shows sampling locations color-coded by region and labeled with abbreviations.

## Data files and structure
- Data files:
  - uk_juniper_snp_data.csv
  - uk_juniper_ssr_data.csv
- Structure: Each file contains individual IDs, population assignments, and biallelic marker data.
  - SNP file: 65 loci (allele calls encoded per locus as allele1/allele2; SNP calls coded as 0=misread/error, 1=A, 2=T, 3=G, 4=C).
  - SSR file: 6 loci (allele sizes for each locus; format described as locus1 allele1/allele2, locus2 allele1/allele2, etc.).
- Population abbreviations correspond to Table 1 in the document.

## Spatial and temporal context
- Year of sampling: 2019.
- Sampling locations span Scotland, the Lake District, and Southern England.
- Geographic data enables map-based representations of population structure and spatial genetic patterns.

## Data cleaning and quality considerations
- Current CSVs have not been cleaned for:
  - Call rates
  - SSR null alleles
  - Loci out of Hardy-Weinberg Equilibrium (HWE)
  - Clonal individuals
- Recommended preprocessing before analyses:
  - Drop loci with more than 10% missing data across all individuals.
  - Screen SSR loci for null alleles using Microchecker (Van Oosterhout et al., 2004).
  - Remove loci out of HWE in more than 50% of populations (assessed with GenAlEx; Peakall & Smouse, 2012).
  - From each population, retain only one individual per multilocus genotype.
- Further methodological details and context are provided in the associated preprint (Baker et al., 2024).

## GIS and data use recommendations
- Suitable for creating map-based visualizations of genetic variation (e.g., spatial distribution of SNP vs. SSR diversity, population structure by region).
- Useful as a data source for joining genetic information to spatial features (population centroids or sampling sites) in GIS workflows.
- Prior cleaning and quality control are essential for reliable spatial analyses and policy-relevant mapping.

## References and data provenance
- Primary source: Baker, J.P. et al. (2024). Evidence of genetic isolation and differentiation among historically fragmented British populations of common juniper, Juniperus communis L. (preprint; bioRxiv link provided).
- Tools referenced for analysis and quality checks: GenAlEx 6.5; Microchecker (Van Oosterhout et al., 2004).