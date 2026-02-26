# OVERVIEW

- Purpose: Test which traits are used by generalist avian predators (chicks) to discriminate among prey, focusing on distinguishing stinging hymenoptera from mimics.
- Approach: Train chicks to forage from lidded dishes in a lab, introduce artificial insect-like stimuli, and assess responses to stimuli that mix fly-like and wasp-like traits (shape, pattern, colour, size).
- Hypothesis: Some traits will influence chick behavior more strongly than others.

## Data collection and generation

- Observations: Chick behavior recorded in real time and via video for timing data.
- Data outputs: Five CSV files capturing growth, behavior, learning, and testing phases.
- Subjects: 74 domestic chicks (Gallus gallus domesticus) across two batches; 8 chicks per batch acted as “buddies.”

## Data quality control

- Validation: Summary data checked against valid codes and plausible value ranges.
- Missing data: Patterns examined to ensure missing values are genuine and not transcription errors.

## Data structure (files and contents)

- trait_exp_chick_weights.csv
  - Weight data: growth measurements for 74 chicks (1387 rows, 3 columns for weight: id, date, weight).
  - Trial data: 12 columns per row detailing trial context (date, grouping, chick IDs, experimenter, buddy IDs, food deprivation start, start time, duration, mealworms left, notes, etc.).
- trait_exp_group_phase.csv
  - 210 rows, 12 columns: chick behavior during initial grouped trials on Day 1.
- trait_exp_training_phase.csv
  - 5024 rows, 12 columns: chick behavior during training to open lids (learning to access mealworms).
- trait_exp_learning_phase.csv
  - 6704 rows, 12 columns: chick behavior during the discrimination learning period (fly vs wasp).
- trait_exp_test_phase.csv
  - 1938 rows, 12 columns: chick behavior during testing with novel trait combinations (latency to approach, etc.).

## Experimental subjects and setting

- Subjects: 74 domestic chicks, two batches, with 8 buddy chicks per batch.
- Arena: 140 x 70 x 40 cm with a 25 x 70 x 40 cm buddy area to allow visual/auditory contact between experimental and buddy chicks; buddies rotated to ensure short exposure.

## Stimuli and materials

- Artificial prey: 3D-printed insect models atop lids; models derived from real insects via 3D scanning and morphing.
- Stimulus types: Fly (non-mimetic) and Wasp (non-reward or reward conditions), plus probe stimuli that are intermediate fly-wasp combinations.
- Trait manipulation: Stimuli combine fly-like and wasp-like traits across shape, pattern, colour, and size.

## Experimental design and procedures

- Initial training
  - Day 1: six two-minute foraging sessions; groups of three, then pairs, then individuals.
  - Procedure: 8 lid-covered/undercovered dishes with mealworms; progressively obscured lids; if a mealworm is eaten, trial ends.
  - Objective: habituate to equipment and learn to access prey by removing lids.
- Learning phase
  - Daily trials: one trial with 16 presentations; one trial per day, until the chick chooses the fly-lid stimulus on ≥80% of presentations (up to ~11 days).
  - Method: two dishes per presentation; one with a fly model and a mealworm (reward), the other with a wasp model and no reward.
  - Side-bias mitigation: dish positions varied randomly along four possible positions (1–4) to discourage left/right preferences.
- Test phase
  - After learning: up to four daily trials; each chick receives 6 fly-reward trials, 6 non-reward wasp trials, and 4 probe trials with novel intermediate stimuli.
  - Probes: 30 possible novel insect stimuli combining fly and wasp traits; each has a mealworm reward but is novel.
  - Measurements: latency to approach and to remove the lid (time to first peck; time to open).

## Key variables and measurements

- Latency and timing
  - time_manual: latency from release to first peck (in situ; stopwatch).
  - time_video: latency from video (0.3x speed; typically more accurate).
  - time_to_open: time from release to lid opening when the dish is opened.
- Behavioral and outcome metrics
  - MW_eaten: whether a mealworm was eaten (Y/N).
  - dish_fly/dish_wasp: positions of stimuli dishes; dish indices reflect stimuli in each presentation.
  - lid_opened: which dish lid the chick opened.
  - dishA/dishB/dish_fly: positional data for stimuli and their associated meals.
  - mealworm presence and dish status across trials.
- Experimental context
  - id, date, grouping, experimenter, batch, buddies, food_dep_start, start_time, duration, notes.
  - dish position and stimulus code (model: TF = fly, VV = wasp, VVP = mimic with reward; and other codes indicating specific trait combinations with 0–5 mimicry levels for each trait).
- Data maturation
  - Three layers of phases (training, learning, test) plus growth data to enable longitudinal analyses.

## Temporal and procedural details

- Training progression: from basic lid-opening to increasingly obscured prey and standardized trials across days.
- Learning progression: until discrimination performance meets threshold (80%).
- Test progression: uses both reinforced and probe stimuli to assess generalization and mimicry detection.

## Relevance for environmental monitoring analysts

- Data richness: standardized, multi-phase behavioral data with precise timing and trait-level stimulus coding, enabling temporal trend analysis and cross-study comparisons.
- Predator-prey insights: illuminates how specific trait cues influence predator discrimination and potential responses to mimicry in natural systems.
- Data interoperability: detailed metadata (dates, experimenters, batch, buddy design) supports integration with environmental monitoring datasets and reproducibility.
- Practical applications: informs models of predation risk and prey-polymorphism dynamics in ecological monitoring, as well as the design of experiments to test cue-based predator responses under controlled conditions.

## Limitations and considerations

- Laboratory context: behavior under controlled stimuli may differ from natural field conditions.
- Artificial stimuli: reliance on 3D-printed models; generalization to real-world insects should consider potential differences in perception.