# Fieldwork and data collection (Adapted from Green JP & Hatchwell BJ (2018) Inclusive fitness consequences of dispersal decisions in a cooperatively breeding bird, the long-tailed tit ( Aegithalos caudatus ). PNAS 115:12011-12016.)

## Context and study design
- Population of 25-72 breeding pairs studied from 1994 to 2019 at a 3 km² site in the Rivelin Valley, Sheffield, UK.
- Mixed habitat (deciduous woodland, farmland, scrub, gardens) with surrounding low-quality habitat.
- All nestlings ringed with unique colour-ring codes; blood samples collected for genetic analysis under Home Office license.
- High coverage: >95% of unringed adults color-ringed and sampled; immigrants presumed mainly one year old.
- Fitness quantified for 879 birds (442 females, 437 males) that hatched 1994–2014 and bred until 2018 with precise offspring data.

## Data collected and data types
- Field data: nesting success, breeding attempts, helpers at nests, and lifespans.
- Genetic data: blood samples, 19 microsatellite loci; paternity and maternity information.
- Offspring data: fledgling counts by sex and unknown sex, recruitment outcomes, and extra-pair paternity (EPP) status.
- Metadata on nests and yearly breeding history; extensive documentation of data sources and lineage.

## Data processing, analysis workflow, and metrics
- Fitness components:
  - Indirect fitness: calculated as the fraction of recruits from a brood attributable to helpers, multiplied by average relatedness between helper and recruits; uses mixed-effects models (GLMM with binomial error) to estimate helper effects on recruitment.
  - Direct fitness: total lifetime recruits attributable to a single parent after subtracting helper-attributable recruitment; adjusted for average relatedness to offspring.
  - Inclusive fitness: sum of direct and indirect fitness.
- Relatedness and paternity:
  - Pairwise relatedness computed using Queller & Goodnight method; KINGROUP used for kin group assignments.
  - Paternity checked via CERVUS v3.0.7; maternity confirmed for recruits; 95% confidence thresholds and delta scores guide sire assignment.
  - Extra-pair paternities considered; when unresolved, social family assignments adjusted or withheld.
- Data handling rules:
  - Unringed or missing genotype data handled with specific criteria; males with missing genotypes excluded from parentage analyses; females with missing genotypes assumed mothers for offspring in nests except when evidence suggested otherwise.
  - Procedures address potential misclassification of immigrants vs. residents, including likelihood-based assignments for unringed adults.
- Software and reproducibility:
  - Analyses performed in R v3.2.3 / RStudio v1.0.136; GLMMs via lme4; relatedness via KINGROUP; paternity via CERVUS.
  - Paternity analyses rely on simulations with explicit assumptions (sampling rates, relatedness among candidate fathers, typing success, and error rates).

## Paternity, maternity, and offspring assignment specifics
- Maternity confirmed by genotype concordance between recruits and social mothers; nearly all cases confirmed.
- Paternity inference uses LOD scores and delta scores with simulations to determine the most likely sire; alternative sires considered only if confidence thresholds are met.
- In cases where genetic data could not resolve paternity, the recruit may be attributed to the social father or remain unassigned, with explicit criteria documented.
- Some recruits stemming from unringed nests or inaccessible nests required special assignment procedures to avoid misclassifying residents as immigrants.

## Data documentation and schema
- Inclusive_fitness_dataset.csv contains a detailed data dictionary and sequential yearly records per individual.
- Key columns (illustrative): ID, Sex, natal nest helpers, year of first breeding, philopatry, lifespan, yearly breeding and helping metrics, counts of male/female/unknown-sex fledglings and recruits, counts corrected for EPP, number of helpers, indirect fitness, and lifetime direct/inclusive fitness metrics.
- Extensive derived metrics track indirect fitness per helper, EPP corrections, grandoffspring, and lifetime fitness outcomes.

## Data quality, limitations, and governance considerations for data stewards
- Strengths: rich integration of behavioral, reproductive, and genetic data across many years; explicit data dictionary and methodology enable reproducibility and reuse.
- Limitations and challenges:
  - Missing genotype data for a subset of individuals necessitated exclusion or special handling in parentage analyses.
  - Some recruits’ paternity remained unresolved, requiring conservative handling.
  - Complex data structure with multi-year records and numerous derived metrics requires careful governance and documentation to maintain consistency.
- Governance implications for data stewards:
  - Maintain and update the data dictionary and methodological notes to support reuse and interoperability.
  - Ensure provenance, versioning, and access controls for sensitive genetic data; document assumptions used in paternity and EPP handling.
  - Provide clear guidance on handling missing data, exclusions, and the criteria used for reassignments to support reproducibility and transparency.