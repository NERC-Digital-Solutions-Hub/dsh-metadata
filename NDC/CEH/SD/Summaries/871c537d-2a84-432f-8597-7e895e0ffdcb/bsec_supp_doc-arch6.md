# To identify loci that contribute to discrimination between males of related species, we genotyped individual genomes of female progeny from a D. sechellia backcross (F2 individuals derived from F1 backcross to D. sechellia) in a two- choice assay.

## Overview
- Study aim: identify genetic loci contributing to discrimination between males of D. simulans and D. sechellia via genotyping female F2 progeny backcrossed to D. sechellia.
- Experimental context: two-choice mate choice assay with tester flies from both species; phenotypic readout is which male species females mated with.
- Data produced: genotype data aligned to D. simulans genome positions, with a phenotype indicating mate preference, plus metadata and parental references.

## Experimental design and sampling
- Subjects: female progeny from a D. sechellia backcross (F2; F1 backcross to D. sechellia).
- Age and housing: adults sexed at eclosion; grouped in triplets of same sex per vial; maintained without yeast.
- Mate-choice testing: three tester females and three tester males of either species, all eclosing on the same day.
- Assay duration: observed for up to four hours or until copulation.
- Sample processing after copulation: vials frozen at -20°C immediately after the first mating occurred.
- Sex and copulation verification: species of copulating male determined by inspecting distinct male genitalia.

## Data columns and genotype data
- ID: library ID followed by a unique barcode.
- pheno: 0 = females that mated with D. simulans males; 1 = females that mated with D. sechellia males.
- Genotype data: columns correspond to specific loci along the D. simulans genome (Hu et al., Genome Res. 2013).
- Parental references: D. simulans A2A2B and D. sechellia D1A1C, sequenced for comparison.
- Genotyping method: Multiplexed Shotgun Genotyping (Andolfatto et al., 2011).
- Data thinning: thinned using David Stern’s pull_thin script (GitHub: dstern/pull_thin).
- Quality filtering: removed genotyped individuals with more than 25% ambiguous calls (NA).
- Coding scheme for genotype calls: BB = sim/sim alleles; BA = sech/sim; NA = data not available.

## Data processing and interpretation notes
- Objective alignment: prepare data to identify genomic loci associated with mate-choice discrimination.
- Data quality considerations: potential low DNA content leading to incomplete genotype calls; applied thresholds to improve reliability.
- Output usability: dataset structured to enable downstream analyses and potential development of data products (e.g., genotype-phenotype associations).

## References
- Andolfatto, P.; Davison, D.; Erezyilmaz, D.; Hu, T. T.; et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping. Genome Res. 2011;21:610-617.
- Hu, T. T.; Eisen, M. B.; Thornton, K. R.; Andolfatto, P. A second-generation assembly of the Drosophila simulans genome provides new insights into patterns of lineage-specific divergence. Genome Res. 2013;23:89-98.