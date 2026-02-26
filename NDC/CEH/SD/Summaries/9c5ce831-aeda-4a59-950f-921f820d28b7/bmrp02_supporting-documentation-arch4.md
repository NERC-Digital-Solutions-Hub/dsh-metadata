# Sampling regime and collection methods

- Context: Long-running study of a wild banded mongoose population (Mungos mungo) on the Mweya Peninsula, Queen Elizabeth National Park, Uganda, in operation since 1995; 10–12 social groups with about 20 adults plus offspring per group; individuals marked for identification and tracked via regular trapping and radio telemetry.

- Data collection cadence and scope:
  - Groups visited every 1–3 days for at least 20 minutes; routine data include group composition, life history, reproductive and cooperative behaviors.
  - Pup marking and genetic sampling: tissue (2 mm tail) collected at ~30 days after birth for parentage using a 43-marker microsatellite panel.
  - Weighing: most individuals weighed weekly with portable electronic scales.
  - Reproduction: synchronized within groups; pregnancy detected by abdomen swelling and ultrasound; birth timing often synchronized; escorting period (~60 days) tracked after birth with continuous behavioral observations.

- Experimental design (provisioning manipulation):
  - Split-plot design to test provisioning effects: fed (provisioned with ~50 g egg/day) vs non-fed controls; random assignment within age-matched pairs; cross-overs to opposite category if previously manipulated; 34 breeding attempts across 7 groups (2013–2016).
  - Each manipulated breeding attempt followed by an unmanipulated control breeding attempt to dissipate provisioning effects before the next manipulation.
  - Outcomes: 101 fed female pregnancies vs 97 non-fed female pregnancies; resulting 50 pups from fed mothers and 50 from non-fed mothers; maternity assignments determined via genetic pedigree with ~90% assignment probability.

- Fieldwork instrumentation:
  - Data capture: bespoke Mongoose 2000 app on Samsung Galaxy tablets; data downloaded into an MS Access database.
  - Measurements: weights via Sartorius TE6100 scales; radio collars (~30 g) for individuals; ultrasound equipment for pregnancy assessment.
  - Calibration: instruments calibrated to factory settings.

- Analytical framework (key analyses):
  - Female condition: baseline weight 67–74 days pre-birth; percent weight change during pregnancy, post-pregnancy, and escorting period.
  - Adult escorting behavior: escorting effort as proportion of group visits; age at escorting period; adult-to-pup ratio.
  - Escorting allocation to pups: distribution of escorting effort by fed vs non-fed adults to pups; age and helper ratio considerations.
  - Pup growth and variance: pup weights at 30–90 days; within-litter weight variance relative to total variance.
  - Escorting received by pups: total escorting, escort frequency per hour, proportion of scans with adult as nearest neighbor.
  - Pup survival: survival to 90, 180, and 365 days; associated end ages and helper ratios during escorting period.

- Quality control and data integrity:
  - In-app checks to enforce presence requirements for data collection; cross-checks in MS Access and bespoke R code to detect anomalies (e.g., inconsistent death records).

- Data structure and metadata:
  - 15 CSV files comprising the full dataset; representative contents include:
    - Female weight change from pre-pregnancy baseline to pregnancy (indiv, repro.litter, breeding attempt, pack, group, current.category, treatment, weight.change).
    - Female weight change to post-pregnancy (same schema with post-pregnancy metric).
    - Female weight change to escorting period (same schema with escorting period metric).
    - Female escorting effort across the escorting period (age, esc.index, esc.freq, category).
    - Male escorting effort across the escorting period (age, esc.index, esc.freq, exp, helper.ratio).
    - Allocation of escorting to pups by fed vs non-fed adults and pups (pup.id, indv, category, esc.index, esc.freq, helper.ratio, ad.category).
    - Pairwise relatedness between pup and adult pairs.
    - Escorts directed toward each pup by fed vs non-fed mothers (pup-focused data with feeding rate, neighbor proximity metrics, obs).
    - Pup weights (weight, age in days, category, sex, helper.ratio).
    - Within-litter variance relative to full variance (age.cat, litter.cat, relative.variance).
    - Escorting received by pups (category, esc.index, esc.freq, helper.ratio).
    - Rate of escort-feeding to focal pup (focal.id, category, feeds.rate, nn.str, obs).
    - Pup survival datasets: survival indicators to 90, 180, and 365 days, with corresponding end ages and sex.

- Data governance implications for data leaders:
  - Showcase of end-to-end data lifecycle: from field collection (apps, devices, protocols) through centralized storage (MS Access) to multi-antecedent analyses.
  - Emphasis on metadata richness (treatment categories T/C/R, breeding attempt IDs, litter IDs, group/pack IDs) to enable reproducibility and cross-dataset joins.
  - Design includes deliberate controls and replication (unmanipulated litter controls between manipulations) to support causal inference.
  - Quality assurance integrated into data collection workflow and analytic pipelines to minimize errors and ensure data integrity.

- Relevance to data strategy:
  - Demonstrates the need for discoverable, well-documented data assets across a multi-year, multi-site study.
  - Highlights the importance of clear data standards (naming conventions, categorical codes, and time-based measures) to enable collaboration and data sharing within a wider research community.