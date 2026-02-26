# Overview: This experiment aimed to test which traits are used by generalist avian predators (chicks) to discriminate among prey items, in particular to distinguish stinging hymenoptera from their mimics.

- Purpose: Identify which trait cues (shape, pattern, colour, size) influence chick responses to fly-like versus wasp-like stimuli.
- Approach: Train chicks in a laboratory arena to access mealworms from lids, then present modified insect-like stimuli that mix fly and wasp traits to assess which traits drive discrimination.
- Experimental prediction: Some traits will have a stronger influence on behaviour than others.

## Data collection and quality control

- Behavioral data collected in real time and via video for timing measures.
- Quality checks ensured data codes were valid and values fell within plausible ranges; missing data patterns checked to distinguish genuine gaps from transcription losses.

## Data structure and contents

Five CSV files documenting the experiment:

- trait_exp_chick_weights.csv
  - Growth/weight data for individual chicks
  - 1387 rows
  - 3 columns (weight-related) plus an accompanying set of 12 columns for trial context per entry
- trait_exp_group_phase.csv
  - Chick behavior during initial grouped trials (Day 1)
  - 210 rows
  - 12 columns
- trait_exp_training_phase.csv
  - Behavior during the training period (learning to open lids)
  - 5024 rows
  - 12 columns
- trait_exp_learning_phase.csv
  - Behavior during the learning period (discriminating fly vs. wasp)
  - 6704 rows
  - 12 columns
- trait_exp_test_phase.csv
  - Behavior during the testing period (novel trait combinations)
  - 1938 rows
  - 12 columns

- For each file, the columns include identifiers (chick IDs, dates), trial metadata (start_time, duration), experimental context (experimenter, batch, buddies), stimulus details (model codes, dish positions, mimicry trait codes), and response measures (latency, time_to_open, MW_eaten, etc.).

## Nature and units of recorded values (highlights)

- Identifiers and timing:
  - id, date, start_time, duration
  - time_manual (latency to attack, in real-time stopwatch)
  - time_video (latency measured from video)
  - time_to_open (latency to open dish if initially closed)
- Experimental structure:
  - grouping (number of chicks per trial), batch (1 or 2), buddies (companion chicks)
  - dish positions (dishA, dishB; later, dish_fly and dish_wasp positions)
  - model (stimulus type; TF = fly, VV = wasp, VVP = mimic with reward; other codes for trait-based combinations)
  - food_dep_start (pre-trial deprivation timing), mealworm presence (MW_eaten, yes/no)
- Stimulus traits and mimicry:
  - trait codes describing fly/wasp trait combinations (S = shape, P = pattern, C = colour, Z = size) with numeric mimicry levels (0 = fly-like to 5 = strong mimicry; unspecified traits default to wasp-like)
  - probe stimuli: a novel insect with intermediate fly/wasp features drawn from a set of 30 possibilities
- Outcomes and notes:
  - MW_eaten (whether a mealworm was consumed)
  - notes column for extra comments
- Experimental context:
  - date, experimenter, batch, lids, dish positions, and other descriptive fields

## Experimental subjects and environment

- Subjects: 74 domestic chicks (Gallus gallus domesticus), tested across two batches (months apart)
- Buddy system: 8 buddies per batch; buddy chicks placed in a separate buddy area to be observed by trial chicks
- Arena: 140 x 70 x 40 cm main area; a 25 x 70 x 40 cm buddy area separated from the main arena
- Buddies rotated regularly; buddies spent no more than an hour in the arena

## Stimuli and apparatus

- Artificial prey: lids covering mealworms; initial lids plain grey during training, later topped with life-sized 3D-printed insect models
- Insect models: created by 3D scanning real insects and morphing features to vary shape, pattern, colour, and size
- Mimicry construction: combinations of fly-like and wasp-like traits; some stimuli included precise fly-wasp trade-offs (0–5 mimicry scale); some stimuli were perfect wasp-like unless otherwise specified

## Experimental design and phases

- Initial training (Day 1 and beyond):
  - Chicks learned to open lids to access mealworms in paired-dish setups
  - Early trials: lid positions gradually obscured the mealworms
  - Daily sessions leading up to Day 7 showed routine lid opening by most chicks
  - Trials included varying group sizes (groups of three, pairs, then individuals) and eventual food deprivation prior to sessions
- Learning phase:
  - Paired-choice discrimination: one lid with a fly stimulus and a mealworm reward vs. a wasp stimulus with no reward
  - Daily trials: 16 presentations per day
  - Criterion: fly choices on at least 80% of presentations; up to 11 days to reach criterion
  - Side-bias mitigation: randomize dish positions along a line of four positions to avoid left-right preferences
- Test phase:
  - Post-learning assessments with a single dish and a single stimulus per presentation
  - Each chick: 6 fly-stimulus trials with mealworms, 6 wasp-stimulus trials with no reward, and 4 probe trials with novel stimuli (intermediate between fly and wasp)
  - Probes used from a set of 30 variations to test generalization
  - Primary measures: latency to approach and lid removal

## Analytical opportunities (from an analyst's perspective)

- Potential analyses:
  - Correlate chick growth/weight (trait_exp_chick_weights) with learning speed and discrimination success
  - Examine effects of stimulus trait combinations (S, P, C, Z) and mimicry levels on approach latency and reward-taking
  - Model learning trajectory across training, learning, and test phases
  - Assess side-position biases and their attenuation when positions are randomized
  - Explore differences between batches and buddy effects on learning outcomes
  - Analyze probe responses to quantify generalization to novel trait combinations
- Data provenance and usability:
  - Detailed trial-level metadata (dates, times, experimenter, batch, dish positions) facilitates reproducibility and meta-analyses
  - Metadata and multiple phases enable tracking of data quality and consistency across stages

## Notes on scope and constraints

- Right scale and local-level detail: dataset provides rich, controlled laboratory data suitable for correlation and predictive analyses but is limited to the experimental arena and chick cohort described
- Data capture: both real-time observation and video timing data enhance precision for latency-based outcomes
- Stimulus coding: a comprehensive set of trait-based codes enables fine-grained modelling of trait influence on predator discrimination behaviors