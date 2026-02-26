# Common juniper single nucleotide polymorphism (SNP) and microsatellite (SSR) genotype data from individuals samples from 18 natural UK populations in 2019

## Purpose and scope
- Genetic dataset for common juniper (Juniperus communis) across 18 natural UK populations (16 J. communis; ssp. nana and ssp. hemisphaerica).
- Samples collected in 2019; enables analysis of genetic isolation, differentiation, and population structure to inform environmental monitoring and policy performance over time.

## Sampling and processing
- Needle samples collected in 2019 and stored at -20°C prior to processing.
- DNA extraction using Qiagen DNeasy Plant Pro kit; prior to extraction, needles were freeze-dried, finely chopped, and ground with a mixer mill (2 minutes at 30/s with metal beads); strict cleaning between samples.

## Genotyping and data produced
- SNP data:
  - Developed from two Sequenom SNP chips, providing data on 74 SNP loci; the current dataset contains 65 SNP loci analyzed in this study.
  - Data structure includes per-sample population assignment and allelic calls for 65 SNP loci.
- SSR data:
  - A new set of six nuclear microsatellite (SSR) markers developed for this study; six loci analyzed.
  - Data structure includes per-sample population assignment and allele sizes (fragment lengths) for the six SSR loci.
- Populations and samples:
  - Population table lists abbreviations, regions, coordinates, and sample sizes for SNP and SSR datasets (e.g., Gleann Dubh, Arran; Blowick Fell; Balnaguard Glen; etc.).

## Data structure
- Two accompanying CSV files:
  - uk_juniper_snp_data.csv (65 SNP loci)
  - uk_juniper_ssr_data.csv (6 SSR loci)
- Format:
  - Rows contain: Sample, Population, Locus1 allele1, Locus1 allele2, …, LocusX allele1, LocusX allele2.
  - SNP data encodes 0 = misread/error, 1 = A, 2 = T, 3 = G, 4 = C; SSR data uses allele fragment lengths.

## Data quality and cleaning recommendations
- The provided data are not yet cleaned for:
  - Call rates and missing data
  - Null alleles (SSR)
  - Loci out of Hardy-Weinberg Equilibrium (HWE)
  - Clonal individuals
- Suggested QC steps:
  - Drop loci with more than 10% missing data across all individuals.
  - Screen SSR loci for null alleles (Microchecker).
  - Remove loci out of HWE in more than 50% of populations (GenAlEx).
  - Remove all but one individual sharing the same genotype within a population.
- Further methodological details are available in the preprint Baker et al. 2024.

## Data provenance and references
- Primary source: Baker, J. P., et al. 2024. Evidence of genetic isolation and differentiation among historically fragmented British populations of common juniper, Juniperus communis L. (bioRxiv preprint; 2024.09.26.615127).
- Software/tools cited for QC and analysis: GenAlEx 6.5; Microchecker (for genotyping error checking).
- Data and methods references:
  - Sequenom SNP chip development and SNP data generation
  - SSR development and multiplex PCR protocols
  - Related population genetics methods (GenAlEx, Microchecker)
- Data availability/links:
  - Plant Genomic Resources Centre (CNRGV, INRAE) page for SNP data
  - Microsynth Ecogenics for SSR development
  - Preprint manuscript with full methods and results

## Data usage and potential applications for environmental monitoring
- Supports assessment of genetic health, differentiation, and connectivity among fragmented juniper populations.
- Can be integrated with environmental and spatial data to monitor the impact of habitat fragmentation on genetic structure.
- Facilitates transparent, reproducible reporting of genetic baselines over time for policy evaluation and conservation planning.