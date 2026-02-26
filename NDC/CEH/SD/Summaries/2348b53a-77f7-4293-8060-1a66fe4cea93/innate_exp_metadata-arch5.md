# OVERVIEW:

## Aim
- To determine whether generalist avian predators (chicks) have unlearned biases toward or against attacking certain insect phenotypes, focusing on stinging hymenoptera or their mimics.
- Use a two-phase design: initial training to forage from lids on dishes, followed by testing with artificial insect-like stimuli to assess preferences in which dishes are opened first.

## Datasets (data files)
- innate_exp_chickweights: 1405 rows, 3 columns; tracks chick growth/weight measurements across the experiment.
- innate_exp_trainingphase: 1139 rows, 14 columns; records chick behavior during training trials.
- innate_exp_testphase: 1508 rows, 14 columns; records chick behavior during test interactions with stimuli.

## Data structure and key columns
- Global identifying fields (present in both training and test data): 
  - id: unique chick identifier
  - date: date of weighing or trial
  - weight: weight in grams
- Training and testing phase columns (14 total; capture trial context and outcomes):
  - date, grouping, chick1/chick2/chick3: identifiers for chicks involved
  - experimenter: initials of the researcher
  - lids: lid positions during the trial
  - buddies: IDs of buddy chicks in the arena
  - food_dep_start: time before trial when the chick was food-deprived
  - start_time, duration: trial start and length
  - mw_2min, mealworms_left: mealworms remaining after intervals or at end
  - notes: extra comments (e.g., x@y notation for mealworms left after y minutes)
  - treatment: 3D-printed stimulus code on lids for 8 of 16 dishes
  - stimulus: coded stimulus shown on lids (mapping to insect types)
  - variant: replicate identifier for a given stimulus
  - dish: dish number (1-16) in the arena
  - fully_closed: whether lids were fully closed (TRUE/FALSE)
  - sequence: ordering of behavioral observations within a trial
  - beh: observed chick behavior (e.g., D, E, F, L, P)
  - Other related fields: food_dep_start, start_time repeated in both datasets to align timing
- Stimulus/treatment mapping (examples):
  - A2: Argogorytes mystaceus (solitary wasp)
  - A6: Vespula vulgaris (social wasp)
  - C: Chrysotoxum (wasp-mimic hoverfly)
  - E0: Eristalis tenax (bee-mimic hoverfly)
  - E1/E2: intermediate or Apis mellifera (honey bee)
  - M: Mesembrina meridiana (non-mimetic fly)
  - S: Syrphus ribesii (wasp-mimic hoverfly)
  - S6: intermediate between S. ribesii and V. vulgaris

## Experimental subjects and setting
- Subjects: 130 domestic chicks (Gallus gallus domesticus), hatched and housed in the lab for 11 days.
- Batch design: two batches, tested in different months; 8 chicks per batch acted as “buddies.”
- Arena: 140 x 70 x 40 cm arena with a 25 x 70 x 40 cm buddy area; buddies are visible to the trial chick throughout sessions.
- Artificial prey: lids initially plain; later lids topped with life-size 3D-printed insect models (real and artificial insect images; some models mimic hymenoptera, hoverflies, or hybrids).

## Training and test procedures
- Initial training: chicks learned to flip lids to access mealworms in 16 lid-covered dishes; sessions included varying groupings (trio, pair, individual) with gradual obscuring of mealworms by lids.
- Training schedule: Day 1 involved six two-minute sessions; subsequent days featured daily trials, up to Day 8, normalizing to consistent lid-opening behavior.
- Test trial: Day 9, each chick encountered 16 dishes (8 with non-mimic fly model M; 8 with test stimuli). Dishes arranged in a 4x4 grid; testing period lasted up to 10 minutes or until mealworms were consumed.

## Data collection and quality control
- Data collection methods: live observation in the laboratory with supplementary video recordings for later review.
- Quality control: summary checks on data ranges and codes; assessment of missing data to ensure gaps reflect actual missingness rather than transcription errors.
- Data provenance: all data stored as CSV files; detailed documentation of trial conditions, stimulus codes, and observational categories to support traceability and reproducibility.

## Data governance and notes for reuse
- Code mappings and experimental design details are explicitly documented (stimulus/treatment codes, dish numbering, sequence of observations).
- The structure supports re-use for analyses of biases toward insect phenotypes, replication across batches, and comparison between training vs. test phases.
- Considerations for interoperability: standard CSV format with clear field names; attention to potential replication of fields across training/test datasets and consistent coding schemes for behavior and stimuli.