# DGRP_traits.csv

## Aims
- Measure the phenotypic variance in locomotor activity, mortality, and pathogen shedding in a panel of Drosophila melanogaster lines infected with Pseudomonas aeruginosa
- Estimate broad-sense heritability for each trait
- Estimate genetic covariances between each pair of traits

## Experimental design and sampling regime
- 60 lines from the Drosophila Genetic Reference Panel (DGRP)
- Flies exposed to orally acquired infection of Pseudomonas aeruginosa
- For each line and sex: 6–10 replicates
- 5 experimental blocks
- Total of approximately 707 samples
- Data collected as individual flies, with measurements tracked until death or end of experiment

## Data collection and measurement methods
- Pathogen shedding: individual flies placed in sterile tubes; quantify viable P. aeruginosa CFUs shed over 24 h post-infection
- CFU plating: using Pseudomonas-selective media (PIM) to count CFUs
- Locomotor activity: flies placed in Drosophila Activity Monitors (DAM); total activity events recorded at 1-minute resolution until death
- Mortality: recorded as the last detected movement
- Timing: June–October 2023 for analysis
- Instrumentation: DAM5 (Trikinetics); climate-controlled incubator at 25°C, 12 h light:12 h dark cycle (7 AM–7 PM)

## Calibration and quality control
- Control tubes without flies included to calibrate zero activity
- Data inspected for obvious outliers; values within expected ranges
- No activity recorded in DAM tubes containing no fly

## Data structure and units (Nature and units of recorded values)
- Dataset file: DGRP_traits.csv (18 columns)
- Columns and key definitions:
  - Genotype: unique DGRP line name (RAL-nnn)
  - Sex: M = Male; F = Female
  - Block: experimental block (1–5)
  - Replicate: replicate number (1–6) for each genotype/sex combination
  - Well: position on 96-well plate
  - Plate: unique 96-well plate identifier
  - Dilution: dilution factor to reach countable CFUs (e.g., 1 = no dilution; 10 = 10-fold)
  - CFU_5ul: CFUs counted in the diluted sample
  - CFUshed: estimated CFUs shed per fly, accounting for dilution and sampled volume
  - Monitor: DAM monitor identifier (12–18)
  - Channel: DAM channel within each monitor (1–32)
  - Movements: total movements recorded during the experiment
  - Activity_bouts: total number of 1-min intervals with activity > 1
  - Lifespan_mins: total minutes until last movement
  - Alive: whether the fly lived or died during the experiment
  - Proportion_active: Activity_bouts / Lifespan_mins
  - Censor: survival analysis censoring (0 = alive; 1 = dead)
  - Movements_per_min: average movements per minute

## Analytical methods
- Values are either recorded directly or calculated in R
- Quality control and basic analyses performed with standard statistical approaches in R

## References (context and background)
- Mackay TFC et al. 2012: The Drosophila melanogaster Genetic Reference Panel
- Siva-Jothy et al. 2018: Oral Bacterial Infection and Shedding in Drosophila melanogaster
- Pfeiffenberger et al. 2010: Locomotor Activity Monitoring Using DAM System
- Anderson et al. 2022: Mitochondrial DNA effects on activity and sleep in Drosophila
- Kutzer et al. 2024: Mitochondrial background and costs of immune deployment

## Opportunities and considerations for data analysts
- Useful for estimating heritability and genetic covariances across multiple traits
- Enables exploration of relationships between infection shedding, locomotor activity, and lifespan
- Can be integrated with other DGRP datasets for broader genotype-phenotype analyses
- Metadata and provenance are clear (experimental design, instrumentation, and calibration steps), aiding reproducibility
- Consider local or block effects due to the 5-block design when modeling
- Data scale and structure (multi-trait, multi-factor) may require mixed-effect models and survival analyses
- Potential limitations to note: dilution and plating steps introduce measurement nuance; censoring variable (Censor) and alive/dead status influence survival modeling
- Data could be shared to data portals with accompanying metadata to improve discoverability and reuse