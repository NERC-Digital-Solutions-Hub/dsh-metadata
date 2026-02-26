# Overview: Innate biases in domestic chicks toward insect phenotypes

- Purpose: Test whether generalist avian predators (chicks) have unlearned biases for or against attacking certain insect phenotypes, particularly stinging hymenoptera and mimics.
- Subjects: 130 domestic chicks (Gallus gallus domesticus), two batches with eight buddy chicks per batch; observed over 11 days.
- Environment: Arena measuring 140 x 70 x 40 cm with a 25 x 70 x 40 cm buddy area to keep visibility/hearing between trial chick and companions.
- Stimuli: 3D-printed insect-like lids on some dishes; real and artificial insect images generated from scans/morphing; 16 dishes per trial.
- Timeline:
  - Training: Day 1 and days 2–8 with progressively obscured lids to access mealworms.
  - Test: Day 9, a single test trial with 8 non-mimic fly stimuli and 8 test stimuli (hymenoptera, hoverflies, or hybrids).
- Data capture: Observations recorded in real time and via video for later review.

## Data collection and quality control

- Data collection methods: In-situ observation complemented by video recordings.
- Quality checks: 
  - Verified that summary data match valid codes and plausible value ranges.
  - Assessed patterns of missing data to distinguish genuine missingness from transcription/processing losses.

## Data files and structure

- Three CSV files:
  - innate_exp_chickweights
    - Purpose: Growth measurements of chicks during the experiment.
    - Size: 1405 rows.
    - Columns: 3 (id, date, weight).
  - innate_exp_trainingphase
    - Purpose: Chick behavior during training trials.
    - Size: 1139 rows.
    - Columns: 14 (highlights include date, grouping, chick1/chick2/chick3, experimenter, lids, buddies, food_dep_start, start_time, duration, mw_2min, mealworms_left, notes, id).
  - innate_exp_testphase
    - Purpose: Chick behavior during test interactions with stimuli.
    - Size: 1508 rows.
    - Columns: 14 (similar structure to training phase with fields for stimulus/treatment, dish, sequence, beh, dish, etc.).
- Shared identifiers and fields:
  - id: unique chick identifier.
  - date: trial date (yyyy-mm-dd).
  - treatment: code for the 3D-printed stimulus used on the dish lid (e.g., A2, A6, C, E0, E1, E2, M, S, S6).
  - stimulus: code identifying specific lid stimulus (same codes as treatment plus M for Mesembrina meridiana).
  - dish: dish number (1–16) in the grid.
  - sequence: ordering of observed behaviors within a trial.
  - beh: behavior code (see below for codes).
  - buds/buddies: IDs for companion chicks present in the buddy area.
  - lids: description of lid configurations during the trial.
  - start_time, duration: timing details for the trial.
  - mw_2min, mealworms_left: worm consumption metrics within specified intervals.

- Behavior codes (beh):
  - D: opened lid but didn’t eat immediately
  - E: opened lid and ate mealworm
  - F: pecked at partially open dish causing lid to fall
  - L: looked at or examined dish/stimulus
  - P: pecked at lid but didn’t open it

- Stimulus/treatment codes:
  - A2: Argogorytes mystaceus (solitary wasp)
  - A6: Vespula vulgaris (social wasp)
  - C: Chrysotoxum (wasp-mimic hoverfly)
  - E0: Eristalis tenax (bee-mimic hoverfly)
  - E1: Novel intermediate between E. tenax and A. mellifera
  - E2: Apis mellifera (honey bee)
  - M: Mesembrina meridiana (non-mimetic fly)
  - S: Syrphus ribesii (wasp-mimic hoverfly)
  - S6: Novel intermediate between S. ribesii and V. vulgaris

## Experimental design and stimuli details

- Initial training:
  - Chicks learned to open lids to access mealworms (Tenebrio molitor) from 16 lid-covered dishes.
  - Lids gradually obscured the mealworms across trials; up to 10 minutes per trial to forage.
  - Trial structure varied groupings: three chicks, then two, then individual, with daily sessions up to Day 8.
  - Food deprivation: 60 minutes before the last three sessions on Day 1 and before subsequent sessions.
- Test trial (Day 9):
  - 16-dish array in a 4x4 grid; 8 dishes with non-mimic fly stimulus (Mesembrina meridiana) lids; 8 with test stimuli (hymenoptera, hoverflies, or hybrids).
  - Stimuli placed in random order; chicks had up to 10 minutes to forage or until all mealworms were eaten.
  - Data include which lids were opened, time to access, and subsequent feeding behavior.

## Experimental subjects and setup

- Animals: 130 domestic chicks housed in the lab for 11 days; split into two batches.
- Buddy design: 8 buddy chicks per batch, rotating to ensure constant visibility/hearing for experimental chicks.
- Arena layout: Main arena (for testing) and a separate buddy area to maintain social cues; 16 dishes arranged across the grid.

## GIS-relevant notes and potential data products

- Spatial layout: 4x4 dish grid with known dish numbers and lid configurations provides a clear spatial framework for mapping behavior.
- Potential GIS data products:
  - Heatmaps of dish-opening frequency by grid location for different stimuli.
  - Spatial analysis of response latency and engagement by dish position and stimulus type.
  - Temporal mapping of behavior during training and testing phases to assess learning curves across space and time within the arena.
- Data integration considerations:
  - Align trial-level data (training/test phases) with dish locations and stimulus types to create geospatially-informed visualization dashboards.
  - Use sequence and beh codes to build event-based maps of approach/approach-and-consume behaviors.

## Endnote

- This document focuses on data collection, structure, and experimental design rather than results. The three CSV files provide a comprehensive, multi-phase dataset suitable for analyzing spatially-resolved avoidance or approach biases toward insect phenotypes, with rich metadata for quality control and reproducibility.