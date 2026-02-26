# To identify loci that contribute to discrimination between males of related species, we genotyped individual genomes of female progeny from a D. simulans backcross (F2 individuals derived from a F1 backcross to D. simulans) in a two- choice assay.

## Overview
- Goal: Identify genomic loci that influence discrimination between males of closely related Drosophila species through mate-choice behavior.
- Approach: Genotype female progeny from a backcross design and relate genomic markers to observed mating outcomes in a controlled two-species choice assay.
- Data types: Phenotypic data from mate-choice tests and genomic genotype data obtained via high-throughput sequencing.

## Experimental design and phenotype collection
- Subjects: Female progeny from a D. simulans backcross (F2 from an F1 backcross to D. simulans).
- Assay setup: Two-choice mate-choice tests with three test females and three males of either species per vial.
- Age criteria: Females 3–28 days old; males 7–28 days old at testing.
- Procedure: Monitor for up to four hours or until copulation occurs; after the first mating, vial frozen (-20°C) for later determination.
- Phenotype coding: pheno column — 0 = female mated with D. simulans males; 1 = female mated with D. sechellia males.
- Species identification: Copulating male determined by distinct genitalia morphology (D. simulans vs D. sechellia).

## Genotyping data generation and references
- Library preparation: Standard Illumina sequencing libraries prepared as described in Andolfatto et al. 2011.
- Library naming: ‘ID’ column includes library ID plus unique barcode.
- Genomic coordinates: Columns correspond to specific genomic locations in D. simulans (Hu et al. 2013; Genome Res. 23:89-98).
- Parental genomes: D. simulans A2A2B (Tsimbazaza strain) and D. sechellia D1A1C (D. sechellia 13 strain).
- Genotyping method: Multiplexed Shotgun Genotyping (Andolfatto et al. 2011).
- Data thinning: Applied pull_thin (David Stern’s script) to reduce data density.
- Data encoding: BB = sim/sim alleles; BA = sech/sim; NA = data not available.

## Data quality, filtering and handling missing data
- Genotype calling: Some samples had low DNA content leading to incomplete/poor calls.
- Filtering criterion: Remove genotyped individuals with more than 25% ambiguous calls (NA).
- Resulting dataset: Cleaned to exclude high-NA samples to ensure reliable mapping.

## Data management and outputs
- Standardized processing: Uses established methods for data verification, quality assurance, cleaning, and transformation.
- Outputs: Genotype data linked to phenotypes (mate-choice outcomes) across predefined genomic locations; categorizations of parental-origin alleles at mapped loci.
- Data storage and access: Ensure datasets are stored appropriately and uploaded to the relevant portals for accessibility and reuse.

## References
- Andolfatto, P., Davison, D., Erezyilmaz, D., Hu, T. T., et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping. Genome Res. 2011;21:610-617.
- Hu, T. T., Eisen, M. B., Thornton, K. R., Andolfatto, P. A second-generation assembly of the Drosophila simulans genome provides new insights into patterns of lineage-specific divergence. Genome Res. 2013;23:89-98.