# Fieldwork and data collection (Adapted from Green JP & Hatchwell BJ (2018) Inclusive fitness consequences of dispersal decisions in a cooperatively breeding bird, the long-tailed tit ( Aegithalos caudatus ). PNAS 115:12011-12016.)

## Overview
- Long-term field study (1994–2019) of a population in the Rivelin Valley, Sheffield, UK, covering 25–72 breeding pairs over a 3 km² area with diverse habitats.
- All nestlings were ringed with color and blood-sampled for genetics; most unringed adults were color-ringed and sampled as helpers or immigrants.
- Fitness quantified for 879 birds with precise offspring-year data, spanning breeding through 2014–2018, enabling analysis of inclusive fitness components.

## Data Collected
- Demographic and reproductive data:
  - Sex, lifespan, year of first breeding, philopatry status, nest IDs, annual breeding outcomes, and presence/number of helpers at nests.
  - Counts of male, female, and unknown-sex fledglings and recruits.
- Genetic data:
  - Blood samples analyzed at 19 microsatellite loci; maternal confirmation for recruits.
  - Paternity assessed for most recruits using CERVUS; adjustments for extra-pair paternity (EPP) applied where known.
  - Relatedness estimates using Queller & Goodnight method; KINGROUP used for pedigree and kinship checks.
- Data handling for unringed individuals and potential immigrants, including residency assignments based on likelihood calculations.

## Fitness Calculations
- Inclusive fitness decomposed into:
  - Indirect fitness: fitness gained through helping relatives, calculated as the fraction of recruits influenced by helping multiplied by relatedness to recruits.
  - Direct fitness: fitness from an individual’s own offspring, adjusted by subtracting helper-attributable recruitment and applying parent-offspring relatedness.
- Modelling approach:
  - Mixed-effects generalized linear model (GLMM) with binomial error structure to estimate how helper number affects offspring recruitment.
  - Fixed effects: sex of the fledgling, fledging date; random effects: Nest ID and year.
  - Derivation of marginal productivity and indirect fitness per helper; adjustments made for multiple recruits and varying relatedness.

## Data Processing and Paternity
- Paternity inference:
  - Maternities confirmed; paternity assigned with CERVUS v3.0.7, using LOD scores and delta score thresholds against simulated expectations (95% confidence).
  - In cases where neither social nor candidate fathers achieved 95% confidence, true sire remained unknown.
- Handling of extra-pair paternity (EPP):
  - Recalculations of fledglings and recruits corrected for EPP; multiple derived metrics computed to reflect direct, indirect, and inclusive fitness with EPP adjustments.
- Immigrant vs. resident designation:
  - Unringed offspring and inaccessible nests addressed via residency assignment attempts; recruits attributed to residents when mother-offspring relationships were established through likelihood-based methods and paternity tests.

## Data Quality, Metadata, and Documentation
- Missing genotype handling:
  - Males with missing genotypes excluded from paternity confirmation; females with missing genotypes assumed mothers; recruits with missing genotypes assigned to social mothers unless paternity could be determined.
- Comprehensive dataset schema:
  - inclusive_fitness_dataset.csv with extensive per-individual, per-year columns capturing breeding activity, helping, offspring and recruit counts, relatedness, indirect/direct fitness components, and EPP-adjusted metrics.
  - Detailed column definitions (e.g., A–AD; EO–FQ) outlining how each metric is computed and what it represents.

## Analytical Tools and Reproducibility
- Software ecosystem:
  - R v3.2.3 with RStudio v1.0.136 for statistical analysis.
  - lme4 package for GLMMs; KINGROUP for kinship and pedigree analyses.
  - CERVUS v3.0.7 for paternity inference; simulations used to set confidence thresholds.
- Documentation and provenance:
  - Clear methodology for data collection, genetic analyses, paternity inference, and data-derived fitness metrics to support reproducibility and cross-study comparability.

## Implications for Data Leaders
- Demonstrates end-to-end data management in a long-term ecological study:
  - Rigorous data capture across multiple domains (phenotypic, genetic, spatial, temporal).
  - Strong emphasis on metadata, standardization, and calculable fitness metrics (including EPP corrections) for robust analysis.
  - Explicit handling of data quality issues (missing data, unringed individuals, immigrant status) to preserve data integrity.
  - Transparent, rule-based derivation of complex derived metrics (indirect, direct, inclusive fitness) enabling clear audit trails and replication.
- Provides a comprehensive dataset schema and variable definitions that can guide governance, metadata standards, and interoperability with broader data communities.