# Innate Bias in Chicks Toward Insect Phenotypes

- Aim
  - Test whether generalist avian predators (chick chicks) have unlearned biases toward attacking certain insect phenotypes, specifically stinging hymenoptera or their mimics.
  - Use a structured laboratory experiment to assess preferences by monitoring which lids (with various insect-like stimuli) chicks choose to open.

- Experimental Design and Setup
  - Experimental subjects: 130 domestic chicks (Gallus gallus domesticus), acquired after hatching and housed for 11 days; two batches with buddy chicks present in the arena.
  - Arena: 140 x 70 x 40 cm with a 25 x 70 x 40 cm buddy area to allow visibility and interaction with buddy birds; buddies rotated to avoid prolonged exposure.
  - Artificial prey and stimuli: lids covering petri dishes containing mealworms; training lids were plain, testing lids featured 3D-printed insect-like stimuli. Stimuli included imitators and mimics of wasps, hoverflies, bees, and non-mimetic flies.
  - Training and test phases:
    - Initial training: chicks learned to flip lids to access mealworms over 16 dish array; sessions varied by group size (groups of three, then pairs, then individuals); progressive obscuring of mealworms under lids.
    - Test phase: Day 9, single test trial with 16 dishes (8 with non-mimic fly stimulus M; 8 with varied test stimuli). Test stimuli were 3D models corresponding to hymenoptera, hoverflies, or hybrids.
  - Trial structure: each trial recorded duration, worm consumption, and chick behavior; buddy area observed simultaneously.

- Data Collection and Quality Control
  - Collection methods: real-time observation in the lab, supplemented by video recording for later review.
  - Quality control: summary data checked against valid codes and plausible ranges; examined patterns of missing data to distinguish true absence from transcription issues.
  - Data governance considerations: data are prepared for sharing via structured CSVs; metadata and dataset provenance are explicit in the data structure to support verification and reuse.

- Data Structure and Files
  - innnate_exp_chickweights (1405 rows, 3 columns): chick weight measurements across the experiment (growth data).
  - innate_exp_trainingphase (1139 rows, 14 columns): chick behavior during training trials (trial-level observations).
  - innate_exp_testphase (1508 rows, 14 columns): chick behavior during testing interactions with stimuli (trial-level observations).
  - Common metadata fields:
    - id: unique chick identifier
    - date: date of weighings or trials (yyyy-mm-dd)
    - weight: weight in grams
  - Key trial-level fields (highlights):
    - date, grouping, chick1/chick2/chick3, experimenter, lids (positions across dishes), stimulus/treatment codes, dish number, variant, beh (behavior category: opened, ate, pecked, looked, etc.), duration, MW_left/mealworms_left, notes, fully_closed, food_dep_start, start_time, etc.
  - Stimulus/treatment codes (examples):
    - A2: Argogorytes mystaceus (solitary wasp)
    - A6: Vespula vulgaris (social wasp)
    - C: Chrysotoxum (wasp-mimic hoverfly)
    - E0–E2: hoverflies/bee mimics
    - M: Mesembrina meridiana (non-mimetic fly)
    - S: Syrphus ribesii (wasp-mimic hoverfly)
    - S6: Novel intermediate
  - Behavioral codes (examples):
    - D: opened lid but not yet eaten
    - E: opened lid and ate mealworm
    - F: lid opened causing lid to fall
    - L: looked at/examined dish
    - P: pecked lid but did not open
  - Notes field captures additional timing and event details (x@y format indicating x mealworms uneaten after y minutes).

- Experimental Subjects and Environment
  - Subjects: 130 domestic chicks, divided into two batches; eight buddy chicks per batch rotated in the buddy area.
  - Environment: controlled laboratory arena with buddy area visibility; daily training sessions spanning up to Day 8 before the Day 9 test.

- Key Findings and Implications (for Monitoring Frameworks perspective)
  - Provides a structured example of linking an experimental design to a rich, multi-file dataset with explicit metadata and event-level details.
  - Demonstrates the importance of data governance, standardization, and metadata completeness to enable replication and secondary analysis.
  - Highlights practical challenges relevant to monitoring frameworks: data richness vs. potential barriers in data sharing (e.g., need for clear metadata, handling of missing data, and consistent data formatting across trials).
  - Useful blueprint for designing monitoring datasets: clear trial-level recording of treatments, stimuli, outcomes, and ancillary factors (grouping, timing, observer, and environmental conditions).

- Considerations for Monitoring Frameworks (lessons learned)
  - Emphasize explicit data structure and standardized coding of stimuli, treatments, and behaviors to facilitate interoperability and reuse.
  - Incorporate robust quality control steps and documentation of missing data to support transparency.
  - Plan for data governance and data-sharing requirements early (e.g., how to share video-augmented data and derived metrics alongside raw data).
  - Use replicates and varied stimuli to enable assessment of biases or effects across conditions, aiding policy-relevant evaluations of environmental interactions and predator-prey dynamics.