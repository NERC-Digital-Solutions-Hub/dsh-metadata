# Overview

- Purpose: Experimental data to measure phenotypic variance in locomotor activity, mortality, and pathogen shedding across Drosophila melanogaster lines infected with Pseudomonas aeruginosa, to estimate broad-sense heritability and genetic covariances between traits.
- Organism and pathogen: Drosophila melanogaster; oral infection with Pseudomonas aeruginosa.
- Source: Institute of Ecology and Evolution, University of Edinburgh; data collected by Megan Kutzer (PDRA in Pedro Vale's lab).

- Experimental design and sampling
  - 60 lines from the Drosophila Genetic Reference Panel (DGRP).
  - For each line and sex: 6–10 replicates, total treatment replicates 5–10; approx. 707 samples.
  - Experimental setup split into 5 blocks with variable replicates per block.

- Data collection and measurements
  - Pathogen shedding: quantify viable P. aeruginosa CFUs shed per fly over 24 hours post-infection, via plating on Pseudomonas-selective media; CFU counts translated through dilution factors to total shed per fly.
  - Locomotor activity: monitored with Drosophila Activity Monitor (DAM) at 1-minute resolution until death or end of experiment; total activity events recorded per fly.
  - Mortality: recorded as last detected movement in DAM.
  - Observational window: extensive recording (roughly 2,500 to 20,000 minutes per fly).

- Laboratory setup and calibration
  - Equipment: DAM5 monitors (Trikinetics).
  - Environmental conditions: climate-controlled incubator at 25°C, 12 h light:12 h dark cycle.
  - Calibration: empty control tubes used to calibrate zero-activity readings.

- Data structure and variables
  - Primary data file: DGRP_traits.csv with 18 columns.
  - Columns (highlights): Genotype (RAL-nnn), Sex (M/F), Block (1–5), Replicate (1–6), Well, Plate, Dilution, CFU_5ul, CFUshed, Monitor, Channel, Movements, Activity_bouts, Lifespan_mins, Alive, Proportion_active, Censor, Movements_per_min.

- Data processing and analysis
  - Raw values are either as recorded or computed via simple arithmetic.
  - Analyses conducted in R; values and derived metrics documented via the described columns.

- Quality control
  - Raw data inspected for outliers; values within expected ranges.
  - Negative/zero activity checks confirmed via empty DAM tubes (no activity detected).

- References and context
  - Related methodology and background literature on the DGRP panel and infection shedding, locomotor activity, and previous work cited (five references provided).

- Relevance to monitoring frameworks (archetype perspective)
  - Demonstrates end-to-end data lifecycle: rigorous experimental design, standardized data collection, explicit metadata (18-column schema), and explicit QA procedures.
  - Emphasizes data provenance and traceability (line/genotype identifiers, replicates, plate/well tracking).
  - Facilitates data sharing and reuse through structured metadata and documentation, while noting the need for appropriate data governance and open sharing considerations.
  - Provides a concrete example of integrating multiple phenotypic traits (behavioral, survival, and pathogen shedding) in a single monitoring dataset, suitable for assessing trait heritability and covariances across genotypes.