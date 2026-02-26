# Common juniper single nucleotide polymorphism (SNP) and microsatellite (SSR) genotype data from individuals samples from 18 natural UK populations in 2019

- Created 20/8/24 by Baker, J.  
- This dataset provides SNP and SSR genotype data from 18 natural UK populations of Juniperus communis sampled in 2019, with two additional subspecies (ssp. nana and ssp. hemisphaerica) included. The data were generated to enable population genetic analyses and cross-population comparisons.

## Data and samples

- Data types
  - SNP data: 65 biallelic SNP loci
  - SSR data: 6 microsatellite loci
- Population coverage
  - 16 populations of J. communis plus ssp. nana and ssp. hemisphaerica (total 18 entries in Table 1)
  - Population abbreviations and metadata provided (Table 1)
  - Lat/long coordinates and regional context (Scotland, Lake District, S. England, etc.)
- Sample processing
  - Needle tissue collected in 2019, stored at -20°C prior to processing
  - DNA extraction: Qiagen DNeasy Plant Pro kit
  - SNP discovery/sequencing: Plant Genomic Resources Centre (CNRGV, INRAE, France)
  - SNP chip development: Sequenom chips providing data on 74 SNP loci; subset used in this dataset
  - SSR development: Microsynth Ecogenics identified 285 SSRs; 6 polymorphic loci selected and amplified with M13-tailed primers; products analyzed on Licor 4300; allele sizes scored
- Data files
  - uk_juniper_snp_data.csv
  - uk_juniper_ssr_data.csv
  - Both files include:
    - Sample ID, population assignment
    - Loci genotypes: SNP data stored as allele1/allele2 per SNP locus; SSR data stored as fragment length per allele
  - SNP encoding: 0 = misread/error; 1/2/3/4 = A/T/G/C
  - SSR data: fragment lengths (allele sizes)

## Structure and organization

- Population table
  - Table 1 provides population names, abbreviations, region, latitude, longitude, and N for SNP and SSR per population
- Spatial context
  - Figure 1 maps sampling locations with region-based color coding
- Data layout
  - Each row corresponds to an individual with its population label and genotype data across all loci

## Data quality and cleaning recommendations

- The accompanying CSVs are not cleaned for:
  - Call rates or missing data
  - Null alleles (SSR)
  - Deviations from Hardy-Weinberg Equilibrium (HWE)
  - Clonal duplicates
- Recommended cleaning steps prior to analysis:
  - Remove loci with more than 10% missing data across all individuals
  - Screen SSR loci for null alleles using Microchecker
  - Remove loci out of HWE in more than 50% of populations (assess with GenAlEx)
  - Within each population, retain only one representative genotype (remove duplicates)
- Further details and context available in the preprint Baker et al. (2024)

## Usage context and references

- Relevance
  - Supports analyses of genetic isolation and differentiation among fragmented British juniper populations
- Key references
  - Baker et al. (2024). Evidence of genetic isolation and differentiation among historically fragmented British populations of common juniper, Juniperus communis L. (preprint)
  - Peakall & Smouse (GenAlEx 6.5) for population genetic analysis in Excel
  - Van Oosterhout et al. (Microchecker) for identifying and correcting genotyping errors in microsatellite data