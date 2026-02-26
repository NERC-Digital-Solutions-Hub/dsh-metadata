# Common juniper single nucleotide polymorphism (SNP) and microsatellite (SSR) genotype data from individuals samples from 18 natural UK populations in 2019

## Overview
- Genotype data for common juniper (Juniperus communis) from 18 natural UK populations collected in 2019.
- Populations: 16 J. communis populations plus Nana (ssp. nana) and Hemi (ssp. hemisphaerica).
- SNP data: 65 loci; SSR data: 6 loci.
- Two accompanying data files: uk_juniper_snp_data.csv and uk_juniper_ssr_data.csv, containing individual IDs, population assignments, and biallelic markers.
- A sub-sample contributed to two Sequenom SNP chips providing data on 74 SNP loci.
- A de novo set of nuclear SSR markers was developed; 285 identified, 48 tested, 6 polymorphic markers amplified consistently.
- Recommended data cleaning and quality checks are provided (see Data cleaning and quality control).

## Sampling and locations
- Needle samples collected in 2019 and stored at -20°C prior to processing.
- Populations and abbreviations (Table 1): AR (Gleann Dubh, Arran, Scotland), BF (Blowick Fell, Lake District), BG (Balnaguard Glen, Scotland), BH (Bulford Hill, S. England), BT (Blea Tarn, Lake District), CD (Clashindarroch, Scotland), DH (Danebury Hill, S. England), FK (Fasnakyle, Scotland), GA (Glen Artney, Scotland), IN (Invernaver, Scotland), LM (Lammermuir, Scotland), MB (Morrone Birkwood, Scotland), PD (Porton Down, S. England), TF (Thwaites Fell, Lake District), TY (Tynron, Scotland), WW (Whitewell, Scotland), ssp. nana (Nana, Scotland), ssp. hemisphaerica (Hemi, region not applicable).
- Population-specific sample sizes vary by marker: N for SNP and N for SSR listed per population (example: BG has SNP N=23, SSR N=30; Nana with SNP N=8; Hemi with SNP N=11, SSR N=7). Exact counts per population are provided in Table 1.
- Geographic coordinates (latitude/longitude) are provided for each population.

## Laboratory methods
- DNA extraction: needles freeze-dried, ground, and DNA extracted per Qiagen DNeasy Plant Pro kit instructions.
- SNP genotyping:
  - Initial SNP identification/sequencing conducted by Plant Genomic Resources Centre (CNRGV, INRAE, France).
  - A sub-sample used to develop two Sequenom SNP chips, providing data on 74 SNP loci.
- SSR genotyping:
  - A new set of nuclear SSR markers identified; 285 SSRs screened; 48 tested by multiplex PCR and gel electrophoresis; 6 polymorphic loci consistently amplified.
  - PCR details: forward primers carried a 5' M13 tail for detection; amplified in 20 µL reactions; products sized on a Licor 4300 DNA sequencer.

## Data structure and files
- uk_juniper_snp_data.csv: contains Sample, Population, and 65 SNP loci (each locus represented by two alleles). SNP data coded as 0=misread/error, 1=A, 2=T, 3=G, 4=C.
- uk_juniper_ssr_data.csv: contains Sample, Population, and 6 SSR loci (each locus represented by allele1/allele2 as fragment lengths in base pairs).
- Format notes:
  - Each row corresponds to an individual sample.
  - Population abbreviations correspond to Table 1.
- Data not cleaned for call rates, null alleles (SSR), Hardy-Weinberg Equilibrium (HWE) across loci, or clonal duplicates at this stage.

## Data cleaning and quality control
- Recommended cleaning steps before analyses:
  - Remove loci with more than 10% missing data across all individuals.
  - For SSR data, screen for null alleles using Microchecker (Van Oosterhout et al., 2004).
  - Exclude loci out of Hardy-Weinberg Equilibrium in more than 50% of populations (assessed with GenAlEx; Peakall & Smouse, 2012).
  - In each population, remove all but one individual sharing a genotype (i.e., reduce clonal duplicates).
- Additional details and considerations are discussed in the preprint by Baker et al. (2024).

## References
- Baker, J. P., Cottrell, J., Ennos, R., Perry, A., A'Hara, S., Green, S., & Cavers, S. (2024). Evidence of genetic isolation and differentiation among historically fragmented British populations of common juniper, Juniperus communis L. [preprint]. https://www.biorxiv.org/content/biorxiv/early/2024/09/27/2024.09.26.615127.full.pdf
- Peakall, R., & Smouse, P. E. (2012). GenAlEx 6.5: genetic analysis in Excel. Population genetics software for teaching and research—an update. Bioinformatics, 28(19), 2537-2539. https://doi.org/10.1093/bioinformatics/bts460
- Van Oosterhout, C., et al. (2004). microchecker: software for identifying and correcting genotyping errors in microsatellite data. Molecular Ecology Notes, 4(3), 535-538. https://doi.org/10.1111/j.1471-8286.2004.00684.x