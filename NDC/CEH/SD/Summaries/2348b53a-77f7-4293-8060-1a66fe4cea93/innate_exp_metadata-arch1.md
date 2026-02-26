# OVERVIEW: This experiment aimed to test whether generalist avian predators (chicks) have any unlearned biases towards or against attacking certain insect phenotypes, specifically those of stinging hymenoptera or their mimics.

- Aim and research question
  - Investigates whether unlearned biases exist in domestic chicks toward insect phenotypes, focusing on stinging hymenoptera and their mimics.
  - Compares responses to a panel of 3D-printed insect-like stimuli during a controlled testing phase after a structured training regime.

- Experimental subjects and setup
  - Subjects: 130 domestic chicks (Gallus gallus domesticus), split across two batches; 8 chicks per batch acted as “buddies.”
  - Arena: 140 x 70 x 40 cm with a separate buddy area (25 x 70 x 40 cm) to keep buddy chicks visible and audible during trials.
  - Training and test environment: laboratory setting with video capture for later review.

- Stimuli and conditions
  - Training phase: lids over 16 petri-dish prey, initially plain lids transitioning to lids obscuring prey.
  - Test phase: 16 dishes arranged in a 4 x 4 grid; 8 lids carry a non-mimic fly model (Mesembrina meridiana) and 8 carry test stimuli that vary by treatment.
  - Stimulus types (3D-printed insect models): A2 (Argogorytes mystaceus - solitary wasp), A6 (Vespula vulgaris - social wasp), C (Chrysotoxum - wasp-mimic hoverfly), E0 (Eristalis tenax - bee-mimic hoverfly), E1 (novel intermediate between E. tenax and A. mellifera), E2 (Apis mellifera - honey bee), M (Mesembrina meridiana - non-mimetic fly), S (Syrphus ribesii - wasp-mimic hoverfly), S6 (novel intermediate between S. ribesii and V. vulgaris).
  - Trials labeled with additional fields: treatment (stimulus on lids), variant (replicate), and fully_closed (whether lids were fully closed or not during training).

- Data collection and quality control
  - Data collected in real-time and supplemented by video review.
  - Quality checks performed on summary data to ensure valid codes, plausible value ranges, and appropriate handling of missing data.
  - Documentation notes that some chicks failed to complete training and received an easier task (accessible worms with partially open lids).

- Data structure and files
  - innate_exp_chickweights: 1405 rows; 3 columns (id, date, weight) tracking chick weight growth over the experiment.
  - innate_exp_trainingphase: 1139 rows; 14 columns detailing each training trial’s conditions and outcomes.
  - innate_exp_testphase: 1508 rows; 14 columns detailing each test trial’s conditions and outcomes.
  - Common identifiers and fields across datasets include:
    - id (unique chick identifier) and date
    - trial-level details: grouping, chick1/chick2/chick3 (IDs), experimenter, lids, buddies
    - timing and exposure: food_dep_start, start_time, duration
    - outcomes: mw_2min (mealworms left after 2 minutes), mealworms_left (total uneaten), and related notes
    - trial-specific descriptors: dish, stimulus, treatment, variant, beh (behavior observed), and fully_closed
  - The 14-column structure for training and test datasets includes detailed descriptors of the trial, stimulus, and observed behavior.

- Experimental procedure summary
  - Initial training (Day 1): six two-minute sessions in which chicks learned to open lids to access mealworms, with changing social configurations (groups of three, then pairs, then individuals) and progressive obstruction of prey by lids.
  - Training progression: trials lasted up to 10 minutes; worms became more obscured over successive trials; 60-minute food deprivation for most sessions after Day 1.
  - Test (Day 9): one test trial per chick with 8 non-mimic (Mesembrina meridiana) lids and 8 test stimuli lids arranged randomly; 10-minute limit or until all mealworms were consumed.

- Analytical relevance for data-driven questions
  - Potential analyses include:
    - Effect of stimulus type (hymenopteran vs. mimic vs. non-mimic) on approach and lid-opening behavior (beh codes: opened, ate, pecked, looked, etc.).
    - Time-to-event analyses for lid-opening or decision to eat, using start_time and duration.
    - Differences between training and test phases to assess learned vs. innate biases.
    - Dose-like effects of social context or buddy presence on responses (grouping, buddies fields).
    - Growth trajectories and their relation to foraging behavior over the training period (innate_exp_chickweights).
  - The dataset supports cross-validation of observed behaviors with automated video review and notes, enabling robust interpretation of subtle bias patterns.

- Considerations and limitations
  - Data gaps may arise from training non-completion or variations in training difficulty.
  - Historical and batch effects: two separate batches and buddy design may introduce variability.
  - The generalizability of results may be bounded by lab conditions and artificial stimuli versus real-world prey.

- Reproducibility and data accessibility
  - Data are organized into clearly labeled CSV files with explicit trial and stimulus metadata.
  - Documentation includes explicit mappings for stimulus codes and trial conditions, enabling replication or secondary analyses.
  - Video data availability (for review) enhances validation and interpretation of coded behaviors.