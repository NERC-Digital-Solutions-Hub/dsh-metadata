# Fieldwork and data collection

- Study context and site
  - Population of long-tailed tits (Aegithalos caudatus) in the Rivelin Valley, Sheffield, UK (3 km²) with diverse habitat types (deciduous woodland, farmland, scrub, gardens).
  - Fieldwork conducted from 1994 to 2019, with fitness data for birds hatched 1994–2014 and breeding up to 2018; adults primarily observed at nests or during helper events.

- Sampling and genetic data
  - All nestlings ringed with unique colour-ring combinations; blood samples collected under Home Office License (PPL 7007834) for genetic analysis.
  - >95% of unringed adults color-ringed and blood-sampled during nest-building or helper appearances.
  - Genotyping performed at 19 microsatellite loci; data underpin estimates of relatedness and parentage.

- Breeding and fitness data
  - Fitness quantified for 879 birds (442 females, 437 males) known to attempt breeding; includes precise offspring production per life year.
  - Identified breeding attempts, offspring production, recruitment into the population, and helper presence at natal nests.
  - Promiscuity observed: ~11% of offspring from extra-pair matings (EPP) in 29% of nests; maternity confirmed for all recruits; paternity assessed for males.

- Indirect and direct fitness calculations
  - Indirect fitness: computed as the fraction of recruits from a brood attributable to helpers times the relatedness between helper and recruits; estimated using GLMMs with fixed effects (number of helpers, sex, fledging date) and random effects (nest ID, year).
  - Direct fitness: calculated from lifetime recruits, subtracting the helper-attributable fraction and adjusting for average parent-offspring relatedness (0.5).
  - Paternity corrections: used CERVUS v3.0.7 to assign genetic paternity, with simulations to determine confidence; mothers confirmed via genotype, sires assigned where confidence reached 95%; unclear sires treated accordingly and unassigned recruits handled conservatively.
  - Adjustments for EPP: genealogical contributions partitioned between genetic and social sires; overall fitness metrics include corrections for EPP outcomes.

- Handling of unringed offspring and data quality
  - Special handling for unringed fledglings from nests within the study site to avoid misclassifying immigrants; likelihood-based assignments used to designate residents vs immigrants.
  - Missing genotype data: males with missing genotypes excluded from parentage analyses; females with missing genotypes assumed mothers; recruits with missing genotypes assigned to social mothers, with no further paternity assignment.
  - Comprehensive data checks to ensure reliability of parentage, recruitment, and relatedness estimates.

- Dataset and metadata
  - Inclusive_fitness_dataset.csv contains extensive longitudinal data per individual across up to seven life years, including:
    - Identity, sex, natal nest information, year of first breeding, philopatry, lifespan.
    - Annual breeding and helping history (up to Year 7), offspring counts by sex, corrections for EPP, recruitment data, and helper counts.
    - Derived metrics: fraction of recruits due to helpers, indirect and direct fitness, coefficients related to relatedness and EPP corrections, lifetime reproductive success, and total inclusive fitness.
  - A detailed guide to column headings (A through F, H–AD, EO–FN, FP–FQ) explains each metric and derived variable, enabling reproducibility and auditing of the fitness calculations.

- Analytical tools and methodology
  - Analyses conducted in R (R v3.2.3) within RStudio (v1.0.136).
  - Mixed-effects models (GLMM with binomial error structure) implemented via lme4 to estimate helper effects on recruitment.
  - Relatedness and parentage analyses employed KINGROUP and CERVUS; paternity inference incorporated data quality considerations, allelic mismatches, and simulation-derived confidence thresholds.
  - Data handling and assignment procedures designed to minimize misclassification of immigrants, non-detectable paternity, and missing data.

- Data governance and transparency
  - Data and metadata are organized to support verification and reuse, with explicit criteria for including or excluding individuals based on genotype availability and paternity confidence.
  - Clear documentation of the dataset structure (column definitions) facilitates transparent reporting of indirect and direct fitness components and the overall inclusive fitness.