# OVERVIEW: This experiment aimed to test whether generalist avian predators (chicks) have any unlearned biases towards or against attacking certain insect phenotypes, specifically those of stinging hymenoptera or their mimics.

## Purpose and scope
- Assess unlearned biases in chick foraging behavior toward insect phenotypes (stinging hymenoptera and mimics) using trained foraging tasks and a test with 3D-printed insect-like stimuli.
- Experimental flow: training phase to teach lids over dishes; test phase presenting 3D-printed stimuli on lids vs a non-mimic fly model.

## Data assets and structure
- Three CSV files capturing different aspects of the experiment:
  - innate_exp_chickweights
    - 1405 rows
    - 3 columns: id (unique chick), date (yyyy-mm-dd), weight (grams)
    - Records growth/weight measurements across the study
  - innate_exp_trainingphase
    - 1139 rows
    - 14 columns detailing chick behavior during training trials
  - innate_exp_testphase
    - 1508 rows
    - 14 columns detailing chick behavior during test interactions with stimuli
- Core identifiers and fields (across files):
  - id: unique chick identifier
  - date: trial or weigh date (yyyy-mm-dd)
  - weight: chick weight (grams) for weight data file
  - date, grouping, chick1/chick2/chick3, experimenter, lids, buddies, food_dep_start, start_time, duration
  - mw_2min, mealworms_left, notes, treatment, stimulus, variant, dish, sequence, beh, fully_closed
- Stimulus/treatment codes in test data include:
  - A2: Argogorytes mystaceus (solitary wasp)
  - A6: Vespula vulgaris (social wasp)
  - C: Chrysotoxum (wasp-mimic hoverfly)
  - E0, E1, E2: hoverflies/bees/mimics
  - M: Mesembrina meridiana (non-mimic fly)
  - S: Syrphus ribesii (wasp-mimic hoverfly)
  - S6: novel intermediate between S. ribesii and V. vulgaris
  - plus other combinations and replicates (variant)

## Experimental design details
- Subjects: 130 domestic chicks (Gallus gallus domesticus), two batches, with eight buddy chicks per batch.
- Arena: 140 x 70 x 40 cm with a separate buddy area (25 x 70 x 40 cm) to enable social visibility.
- Buddies: two buddy chicks per trial area, rotated to keep exposure balanced.
- Stimuli: lids on dishes in testing phase topped with 3D-printed insect models; stimuli created from real/combined images to vary mimicry accuracy.
- Training phase: sequential exposure to lids over 16 dishes across multiple sessions; gradually obscured prey to enforce lid-flipping behavior; food deprivation applied before later sessions.
- Test phase: single Day 9 trial per chick with 16 dishes arranged 4x4; 8 dishes with non-mimic model (Mesembrina meridiana) and 8 with test stimuli; trials allowed up to 10 minutes or until prey is consumed.

## Data collection and quality assurance
- Collection methods:
  - Real-time observation in the lab supplemented by video recording for later review.
- Quality control:
  - Summary data checked for valid codes and plausible value ranges.
  - Examination of missing data to distinguish genuine absence from transcription errors.
- Data structure and metadata:
  - Detailed schema with both high-level trial data and per-trial observations (including timing, behavior codes, and consumption metrics).
  - Notes field captures nuanced observations (e.g., x@y format for meals uneaten after y minutes).

## Data content details and usability
- Training and test phases provide rich, event-level data on foraging decisions, lid manipulation, and responses to different insect-like stimuli.
- Behavioral coding:
  - Beh categories include actions such as opened lid and ate (E), opened lid but didn’t eat (D), pecked at lid (P), examined stimulus (L), etc.
- Time and outcome metrics:
  - Start times, trial durations, meals remaining at 2 minutes, total meals uneaten, and other temporal markers support analysis of latency, persistence, and efficiency.
- Data governance and re-use considerations:
  - Clear identifiers enable join across training and test data; multiple replicates and variant codes aid comparative analyses.
  - Comprehensive metadata supports reproducibility, but the dataset’s complexity and coding scheme may require careful harmonization for new analyses.

## Practical implications for data leaders
- The dataset provides a well-documented, multi-file asset capturing behavioral response to engineered stimuli, suitable for studies on innate biases, learning, and decision-making in animals.
- Strong metadata and coding conventions facilitate cross-study integration, but analysts should account for complex, nested trial structures (groupings, buddy dynamics, and replicate variants).
- Opportunities to improve data standards include harmonizing date formats, consolidating overlapping fields across files, and clarifying the interpretation of notes and replicate variants for broader dissemination.