# To identify loci that contribute to discrimination between males of related species

## Overview
- Objective: identify genomic loci that differentiate mating success with D. simulans vs D. sechellia using backcross-derived female progeny.
- System: Drosophila simulans and D. sechellia; backcross design yielding F2 individuals for analysis.
- Behavioral assay: two-choice mate preference tests with three test females and three males of either species; monitored up to four hours or until copulation.
- Outcome: species of copulating male determined post-mov­ing to confirm mating partner.

## Experimental design and data collection
- Cross design: F2 individuals derived from a F1 backcross to D. simulans.
- Subject details: adults sexed at eclosion; females aged 3–28 days, males 7–28 days used in mate-choice tests.
- Assay setup: three test females and three males (from either species) per vial; same-day eclosion for all individuals in a test.
- Post-mating processing: once a pair mated, vial frozen at -20°C; male species identified by distinct genitalia.
- Molecular data generation: standard Illumina library preparation; genotyping via Multiplexed Shotgun Genotyping (MSG).

## Genotyping data structure and genome references
- ID column: library ID plus unique barcode.
- Pheno column: 0 = female mated with D. simulans males; 1 = female mated with D. sechellia males.
- Genomic data columns: specific genome locations corresponding to D. simulans (Hu et al., Genome Res. 2013) coordinates.
- Parental genomes:
  - D. simulans A2A2B (Tsimbazaza strain)
  - D. sechellia D1A1C (D. sechellia 13 strain)
- Genotype encoding:
  - BB = sim/sim alleles
  - BA = sech/sim
  - NA = data not available
- Data thinning: raw MSG data thinned with pull_thin script (David Stern, Janelia Farm).

## Data processing and quality control
- Data quality issue: some samples had low DNA content leading to incomplete genotype calls.
- Filtering criterion: remove individuals with more than 25% ambiguous calls (NA).
- Data provenance: genotypes obtained by MSG (Andolfatto et al., 2011); thinning performed with pull_thin.

## Data provenance and references
- Methods and background:
  - Multiplexed Shotgun Genotyping for rapid genetic mapping (Andolfatto et al., Genome Res. 2011)
  - Second-generation assembly of D. simulans and divergence insights (Hu et al., Genome Res. 2013)
- Data formatting and thinning scripts referenced (pull_thin): https://github.com/dstern/pull_thin

## How this data can be used (data products and exploration)
- Enable genotype-phenotype association analysis for mate-choice behavior across the D. simulans–D. sechellia divergence.
- Build allele-origin maps across the genome to identify loci contributing to discrimination in mating.
- Create self-serve data products (e.g., dashboards or pivot-like analyses) to explore:
  - Defendant genotypes by genomic location
  - Pheno classifications (0 vs 1) across individuals
  - Missing data patterns and their impact on locus-level inferences
- Reproducibility: follow the documented mating assay design and MSG workflow to replicate or extend the study with additional samples or related species.

## Caveats and considerations for analysts
- Potential bias due to incomplete genotype calls from low DNA content; must account for NA-rich regions or exclude affected individuals.
- Interpretation depends on accurate male species identification via post-mop genitalia analysis; consider validation for ambiguous cases.
- Ensure alignment of genomic coordinates to the Hu et al. (2013) reference framework for consistent locus mapping.