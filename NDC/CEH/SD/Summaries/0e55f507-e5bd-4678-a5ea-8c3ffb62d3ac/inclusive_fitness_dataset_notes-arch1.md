# Fieldwork and data collection (Adapted from Green JP & Hatchwell BJ (2018) Inclusive fitness consequences of dispersal decisions in a cooperatively breeding bird, the long-tailed tit ( Aegithalos caudatus ). PNAS 115:12011-12016.)

- Study system and scope
  - Population of 25-72 breeding pairs studied from 1994 to 2019 at a 3 km² site in the Rivelin Valley, Sheffield, UK.
  - Habitat mix includes deciduous woodland, farmland, scrub, and gardens; surrounding habitat is generally low quality.
  - All nestlings were ringed with unique colour-ring combinations; blood samples collected under Home Office license for genetic analyses.
  - >95% of unringed adults were colour-ringed and blood-sampled either during nest-building or when assisting at nests.

- Genetic data and individuals
  - 19 microsatellite loci genotyped for individuals with blood samples.
  - Fitness quantified for 879 birds (442 females, 437 males) hatched 1994–2014 and bred through 2018, with precise offspring production data.
  - Included birds known to attempt breeding; some were observed as helpers after failed breeding attempts.

- Fitness components and calculations
  - Inclusive fitness combines indirect (through helping relatives) and direct fitness (own offspring).
  - Indirect fitness: calculated as the fraction of recruits from a brood due to helping, multiplied by the average relatedness between the helper and recruits.
  - Model used to estimate helper effects on recruitment: generalized linear mixed model (GLMM) with binomial error (glmer in lme4, R).
    - Fixed effects: number of helpers at the nest, helper sex (to account for greater male philopatry), and date of fledging (earlier fledging linked to higher recruitment).
    - Random effects: nest ID and year.
  - Indirect fitness per helping event and helper-relatedness to recruits computed from model outputs and pairwise relatedness (Queller & Goodnight) via KINGROUP.

- Paternity and relatedness analyses
  - Paternity checked for all males using CERVUS v3.0.7; LOD scores and delta scores used to assign sires with 95% confidence, considering maternities by genotypes.
  - Extra-pair paternity (EPP) accounted for: recruits attributed to genetic fathers; social fathers removed if not genetically confirmed.
  - When multiple loci mismatched with potential sires, true sire was deemed unknown and recruits were not reassigned.
  - For unringed offspring in inaccessible nests, attempts were made to assign them to resident breeders using KINGROUP; paternity checks then applied where possible.

- Data handling for incomplete data and special cases
  - Males with missing genotypes excluded from parentage assignments; females with missing genotypes treated as mothers by default due to low rates of conspecific brood parasitism.
  - Recruits with missing genotypes assigned to social mothers; no paternity assignment attempted for those recruits.
  - Some offspring fledged in years with poor data coverage; affected years excluded from recruitment analyses.

- Data structure and usage
  - Inclusive_fitness_dataset.csv described with extensive fields:
    - Individual identifiers, sex, natal nest/immigration status, first breeding year, philopatry, lifespan.
    - Year-by-year breeding and helping metrics for up to seven life years (e.g., fledglings, recruits, helpers, relatedness, indirect fitness, EPP corrections).
    - Summary metrics: lifetime fledglings/recruits, direct fitness, indirect fitness, and total inclusive fitness.
    - Detailed columns track EPP corrections, grand-offspring counts, and relatedness for each recruitment event.

- Software and reproducibility
  - Analyses performed in R (R v. 3.2.3) and RStudio (v. 1.0.136); GLMMs via lme4; relatedness via KINGROUP.
  - Paternity and pedigree inferences supported by CERVUS v3.0.7; simulations used to establish confidence thresholds.
  - Data and metadata prepared to enable discovery and reuse (including explicit column explanations and coding).

- Key methodological considerations
  - Direct fitness estimated by subtracting helper-attributable recruits from total recruits, then adjusting for parent-offspring relatedness (0.5).
  - Emphasis on correcting for EPP to avoid inflating indirect or direct fitness due to non-parental paternity.
  - Recognition of potential uncertainties in paternity, missing data, and unringed individuals, with explicit handling rules to maintain analytical rigor.