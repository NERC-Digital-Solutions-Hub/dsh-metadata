# README.doc for:
Movement metrics of singing and silent Hawaiian field crickets (Teleogryllus oceanicus) in a semi-natural arena.

## Purpose and scope
- Document describes movement metrics collected from tracking multiple groups of crickets during three-hour trials.
- Results published in a related paper: Behavioural plasticity compensates for adaptive loss of cricket song (doi: 10.1111/ele.14404).
- Cricket locations were derived from overhead camera images; movement metrics calculated in MATLAB and compiled into this file.

## Experimental design and sampling regime
- Tracking conducted between 20 March and 5 April 2017.
- Eight crickets per trial: four females and four males.
- Treatments: Silent (flatwing morphs; males mute) and Singing (normal-wing morphs; males can sing).
- Each day a single trial; Silent and Singing treatments alternated.
- Arena setup: crickets released from four boxes near corners (controlled by a ceiling pulley system); habituation 5 minutes, then 5 more minutes before triggering cameras.
- Trial duration: 3 hours.
- Trials total: 16 (8 Silent, 8 Singing) initially; after quality control, 7 Silent and 6 Singing trials remained.
- Post-trial: females laid eggs; hatchlings counted.

## Nature and units of recorded values
- Sex: M (male) or F (female).
- Trial: trial number; eight crickets tracked per trial for 3 hours.
- Treatment: fw (flatwing) or n (normal wing).
- Weight: body weight in milligrams.
- Offspring: for females, number of hatchlings counted after the trial.
- Mated: binary indicator whether the female produced any offspring.
- TotalDistance: cumulative distance travelled; units given in pixels moved (convert to meters by dividing by 4000).
- MinsStill: minutes spent stationary.
- MinsSocial: minutes spent within 15 cm of another cricket.
- OtherSexPropVar: proportional variation in time spent with crickets of the opposite sex.
- ID: individual cricket tag ID.
- Age: age in days.

## Data quality control
- Trials omitted if a tag was lost or a camera malfunction occurred.
- This resulted in three trials being removed, leaving seven Silent and six Singing trials.
- Data are structured so each row represents metrics for a single tracked individual within a given trial and treatment.

## Data structure and data handling
- Data are organized with metrics for each tracked cricket per row.
- Each row includes trial ID and treatment, enabling linkage across measurements and experimental conditions.
- The dataset provides a comprehensive set of behavioral and life-history variables (e.g., weight, offspring, mating, movement, social interactions) suitable for monitoring-style analyses and cross-study comparability with clear unit definitions and transformation notes.