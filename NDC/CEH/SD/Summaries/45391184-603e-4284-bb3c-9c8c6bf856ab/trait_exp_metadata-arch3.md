# OVERVIEW:

- Purpose: An experiment to identify which traits generalist avian predators (chicks) use to discriminate prey, specifically distinguishing stinging hymenoptera from mimics. Chicks were trained in a lab to forage from lids on dishes, then exposed to artificial insect-like stimuli and to stimuli combining fly-like and wasp-like traits. The goal was to determine which traits (shape, pattern, colour, size) most influence decision-making.

- Experimental approach: 
  - Training phase: chicks learned to open lids to access mealworms; lids progressed from plain to insect-like with increasing concealment.
  - Learning phase: chicks learned to discriminate between fly (rewarded) and wasp (unrewarded) stimuli, using 2-dish presentations and variable dish positions to prevent side bias.
  - Test phase: after learning, chicks faced single-dish presentations with fly stimuli (rewarded), wasp stimuli (unrewarded), and novel probe stimuli that combined fly-like and wasp-like traits.

- Data collection and documentation:
  - Observations recorded live and via video for timing data.
  - Five structured CSV files capture behaviour, training, learning, and testing data, plus chick weights.

- Data structure and key files:
  - trait_exp_chick_weights.csv (1387 weight measurements + trial-level metadata per row)
  - trait_exp_group_phase.csv (210 grouped-trial behaviours, 12 columns)
  - trait_exp_training_phase.csv (5024 entries, 12 columns)
  - trait_exp_learning_phase.csv (6704 entries, 12 columns)
  - trait_exp_test_phase.csv (1938 entries, 12 columns)
  - Each file contains standardized fields such as date, start_time, duration, dish positions (dishA, dishB, dish_fly, dish_wasp), stimulus model codes (e.g., TF, VV, VVP), mealworm presence, latency measures (time_manual, time_video, time_to_open), and outcome indicators (MW_eaten).

- Nature and units of recorded values:
  - Weight data: id, date, weight (grams).
  - Trial data: date, grouping, chick IDs, experimenter, buddy companions, food deprivation start, start_time, duration, dishes and lids status, stimulus models, mealworm presence, latency measures (manual and video-based), and related notes.

- Experimental subjects and setting:
  - 74 domestic chicks (Gallus gallus domesticus), across two batches; 8 buddies per batch.
  - Arena: 140 x 70 x 40 cm with a separate buddy area (25 x 70 x 40 cm) to provide visual/hearing contact; buddies rotated to keep exposure fresh.

- Artificial prey and stimuli:
  - Lids initially plain, then topped with life-sized 3D-printed insect models.
  - Stimuli manipulated to combine or contrast fly-like and wasp-like traits across shape, pattern, color, and size.
  - Some probe stimuli were novel combinations (intermediate between fly and wasp).

- Experimental phases in detail:
  - Initial training: six 2-minute sessions on Day 1; food deprivation introduced in later sessions; 8 lidless dishes initially, then two-dish lid presentations with mealworms; sessions end when a worm is eaten or after 30 seconds.
  - Learning phase: daily trials with two-dish presentations; one dish with a fly stimulus and a mealworm (rewarded) and the other with a wasp stimulus (no reward); learning continues until the fly-discriminate criterion (≥80% correct) is met, up to ~11 days; randomization of dish positions to reduce side bias.
  - Test phase: after learning, up to four days of testing; six fly-rewarded trials, six wasp-unrewarded trials, and four probe trials with novel insect stimuli; latency to approach and lift the lid is recorded as a primary measure.

- Data governance and accessibility considerations:
  - The dataset emphasizes transparency with explicit metadata, unit definitions, and detailed data structure to facilitate replication and secondary analysis.
  - Potential challenges for reuse include complex, multi-file structure, some missing video timing data, and the need to interpret coded stimulus and dish-position fields.