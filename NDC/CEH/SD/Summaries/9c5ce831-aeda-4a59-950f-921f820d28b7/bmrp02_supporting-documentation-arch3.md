# Sampling regime and collection methods

- Long-term study of wild banded mongooses (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′E).
- Continuous study since 1995; typical population: 10–12 social groups across distinct territories; groups ~20 adults plus offspring.
- Individual identification through unique marks (shave patches in adults; dye marks in pups) maintained via regular trapping every two months.
- One to two individuals per group fitted with radio collars for group localization; most groups habituated to observers at close range (<5 m).
- Data collection cadence: groups visited every 1–3 days for at least 20 minutes to record group composition, life history, reproductive and cooperative behaviour.
- Reproduction: highly synchronized within groups; pregnancy detectable by abdominal swelling and ultrasound; communal birth and pup care by group members.
- Pups tracked from birth (~30 days old) with tagging and tissue sampling for genetic analyses (tail biopsy, 2 mm) to determine parentage via 43 microsatellite markers.
- Post-emergence, pups receive escorting from adults for ~60 days, with daily visits to monitor caregiving and social interactions.
- Weighing conducted weekly using portable electronic scales; most individuals trained to step onto scales for measurement.

- Experimental design: manipulated provisioning to pregnant females to create early-life asymmetries.
  - Split-plot design: half of pregnant females in a breeding attempt provisioned (fed) and half unprovisioned (non-fed).
  - Randomization rules ensure balanced pairing and avoid predictable provisioning; overlapping with unmanipulated (control) breeding attempts.
  - Provisioning: average 50 g of eggs per day from about 2–4 days post-pregnancy confirmation until parturition; daily amounts randomized (0, 50, or 100 g) and timing randomized (morning or evening).
  - Across study period (2013–2016): 34 breeding attempts in 7 groups; 101 fed pregnancies and 97 non-fed pregnancies.
  - Outcomes tracked: offspring (treatment vs control pups) and maternal effects; genetic maternity assignments with ~90% probability.

- Fieldwork instrumentation:
  - Data collection app (Mongoose 2000) on Samsung Galaxy tablets; data downloaded to MS Access database.
  - Weighing with Sartorius TE6100 portable scales.
  - Radio collars (~30 g) with 20 cm whip antenna.
  - Pregnancy and birth monitoring via ultrasound: SIUI CTS-900V or Sonoscape S6BW ultrasound machines.

- Calibration and data quality:
  - Field instruments calibrated to factory settings.
  - Embedded app checks to reduce data collection errors (e.g., presence required to collect certain behavioural data).
  - Data quality checks via MS Access queries and bespoke R code to detect inconsistencies (e.g., multiple death records for an individual).

- Analytical framework:
  - (1) Effect of provisioning on female condition: analyze pre-pregnancy baseline weight and weight changes during pregnancy, post-pregnancy, and during escorting.
  - (2) Effect on adult escorting behaviour: compute escorting effort as proportion of group visits; incorporate age and helper-to-pup ratios.
  - (3) Allocation of escorting to pups: quantify escorting effort directed toward each focal pup, by fed vs non-fed adults.
  - (4) Pup weight and growth: extract pup weights (30–90 days), compute age at weighing, and analyze within-litter weight variance for litters with at least four pups.
  - (5) Escorting received by pups: total escorting, feeding rate by escorts (feeds per hour), and proximity metrics (proportion of scans Escorts near focal pup).
  - (6) Pup survival: track survival to 90 days, 180 days, and 365 days, with corresponding end ages and adult-to-pup ratios during escorting.

- Data structure and contents:
  - Data stored in 15 CSV files detailing:
    - Female weight change from pre-pregnancy baseline to pregnancy, post-pregnancy, and escorting periods.
    - Maternal weight change to post-pregnancy and to escorting period.
    - Female and male escorting effort across the escorting period.
    - Escorting directed toward each pup by fed and non-fed adults.
    - Pairwise relatedness data for pup–adult dyads.
    - Pup-directed escorting by males.
    - Pup weights (individual records with age, sex, litter, category, and helper ratios).
    - Proportions of escorting received by focal pups (feeds rate and neighbour proximity).
    - Pup survival to 90 days, 180 days, and 365 days with end ages and sex.
  - Column conventions:
    - IDs: indiv (individual), repro.litter, breeding attempt ID, pack, social group ID.
    - Category and treatment: current.category or experimental treatment group (T = fed, C = non-fed, R = unmanipulated).
    - Measurements: weight.change, escort.index/esc.freq, age, feeds.rate, nn.str, surv.90days/6mo/year, etc.
  - Data structure supports linkage across multiple levels (individuals, litters, breeding attempts, packs, groups) for multilevel analyses and reproducibility.