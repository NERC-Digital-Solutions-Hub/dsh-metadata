# README.doc for:
Movement metrics of singing and silent Hawaiian field crickets (Teleogryllus oceanicus) in a semi-natural arena.

## What this dataset contains
- Tracking data from multiple cricket groups over a 3-hour period, with movement metrics calculated in MATLAB and collated in this file.
- Context and provenance linked to the publication: Behavioural plasticity compensates for adaptive loss of cricket song (DOI: 10.1111/ele.14404).

## Experimental design and sampling
- Timeframe: 20 March – 5 April 2017; daily trials with 08:00 start, aligned to time-of-sunset under a photo-reversed cycle.
- Setup: Eight crickets per trial (4 females, 4 males).
- Treatments: Silent (fw/flatwing morphs) vs Singing (n/normal-wing morphs).
- Procedure: Crickets placed under four release boxes, habituation 5 minutes, then boxes raised; 3-hour trials.
- Replication: 16 trials total (8 Silent, 8 Singing) before quality control; after QC, 7 Silent and 6 Singing trials remained.

## Data fields and units
- Sex: M or F
- Trial: trial identifier
- Treatment: fw (flatwing) or n (normal wing)
- Weight: milligrams
- Offspring: hatchlings count for females after trial
- Mated: binary (whether female produced offspring)
- TotalDistance: total distance moved (pixels); convert to meters by dividing by 4000
- MinsStill: minutes stationary
- MinsSocial: minutes within 15 cm of other crickets
- OtherSexPropVar: proportional variation in time spent with crickets of the opposite sex
- ID: individual cricket tag ID
- Age: age in days

## Quality control and data completeness
- Trials omitted if tag lost or camera malfunction occurred.
- Result: three trials removed; final dataset includes 7 Silent and 6 Singing trials.

## Data structure and provenance
- Data are structured with metrics for each individual cricket per row; each row includes trial ID and treatment.
- Generated from tracking data (overhead camera array) and movement metrics calculated in MATLAB, then collated in this file.
- Linked publication provides full experimental context and analysis.