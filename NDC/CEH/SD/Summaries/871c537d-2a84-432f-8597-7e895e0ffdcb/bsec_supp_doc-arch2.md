# To identify loci that contribute to discrimination between males of related species

## Overview
- Objective: Identify genetic loci that distinguish mating discrimination between males of two closely related Drosophila species (D. simulans and D. sechellia) using genomes from female progeny of a backcross population in a two-choice mate-choice assay.
- Experimental context: Backcross design (F2 from F1 backcross to D. sechellia) with standardized age and housing conditions; mating outcomes recorded to link genotypes with mating preference.

## Methods and Data Generation
- Biological design:
  - Adults: females >3 days but <28 days; males 7–28 days.
  - Setup: in each test, three tester females and three tester males of either species eclosed on the same day.
  - Assay: two-choice mate selection observed for up to four hours or until copulation occurs.
  - Outcome determination: after first mating event, vial is frozen; male species identified by distinct genitalia.
- Genotyping and ancestry:
  - Parental genomes: D. simulans A2A2B (Tsimbazaza strain) and D. sechellia D1A1C (D. sechellia 13 strain) used as comparison baselines.
  - Genotyping method: Multiplexed Shotgun Genotyping (MSG) as per Andolfatto et al. 2011.
  - Data processing: thinning with pull_thin (David Stern’s script).
  - Quality control: remove individuals with more than 25% ambiguous genotype calls (NA).
- Data file structure:
  - ID column: library ID with a unique barcode.
  - pheno column: 0 = female mated with D. simulans males; 1 = female mated with D. sechellia males.
  - Remaining columns: genotypic information at specified D. simulans genomic locations (as defined in Hu et al., 2013).
  - Genotype encoding: BB = sim/sim alleles; BA = sech/sim; NA = data not available.

## Data Structure and Interpretation
- Primary data product: genotype matrix aligned to specific D. simulans genomic loci plus a phenotypic mating outcome for each female.
- Purpose: map and identify loci associated with discrimination in mating between the two species.

## Quality Assurance and Challenges
- Quality control:
  - Exclude samples with excessive missing data (>25% NA) to ensure reliable genotype calls.
  - Acknowledge potential low DNA content leading to incomplete calls and incorporate downstream filtering.
- Key challenges:
  - Ensuring robust linkage signals in regions with variable data density due to sample quality.
  - Integrating the genotype data with phenotypic mate-choice outcomes to robustly identify loci of interest.

## Outputs, Reuse, and Data Management
- Outputs:
  - A flagged dataset linking individual-level genotypes at specified loci to mating-discrimination phenotypes.
  - Clear genotype codes (BB, BA, NA) and standardized locus coordinates for cross-study compatibility.
- Data management:
  - Follow standard practices to store and upload datasets to appropriate data portals with accompanying metadata.
  - Documentation should include genotype calling method, thinning process, and QC filters for reproducibility.
- Data accessibility and reuse:
  - Dataset designed to be reusable in future analyses of mate-choice genetics and cross-species discrimination, with references to foundational methods and genome assemblies.

## References
- Andolfatto, P.; Davison, D.; Erezyilmaz, D.; Hu, T. T.; et al. Multiplexed shotgun genotyping for rapid and efficient genetic mapping. Genome Res. 2011; 21: 610-617.
- Hu, T. T.; Eisen, M. B.; Thornton, K. R.; Andolfatto, P. A second-generation assembly of the Drosophila simulans genome provides new insights into patterns of lineage-specific divergence. Genome Res. 2013; 23: 89-98.