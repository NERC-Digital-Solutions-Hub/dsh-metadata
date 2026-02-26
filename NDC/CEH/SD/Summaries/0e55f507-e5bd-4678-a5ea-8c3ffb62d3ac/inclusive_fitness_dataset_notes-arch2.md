# Fieldwork and data collection

- Study site and population
  - 3 km² site in the Rivelin Valley, Sheffield, UK (coordinates 52°23'N, 1°34'W)
  - Deciduous woodland, farmland, scrub and gardens; surrounded by low-quality habitat
  - Population of 25–72 breeding pairs observed from 1994 to 2019

- Sampling and marking
  - All nestlings ringed with unique colour-ring combinations
  - Blood samples taken under Home Office License for genetic analysis
  - >95% of unringed adults colour-ringed and blood-sampled
  - Adults assumed to be immigrants born outside the study site if observed as helpers

- Genetic data and offspring
  - Blood samples genotyped at 19 microsatellite loci
  - Fitness quantified for 879 birds (442 females, 437 males) hatched 1994–2014 and bred through 2018
  - Dataset includes only birds known to attempt breeding; some breeding attempts missed but birds later observed as nest helpers

- Data and methods overview
  - Indirect (through helping) and direct (through own offspring) fitness quantified as genetic offspring equivalents
  - Analyses conducted in R v3.2.3 within RStudio v1.0.136
  - Mixed-effects modeling used to estimate helper effects on offspring recruitment
  - Paternity assessed to assign genetic fathers; corrections made for extra-pair paternity (EPP)

- Fitness calculations
  - Indirect fitness
    - Calculated as the fraction of recruits from a brood due to helper presence × average relatedness between helper and recruits
    - Model: GLMM with binomial error, response = whether a ringed individual recruited next year; fixed effects = number of helpers, fledging date, sex; random effects = Nest ID, year
    - For each helping event, indirect fitness = fraction attributable to the helper × average relatedness to recruits
    - Relatedness between helpers and recruits calculated with Queller & Goodnight method using KINGROUP v2
    - If recruitment did not occur, no indirect fitness gained; if relatedness ≤ 0, indirect fitness not gained
  - Direct fitness
    - Measured as total number of recruits produced over lifetime, in genetic offspring equivalents
    - Subtract the fraction of recruits attributable to helpers, then adjust by relatedness (0.5 for parent-offspring)
  - Paternity and maternity checks
    - Confirm maternity for all recruits; check paternity with CERVUS v3.0.7
    - Use LOD scores and delta scores to assign genetic sire; exclude social father if not supported
    - If no clear sire, recruit identity considered unknown; in some cases recruits are reassigned to genetic fathers
  - Handling unringed offspring and immigrants
    - Unringed offspring fledging within the site could be misclassified as immigrants
    - Attempt to assign unringed adults to known breeders with prior unringed offspring
    - If mother-offspring relationship established, designate resident status and reassign paternity as needed

- Data quality and missing data
  - Males with missing genotypes excluded from analyses; females with missing genotypes assumed mothers
  - Recruits with missing genotypes assigned to social mothers; no paternal assignment if data insufficient

- Dataset structure: inclusive_fitness_dataset.csv
  - Contains per-individual and per-year information on:
    - Identity, sex, natal nest helpers, first breeding year, philopatry, lifespan
    - Breeding data, year-by-year breeding and helping history (up to year 7)
    - Offspring production (male, female, unknown sex; corrected for EPP)
    - Recruits produced and recruited (corrected for EPP)
    - Helpers at nests, proportion of recruits from helping, and relatedness to recruits
    - Indirect fitness gains, lifetime reproductive metrics, and inclusive fitness
  - Numerous derived fields calculating indirect fitness, direct fitness, and inclusive fitness with corrections for EPP and relatedness

- Special notes
  - Proportion of extra-pair matings estimated at ~11% of offspring in 29% of nests (unpublished)
  - Paternity inference integrates genotype data, social pairing, and simulations to determine confidence in paternity assignments
  - Data stored and managed to support standardized, comparable outputs across years and nests

- Tools and references
  - R v3.2.3, RStudio v1.0.136
  - GLMMs used for assessing helper effects
  - KINGROUP for relatedness and pedigree analyses
  - CERVUS v3.0.7 for paternity inference