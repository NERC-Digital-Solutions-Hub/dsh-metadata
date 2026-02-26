# Sampling regime and collection methods

- Study context and scope
  - Wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda; population studied since 1995.
  - Groups typically 10–12 social groups, around 20 adults plus offspring; individuals uniquely marked for long-term identification.
  - Data collected on group composition, life history, reproductive and cooperative behaviours, with DNA parentage and weight measurements.

- Data collection and variables
  - Regular trapping every 2 months to maintain marks; radio collars fitted to 1–2 individuals per group for location.
  - Observations occur every 1–3 days for at least 20 minutes; focal follows and continuous recording of social interactions.
  - Reproduction: pregnancy detected by abdomen swelling and ultrasound; pups marked and DNA genotyped using 43 microsatellite markers.
  - Escorting period: pups receive care from adults for ~60 days post-pup emergence; data include number of escorting visits, proximities, and feeding events.
  - Measurements: weights obtained on portable scales; pups weighed weekly; individuals weighed during specified windows.

- Experimental design
  - Split-plot provisioning experiment across 34 breeding attempts in 7 groups (2013–2016).
  - Pregnant females assigned to fed (T) or non-fed (C) groups; randomization scheme to balance prior manipulations; unmanipulated controls (R) used after each manipulated attempt.
  - Fed females receive ~50 g eggs daily until birth; amount and timing randomized (0, 50, 100 g; morning or afternoon) to prevent predictability.
  - Outcome focus includes offspring birth outcomes and subsequent behaviours; manipulated litters followed by unmanipulated controls to dissipate effects.

- Fieldwork instrumentation
  - Data captured via bespoke Mongoose 2000 app on Samsung Galaxy tablets; data stored in MSAccess database.
  - Equipment: portable electronic scales, radio collars, ultrasound machines (pre-2017) and associated probes.
  - Calibration performed to factory settings; multiple data collection checks embedded in the app.

- Analytical methods (primary analyses)
  1) Effect of provisioning on female condition: pre-pregnancy weight baseline (67–74 days before birth) and percentage weight changes during pregnancy, post-pregnancy, and escorting period.
  2) Effect on adult escorting behaviour: escorting effort as proportion of group visits; age and helper-to-pup ratios considered.
  3) Allocation of escorting to pups: escorting effort by fed vs non-fed adults directed to each pup; includes pup and adult ages and helper ratios.
  4) Pup weight and growth: pup weights between 30–90 days, age at weighing, litter variance within litters (relative to all litters).
  5) Amount of escorting received by pups: total escorting as proportion of visits; feeding rate by escorts; proximity measures to focal pups.
  6) Pup survival: survival to 90 days, 180 days, and 365 days; end ages recorded; continued consideration of helper ratios.

- Quality control and data integrity
  - Built-in app checks to minimize collection errors (e.g., presence required for further data collection).
  - Data quality checks via MSAccess queries and custom R scripts to detect inconsistencies (e.g., duplicate death records).

- Data structure and content
  - Data stored in 15 CSV files with detailed, protocol-driven content.
  - Example content areas:
    - Female weight change: pre-pregnancy baseline to birth, to post-pregnancy, and to escorting period (with fields for individual ID, litter, breeding attempt, group, category, and weight change).
    - Escorting data: male and female escorting effort across the escorting period (age, escort index, frequency, treatment group).
    - Pup-focused data: pup weights, survival outcomes (90 days, 180 days, 365 days), pup category (fed/non-fed/unmanipulated), feeding rate, nearest-neighbour metrics, and helper ratios.
    - Pairwise relatedness: dyadic relatedness between pup-adult pairs.
  - File naming conventions reflect study variables (e.g., maternal weight change files, escorting files, pup weight and survival files) and include treatment group indicators (T, C, R).

- Data availability and workflow
  - Primary data collection via Mongoose 2000 app; data exported to 15 CSV files for analysis.
  - Study provides a comprehensive, multi-faceted dataset linking provisioning, maternal condition, social behaviour, and offspring outcomes across multiple breeding attempts and groups.