# Common juniper single nucleotide polymorphism (SNP) and microsatellite (SSR) genotype data from individuals samples from 18 natural UK populations in 2019

- Overview
  - Genetic dataset describing SNP and SSR genotypes from Juniperus communis across 18 natural UK populations collected in 2019.
  - Aims to support understanding of genetic isolation and differentiation among historically fragmented British populations.

- Sampling design and populations
  - 16 populations of J. communis and 1 each of Nana (ssp. nana) and Hemi (ssp. hemisphaerica) sampled.
  - Needle samples collected in 2019 and stored at -20°C prior to processing.
  - Population details and counts provided in Table 1 (abbreviations, regions, coordinates, and N for SNP/SSR per population).

- Laboratory methods
  - DNA extraction: needles freeze-dried, ground, and DNA extracted with Qiagen DNeasy Plant Pro kit.
  - SNP data: Sequenom SNP chips developed from sub-sample; data on 65 SNP loci used in this dataset (earlier development involved 74 loci).
  - SSR data: six nuclear microsatellite (SSR) markers identified and validated; multiplex PCR with M13-tailed primers; products analyzed on Licor 4300 sequencer.
  - Data files produced: two CSVs (SNP and SSR) with individual IDs, population assignments, and genotypes.

- Data structure and contents
  - uk_juniper_snp_data.csv: 65 bipartite SNP loci per individual.
  - uk_juniper_ssr_data.csv: 6 SSR loci per individual.
  - Data format across both files: columns encode sample ID, population, and allele calls (for SNP: alleles coded as 0–4 with 0 = misread/error, 1 = A, 2 = T, 3 = G, 4 = C; for SSR: allele fragment lengths).
  - Each row corresponds to a sample; loci are represented by allele1/allele2 for each locus.

- Data cleaning and quality considerations
  - The accompanying CSVs have not been cleaned for call rates, nor screened for null alleles (SSR) or loci out of Hardy–Weinberg equilibrium (HWE).
  - Recommended cleaning steps:
    - Drop loci with >10% missing data across all individuals.
    - Screen SSR loci for null alleles (e.g., Microchecker).
    - Remove loci out of HWE in more than 50% of populations (assess via GenAlEx).
    - Remove all but one duplicate genotype within a population.
  - Further methodological details provided in the preprint by Baker et al. (2024).

- Data provenance, accessibility, and governance
  - Data collected and prepared under the context of studying genetic differentiation in fragmented British juniper populations.
  - Works cited include Baker et al. (2024) preprint, GenAlEx 6.5, and Microchecker software.
  - Data are accompanied by methodological notes and links to resources for SNP chip development and SSR identification.
  - Potential data governance considerations include ensuring metadata completeness, openness of underlying data, and appropriate data sharing practices to enable reuse for monitoring and policy evaluation within environmental health contexts.