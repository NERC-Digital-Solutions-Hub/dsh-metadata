# To identify loci that contribute to discrimination between males of related species

## Objective
- Identify genomic loci that contribute to discrimination between males of the related species D. simulans and D. sechellia via mate-choice behavior.

## Experimental design
- Use female progeny from a D. sechellia backcross (F2 after backcross to D. sechellia).
- Conduct two-choice mate assays with three tester females and three tester males of either species, all eclosed the same day.
- Monitor for up to four hours or until copulation; after the first mating, freeze the vial and determine the species of the mating male by inspecting primary male genitalia.

## Phenotype and genotype data
- ID column: library ID plus a unique barcode.
- pheno column: 0 = female mated with D. simulans males; 1 = female mated with D. sechellia males.
- Genotype columns: specific locations in the D. simulans genome (based on Hu et al. 2013).
- Parental references:
  - D. simulans A2A2B (Tsimbazaza strain)
  - D. sechellia D1A1C (D. sechellia 13 strain)
- Genotyping method: Multiplexed Shotgun Genotyping (Andolfatto et al. 2011).
- Data processing: thinning with pull_thin (David Stern’s script).

## Data quality and processing
- Some samples had low DNA content leading to incomplete/poor genotype calls.
- Excluded individuals with more than 25% ambiguous calls (NA) in the data file.
- Allele coding:
  - BB = sim/sim alleles
  - BA = sech/sim
  - NA = data not available

## Data structure and references
- Genotype data aligned to the D. simulans genome coordinates.
- Key references:
  - Andolfatto et al. Multiplexed shotgun genotyping (Genome Res. 2011)
  - Hu et al. second-generation assembly of the Drosophila simulans genome (Genome Res. 2013)