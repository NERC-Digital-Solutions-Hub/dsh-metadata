# Fieldwork and data collection

- Study population and site: 25–72 breeding pairs of long-tailed tits observed from 1994 to 2019 on a 3 km² site in the Rivelin Valley, Sheffield, UK, with habitat variability (woodland, farmland, scrub, gardens; mostly low-quality habitat surrounding).
- Field methods and sampling: every year, all nestlings were ringed with a unique colour-ring combination; blood samples collected under a Home Office license for genetic analysis. >95% of unringed adults were colour-ringed and blood-sampled during nest-building or as helpers at nests.
- Genotyping: blood samples genotyped at 19 microsatellite loci; detailed references provided for loci and earlier related methods.
- Study scope for fitness: fitness quantified for 879 birds (442 females, 437 males) that hatched 1994–2014 and bred up to 2018 with precise offspring production data; only birds known to attempt breeding included.
- Immigrant/ natal classifications: adults from nests not ringed at the study site treated as immigrants; individuals observed as helpers after failed breeding presumed to have failed breeding first, enabling inclusion in indirect effects.
- Handling of missing data: individuals with missing genotypes excluded from parentage checks; females with missing genotypes assumed mothers for all offspring due to low extra-pair brood parasitism; specific rules applied for unringed offspring and unringed adults to avoid misclassification.

# Fitness calculations

- Inclusive fitness framework: both indirect (through helping relatives) and direct fitness (through own offspring) calculated as genetic offspring equivalents.
- Indirect fitness (social effects): proportion of recruits from a brood attributable to helping, multiplied by average relatedness between helper and recruits. Estimation used a GLMM (binomial) in R, with response being whether a ringed individual recruited the following year; fixed effects included number of helpers, helper sex, and fledging date; nest ID and year as random effects.
- Direct fitness: total lifetime recruits attributed to an individual, after subtracting the helper-attributable portion; the remaining fraction is halved to reflect direct parental contribution, then halved again to reflect average parent-offspring relatedness (0.5).
- Extra-pair paternity (EPP) context: given promiscuity (11% of offspring in 29% of nests), paternity was checked to assign recruits to genetic sires where possible; paternity is used to refine both direct and indirect fitness estimates.

# Paternity, maternity, and relatedness

- Paternity assessment: all recruits’ mothers confirmed by matching to social mothers; paternity assigned using CERVUS v3.0.7 with likelihood-based LOD scores; 95% confidence threshold via delta scores from simulations; social father rejected if criteria not met; true sire assigned if another male matched with 95% confidence.
- Handling uncertain paternity: if no male achieved 95% confidence, the recruit’s sire remained unknown and was not reassigned.
- Relatedness: pairwise relatedness between helpers and recruits calculated using Queller & Goodnight method via KINGROUP; used to determine indirect fitness contributions.
- Paternity corrections: recruits inferred to be offspring of genetic sires (not social sires) where identified; maternity checked for all recruits; maternity confirmation used to reassign paternity where necessary.
- Unringed offspring and resident classification: for unringed offspring, likelihood-based assessments (KINGROUP and CERVUS) were used to determine residency vs. immigrant status; residents receive adjusted recruitment tallies.

# Data handling and quality checks

- Data completeness: genotype data missing for a subset; males with missing genotypes excluded from parentage checks; females with missing genotypes treated as mothers.
- Coverage constraints: note that some years had incomplete site coverage (e.g., 2001 data incomplete; 2000 data excluded due to poor coverage).
- Data integration: field observations, genetic data, and pedigree inferences merged into a comprehensive dataset for analysis.

# Dataset and variable structure

- Inclusive_fitness_dataset.csv: extensive columnar dataset with annual and lifetime measures.
- Column descriptions (examples):
  - A–B: ID and sex (F/M).
  - C–F: natal nest helper status, year of first breeding attempt, philopatry status, lifespan.
  - G–T: breeding and helping data across years (e.g., offspring counts by sex, recruits produced, helper counts, and related metrics).
  - U–AD: derived metrics per individual and per year (e.g., fraction of recruits due to help, whether individual helped, number of nest helpers, relatedness to recruits, counts of fledglings and recruits, EPP-adjusted totals, indirect fitness, direct fitness, and cumulative inclusive fitness).
  - EO–ES, ET–EU, etc.: lifetime measures corrected for EPP, including glimmers of direct, indirect, and inclusive fitness.
  - FJ–FK–FL–FQ: lifetime indirect fitness, indirect fitness by cuckolded relatedness, total indirect fitness, and total inclusive fitness.
  - Missing-data indicators and corrections for EPP and life-history corrections are embedded throughout.

# Analytical tools and references

- Software: R v3.2.3 in RStudio v1.0.136; lme4 package for GLMMs; KINGROUP for relatedness and sibship inferences; CERVUS v3.0.7 for paternity inference.
- Key methodological references: Queller & Goodnight relatedness method (1989); KINGROUP (2004); CERVUS (1998/2007) for paternity simulations and inference.
- Analytical model specifics: mixed-effects models to estimate helper effects on recruitment; binomial GLMM with nest ID and year as random effects.

# Data use, limitations, and notes

- Scope and purpose: data enable estimation of inclusive fitness via direct and indirect components, accounting for social structure, kinship, and EPP.
- Limitations: incomplete yearly coverage in some years; reliance on assumptions for natal vs immigrant status in uncertain cases; some individuals lacking genotype data excluded from certain analyses.
- Documentation: comprehensive guide to dataset columns provided to support reuse and transparency of calculations and corrections.