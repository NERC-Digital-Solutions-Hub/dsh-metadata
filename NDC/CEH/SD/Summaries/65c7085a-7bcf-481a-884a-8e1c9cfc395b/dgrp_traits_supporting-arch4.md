# Overview

- This resource contains experimental data collected at the Institute of Ecology and Evolution, University of Edinburgh from January to October 2023.
- Purpose: to measure phenotypic variance in locomotor activity, mortality, and pathogen shedding in a panel of Drosophila melanogaster lines after infection with the bacterial pathogen Pseudomonas aeruginosa, aiming to estimate broad-sense heritability and genetic covariances between traits.
- Principal investigator/work: Megan Kutzer (PDRA) in Pedro Vale's lab.

## Experimental design

- Population: 60 lines from the Drosophila Genetic Reference Panel (DGRP).
- Infection: Orally acquired infection with Pseudomonas aeruginosa.
- Replication: 6–10 replicates per line and sex, with 5–10 treatment replicates, totaling 707 samples.
- Structure: Experiment conducted across 5 blocks with variable replicate counts per block.

## Data collection and instruments

- Pathogen shedding: After infection, individual flies were placed in sterile tubes to quantify viable P. aeruginosa colony-forming units (CFUs) shed over 24 hours. CFUs were measured on Pseudomonas-selective media (PIM).
- Locomotor activity: Individual flies were placed in a Drosophila Activity Monitor (DAM) to record activity events at 1-minute resolution until death or end of experiment.
- Mortality: Recorded as the last movement detected in the DAM.
- Environment: Flies maintained at 25°C with a 12h light:12h dark cycle.
- Calibration: Controls (empty tubes) used to calibrate zero-activity readings.

## Data structure and variables

- Data file: DGRP_traits.csv
- Key columns (18 total) include:
  - Genotype (RAL-nnn)
  - Sex (M or F)
  - Block (1–5)
  - Replicate (1–6)
  - Well, Plate, Dilution, CFU_5ul, CFUshed
  - Monitor (DAM unit), Channel (1–32)
  - Movements, Activity_bouts
  - Lifespan_mins, Alive, Proportion_active
  - Censor (survival analysis status; 0 alive, 1 dead)
  - Movements_per_min
- Derived/summary metrics:
  - CFUshed accounts for dilution and sampled volume to estimate shedding per fly
  - Proportion_active = Activity_bouts / Lifespan_mins
- Data processing: Values are either recorded directly or calculated with simple arithmetic in R.

## Processing and analysis

- Analytical approach: All reported values are either as recorded or calculated via simple arithmetic in R.
- Quality checks: Raw data inspected for obvious outliers; no activity detected in DAM tubes without flies; all values within expected ranges.

## Quality control and data integrity

- Equipment calibration: Included zero-activity controls (empty DAM tubes).
- Data validation: Outliers checked; DAM readings validated against expected ranges; no spurious activity detected in empty controls.

## Data access and provenance

- Data collection period: June–October 2023 for data analysis steps.
- Instrumentation and environment details provided to support reproducibility and data discoverability.
- References supporting methods and context are provided, including foundational work on the DGRP resource and the DAM system.

## References

- Mackay TFC et al. 2012. The Drosophila melanogaster Genetic Reference Panel. Nature.
- Siva-Jothy et al. 2018. Oral Bacterial Infection and Shedding in Drosophila melanogaster. JoVE.
- Pfeiffenberger et al. 2010. Locomotor Activity Level Monitoring Using the Drosophila Activity Monitoring (DAM) System. Cold Spring Harbor Protocols.
- Anderson et al. 2022. Variation in mitochondrial DNA affects locomotor activity and sleep in Drosophila melanogaster. Heredity.
- Kutzer et al. 2024. Mitochondrial background can explain variable costs of immune deployment. Journal of Evolutionary Biology.