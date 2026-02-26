# Overview

- Experimental data collected at the Institute of Ecology and Evolution, University of Edinburgh, Jan–Oct 2023.
- Purpose: measure phenotypic variance in locomotor activity, mortality, and pathogen shedding in a panel of Drosophila melanogaster lines when infected with Pseudomonas aeruginosa; estimate broad-sense heritability for each trait and genetic covariances between trait pairs.
- Collected by Megan Kutzer (PDRA in Pedro Vale's lab).

## Experimental Design / Sampling Regime

- 60 DGRP lines exposed to oral infection with Pseudomonas aeruginosa.
- 6–10 replicate flies per line and sex; 5–10 replicates per treatment (707 samples total).
- Experiment conducted across 5 blocks with variable replication per block.

## Data Collection / Generation Methods

- Pathogen shedding: individual fly placed in a sterile tube; colony-forming units (CFUs) defecated over 24 hours quantified after plating on PIM medium.
- Locomotor activity: after infection, each fly placed in a Drosophila Activity Monitor (DAM); total activity events recorded at 1-minute resolution until death or experiment end.
- Mortality: determined from last detected movement in the DAM.
- Data analysis window: June–October 2023.

## Laboratory Instrumentation / Environment

- Drosophila Activity Monitor (DAM5, Trikinetics) used for activity data.
- Flies housed in climate-controlled incubator at 25°C, 12:12 light:dark cycle (7:00–19:00).
- Calibration: control tubes with no flies used to calibrate for zero activity.

## Calibration Steps and Values

- Included empty control tubes in the DAM setup to establish zero-activity baseline.

## Nature and Units of Recorded Values

- One CSV file: DGRP_traits.csv with 18 columns:
  - Genotype: DGRP line name (RAL-nnn)
  - Sex: M or F
  - Block: 1–5
  - Replicate: 1–6 within genotype/sex
  - Well: position on 96-well plate
  - Plate: plate identifier
  - Dilution: CFU dilution factor (e.g., 1 = no dilution; 10 = 10-fold)
  - CFU_5ul: CFUs counted in the diluted sample
  - CFUshed: estimated CFUs shed per fly, accounting for dilution and sampled volume
  - Monitor: DAM monitor identifier
  - Channel: DAM channel (1–32)
  - Movements: total movements recorded
  - Activity_bouts: total 1-minute intervals with activity
  - Lifespan_mins: minutes from start to last movement
  - Alive: alive or dead at end
  - Proportion_active: Activity_bouts / Lifespan_mins
  - Censor: survival analysis censoring (0 = alive, 1 = dead)
  - Movements_per_min: average movements per minute

## Analytical Methods

- Reported values are either raw measurements or simple arithmetic-derived values calculated in R.

## Quality Control

- Raw data screened for obvious outliers; values fell within expected ranges.
- No activity detected in DAM tubes without flies.

## Data Governance and Documentation

- The dataset is documented with a clear data dictionary embedded in the description, detailing each column and its meaning.
- File naming: DGRP_traits.csv; dataset structure aligned with along-line and sex/block replication design.
- Metadata supports secondary use, including experimental design, instrumentation, calibration, and data processing steps.

## Reuse Considerations

- Structure reflects a balanced design across 60 lines and 5 blocks, enabling estimation of heritability and genetic covariances; account for block and replicate factors in analyses.
- Derived metrics (e.g., Proportion_active) rely on Lifespan_mins and Activity_bouts; interpretations should consider censoring (Censor) in survival analyses.

## References

- Mackay TFC et al. 2012. The Drosophila melanogaster Genetic Reference Panel. Nature.
- Siva-Jothy JA et al. 2018. Oral Bacterial Infection and Shedding in Drosophila melanogaster. JoVE.
- Pfeiffenberger C et al. 2010. Locomotor Activity Level Monitoring Using the Drosophila Activity Monitoring (DAM) System. Cold Spring Harbor Protoc.
- Anderson L et al. 2022. Variation in mitochondrial DNA affects locomotor activity and sleep in Drosophila melanogaster. Heredity.
- Kutzer MAM et al. 2024. Mitochondrial background can explain variable costs of immune deployment. Journal of Evolutionary Biology.