# OVERVIEW:

- Purpose and scope
  - A dataset from three closely related experiments examining how different invertebrate predators of flower-visiting insects respond to 3D-printed wasp-like and fly-like stimuli.
  - Predators studied: praying mantises (three species), jumping spiders, and crab spiders.
  - Training phase: predators learned to associate wasp-like stimuli with a negative experience; fly-like stimuli were not associated with any reward or punishment.
  - Testing phase: predators faced a range of novel mimetic stimuli with varying similarity to the wasp stimulus to determine the level of resemblance required for misidentification as the wasp.

- Experimental design and stimuli
  - Stimuli design
    - Based on scanned 3D images of real insects; created transects of mimetic similarity between endpoints (wasp, fly, hoverfly, etc.).
    - Five transect points used: M100, M75V25, M50V50, M25V75, V100; some experiments included a Chrysotoxum-based transect for jumping spiders; some crab spider models extended beyond V100.
    - Stimuli named with codes indicating insect contributions (e.g., M25V75 = 25% Mesembrina meridiana, 75% Vespu la vulgaris) and variant a/b/c for intraspecific variation.
  - Experimental arenas
    - Mantises and jumping spiders: small opaque boxes with a motorized stimulus suspended to move in three dimensions, encouraging engagement/strike.
    - Crab spiders: larger arena with a perch (purple milk thistle) to simulate natural hunting context; different stimulus presentation (vertical movement).
  - Training phase
    - Mantises and jumping spiders: six aversive conditioning trials across days; wasp stimuli punished upon attack to create negative association; fly stimuli were neutral.
    - Crab spiders: condensed training with three treatment options (punishment with wasp stimulus, punishment with fly stimulus, or no punishment); no exposure to wasp vs. fly trials as in mantises/spiders.
  - Testing phase
    - Mantises and jumping spiders: nine trials per subject, including five probe stimuli (the transect points) in random order and four reinforcement trials (two M100 and two V100).
    - Crab spiders: each subject tested once with a single stimulus due to captivity time constraints.
    - Outcome measures: mantises – latency to attack from start of trial; jumping spiders – a range of behaviours recorded due to low attack rate; crab spiders – count-based behavioural observations.

- Data collection, quality control, and structure
  - Data collection: real-time observations with video capture and stopwatch timings where applicable.
  - Data processing: cleaning and formatting with custom R v4.3.2 scripts.
  - Quality control: checks for valid codes, plausible data ranges, and assessment of missing data patterns to ensure data integrity.
  - Data files and structure
    - mantis_data.csv: 88 trials, 7 columns; fields include species, id, instar, trial, model, phase, time_to_attack.
    - jumping_spider_data.csv: 1,355 rows, 6 columns; fields include id, phase, trial, model, behaviour, count.
    - crab_spider_data.csv: 1,260 rows, 8 columns; fields include id, sex, colour, day, treatment, model, behaviour, count.
  - Nature/units note: detailed description of column values is available in the dataset’s “Nature and units of recorded values” section (not reproduced here).

- Study organisms and housing
  - Mantises: Rhombodera kirbyi, Polyspilota aeruginosa, Pseudoxyops perpulchra; housed individually at 26°C, 12:12 light cycle; fed twice weekly, trials 30 h post-feeding.
  - Jumping spiders: Phidippus audax; housed individually under similar conditions for mantises; fed accordingly.
  - Crab spiders: Synema globosum; wild-caught, housed individually at 22°C; not fed for 48 hours before use.

- Experimental details: stimuli and training
  - Stimulus design
    - 3D-printed models created from scanned insect images; some stimuli are direct representations, others blend features from different species; multiple variants to capture intraspecific variation.
    - An explicit naming convention ties each stimulus to a pair of parent species and a variation variant.
  - Training specifics
    - Aversion conditioning used to associate wasp-like stimuli with negative outcomes; fly stimuli remained neutral.
    - The training sequence alternated stimulus type across trials to reinforce learning.
  - Testing specifics
    - Mantises: five probe stimuli plus reinforcement trials, with latency to attack measured as a primary metric.
    - Jumping spiders: attack rates were low; researchers recorded a broader set of behaviours (e.g., orientation, alert, display, approach, retreat) across trials.
    - Crab spiders: single-stimulus test per subject, with recorded behaviours and counts.

- Behavioral outcomes and interpretation
  - Mantises: reliable attacks on stimuli; latency to attack used to gauge response dynamics after conditioning.
  - Jumping spiders: varied behaviours documented; high-detail behavioural categories captured to assess responses to mimetic stimuli.
  - Crab spiders: limited testing per individual; behaviour counts provide baseline responses to selected stimuli.
  - Behavioural table (Table 1) includes categories such as Bungee, Hide, Orientation, Alert, Display, Approach, and Attack, with positive/negative valence annotations tied to responses.

- Relevance for environmental monitoring and data stewardship
  - The dataset demonstrates standardized data collection and coding across multiple species and experimental contexts.
  - Uses clearly defined stimulus designs and trial structures, enabling cross-study comparability and integration into monitored datasets.
  - Rigorous quality checks and transparent data structure support data reuse, validation, and long-term usability for assessing predator–prey interaction dynamics in response to mimetic cues.