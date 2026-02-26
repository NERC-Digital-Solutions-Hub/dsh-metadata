# Overview

- Purpose and aim
  - Experimental resource to measure phenotypic variance in locomotor activity, mortality, and pathogen shedding in Drosophila melanogaster lines infected with Pseudomonas aeruginosa.
  - Objective to estimate broad-sense heritability for each trait and genetic covariances between trait pairs.

- Experimental design
  - 60 lines from the Drosophila Genetic Reference Panel (DGRP).
  - Each line and sex exposed to oral P. aeruginosa infection.
  - 6–10 replicates per line per sex; 707 total samples.
  - 5 experimental blocks with varying replicates.
  - Infections conducted overnight; outcomes tracked over time.

- Data collection and key variables
  - Pathogen shedding
    - CFU plating on Pseudomonas-selective media; measurements per fly.
    - Columns related: Plate, Dilution, CFU_5ul, CFUshed.
  - Locomotor activity
    - Drosophila Activity Monitor (DAM) recorded events with 1-minute resolution.
    - Columns related: Movements, Activity_bouts, Lifespan_mins, Proportion_active, Movements_per_min.
  - Mortality
    - Recorded as last detected movement; Censor variable for survival analysis (0 alive, 1 dead).
  - Metadata and identifiers
    - Genotype, Sex (M/F), Block (1–5), Replicate (1–6), Well, Plate, Monitor, Channel.
  - Data format and scope
    - One CSV file: DGRP_traits.csv with 18 columns total.

- Data processing and analysis
  - Values are either raw observations or derived via simple arithmetic (e.g., deriving CFUshed from CFU counts and dilution).
  - Analyses performed in R.
  - Calibration and quality checks included (e.g., zero activity in empty DAM tubes).

- Laboratory instrumentation and conditions
  - DAM5 activity monitors (Trikinetics).
  - Incubation at 25°C, 12 h light:12 h dark cycle.
  - Calibration using empty tubes to establish zero activity.

- Units and data interpretation
  - CFU counts and derived shedding estimates represent viable bacteria per fly.
  - Activity metrics include total movements, activity bouts, and activity proportion over lifespan.
  - Lifespan_mins represents total minutes until last movement or end of experiment.

- Quality control
  - Raw data screened for obvious outliers; values within expected ranges.
  - Validation that empty DAM tubes show no activity.

- Access and reference
  - Dataset file: DGRP_traits.csv (18 columns).
  - Key references supporting methods and context are provided in the documentation.

- Practical data-use notes for data support role
  - The dataset enables cross-line and cross-sex comparisons of heritable components for three trait categories (behavior, survival, and bacterial shedding).
  - Suitable for creating dashboards or self-serve reports showing per-line summaries, distribution of traits, and correlations among traits and genotypes.
  - Potential to link this phenotype dataset with genotype data for meta-analyses of genetic correlations and heritability across traits.