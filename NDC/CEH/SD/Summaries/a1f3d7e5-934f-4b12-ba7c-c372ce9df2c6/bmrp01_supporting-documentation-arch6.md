# Sampling regime and collection methods

- Study setting and population
  - Wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′E).
  - Long-term population study since 1995; typically 10–12 social groups; ~20 adults per group plus offspring.
  - Individuals uniquely marked (fur shave patches in adults; dye marks in pups); regular trapping every two months.
  - 1–2 individuals per group fitted with radio collars for group location via radio telemetry.
  - Groups habituated to observers (within <5 m); visits every 1–3 days for at least 20 minutes to record group composition, life history, and reproductive behaviour.
  - Pups marked around 30 days old; 2 mm tail-tip tissue samples taken for genetic analyses to determine parentage.
  - DNA genotyped with 43 microsatellite markers (or 35 for a subset); intergroup interactions (IGIs) recorded ad libitum during visits.
  - IGI defined as any sighting of two groups with vocalizing, chasing, or fighting.

- Data capture and instrumentation
  - Field data recorded with Psion II data loggers (until 2014) and later via a bespoke Mongoose 2000 data collection app on Samsung Galaxy tablets.
  - Data downloaded and imported into a database (MS Access).
  - Individuals wear radio collars (~30 g) with long (≈20 cm) antennas.
  - Calibration: field instruments calibrated to factory settings.

- Analytical scope and methods
  - Mortality from intergroup conflict (males and females) calculated from adults (>1 year) observed between 2000–2015; 19 deaths (17 males, 2 females) used for analysis.
  - Exposure measured in mongoose-years; mortality rate for each sex per group computed as (deaths/exposure) × 100.
  - Fitness benefits from intergroup conflict:
    - LEGO: lifetime extra-group pups conceived with an extra-group partner.
    - LRS: total lifetime pups (including both extra-group and within-group partners).
    - Parentage assigned via genetic pedigree with probabilities 90% (full 43-marker panel) or 95% (35-marker subset); IGIs experienced over lifetime; age at death recorded.
  - Frequency of IGIs and female estrus:
    - For IGIs (Jan 2000–Mar 2019), assign focal and rival groups; when both observed or unknown, assignment is random.
    - For IGIs with known estrus states of focal/rival females (n = 539), categorize into four states: FE RE, FE RNE, FNE RE, FNE RNE.
    - Compute the number of IGIs by focal-rival pair and estrus state; total days observed in each estrus state.

- Quality control and data validation
  - Mongoose 2000 app includes internal checks (e.g., ensuring presence before recording further data such as reproductive status).
  - Data quality checked via MS Access queries and custom R code to detect inconsistencies (e.g., duplicate death records).

- Data structure and files
  - Data stored in three CSV files, each with descriptive columns:
    - Mortality rates from intergroup conflict (Jan 2000–Dec 2015)
      - Columns: group.id, sex, death, exposure, mortality.rate, number of observed mongoose-years (per sex in group)
    - Fitness benefits from intergroup conflict (Jan 2000–Mar 2019)
      - Columns: sex, lego (lifetime extra-group pups), lrs (lifetime reproductive success), number.igis, age.at.death
    - Frequency of intergroup interactions by estrus state (Jan 2000–Mar 2019)
      - Columns: focal.group.id, rival.group.id, focal.rival.estrus.state, number.igis, days.in.estrus.state, olre (observation identity)
  - Additional notes
    - DNA parentage assignments: 90% (full panel) or 95% (subset) confidence.
    - IGIs and estrus state data cover a multi-year span with structured summarization for downstream analyses.

- Practical implications for data use
  - Rich longitudinal data enabling analysis of intergroup conflict mortality, reproductive benefits of intergroup interactions, and how female estrus states influence interaction frequency.
  - Structured data in three CSV files supports targeted dashboards, tables, and reproducible analyses, with explicit exposure and event counts for robust rate calculations.