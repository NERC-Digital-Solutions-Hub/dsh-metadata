# Fieldwork and data collection

- Study site and population: 3 km² area in the Rivelin Valley, Sheffield, UK (52°23'N, 1°34'W) with mixed deciduous woodland, farmland, scrub, and gardens; population comprised 25–72 breeding pairs observed from 1994–2019.
- Field data collection: All nestlings ringed with unique colour-ring combinations; blood samples taken under Home Office License for genetic analysis; colour-ringing and blood-sampling succeeded for >95% of unringed adults, either during nest-building or as helpers at nests.
- Population scope: Fitness quantified for 879 birds (442 females, 437 males) hatched 1994–2014 and bred through 2018; includes only individuals known to attempt breeding.
- Data scope and site details: Adults often immigrate; individuals assumed to be one year old after first breeding season; study provides long-term data across multiple years and nests.

## Data collection and genetic groundwork

- Sampling and genetics: Blood samples collected for genotyping; individuals genotyped at 19 microsatellite loci; linkage to prior methodological work described in related publications.
- Age and movement: Very limited dispersal after first breeding, enabling inference of residency and immigrant status over time.
- Offspring tracking: Offspring production tracked per individual across life; includes a subset of birds observed as helpers when their own breeding failed.

## Fitness calculations and concepts

- Inclusive fitness framework: Indirect fitness (through helping relatives) and direct fitness (through own offspring) quantified as genetic offspring equivalents.
- Indirect fitness estimation: Fraction of recruits from a brood attributable to helpers multiplied by average relatedness between helper and recruits; estimated via mixed-effects modelling (GLMM with binomial error) in R.
- Model specifics: Response variable is whether an individual recruited in the following year; fixed effects include number of helpers at the nest, sex of the fledgling, and fledging date; random effects include Nest ID and year.
- Direct fitness estimation: Total lifetime recruits (genetic offspring equivalents) minus the portion attributable to helpers; then adjusted by halving to reflect parent-offspring relatedness (0.5) and average parent-offspring relatedness.
- Paternity and extra-pair paternity (EPP): Paternity checked for all males; recruits attributed to genetic father where possible using CERVUS v3.0.7 with LOD and delta scores and 95% confidence thresholds; cases with ambiguous paternity treated accordingly. Maternity confirmed for recruits; EPP corrections applied to direct and indirect fitness calculations.

## Data cleaning, paternity handling, and data integrity

- Unringed offspring: Nests inaccessible offspring attempted to be assigned to known breeders; unringed adults assigned to breeders based on likelihood of mother-offspring relationships; paternity then re-assessed where possible.
- Genotype availability: Individuals with missing genotype data excluded from parentage analyses; female missing genotype assumed to be the mother for offspring in nests with negligible brood parasitism; paternal assignments made when criteria met.
- Recording gaps and exclusions: Some years or data points excluded due to incomplete coverage (e.g., year 2000; data available for 1994–2015 with 1706 data points); specific handling rules for missing data applied to maintain dataset integrity.

## Software, tools, and methodological references

- Primary analysis tool: R v3.2.3 in RStudio v1.0.136; GLMMs implemented with lme4 package.
- Pedigree and relatedness analyses: KINGROUP v2 for pedigree/kinship calculations; Queller & Goodnight (1989) relatedness method.
- Paternity inference: CERVUS v3.0.7 for likelihood-based paternity assignment; simulations used to derive delta score thresholds and confidence levels.
- Related literature: Methods described and validated in Green & Hatchwell and associated works; genetics and social structure analyses linked to prior publications on long-tailed tits.

## Dataset structure and column highlights

- Inclusive_fitness_dataset.csv contains a comprehensive set of fields, including:
  - A–F: ID, Sex, natal nest helper status, first breeding year, philopatry status, lifespan.
  - H–AD (and yearly expansions up to Year 7): Breeding and helping metrics for each year of life, including numbers of male/female/fledglings, fledglings corrected for EPP, recruits produced (and corrected for EPP), counts of helpers, and calculated metrics such as indirect fitness gained through helping.
  - U–AB: Helper presence indicators, total number of helpers, nest identities, and relatedness values.
  - AC–AD: Fledgling and recruit counts, proportions recruited, and indirect fitness measures for each individual.
  - AE–FJ: Lifetime and lifetime-corrected fitness outcomes (fledglings, recruits, direct fitness, indirect fitness, and inclusive fitness).
  - FK–FL: Total indirect fitness, data on missing genetic information, and corrected lifetime fitness accounting for EPP.
  - FN–FO: Adjusted lifetime recruits and corrected direct/recruit metrics.
  - FP–FQ: Final tallies for direct fitness and inclusive fitness, integrating EPP corrections and kinship considerations.

- Purpose of the dataset: To enable analyses of how helping behavior affects recruitment and lifetime fitness, incorporating genetic parentage, EPP adjustments, and longitudinal life-history data across multiple nests and years.

## Relevance to GIS-focused data products

- Spatial linkage potential: Nest IDs and study site coordinates enable mapping of breeding territories, helper presence, and dispersal patterns across space and time.
- Temporal depth: Longitudinal data across multiple years supports temporal GIS analyses of habitat use, movement, and social structure dynamics.
- Data integration: Rich metadata on individuals, nests, and kin relationships facilitates integration with spatial layers (habitat types, nest locations, and movement corridors) for map-based visualisations of social networks and fitness landscapes.
- Data quality and standards: Detailed data-cleaning rules, paternity verification, and EPP corrections illustrate rigorous data governance suitable for reproducible map-based data products.