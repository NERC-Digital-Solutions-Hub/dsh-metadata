# To identify loci that contribute to discrimination between males of related species, we genotyped individual genomes of female progeny from a D. sechellia backcross (F2 individuals derived from F1 backcross to D. sechellia) in a two- choice assay

## Study design and objectives
- Aim: Identify genomic loci that contribute to discrimination between males of Drosophila simulans and D. sechellia.
- Approach: Genotype female progeny from a D. sechellia backcross (F2) and assess mate choice in a two-choice assay.
- Experimental setup: Flies were sexed at eclosion and cultured in groups of three of the same sex per vial; tester groups included three tester females and three males of either species, all eclosed on the same day.
- Mate choice assay: Monitored for four hours or until copulation; upon first mating, vials were frozen to determine the species of the copulating male by inspecting male genitalia (distinct between D. simulans and D. sechellia).

## Data structure and contents
- ID column: Library ID followed by a unique barcode.
- pheno column: 0 = female mated with D. simulans males; 1 = female mated with D. sechellia males.
- Genotype data: Columns corresponding to specific locations in the D. simulans genome (Hu et al., Genome Res. 2013).
- Parental genomes for comparison: D. simulans A2A2B (Tsimbazaza strain) and D. sechellia D1A1C (D. sechellia 13 strain).
- Genotyping method: Multiplexed Shotgun Genotyping (MSG) (Andolfatto et al., 2011).
- Data thinning: Files were thinned using David Stern's pull_thin script (https://github.com/dstern/pull_thin).

## Data processing and quality control
- Handling low-quality data: In cases of low DNA content leading to incomplete genotype calls, genotyped individuals with more than 25% NA calls were removed.
- Coding of genotypes: BB = sim/sim alleles; BA = sech/sim; NA = data not available.

## Metadata and references
- References for methods and genome assemblies:
  - Andolfatto et al., Multiplexed shotgun genotyping for rapid and efficient genetic mapping (Genome Res. 2011)
  - Hu et al., A second-generation assembly of the Drosophila simulans genome (Genome Res. 2013)

## Data governance and stewardship considerations
- Provenance: Data generated from a defined cross and subsequent genotyping with explicit filtering criteria.
- Reproducibility: Clear documentation of library IDs, barcodes, phenotypes, genomic locations, and the thinning process enables reproducibility and re-use.
- Data sharing implications: Dataset includes genotype calls with missing data handled by exclusion, and phenotype labels tied to mate choice outcomes, which should be accompanied by metadata describing assay conditions and sample demographics.