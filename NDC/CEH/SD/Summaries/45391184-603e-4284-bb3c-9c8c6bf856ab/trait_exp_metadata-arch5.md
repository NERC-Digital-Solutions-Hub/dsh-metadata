# Trait-based discrimination of mimic prey by generalist avian predators (chicks)

## Overview
- Aimed to identify which traits drive generalist avian predators (domestic chicks) to discriminate prey, focusing on distinguishing stinging hymenoptera from mimics.
- Chicks were trained in a lab to forage from lidded dishes, then exposed to artificial insect-like stimuli on lids.
- Tests used stimuli that combined fly-like and wasp-like traits (shape, pattern, colour, size) to see which traits most influence approach and lid-opening behavior.
- Hypothesized that some traits would disproportionately guide chick responses.

## Data collection and generation methods
- Behavioral data collected live during experiments and recorded on video for later review (notably timing data).
- Data capture included latency measures, dish interactions, and reward outcomes.
- Observations span training, learning, and testing phases, with detailed timing and event logging.

## Quality control
- Summary checks performed to ensure data entries used valid codes and plausible ranges.
- Patterns of missing data assessed to distinguish true absence from transcription/processing gaps.

## Data structure and contents
- Five CSV files total:
  - trait_exp_chick_weights.csv
    - Weight measurements across 1387 observations (3 columns: id, date, weight)
    - Also includes extensive trial-context fields (dates, grouping, chick identifiers, experimenter, buddy pairing, timing, dish and stimulus details, rewards, and latency measures)
  - trait_exp_group_phase.csv
    - 210 rows, 12 columns
    - Chick behaviour during initial grouped trials on day 1
  - trait_exp_training_phase.csv
    - 5024 rows, 12 columns
    - Chick behaviour during training to open lids
  - trait_exp_learning_phase.csv
    - 6704 rows, 12 columns
    - Chick behaviour during learning to discriminate between flies and wasps
  - trait_exp_test_phase.csv
    - 1938 rows, 12 columns
    - Chick behaviour during testing with novel stimulus combinations
- Column details (high-level): identifiers (chick IDs, dates), trial structure (grouping, phase), timing (start_time, duration, food_dep_start), performance (latency to approach, time to open, whether mealworm eaten), dish/stimulus specifics (positions, lid status, dish_fly, dish_wasp, model codes, mimicry degrees), and metadata (experimenter, batch, buddies, notes).

## Nature and units of recorded values
- id: unique chick identifier
- date: date stamps (YYYY-MM-DD)
- weight: grams (for weight measurements)
- start_time, food_dep_start: HH:MM
- duration: seconds
- latencies (time_manual, time_video): seconds
- mealworm presence: Y/N
- MW_eaten: Y/N
- dish and stimulus fields: coded positions and model types
- mimicry and feature codes: numeric scales (e.g., 0–5 for certain traits)
- grouping, batch, buddy identifiers, and experimenter initials as categorical codes
- All datasets align trial events with corresponding timestamps and experimental conditions

## Experimental subjects and setup
- Subjects: 74 domestic chicks (Gallus gallus domesticus)
- Batches: two cohorts tested in different months
- Buddy system: 8 buddy chicks per batch; buddy area visible to experimental chicks; buddies rotated to minimize prolonged exposure
- Arena: 140 x 70 x 40 cm, with a separate buddy area (25 x 70 x 40 cm) to maintain visual/h auditory contact

## Stimuli and experimental design
- Artificial prey: life-sized 3D-printed insect images placed on lids; 3D models generated from real insect scans and morphed to create varied trait combinations
- Stimulus coding:
  - TF: fly stimulus with a mealworm reward
  - VV: wasp stimulus with no reward
  - VVP: wasp-like stimulus with a reward (probe)
  - Remaining codes indicate specific trait combinations (shape, pattern, colour, size) and degree of mimicry (0 = fly-like, 5 = intermediate; higher indicates more wasp-like traits)
- Training phase: chicks learned to flip lids to access mealworms; gradual obscuring of mealworms beneath lids
- Learning phase: paired-choice discrimination between fly (reward) and wasp (no reward); daily sessions until the chick achieved ≥80% correct responses
  - To mitigate left/right bias, dish positions varied randomly along four possible positions (excluding simultaneous 1 and 4)
- Test phase: after learning, up to four daily trials with:
  - 6 fly-reward trials, 6 non-reward wasp trials, and 4 probe trials with novel intermediate insect stimuli
  - Primary measures: approach latency and lid removal latency

## Data governance and stewardship considerations
- Provenance and traceability: clear linkage between raw observations, video recordings, and tabulated CSV data across training, learning, and testing phases
- Metadata completeness: extensive contextual fields (dates, groupings, dish positions, stimulus types, experimenter, batch, buddy information) support data discovery and reuse
- Data quality and validation: documented quality checks for code validity, plausible value ranges, and missing data patterns
- Reuse and interoperability: structured, phase-separated datasets with consistent column naming and units facilitate secondary analyses and meta-studies
- Data lineage and versioning: multiple related files capturing evolving experimental stages; maintainers should track any updates or corrections to the datasets
- Ethical considerations: non-human subjects data with welfare considerations implicit in experimental design; ensure appropriate approvals and documentation accompany data sharing