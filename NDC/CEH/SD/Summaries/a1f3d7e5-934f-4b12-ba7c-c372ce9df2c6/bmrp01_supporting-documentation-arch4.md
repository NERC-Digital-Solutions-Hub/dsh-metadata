# Sampling regime and collection methods

- Study context and population
  - Banded mongoose (Mungos mungo) population on Mweya Peninsula, Queen Elizabeth National Park, Uganda.
  - Long-term study ongoing since 1995; 10–12 social groups typically present, with around 20 adults per group plus offspring.
  - Individuals are uniquely marked for life-long identification (adult shave patches; pups dye marks); regular trapping every two months.
  - 1–2 individuals per group fitted with radio collars for location via radio telemetry; most groups habituated to observers at close range.

- Field observations and data collection
  - Groups visited every 1–3 days for at least 20 minutes to record group composition, life history, and reproductive behavior.
  - Estrus dynamics: females in estrus within a few days of one another; intensive male mate guarding during this period.
  - Births recorded when females are pregnant; pups marked at ~30 days; tissue samples (2 mm tail) collected for genetic analyses to determine parentage.

- Genetic and measurement methods
  - DNA genotyping using a panel of 43 polymorphic microsatellite markers (or 35 for a subset).
  - Genetic pedigree used for maternity/paternity assignments with high assignment probabilities (90% or 95%).

- Field instruments and data capture
  - Data recorded with a Psion II data logger (until 2014) and later with a bespoke Mongoose 2000 app on Samsung Galaxy Note 10.1 tablets.
  - Data downloaded and imported into an MS Access database.
  - Radio collars weigh ~30 g with a 20 cm whip antenna.

- Calibration and data integrity
  - Field instruments calibrated to factory settings.
  - The Mongoose 2000 app includes internal checks to reduce data collection errors (e.g., presence requirement for data on individuals in group composition).

- Analytical focus and data products
  - Long-term observational data used to quantify:
    - Mortality from intergroup conflict by sex (2000–2015) and exposure in mongoose-years; calculation yields mortality rate as (deaths/exposure) × 100.
    - Fitness benefits from intergroup conflict: lifetime extra-group offspring (LEGO) and lifetime reproductive success (LRS) for adults post-2000; offspring assignments via genetic pedigree; includes number of intergroup interactions and age at death.
    - Frequency of intergroup interactions (IGIs) with female estrus states (2000–2019): focal vs. rival groups; estrus state combinations (FE RE, FE RNE, FNE RE, FNE RNE); totals of IGIs by state and days observed in each state.

- Quality control and data governance
  - Data quality checks via MS Access queries and bespoke R scripts to detect inconsistencies (e.g., multiple death records for a single individual).
  - Longitudinal data management across multiple years with standardized procedures for marking, sampling, and pedigree construction.

- Data structure and content
  - Three CSV files detailing distinct data domains:
    - Mortality rates from intergroup conflict (2000–2015)
      - Columns: group.id, sex, death, exposure, mortality.rate, number of observed mongoose-years
      - Purpose: group-level mortality by sex and rate calculation
    - Fitness benefits from intergroup conflict (2000–2019)
      - Columns: sex, lego (lifetime extra-group pups), lrs (lifetime reproductive success), number.igis, age.at.death
      - Purpose: individual-level reproductive success metrics and exposure to IGIs
    - Frequency of IGIs by estrus state (2000–2019)
      - Columns: focal.group.id, rival.group.id, focal.rival.estrus.state, number.igis, days.in.estrus.state, olre (unique observation identity)
      - Purpose: IGI counts stratified by estrus state and observation duration

- Accessibility and references
  - Data collection tools and platforms referenced (Mongoose 2000 app available via Google Play; MS Access for data management).
  - Genetic pedigree data underpin paternity/maternity assignments and related analyses.