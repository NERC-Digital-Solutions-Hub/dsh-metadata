# Movement metrics of singing and silent Hawaiian field crickets (Teleogryllus oceanicus) in a semi-natural arena

## Study and data purpose
- Tracking data from multiple cricket groups during a 3-hour period, to study movement patterns under different male song phenotypes.
- Findings published in Behavioral Ecology and Sociobiology; DOI provided in the documentation.
- Movement metrics were extracted from overhead camera images and calculated in MATLAB, then compiled into this dataset.

## Experimental design and sampling
- Timeframe: tracking experiments conducted between 20 March and 5 April 2017.
- Subjects per trial: eight crickets (4 females, 4 males).
- Treatments (two conditions):
  - Silent: four male flatwing morphs (non-singing).
  - Singing: four male normal-wing morphs (capable of singing).
- Procedure per trial:
  - Crickets placed under one of four release boxes near arena corners, two of each sex per box.
  - Habituation: 5 minutes in low light; camera trigger starts after a further 5 minutes.
  - Boxes raised simultaneously; 3-hour trial.
- Experimental replication: 16 trials in total, evenly split across treatments; trials alternated between Silent and Singing.
- Post-trial: females laid eggs; hatchlings counted.

## Recorded data and units
- Sex: M (male) or F (female).
- Trial: numerical identifier for the trial.
- Treatment: fw (flatwing) or n (normal wing).
- Weight: cricket weight in milligrams.
- Offspring: for females, number of hatchlings counted after the trial.
- Mated: binary indicator if the female produced any offspring.
- Movement metrics (per individual per row):
  - TotalDistance: cumulative distance travelled, in pixels. Convert to meters by dividing by 4000.
  - MinsStill: minutes spent stationary.
  - MinsSocial: minutes spent within 15 cm of other crickets.
  - OtherSexPropVar: proportional variation in time spent with crickets of the opposite sex.
- ID: individual cricket tag ID.
- Age: age of the cricket in days.

## Data quality and exclusions
- Quality control: trials with tag loss or camera malfunction were omitted.
- Resulting dataset after QC: 7 Silent trials and 6 Singing trials (i.e., 3 trials removed from the original 16).

## Data structure and accessibility
- Data are structured with metrics for each individual cricket per row.
- Each row includes trial ID and treatment; hence cross-trial comparisons are straightforward.
- Age, weight, and identity (ID) allow linking movement metrics to biological characteristics and treatment groups.

## Potential analyses and considerations for analysts
- Compare movement metrics (TotalDistance, MinsStill, MinsSocial) between Silent (flatwing) and Singing (normal-wing) treatments.
- Assess effect of wing phenotype on social interactions (MinsSocial, OtherSexPropVar) and proximity dynamics (within-15 cm measure).
- Explore relationships between movement profiles and reproductive outcomes (Offspring, Mated) for females.
- Investigate how age, weight, and trial-level factors influence movement and social behavior.
- Data preparation steps: convert TotalDistance to meters; ensure consistent time frames; handle any residual missing values from QC exclusions.
- Note on data scope: three-hour single-trial window per cricket; interpretation should consider temporal constraints and potential diurnal alignment with sunset cycle.