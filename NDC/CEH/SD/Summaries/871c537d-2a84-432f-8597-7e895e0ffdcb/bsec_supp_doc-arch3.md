# To identify loci that contribute to discrimination between males of related species, we genotyped individual genomes of female progeny from a D. sechellia backcross (F2 individuals derived from F1 backcross to D. sechellia) in a two- choice assay.

## Objective
- Identify genomic loci contributing to discrimination between males of two closely related species, Drosophila simulans and Drosophila sechellia, by genotyping female F2 progeny from a D. sechellia backcross in a two-choice mate assay.

## Experimental design and workflow
- Adults were sexed at eclosion and cultured in groups of three same-sex individuals per vial without yeast.
- Females aged >3 days and <28 days; males aged 7–28 days were used in mate choice tests.
- Each assay included three tester females and three tester males of either species that hatched on the same day.
- The assay was monitored for four hours or until copulation occurred; after the first mating, vials were frozen for later analysis.
- Species of copulating males were determined by inspecting genitalia, which differ between D. simulans and D. sechellia.

## Data structure and genomic framework
- ID column: library ID plus a unique barcode.
- pheno column: 0 = females that mated with D. simulans males; 1 = females that mated with D. sechellia males.
- Remaining columns: specific genomic locations in the D. simulans genome (as referenced by Hu et al., Genome Res. 2013).
- Parental genomes used for comparison: D. simulans A2A2B (Tsimbazaza strain) and D. sechellia D1A1C (D. sechellia 13 strain).

## Genotyping and data processing
- Genotypes obtained via Multiplexed Shotgun Genotyping (MSG) per Andolfatto et al. 2011.
- Files thinning performed using pull_thin (David Stern’s script).
- Quality control: removed individuals with more than 25% ambiguous calls (NA).

## Data coding and interpretation
- BB = sim/sim alleles; BA = sech/sim; NA = data not available.

## References
- Andolfatto, Davison, Erezyilmaz, Hu, et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping. Genome Res. 2011.
- Hu, Eisen, Thornton, Andolfatto. A second-generation assembly of the Drosophila simulans genome provides new insights into patterns of lineage-specific divergence. Genome Res. 2013.