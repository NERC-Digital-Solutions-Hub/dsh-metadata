# OVERVIEW

- Purpose: The dataset documents three related experiments examining how invertebrate predators (mantises, jumping spiders, crab spiders) respond to 3D-printed wasp-like and fly-like stimuli after aversive conditioning to wasp stimuli. The goal is to determine how much mimetic similarity is needed before a predator mistakes a mimic for a wasp.
- Approach: Train predators to associate wasp stimuli with a negative outcome while fly stimuli have no outcome, then test responses to a range of novel mimetic stimuli with varying similarity to the wasp stimulus.
- Output: Data collected as structured observations and trials, including behavioural measures and timing, intended for analysis and visualization (e.g., GIS-ready mapping of responses across stimuli or trials).

## Study design and stimuli

- Three experiments with similar methodologies using different predator species.
- Stimuli design: 3D scanned images of real insects, assembled into transects along mimetic similarity (endpoints M. meridiana and V. vulgaris; alternative Chrysotoxum-based transect for some spiders; some stimuli beyond endpoints to exaggerate traits).
- Stimulus naming: formats like M100, M75V25, M50V50, M25V75, V100; extra variants include A-25V125, A-50V150 for wasp-exaggeration. Variants a, b, c reflect intraspecific variation.
- Experimental phases:
  - Training phase: six aversive conditioning trials for mantises and jumping spiders (random initial stimulus, then alternating); punishments delivered when wasp stimuli are encountered or attacked. Crabs receive three treatment regimes (direct punishment, punishment with fly stimulus, or no punishment) due to wild-caught status.
  - Testing phase: nine trials per mantis/spider (five probe stimuli from transect, four reinforcement trials). Mantises and spiders punished for encounters with wasp stimuli; crabs tested with a single stimulus due to time/containment constraints.
- Measured outcomes:
  - Mantises: latency to attack (time from trial start to first attack).
  - Jumping spiders: various behaviours recorded (e.g., orientation, alert, display, approach, attack) with counts per trial.
  - Crab spiders: similar behavioural counts per trial (noting sex, colour morphs, day, and training treatment).

## Study organisms and housing

- Mantises: three species (Rhombodera kirbyi, Polyspilota aeruginosa, Pseudoxyops perpulchra); housed individually at 26°C with 12:12 h light-dark cycle; trials conducted 30 h after feeding.
- Jumping spiders: Phidippus audax; housed individually under laboratory conditions; trials conducted 30 h after feeding.
- Crab spiders: Synema globosum; wild-caught, kept at 22°C; not fed for 48 hours before use; housed individually without an artificial light:dark cycle.

## Experimental arena and equipment

- Mantises and jumping spiders: small opaque arenas with a motor-driven stimulus on a fishing-line rig to create three-dimensional movement (left-right or vertical), encouraging approach or striking.
- Crab spiders: larger arena with a similar setup plus a flower perch (purple milk thistle) to mimic a natural hunting context.
- Stimulus presentation: consistent, motor-driven motion patterns to elicit natural responses while enabling controlled measurement.

## Data collection and quality control

- Data collection: real-time behavioural observations during trials; video recording used for reference; timings captured with a stopwatch.
- Data processing: cleaning (removing invalid/unused points) and formatting via custom R v4.3.2 scripts.
- Quality checks: review of summary statistics and plausible value ranges; assessment of pattern and presence/absence of missing data to ensure values are genuinely missing rather than transcription errors.

## Data structure and contents

- Three CSV files:
  - mantis_data.csv
    - Purpose: mantis behavioural response to presented stimuli
    - 88 rows (one per trial)
    - 7 columns
    - Key columns: species, id, instar, trial, model, phase, time_to_attack
  - jumping_spider_data.csv
    - Purpose: jumping spider behavioural response to presented stimuli
    - 1,355 rows (behaviour type within each trial)
    - 6 columns
    - Key columns: id, phase, trial, model, behaviour, count
  - crab_spider_data.csv
    - Purpose: crab spider behavioural response to presented stimuli
    - 1,260 rows (behaviour type within each trial)
    - 8 columns
    - Key columns: id, sex, colour, day, treatment, model, behaviour, count

- Nature and units of recorded values (summary):
  - Mantises: time_to_attack in seconds; other fields describe trial identifiers and stimulus models.
  - Spiders: behaviour categories (as per Table 1) with counts per trial.
  - Crab spiders: similar behavioural counts with additional metadata (sex, colour morph, day, treatment).

## Data dictionary highlights (key fields)

- mantis_data.csv
  - species: Latin binomial for the mantis species
  - id: unique identifier per individual
  - instar: developmental stage
  - trial: trial number
  - model: stimulus code used in the trial
  - phase: experimental phase (training or testing)
  - time_to_attack: latency to first attack (seconds)

- jumping_spider_data.csv
  - id: individual identifier
  - phase: experimental phase
  - trial: trial number
  - model: stimulus code
  - behaviour: observed behaviour category (e.g., orientation, alert, display, approach, attack)
  - count: occurrences of the behaviour in the trial

- crab_spider_data.csv
  - id: individual identifier
  - sex: M or F
  - colour: morph code for females; X for males
  - day: days from start of experiment
  - treatment: training treatment type
  - model: stimulus code
  - behaviour: observed behaviour category (as per Table 1)
  - count: occurrences of the behaviour in the trial

## Metadata and accessibility

- Data generation and formatting described, with explicit coding schemes for stimuli and behaviours.
- A related dataset with full 3D stimulus files and methods is available via the provided DOI link.
- Structured CSVs and accompanying codes enable integration into data workflows and potential GIS-based visualization of responses by stimulus type, trial, or predator species.