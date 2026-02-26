# Movement metrics of singing and silent Hawaiian field crickets (Teleogryllus oceanicus) in a semi-natural arena.

- Purpose of the dataset: Tracking movement metrics of multiple groups of crickets to understand behavioral responses under different wing morphs (singing vs. silent) in a semi-natural arena; results relate to a broader study on behavioural plasticity and song loss.

## Data collection and generation

- Source: Overhead camera array captured cricket positions; movement metrics calculated in MATLAB; compiled in this file.
- Timeframe: Experiments conducted from 20 March to 5 April 2017.
- Subjects: 8 crickets per trial (4 females, 4 males).
- Treatments: Silent (flatwing morph males, non-singing) and Singing (normal-wing morph males, capable of singing).
- Setup: Crickets released from four boxes near arena corners; a 5-minute habituation, 5-minute pre-trigger period, then 3-hour trial per day.
- Trials: 16 trials total, alternating Silent and Singing; quality-controlled to remove trials with tag loss or camera failure.

## Experimental design and sampling regime

- Release protocol: Two crickets of the same sex under each of four release boxes; timing coordinated by ceiling pulley system.
- Observation window: 3 hours of continuous tracking per trial, starting at 08:00 AM to align with sunset cycle.
- Post-trial procedure: Females laid eggs; hatchlings counted after trials.
- Replication: 16 trials originally; after quality control, 7 Silent and 6 Singing trials remained.

## Variables recorded (Nature and units)

- Identity and basics:
  - ID: individual cricket tag identifier.
  - Sex: M or F.
  - Age: days old.
  - Weight: milligrams.
- Experimental metadata:
  - Trial: trial number.
  - Treatment: fw (flatwing) or n (normal wing).
- Movement and social metrics:
  - TotalDistance: cumulative distance moved (pixels). Convert to meters by dividing by 4000.
  - MinsStill: minutes spent stationary.
  - MinsSocial: minutes spent within 15 cm of another cricket.
  - OtherSexPropVar: proportional variation in time spent with crickets of the opposite sex.
- Reproductive outcomes (females only):
  - Offspring: number of hatchlings counted after the trial.
  - Mated: binary indicator if the female produced any offspring.

## Data processing and units

- Movement calculations performed in MATLAB; raw outputs collated in the dataset.
- Distance conversion note: TotalDistance in pixels; convert to meters by dividing by 4000.
- Data rows correspond to metrics for each tracked individual per trial, with trial ID and treatment recorded.

## Quality control and data cleaning

- Exclusions: Trials where a tag was lost or a camera malfunction occurred were omitted.
- Impact: From 16 initial trials, three were removed, leaving 7 Silent and 6 Singing trials.

## Data structure and accessibility

- Structure: Each row represents metrics for an individual cricket, including trial ID and treatment.
- Data lineage: Collected from a published study, with methods and results reported in the associated paper “Behavioural plasticity compensates for adaptive loss of cricket song” (DOI provided).
- Dataset provenance: Derived from a controlled, semi-natural arena experiment, designed to compare movement and social behaviors between silent and singing male morphs.

## Relevance for environmental monitoring and policy analysis

- Standardized outputs: Provides clear, comparable movement and social metrics across time and treatment, suitable for long-term environmental monitoring and policy evaluation.
- Data transparency: Includes explicit data provenance, units, and a quality-control log, enabling reuse and verification.
- Interoperability: Metrics are defined and documented (with unit conversions), facilitating integration with other environmental datasets (e.g., habitat disturbance, population dynamics, or behavioral responses to environmental change).
- Data accessibility goals: Highlights the importance of making underlying data available to others, aligning with best practices for environmental data sharing and reuse.