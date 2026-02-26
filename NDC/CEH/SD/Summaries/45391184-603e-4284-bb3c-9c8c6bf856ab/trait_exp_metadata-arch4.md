# OVERVIEW: This experiment aimed to test which traits are used by generalist avian predators (chicks) to discriminate among prey items, in particular to distinguish stinging hymenoptera from their mimics.

- Purpose and approach
  - Investigates how juvenile birds discriminate prey by isolating fly-like vs wasp-like traits.
  - Uses an arena-based foraging task where chicks remove lids from dishes to access mealworms, with stimuli that vary in fly vs wasp characteristics.
  - Tests responses to novel trait combinations to identify which traits most influence behavior.

- Data collection and quality control
  - Observations recorded live and via video for timing and behavioral data.
  - Quality checks include verifying valid codes, plausible value ranges, and examination of missing data patterns to distinguish genuine absence from transcription loss.

- Data structure and files
  - Five CSV files capturing different aspects of the experiment:
    - trait_exp_chick_weights.csv
      - Chick growth data
      - 1387 weight measurements
      - 3 columns
    - trait_exp_group_phase.csv
      - Initial grouped trials on day 1
      - 210 trials
      - 12 columns
    - trait_exp_training_phase.csv
      - Training period (learning to open lids)
      - 5024 presentations
      - 12 columns
    - trait_exp_learning_phase.csv
      - Learning period (fly vs wasp discrimination)
      - 6704 presentations
      - 12 columns
    - trait_exp_test_phase.csv
      - Testing period (responses to novel trait combinations)
      - 1938 presentations
      - 12 columns
  - All files share consistent metadata structure; detailed field descriptions provided in the dataset.

- Nature and units of recorded values (highlights)
  - trait_exp_chick_weights.csv
    - id: unique chick identifier
    - date: weighing date (YYYY-MM-DD)
    - weight: grams
    - For trial data: date, grouping, chick IDs, experimenter, buddy IDs, food deprivation start, start_time, duration (s), mealworms_left, notes
  - Detailed trial fields (common across files)
    - dish and lid statuses, stimulus identifiers (model codes), mimics, and trait encoding (shape, pattern, colour, size)
    - MW_eaten/mealworm presence flags
    - time_to_open, time_manual, time_video (latencies), latency to first peck
  - pillared by a standardized set of codes:
    - model: TF (fly), VV (wasp), VVP (probe with mimic), and trait codes (S, P, C, Z) with numeric mimicry levels (0–5)
    - dish positions and movement, trial start/end times, durations

- Experimental subjects and setup
  - Subjects: 74 domestic chicks (Gallus gallus domesticus)
  - Batch structure: two cohorts tested in different months
  - Buddy system: 8 chicks per batch served as buddies; buddies observed in a separate “buddy” area to maintain social context
  - Arena: 140 x 70 x 40 cm, with a companion buddy area measuring 25 x 70 x 40 cm

- Stimuli and experimental design
  - Artificial prey: life-sized 3D-printed insect models atop lids; images generated from real insect scans and morphed features
  - Stimulus coding:
    - fly-like (e.g., accuracy of shape, pattern, colour, size) vs wasp-like traits
    - Model codes include TF (fly), VV (wasp), VVP (probe mimic with reward), and trait-based codes (e.g., S0–S5, P0–P5, C0–C5, Z0–Z5)
  - Reward structure: mealworms offered with some stimuli; some probe presentations with novel insect traits

- Experimental phases
  - Initial training
    - Chicks learn to open lids to access mealworms across multiple sessions
    - Gradual obscuring of worms under lids; trials progress from group to pair to individual formats
  - Learning phase
    - Paired-choice discrimination: fly stimulus (reward) vs wasp stimulus (no reward)
    - Daily trials with 16 presentations; learning threshold defined as ≥80% correct fly choices
    - Position randomization introduced to mitigate side bias
  - Test phase
    - After learning, chicks faced single-dish presentations per trial
    - 6 rewarded fly trials, 6 non-rewarded wasp trials, plus four probe trials with novel insect stimuli
    - Primary measures include latency to approach and lid removal

- Data governance and usability notes for data leaders
  - Data are organized to capture individual and trial-level details with clear identifiers ( chick IDs, trial dates, batch, experimenter)
  - Metadata includes encoding schemes for stimuli, trait mimicry levels, and dish/stimulus positions to support reproducibility
  - Consistent timestamping (dates and times) and explicit duration metrics facilitate cross-phase analyses
  - The dataset supports assessment of which specific trait combinations most influence approach latency, decision-making, and feeding behavior, while controlling for social context and positional biases

- Practical implications for data strategy
  - Demonstrates comprehensive data capture across multiple experimental phases with robust quality controls
  - Highlights importance of detailed metadata for complex stimuli and behavioral assays
  - Illustrates structured data organization (separate phase-specific files) to support modular analyses and data discoverability
  - Emphasizes the need to document coding schemes (stimulus models, trait codes) for clarity and future reuse across studies