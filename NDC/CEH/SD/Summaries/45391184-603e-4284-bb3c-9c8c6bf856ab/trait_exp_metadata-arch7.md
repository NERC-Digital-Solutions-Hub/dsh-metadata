# OVERVIEW: This experiment aimed to test which traits are used by generalist avian predators (chicks) to discriminate among prey items, in particular to distinguish stinging hymenoptera from their mimics.

## Purpose and scope
- Investigates how chicks discriminate prey items using specific trait cues (shape, pattern, colour, size) and how these cues influence foraging choices.
- Examines learning to distinguish fly-like vs wasp-like stimuli and reactions to novel, intermediate stimuli (probes).
- Aims to identify which traits most strongly drive chick behaviour and decision-making during foraging.

## Data collection and quality
- Data collected in a laboratory arena with direct observation and video recordings for timing and behavior review.
- Quality control includes checks for valid codes, plausible value ranges, and patterns of missing data to ensure data integrity.

## Experimental setup and subjects
- Subjects: 74 domestic chicks (Gallus gallus domesticus), split into two batches with 8 “buddy” chicks per batch to act as companions.
- Arena: 140 x 70 x 40 cm with a separate buddy area (25 x 70 x 40 cm) to keep chicks visually/hearing companions; buddies rotated so none remained long in the arena.
- Artificial prey: Petri dishes with lids; training used plain lids, learning/testing used 3D-printed insect lids representing real/mimic features. Stimuli encoded as combinations of mimicry traits.

## Data structure and content
- Five CSV files total:
  - trait_exp_chick_weights.csv
    - 1387 rows of weight measurements; 3 columns (id, date, weight).
    - 12 additional columns capturing trial-level metadata (date, grouping, chick IDs, experimenter, buddy IDs, food deprivation start, start time, duration, mealworms left, notes, lid and dish positions, stimulus details, latency measures, and outcomes such as MW_eaten, time_to_open, etc.).
  - trait_exp_group_phase.csv
    - 210 rows; 12 columns; chick behaviour during initial grouped trials on day 1.
  - trait_exp_training_phase.csv
    - 5024 rows; 12 columns; training period data (learning to flip lids to access mealworms).
  - trait_exp_learning_phase.csv
    - 6704 rows; 12 columns; learning period data (discrimination between fly and wasp stimuli).
  - trait_exp_test_phase.csv
    - 1938 rows; 12 columns; testing period data (responses to novel, probe-like stimuli).
- Key recorded values and structure:
  - Per-presentation and per-trial data including: date, trial grouping, chick IDs, experimenter, buddy IDs, food deprivation timing, start times, duration, dish and lid positions, which dish was opened, stimulus code (e.g., TF for fly, VV for wasp, VVP probe), mimicry trait codes (S, P, C, Z with numeric mimicry levels 0–5), mealworm presence, latency measures (time_manual, time_video), time to open, and outcome (MW_eaten, etc.).
  - Detailed trait encoding for stimuli:
    - TF: fly stimulus with mealworm
    - VV: wasp stimulus without reward
    - VVP: probe (mimic) with reward
    - Other codes describe degree/combination of mimicry across shape, pattern, colour, size (0 = highly fly-like; 5 = intermediate; missing/other codes imply wasp-like).

## Experimental design and phases
- Initial training phase:
  - Chicks learned to open lids to access mealworms; sessions included progressively obscured prey under lids.
  - Group sizes varied (groups of three, then pairs, then individuals); daily trials through Day 7.
- Learning phase:
  - Paired-choice discrimination between fly-present (reward) and wasp-present (no reward) stimuli.
  - Daily trials with 16 presentations; progress until each chick chose the fly dish in ≥80% of presentations (up to 11 days).
  - To mitigate side bias observed in some chicks, dish positions were varied along four positions (randomly selected pairs) to avoid fixed left/right bias.
- Test phase:
  - Up to four additional daily trials after learning; each trial included six fly-with-reward, six wasp-without-reward, and four probe presentations using novel intermediate stimuli (30 variants) representing different fly/wasp trait combinations.
  - Measured approach latency and lid removal.

## Measurements and key variables
- Latency metrics:
  - time_manual: manual stopwatch latency to first peck/attack.
  - time_video: video-derived latency (often more precise; missing for some trials).
  - time_to_open: time from release to lid opening (when applicable).
- Behavioral and outcome metrics:
  - MW_eaten: whether a mealworm was eaten (Y/N).
  - mealworms_left: number of mealworms remaining at end of trial.
  - duration: trial length (seconds).
  - lid_opened: which lid was opened (dish number).
  - dish and stimulus details: positions and identities of fly/wasp dishes, including probe stimuli.
- Experimental context fields:
  - grouping, batch, experimenter, buddy relationships; food deprivation timing; start times; notes.

## Data use implications for GIS specialists
- The dataset captures time-stamped, event-level behavioral responses within a spatial arena, enabling:
  - Spatial-temporal mapping of approach decisions relative to dish positions and stimulus placement.
  - Analysis of how different mimicry traits (shape, pattern, colour, size) influence decision-making across space and time.
  - Integration of multi-source data (behavior, timing, stimulus type) into geospatial-like data products or dashboards depicting foraging responses.
- Potential data products:
  - Spatio-temporal visualizations of chick trajectories (if augmented with movement data) and decision points.
  - Maps of latency distributions by stimulus type and mimicry trait combinations.
  - Dashboards comparing learning curves across batches, dish positions, and buddy configurations.
- Considerations for GIS-style data handling:
  - Time-series alignment across phases; consistent unique identifiers for chicks and trials.
  - Encoding of categorical stimulus traits and continuous latency/duration metrics.
  - Handling of missing video-derived times and potential biases due to dish-position changes.

## Practical notes and limitations
- Lab-based setting with a relatively small, specific subject pool (74 chicks) may limit generalizability to wild populations.
- Side-bias mitigation required adjustments to dish positioning; important to account for positional effects in analyses.
- Data encoding includes complex mimicry trait codes; careful interpretation required for trait-based analyses.

## Summary of potential GIS-relevant takeaways
- Rich, time-stamped, event-level data with explicit spatial references (dish positions) and multi-attribute stimuli.
- Opportunity to build map-based data products showing how spatial arrangement and trait features influence foraging decisions over time.
- Structured, phase-wise data suitable for layered GIS analyses and interactive visualization panels highlighting trait influence and learning progression.