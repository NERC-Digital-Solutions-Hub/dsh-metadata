# Sampling regime and collection methods

- Study context and population
  - Wild banded mongoose (Mungos mungo) population on Mweya Peninsula, Queen Elizabeth National Park, Uganda (0°12′ S, 29°54′E).
  - Studied continually since 1995; groups typically 10–12 social groups, ~20 adults plus offspring per group.
  - Individuals uniquely marked; radio collars fitted to 1–2 individuals per group for location; most groups habituated to observers.

- Data collection regime
  - Groups visited every 1–3 days (≥20 minutes per visit) to record group composition, life history, reproduction, and cooperative behaviour.
  - Reproduction highly synchronized within groups; pregnancy detected by abdomen swelling and ultrasound confirmation during routine trapping.
  - Birth occurs communally; pups are marked and sampled for genetics at ~30 days old; DNA genotyped with 43 microsatellite markers.
  - Escorting behaviour observed for ~60 days post-birth; pups monitored to quantify escorting by adults.
  - Weighing conducted weekly using portable electronic scales; most individuals trained to stand on scales for measurement.

- Experimental design
  - Split-plot provisioning experiment to create early-life asymmetries: pregnant females in each breeding attempt allocated to fed (provisioned) or non-fed (control) groups.
  - Randomization rules implemented to minimize predictability; provisioning began 2–4 days after pregnancy confirmation and continued until parturition.
  - Provisioning details: average 50 g of egg per day (n=101 fed pregnancies) vs approached but not provisioned for non-fed (n=97 non-fed pregnancies).
  - Random daily amount and timing (0, 50, or 100 g; morning or evening) to avoid cueing foraging behavior.
  - Across all groups, manipulated breeding attempts followed by unmanipulated controls to dissipate effects before next manipulation.
  - Total manipulation: 34 breeding attempts in 7 mongoose groups over 2013–2016; 101 fed pregnancies and 97 non-fed pregnancies; resulting 50 treatment pups (fed) and 50 control pups (non-fed).

- Field instrumentation and calibration
  - Data captured with a bespoke Mongoose 2000 app on Samsung tablets; data stored in MS Access databases.
  - Weighing with Sartorius TE6100 scales; radio collars ~30 g with 20 cm whip antennas.
  - Pregnant females scanned with ultrasound machines (pre-2017: SIUI CTS-900V; post-2017: Sonoscape S6BW with L742 probe).
  - Instruments calibrated to factory settings; internal app checks reduce data collection errors.

- Analytical framework (key outcomes and measures)
  - (1) Female condition: pre-pregnancy weight (baseline ~67–74 days pre-birth) and percentage change during pregnancy, post-pregnancy, and escorting period.
  - (2) Adult escorting behaviour: escorting effort during escorting period (proxied by proportion of group visits with escorting) plus age and helper-to-pup ratio.
  - (3) Allocation of escorting to pups: escorting effort directed to each pup by fed vs non-fed mothers and by males; related to pup age and adult-to-pup ratios.
  - (4) Pup weight and growth: pup weights from 30–90 days; age at weighing; within-litter weight variance (relative variance) in litters with ≥4 pups.
  - (5) Escorting received by pups: total escorting per pup (proportion of visits) and rate of escort-feeding (feeds per hour) and nearest-neighbour proximity metrics.
  - (6) Pup survival: survival to 90 days, 180 days, and 365 days; end ages when survival observed; continued tracking of adult-to-pup ratio during escorting.

- Data structure and content
  - Data stored in 15 CSV files, detailing each aspect of the experiment (maternal weight changes, escorting effort, pup weights, pup survival, relatedness, etc.).
  - Examples of content and key columns:
    - Female weight change to pregnancy (indiv, female ID, litter, breeding attempt, category T/C/R, weight.change).
    - Female weight change to post-pregnancy and to escorting period (similar schema).
    - Maternal and pup escorting data (esc.litter, breeding attempt, age, esc.index, esc.freq, category; focalPup data with feeds.rate and nn.str).
    - Pup weights and growth (pup ID, weight, litter, category, age in days, helper.ratio).
    - Relative within-litter variance (age.cat, litter.cat, relative.variance).
    - Pup survival datasets (surv.90days, surv.6mo, surv.year with end.age fields; category and sex).
    - Pairwise relatedness data (r dyadic, escort-pup pair indicator).

- Quality control and data integrity
  - Built-in Mongoose 2000 checks enforce presence of individuals in group data before recording related behaviours.
  - Data quality checks performed in MS Access and bespoke R scripts to detect inconsistencies (e.g., multiple death records for an individual).

- Data access and structure considerations for analysts
  - Comprehensive, multi-file dataset enabling analyses of causal effects of early-life provisioning on maternal condition, social dynamics (escort networks), offspring development, and long-term survival.
  - Pedigree information derived from genetic data to inform parentage and relatedness analyses.
  - Datasets encompass both group-level and individual-level measures, with explicit treatment categories (fed, non-fed, unmanipulated) for pups and adults.

- Summary takeaways for analysts
  - The study provides a rigorously randomized, controlled manipulation of early-life resources in a wild mammal population, with rich longitudinal data on maternal condition, social behaviour, pup care, growth, and survival.
  - The data enable testing of how provisioning alters:
    - Female condition trajectories across pre-pregnancy, pregnancy, post-pregnancy, and escorting phases.
    - Distribution of escorting effort among pups and the role of adult helpers.
    - Within-litter growth dynamics and variance among pups.
    - Long-term pup survival across developmental milestones.
  - Meta-analytic and modelling opportunities include: provisioning effects on maternal investment, social network dynamics, kinship-driven care, growth-survival trade-offs, and population-level implications of early-life resource manipulation.