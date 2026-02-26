# Innate biases in chicks towards insect phenotypes (stinging hymenoptera or mimics)

## Aim
- To determine whether generalist avian predators (domestic chicks) have unlearned biases for or against attacking certain insect phenotypes, focusing on stinging hymenoptera and their mimics.
- Train chicks to forage from lids on dishes, then test preferences when lids carry different artificial insect stimuli.

## Data collection and generation methods
- Behaviour observed in real time in the laboratory and recorded on video for later review.
- Data captured across training and test phases, plus growth data for individuals.

## Quality control
- Summary data checked for valid codes and plausible value ranges.
- Patterns of missing data examined to distinguish true missingness from transcription loss.
- Data documented with clear coding for later verification and reuse.

## Data structure
- Three CSV files:
  - innate_exp_chickweights
    - 1405 rows
    - 3 columns
    - Chick weight measurements across the experiment
  - innate_exp_trainingphase
    - 1139 rows
    - 14 columns
    - Behavioural trials during training
  - innate_exp_testphase
    - 1508 rows
    - 14 columns
    - Behavioural interactions with stimuli during testing
- Common fields across files:
  - id: unique chick identifier
  - date: date of weighing or trial (yyyy-mm-dd)
  - weight: chick weight in grams (for weight file)
- Training/test phase specifics (14 columns in each of the latter two files) include:
  - date, grouping, chick1/chick2/chick3 ( IDs for chicks in a trial)
  - experimenter, lids (lid configurations), buddies (companion chicks)
  - food_dep_start, start_time, duration
  - MW_left_2min, mealworms_left
  - notes (comments; “x@y” indicates x mealworms uneaten after y minutes)
  - treatment and stimulus (3D-printed stimuli; ‘M’ indicates Mesembrina meridiana as non-mimic)
  - fully_closed, sequence, dish, variant, beh (behaviour observed)
  - behaviour codes: D (lid opened but not eaten immediately), E (lid opened and mealworm eaten), F (lid pecked causing lid to fall), L (looked/examined), P (pecked lid but did not open)

## Experimental subjects
- 130 domestic chicks (Gallus gallus domesticus)
- Housed from hatching for 11 days and organized into two batches
- Each batch included 8 buddy chicks, rotated to ensure exposure without long-term isolation

## Experimental arena
- Size: 140 x 70 x 40 cm general arena with a 25 x 70 x 40 cm buddy area
- Buddy area allows visual/hearing contact with companion chicks
- Buddies rotated so no chick spends more than an hour in the arena

## Artificial prey and stimuli
- Chicks learned to remove lids from petri dishes to access mealworms (Tenebrio molitor)
- Training lids were plain grey; test lids carried 3D-printed insect stimuli
- Stimuli: life-sized 3D prints generated from real insect scans, with variations to create mimicry or novelty
- Stimulus codes used in the test phase indicate different insects or mimics (see below)

## Initial training
- Day 1: six 2-minute sessions; 16 lidless dishes with mealworms placed in the arena
- Group sizes varied across sessions (groups of three, then pairs, then individuals)
- Food deprivation: 60 minutes before later sessions
- Subsequent days: daily trials over Day 1–Day 8
  - Lids progressively obscured the worms to increase task difficulty
  - Up to 10 minutes per trial for foraging

## Test trial
- Day 9: single test trial per chick
- 16 dishes arranged in a 4 x 4 grid
- 8 lids with non-mimic stimulus (Mesembrina meridiana) without a clear wasp-like pattern
- 8 lids with test stimuli (varying by treatment): 3D models resembling hymenoptera, hoverflies, or intermediates
- Trials lasted up to 10 minutes or until all mealworms were consumed
- Stimuli were randomly distributed across the grid

## Stimulus details (treatments and mimics)
- A2: Argogorytes mystaceus (solitary wasp)
- A6: Vespula vulgaris (social wasp)
- C: Chrysotoxum (wasp-mimic hoverfly)
- E0: Eristalis tenax (bee-mimic hoverfly)
- E1: Novel intermediate between E. tenax and Apis mellifera
- E2: Apis mellifera (honey bee)
- M: Mesembrina meridiana (non-mimetic fly)
- S: Syrphus ribesii (wasp-mimic hoverfly)
- S6: Novel intermediate between S. ribesii and V. vulgaris
- fully_closed: indicator of whether lids were fully closed during trials
- notes: additional observations, including timing of uneaten mealworms

## End of document relevance
- The dataset provides structured, quality-checked observations of predator responses to a controlled set of insect-like stimuli, enabling analysis of innate biases toward specific phenotypes or mimicry patterns.
- Suitable for revisiting concepts in ecological risk assessment, predator-prey perception, and the potential influence of visual mimicry on foraging decisions.