# To identify loci that contribute to discrimination between males of related species, we genotyped individual genomes of female progeny from a D. sechellia backcross (F2 individuals derived from F1 backcross to D. sechellia) in a two- choice assay.

## Overview
- Objective: identify genomic loci contributing to discrimination between males of related species (D. simulans vs D. sechellia) by genotyping female F2 progeny from a backcross in a two-choice mate assay.
- Study organism and design: backcross-derived F2 females tested for mate preference against tester individuals of the two species.

## Experimental design and sample collection
- Fly handling:
  - Adult flies sexed at eclosion and cultured in groups of three of the same sex per vial.
  - Conditions: no yeast provided in culture.
- Age criteria for tests:
  - Females: older than 3 days but younger than 28 days.
  - Males: between 7 and 28 days old.
- Mating assay:
  - Three tester females and three tester males of either species that eclosed on the same day.
  - Observed for four hours or until copulation, whichever occurs first.
  - After the first mating, vials frozen at -20°C.
  - Species of copulating male determined by inspecting distinct genitalia.

## Data collected and fields
- Identifier information:
  - ID column: library ID followed by a unique barcode.
- Phenotype data:
  - pheno column: 0 = females mated with D. simulans males; 1 = females mated with D. sechellia males in the two-choice assay.
- Genotypic data:
  - Remaining columns: genotype locations in the D. simulans genome (as per Hu et al., Genome Res. 2013).
- Parental references:
  - D. simulans A2A2B (Tsimbazaza strain) and D. sechellia D1A1C (D. sechellia 13 strain) genomes sequenced for comparison.

## Genotyping and data processing
- Genotyping method: Multiplexed Shotgun Genotyping (Andolfatto et al., 2011).
- Data processing:
  - Files thinned using David Stern’s pull_thin script (GitHub: dstern/pull_thin).
- Quality filtering:
  - Excluded individuals with more than 25% ambiguous genotype calls (NA).

## Data quality considerations and notes
- Low DNA content led to incomplete and poor genotype calls, necessitating removal of problematic samples.
- Data annotations include concise allele designations: BB = sim/sim alleles; BA = sech/sim; NA = data not available.

## References
- Andolfatto, Davison, Erezyilmaz, Hu, et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping. Genome Res. 2011.
- Hu, Eisen, Thornton, Andolfatto. A second-generation assembly of the Drosophila simulans genome provides new insights into patterns of lineage-specific divergence. Genome Res. 2013.