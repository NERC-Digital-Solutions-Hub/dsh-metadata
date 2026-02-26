# Common juniper single nucleotide polymorphism (SNP) and microsatellite (SSR) genotype data from individuals samples from 18 natural UK populations in 2019

## Overview
- Study of genetic variation in common juniper (Juniperus communis) using SNP and SSR data from 18 populations in the UK (2019).
- Samples collected as needle tissue in 2019; stored at -20°C prior to processing.
- Populations include 16 J. communis, plus subspecies Nana and Hemisphaerica; location details and sample counts provided in Table 1.
- DNA extraction performed per sample; SNP data generated via Plant Genomic Resources Centre and Sequenom SNP chips (74 SNP loci); new SSR markers developed (6 polymorphic loci).
- Data are provided as two CSV files:
  - uk_juniper_snp_data.csv (65 SNP loci)
  - uk_juniper_ssr_data.csv (6 SSR loci)
- Data provenance references: CNRGV (France) for SNP detection; Microsynth Ecogenics for SSR development; preprint Baker et al. 2024 for methods and findings.

## Data collection and processing
- Sample collection and storage:
  - Needle tissue from 16 J. communis populations plus Nana and Hemi subspecies (Table 1; Figure 2) collected in 2019; stored at -20°C prior to DNA extraction.
- Laboratory processing:
  - DNA extraction using Qiagen DNeasy Plant Pro kit following manufacturer instructions.
  - SNPs:
    - Identified/sequenced by CNRGV (France).
    - Sequenom SNP chips used to generate data on 74 SNP loci; a subset used in this dataset comprises 65 SNP loci.
  - SSRs:
    - 285 initial SSRs identified; 48 tested; 6 polymorphic markers consistently amplified.
    - PCR setup included M13-tailed forward primers; products scored by gel/fragment sizing on a Licor 4300 sequencer.
- Data structure:
  - Two accompanying CSV files:
    - uk_juniper_snp_data.csv contains per-individual SNP genotypes (65 loci).
    - uk_juniper_ssr_data.csv contains per-individual SSR genotypes (6 loci).
  - Each row includes sample ID, population assignment, and genotype data in a locus-by-locus format.
  - SNP data encoding: 0 = misread/error; 1 = A; 2 = T; 3 = G; 4 = C.
  - SSR data encoding: allele sizes (fragment lengths).

## Data structure and files
- uk_juniper_snp_data.csv:
  - Columns include: Sample, Population, Locus1 allele1, Locus1 allele2, Locus2 allele1, Locus2 allele2, ..., Locus65 allele1, Locus65 allele2.
- uk_juniper_ssr_data.csv:
  - Columns include: Sample, Population, Locus1 allele1, Locus1 allele2, ..., Locus6 allele1, Locus6 allele2.
- Population metadata:
  - Table 1 lists population names, abbreviations, regions, geographic coordinates (lat/long), and N for SNP and SSR per population.
  - Includes all 18 sampled populations plus subspecies designations (Nana and Hemi) with location context.

## Data quality and cleaning recommendations
- Current datasets are not cleaned for:
  - Call rates (missing data)
  - SSR null alleles
  - Loci out of Hardy-Weinberg Equilibrium (HWE)
  - Clone work (duplicate genotypes)
- Recommended cleaning steps:
  - Exclude loci with more than 10% missing data across all individuals.
  - Screen SSR loci for null alleles using MicroChecker (Van Oosterhout et al., 2004).
  - Remove loci with HWE violation in more than 50% of populations (assessed with GenAlEx; Peakall & Smouse, 2012).
  - Remove all but one individual sharing a genotype within a population (to avoid clonal redundancy).
- These steps are outlined for appropriate reuse and are described in the preprint Baker et al. 2024 (bioRxiv).

## Data governance and stewardship considerations
- Provenance and lineage:
  - Clear source attribution for SNP (CNRGV INRAE) and SSR (Microsynth Ecogenics) data generation.
  - Link to preprint detailing methodology and context (Baker et al., 2024) for transparency.
- Metadata and discoverability:
  - Population metadata (names, abbreviations, regions, coordinates, sample counts) essential for data discovery and re-use.
  - Ensure CSV headers and coding schemes (SNP 0–4 encoding; SSR allele sizes) are documented for interoperability.
- Data quality governance:
  - Implement versioning of datasets, with documentation of cleaning steps and rationale for locus removal.
  - Maintain a data quality plan detailing how to apply the recommended filters and how updates are handled.
- Reuse and policy:
  - Data are suitable for analyses of population structure and genetic differentiation after cleaning.
  - Consider providing a mapped, machine-readable metadata file (e.g., CSV/JSON) describing each population’s coordinates, sample sizes, and data quality flags.
- Access and updates:
  - Clarify data access terms, licensing, and any restrictions; establish a process to incorporate corrected or updated genotype data as recommended by quality checks.

## References and provenance
- Baker, J. P., Cottrell, J., Ennos, R., Perry, A., A'Hara, S., Green, S., & Cavers, S. (2024). Evidence of genetic isolation and differentiation among historically fragmented British populations of common juniper, Juniperus communis L. bioRxiv preprint.
- Peakall, R., & Smouse, P. E. (2012). GenAlEx 6.5: genetic analysis in Excel. Bioinformatics.
- Van Oosterhout, C., et al. (2004). microchecker: software for identifying and correcting genotyping errors in microsatellite data. Molecular Ecology Notes.