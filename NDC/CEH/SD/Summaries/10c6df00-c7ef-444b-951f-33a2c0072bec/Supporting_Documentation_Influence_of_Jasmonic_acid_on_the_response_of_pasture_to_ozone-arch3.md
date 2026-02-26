# Influence of jasmonic acid on the effect of ozone on pasture

- Purpose and context
  - Investigates interactive effects of ozone exposure and methyl jasmonate (MeJa) signaling on white clover (T. repens cv. Crusader) to understand above- and below-ground responses relevant to pasture health.
  - Uses a phytometer-based, controlled environment setup to simulate ozone profiles and assess plant injury, growth, and nodulation.

- Experimental design and setting
  - Seedlings propagated in plug trays, transferred to 7.5 L pots with soil inoculation to introduce a soil microbe population.
  - Plants grown under six solardomes (hemispherical glasshouses) at the CEH solardome facility, near Bangor, UK.
  - Randomized application of ozone profiles across solardomes; monitoring of temperature, soil moisture, PAR, and relative humidity in at least one dome.

- Treatments
  - Uncut control (no clipping or MeJa)
  - Cut+ (single cut to 4 cm height immediately before ozone exposure)
  - MeJa+ (uncut with weekly foliar application of methyl jasmonate solution)
    - MeJa solution: 8 mM stock in alcohol, diluted to 500 μM final concentration; weekly spray in late afternoon to run-off
    - Control treatments sprayed with 0.1% ethanol to account for solvent effects
  - All pots included 3 seedlings; repeated watering and rotation within domes

- Ozone exposure and measurements schedule
  - Ozone profiles divided into low (profiles 1, 2, 3) and high background (profiles 4, 5, 6) and then pooled for analysis.
  - Exposure period: 4 weeks (start 28 May 2014, end 24 June 2014).
  - Measurements taken weekly; shoots and leaves assessed for injury and senescence; a representative quarter of each pot photographed/evaluated for healthy, injured, or senesced status.
  - Injury and senescence thresholds: >25% of adaxial leaf surface affected considered injured or senesced.
  - Post-exposure harvest: above- and below-ground biomass, root nodules, and leaf area index (LAI) of undamaged leaves; nodules counted and weighed; biomass dried at 60°C for at least 48 hours.

- Data collection, processing, and analysis
  - Biomass and injury data expressed per pot or per representative pot quarter; adjustments made for differences in shoot biomass to calculate injury metrics on a per-biomass basis.
  - Statistical analysis (R v3.1.2) with:
    - Analysis of variance (ANOVA) using ozone background and treatment as factors
    - Post-hoc Tukey’s HSD tests to determine factor significance
    - Pearson correlations between total root nodule biomass and biomass/injury parameters
    - Arcsine transformation applied to injury data prior to ANOVA
  - Sampling and replication:
    - 5 replicate pots per treatment per solardome
    - Ozone profiles applied randomly; plant rotation within domes to minimize positional effects

- Data files and structure
  - Biomass data: biomass1worksheet.csv (23 columns)
    - Key fields: pot, treatment.code, MeJa+ / Cut+ / Control, jasmonate treatment, cutting, dome, mean.ozone, ozone category, shoot.dry, shoots.bag, shoot.biomass, roots.dry, roots.bag, root biomass, roots.pot, root:shoot, nodules, nodules.pot, nodule.bag, dry, nodule.biomass, nodule.biomass.pot, total.biomass, mass.per.nodule
  - Injury assessments: injury_first_assessment.csv, injury_second_assessment.csv, injury_third_assessment.csv (each 11 columns)
    - Key fields: pot, treatment (codes a-d for MeJa+/Cut+ etc.), jasmonate, cutting, dome, mean.ozone, total.injury, total.senescence, total.leaves, percent.injured, percent.senesced
  - Notes
    - The biomass dataset includes a complete outline of pot-level measurements and derived metrics (e.g., root:shoot, nodule metrics, total biomass).
    - Injury datasets document raw injury and senescence scores across three assessment time points, enabling temporal analysis of ozone and MeJa effects.

- Replicability, controls, and data integrity
  - Experimental controls for solvent effects (0.1% ethanol) and randomization of ozone profiles.
  - Measures to prevent cross-contamination (overnight enclosure after MeJa application) and plant rotation to mitigate positional biases.
  - Clear definitions of injury thresholds and consistent measurement protocols to facilitate comparability and re-analysis.

- Relevance for monitoring, evaluation, and policy guidance
  - Demonstrates a structured approach to monitoring plant health under environmental stressors (ozone) and regulatory-relevant signaling mechanisms (MeJa).
  - Provides a transparent data framework (comprehensive metadata in column descriptions) enabling policymakers and researchers to assess ozone impacts on pasture production, including growth, stress injury, and nodulation, which influence long-term pasture productivity.
  - Highlights integration of treatment effects, dose (ozone background), and plant defense signaling in a controlled setting, informing policy-science collaborations on air quality impacts in agricultural systems.