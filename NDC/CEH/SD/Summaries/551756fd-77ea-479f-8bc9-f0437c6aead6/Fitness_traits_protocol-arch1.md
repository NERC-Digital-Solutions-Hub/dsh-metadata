# Fitness traits of experimentally selfed and outcrossed Eschscholzia californica plants

- Objective and context
  - Assess effects of self-fertilisation on fitness traits in Eschscholzia californica, a plant with low selfing propensity.
  - Part of a larger experiment on how floral resources influence pollination services to isolated plants.
  - Dataset collected and interpreted by Evans, T.M.

- Experimental design
  - Glasshouse experiment with 40 artificially crossed plants.
  - On each plant: emasculated two flowers; one flower received outcrossed pollen, the other self-pollen.
  - From each supplemented plant, sowed a seed from the outcrossed fruit and a seed from the selfed fruit (selfed fruits typically yield one seed).
  - Growth conditions: 1 L pots; day/night 20°C/15°C; light/dark 12:12 hr.
  - Measured fitness-related outcomes at reproductive maturity.

- Observed fitness traits (per seed/lineage)
  - Germination (binary: 1 = germinated, 0 = did not)
  - Duration from germination to reproductive maturity (days to first flower)
  - Height at reproductive maturity (cm)
  - Number of flowers at reproductive maturity
  - Number of buds at reproductive maturity
  - Total biomass at reproductive maturity (flowers + buds)

- Data structure and key variables
  - File: Fitness_traits_of_outcrossed_and_selfed_plants.csv
  - Plant: identifier for the artificially supplemented plant
  - Parentage: whether the seed originated from outcrossed or selfed pollen
  - Germination: 1/0
  - Duration_from_germination_to_reproductive_maturity: days
  - Height_at_reproductive_maturity: cm
  - Number_of_flowers_at_reproductive_maturity
  - Number_of_buds_at_reproductive_maturity
  - Total_biomass_at_reproductive_maturity
  - NA values recorded when seeds did not germinate

- Provenance and usage
  - Data is described as complete.
  - Data supports broader investigation into pollination services in isolated plants and is tied to the experimental framework on floral resources.

- Suggested analyses for data-driven researchers
  - Compare selfed vs outcrossed treatments across germination, growth, and reproductive traits using paired tests or mixed models to account for plant-level pairing.
  - Use logistic regression to model germination probability by parentage (and potential covariates if available).
  - Apply ANOVA or GLM to compare continuous traits (time to maturity, height, flower count, bud count, biomass) by parentage.
  - Explore correlations between early germination and later traits (growth and reproductive output).
  - Implement mixed-effects models with Plant as a random effect to capture within-plant correlations between the two treatments.

- Data quality considerations
  - Sample size is 40 plants with paired selfed/outcrossed measures per plant; consider paired analytical approaches.
  - NA entries occur where germination failed; handle appropriately in analyses (e.g., exclude or impute where justified).
  - Findings are specific to controlled glasshouse conditions and may reflect responses under that environment for this species.