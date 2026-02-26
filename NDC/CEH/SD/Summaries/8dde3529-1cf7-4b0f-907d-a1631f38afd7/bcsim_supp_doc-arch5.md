# To identify loci that contribute to discrimination between males of related species

## Overview
- Study aims to identify genomic loci that differentiate mating outcomes between Drosophila simulans and D. sechellia.
- Uses female progeny from a D. simulans backcross (F2 from F1 backcross) in a two-choice mate selection assay.
- Data generated include sequencing libraries, genotype calls, and metadata describing samples and phenotypes.

## Study design and sampling
- Adult flies were sexed at eclosion and cultured in same-sex groups (three per vial).
- Mate-choice tests used three test females and three males of either species, all eclosed on the same day.
- Assay duration: up to four hours or until copulation; once a first pair mated, vial frozen for later analysis.
- Male species of copulating pair identified by distinct genitalia.
- Females aged 3–28 days; males 7–28 days used in tests.

## Genotyping and sequencing
- Libraries prepared with standard molecular biology methods (Illumina sequencing) per Andolfatto et al. 2011.
- Data structure:
  - ID column: library name with unique barcode.
  - pheno column: 0 = female mated with D. simulans; 1 = female mated with D. sechellia.
  - Other columns: specific genomic locations in D. simulans (Hu et al. 2013).
  - Parental genomes: D. simulans A2A2B (Tsimbazaza strain) and D. sechellia D1A1C (D. sechellia 13 strain).
- Genotypes obtained by Multiplexed Shotgun Genotyping (Andolfatto et al., 2011).
- Data thinning performed with pull_thin (David Stern, Janelia Farm).

## Data cleaning and quality control
- Low DNA content led to incomplete/poor genotype calls.
- Removed genotyped individuals with more than 25% ambiguous calls (NA).

## Data fields and coding conventions
- BB = sim/sim alleles; BA = sech/sim; NA = data not available.
- pheno values correspond to mating outcome as described above.
- Genotype positions align with the referenced D. simulans genome coordinates (Hu et al., Genome Res. 2013).

## Data management and provenance
- Sequencing and genotyping workflows are documented (Multiplexed Shotgun Genotyping; thinning with pull_thin).
- References:
  - Andolfatto et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping (Genome Res. 2011).
  - Hu et al. A second-generation assembly of the Drosophila simulans genome (Genome Res. 2013).
- The document records parental strains, library IDs, barcodes, and processing steps to support reproducibility.

## Implications for data governance
- Metadata completeness: clear labeling of library IDs, barcodes, phenotypes, and genomic coordinates.
- Versioning and provenance: tracking of thinning script and filtering thresholds (e.g., NA cutoff) critical for reproducibility.
- Data sharing and reuse: clearly defined data formats and column definitions facilitate reuse by researchers studying hybridization, mate choice, and genetic mapping.
- Quality assurance: explicit criteria for data inclusion (NA threshold) helps ensure dataset reliability.
- Storage considerations: handling of incomplete or low-DNA samples may require retention notes or separate QC reports.

## Key takeaways for data stewards
- Maintain detailed metadata for samples, including age windows, mating outcomes, and library information.
- Preserve both raw sequencing data and processed genotype calls, with a record of all filtering steps and thresholds.
- Ensure data formats are consistent with referenced genomic coordinates and parental strain designations.
- Provide access to the scripts used for data thinning and any QC procedures to enable reproducibility.
- Document limitations (e.g., instances of incomplete data due to low DNA content) and their impact on analyses.