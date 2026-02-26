# OVERVIEW: This experiment aimed to test which traits are used by generalist avian predators (chicks) to discriminate among prey items, in particular to distinguish stinging hymenoptera from their mimics.

## Purpose and design summary
- Investigates which trait cues (shape, pattern, colour, size) most influence chick foraging decisions when distinguishing fly-like prey from wasp-like prey.
- Experimental progression: initial training to open lids for mealworms, learning phase to discriminate fly vs wasp stimuli, and a test phase with novel, intermediate stimuli to probe generalization.
- Stimuli-based decisions measured via approach latency and lid-opening behavior, with reward contingencies guiding learning in the training and learning phases.

## Data files and structure
- Five CSV data files capturing different aspects of the experiment:
  - trait_exp_chick_weights.csv: chick growth/weight data across 1387 measurements (plus 3 core fields: id, date, weight).
  - trait_exp_group_phase.csv: behavior during initial grouped trials (210 rows, 12 columns).
  - trait_exp_training_phase.csv: training period behavior (5024 rows, 12 columns).
  - trait_exp_learning_phase.csv: learning period behavior (6704 rows, 12 columns).
  - trait_exp_test_phase.csv: testing period behavior with novel stimuli (1938 rows, 12 columns).
- For all datasets, key identifiers link data to individual chicks and trials (e.g., id, date, experimenter), with detailed trial-level fields describing timing, stimuli, dish positions, rewards, and outcomes.

## Data collection and quality control
- Data collected in real time during laboratory sessions and supplemented with video recordings (timing data emphasized).
- Quality control includes:
  - Validation of codes and plausible value ranges.
  - Examination of missing data patterns to distinguish genuine missingness from transcription errors.

## Experimental subjects and setup
- Subjects: 74 domestic chicks (Gallus gallus domesticus) from two batches, with 8 chicks per batch acting as “buddies.”
- Experimental arena: 140 x 70 x 40 cm with a separate buddy area (25 x 70 x 40 cm) to allow visibility and sound exposure between experimental chicks and buddies.
- Buddies: Rotated regularly to prevent prolonged exposure in the buddy area.

## Stimuli and artificial prey
- Prey access via lids on petri dishes containing mealworms; lids are plain during training and bear life-sized 3D-printed insect models during learning and testing.
- Stimuli:
  - Fly (TF) and Wasp (VV) models, with a probe condition (VVP) mirroring a perfect mimic but with rewards as appropriate.
  - Feature-based stimuli combinations (S shape, P pattern, C colour, Z size) with degrees of mimicry; 0 = fly-like, 5 = intermediate between fly and wasp; remaining codes indicate wasp-like traits.
- Mealworms are the reward, with latencies and whether a mealworm was eaten recorded.

## Experimental phases and procedures
- Initial training (Day 1 and following days):
  - Chicks learn to flip lids to access mealworms across 6 two-minute sessions per day, with groupings changing (groups of three, then pairs, then individuals).
  - Progressive obscuring of mealworms under lids to increase task difficulty, with trials ending when a mealworm is eaten or after ~30 seconds.
  - Food deprivation (~60 minutes) prior to most sessions.
- Learning phase:
  - Daily sessions of 16 presentations, where one dish bears a fly model with a mealworm inside (reward) and the other bears a wasp model with no reward.
  - Trials continue until a chick chooses the fly dish on at least 80% of presentations.
  - To prevent side bias, dish positions were varied along up to four positions with random pairings, excluding positions 1 and 4 together in a small number of cases.
- Test phase:
  - Up to four additional daily trials per chick.
  - Each trial includes: 6 fly-reward presentations, 6 with no reward (wasp), and 4 probe presentations with novel intermediate stimuli.
  - Probes test generalization across a broader range of trait combinations; latency to approach and lid removal measured.

## Data fields and units of recorded values (highlights)
- Chick-level data: unique chick ID, dates, weight measurements, and growth data.
- Trial-level data: date, group size, chick IDs involved, experimenter, buddy identifiers, food deprivation start time, trial start time, duration, number of mealworms left, and notes.
- Stimulus and response data: lids description, dish positions (dishA, dishB, dish_fly, dish_wasp), model codes (TF, VV, VVP; and trait codes like S, P, C, Z), mealworm presence, latency measurements (time_manual, time_video), time to open, and MW_eaten (Y/N).
- Data alignment keys allow joining across files by chick ID, trial, date, and phase.

## Practical implications for data use (Data Support perspective)
- Enables analysis of learning curves and discrimination performance by chick, phase, and stimulus trait combination.
- Supports cross-file joins to study how early training and exposure influence later probe responses and generalization.
- Facilitates dashboards and reports on:
  - Latency distributions by phase and stimulus type.
  - Proportion of correct choices (fly vs wasp) over time.
  - Impact of dish-position variation on learning progress.
  - Weight changes relative to experimental timeline (growth analysis).
- Potential data quality checks:
  - Consistency of IDs across phases and with weight records.
  - Missing timing fields in video-derived measurements.
  - Verification of model codes and trait combinations against the defined encoding scheme.

## Notes and caveats
- Some fields are duplicated or contain repeated metadata within the trait_exp_chick_weights.csv description; users should align and deduplicate where needed during data integration.
- Probe stimuli are drawn from a larger set of 30 intermediate insect stimuli, ensuring broad generalization assessment.