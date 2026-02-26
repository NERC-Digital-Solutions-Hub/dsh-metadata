# OVERVIEW: This experiment aimed to test whether generalist avian predators (chicks) have any unlearned biases towards or against attacking certain insect phenotypes, specifically those of stinging hymenoptera or their mimics.

## Aim and scope
- Test for unlearned biases in chick foraging toward insect phenotypes: stinging hymenoptera or mimics vs non-mimics.
- Assess whether chicks’ responses differ when presented with 3D-printed insect-like stimuli on lids of 16 dishes during a controlled foraging task.

## Experimental design and workflow
- Training phase: chicks learned to open lids to access mealworms in 16 dishes during a series of two-minute trials; lids gradually obscured mealworms to increase task difficulty.
- Testing phase: on a single Day 9 test trial, chicks encountered 16 dishes with eight non-mimic stimuli (Mesembrina meridiana) and eight test stimuli representing hymenopterans, hoverflies, or hybrids.
- Stimuli: 3D-printed life-like insects placed on dish lids; “treatment” codes identify six insect types, plus a non-mimic fly.
- Trial structure: randomised dish arrangement in a 4x4 grid; chicks forage for up to 10 minutes or until worms are consumed.

## Data collection and quality control
- Real-time observation in the lab supplemented by video recordings for later review.
- Quality control included: verifying data codes against plausible ranges and examining patterns of missing data to ensure integrity and avoid transcription errors.

## Data structure and files
- Three CSV files capture different aspects of the experiment:
  - innate_exp_chickweights
    - Growth data: 1405 weight measurements per chick.
    - Columns: id, date, weight (grams); summary/units described as “nature and units of recorded values.”
  - innate_exp_trainingphase
    - Behavioral data during the training phase: 1139 rows, 14 columns.
    - Main fields include: date, grouping, chick1/chick2/chick3, experimenter, lids, buddies, food_dep_start, start_time, duration, MW_left_2min, mealworms_left, notes, id, date, treatment, stimulus, variant, beh, dish, dish, stimulus, etc.
  - innate_exp_testphase
    - Behavioral data during the testing phase: 1508 rows, 14 columns.
    - Similar structure to training phase with fields for: date, grouping, chick1/chick2/chick3, experimenter, lids, buddies, food_dep_start, start_time, duration, MW_left_2min, mealworms_left, notes, id, date, treatment, stimulus, variant, beh, dish, dish, stimulus, etc.
- Shared identifiers and fields:
  - id: unique chick identifier
  - date: trial or weighing date (YYYY-MM-DD)
  - weight: grams (for chickweights file)
  - trial-related fields include: grouping, chick1/chick2/chick3, experimenter, lids, buddies, food_dep_start, start_time, duration, MW_left_2min (mealworms left after 2 minutes), mealworms_left, notes, dish, stimulus, treatment, variant, beh (behaviour code), sequence.

## Subjects and setting
- Experimental subjects: 130 domestic chicks (Gallus gallus domesticus) hatched and housed in the lab for ~11 days; two batches with buddy chicks (8 per batch) acting as companions.
- Arena: 140 x 70 x 40 cm enclosure with a 25 x 70 x 40 cm buddy area to enable social presence; buddy chicks rotated to avoid prolonged exposure.

## Stimuli and treatments
- Visual stimuli: life-sized 3D-printed insects on dish lids, generated from real insects or morphs to create mimics and non-mimics.
- Stimulus codes in dataset include:
  - A2: Argogorytes mystaceus (solitary wasp)
  - A6: Vespula vulgaris (social wasp)
  - C: Chrysotoxum (wasp-mimic hoverfly)
  - E0: Eristalis tenax (bee-mimic hoverfly)
  - E1/E2: novel intermediates or Apis mellifera (honey bee)
  - M: Mesembrina meridiana (non-mimetic fly)
  - S: Syrphus ribesii (wasp-mimic hoverfly)
  - S6: novel intermediate between S. ribesii and V. vulgaris
- Non-mimic control: Mesembrina meridiana used as baseline in both training and test phases.

## Phases and procedures
- Initial training (Day 1 and following days): chicks learn to flip lids to access mealworms; task complexity increased by progressively obscuring worms with lids; food deprivation applied prior to many sessions to motivate foraging.
- Training duration: daily trials from Day 1 through Day 8; most chicks achieved the ability to open lids routinely by end of training.
- Test trial (Day 9): each chick faced 16 dishes (8 with non-mimic, 8 with test stimuli) in a randomized grid; trial lasted up to 10 minutes or until all mealworms eaten.

## How the data can be used
- Analyze innate preferences for specific insect phenotypes by comparing choices and foraging patterns across stimuli categories.
- Examine learning effects from training to test phases and assess the impact of social companions (buddies) on performance.
- Explore weight progression (growth) alongside foraging behavior to identify any correlations with learning or motivation.
- Build dashboards or self-serve analyses to compare response sequences (sequence field) and behavioral outcomes (beh codes) across chicks and stimuli.

## Endnotes
- The dataset provides a comprehensive, multi-file structure capturing growth, training behavior, and testing behavior, enabling exploration of innate bias to insect-like stimuli and the effect of learning on foraging decisions.