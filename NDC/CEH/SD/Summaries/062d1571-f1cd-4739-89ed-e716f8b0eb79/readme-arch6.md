# Movement metrics of singing and silent Hawaiian field crickets (Teleogryllus oceanicus) in a semi-natural arena.

## Overview
- Data track movement metrics from multiple cricket groups over a 3-hour period per trial.
- Tracking used overhead camera arrays; movement metrics calculated in MATLAB and compiled in this README.
- Experimental results published in Behavioural Ecology: Behavioral plasticity compensates for adaptive loss of cricket song. DOI: https://doi.org/10.1111/ele.14404

## Experimental design and data collection
- Eight crickets per trial: four females and four males.
- Treatments: Silent (fw = flatwing morphs) and Singing (n = normal-wing morphs capable of singing); trials alternate between treatments.
- Timing: Trials run daily from 08:00, aligning with time-of-sunset; habitat in low light with release boxes controlled from the ceiling.
- Procedure: Habituation (5 minutes), trigger camera, release boxes raised, 3-hour tracking period.
- Post-trial: Females lay eggs; hatchlings counted.

## Recorded values and units
- Sex: M (male) or F (female).
- Trial: trial number; eight crickets tracked for 3 hours per trial.
- Treatment: fw (flatwing) or n (normal wing).
- Weight: cricket mass in milligrams.
- Offspring: number of hatchlings produced by each female after the trial.
- Mated: binary indicator if the female produced any offspring.
- TotalDistance: cumulative distance traveled in pixels; convert to meters by dividing by 4000.
- MinsStill: minutes spent stationary.
- MinsSocial: minutes spent within 15 cm of other crickets.
- OtherSexPropVar: proportional variation in time spent with crickets of the opposite sex.
- ID: individual tag ID.
- Age: age in days.

## Data structure
- Metrics are recorded per individual cricket per row.
- Each row includes trial ID and treatment.

## Quality control
- Trials discarded if a tag was lost or a camera malfunction occurred.
- Three trials removed due to issues; remaining data: seven Silent trials and six Singing trials.

## Usage notes and considerations
- TotalDistance should be converted to meters via dividing by 4000.
- Female reproductive output (Offspring, Mated) can be linked to movement/interaction metrics.
- The dataset is structured to enable self-contained per-cricket analyses within a trial and comparisons across treatments (Silent vs Singing).