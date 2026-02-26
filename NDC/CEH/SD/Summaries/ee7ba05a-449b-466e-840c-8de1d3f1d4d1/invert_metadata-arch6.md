# OVERVIEW

- This dataset comprises three related experiments examining how different invertebrate predators (mantises, jumping spiders, and crab spiders) respond to 3D printed mimetic stimuli resembling wasps and flies.
- The aim is to determine how accurately a stimulus must mimic a negatively conditioned wasp before being misidentified as the wasp by the predators.
- Stimuli are presented in a controlled arena and predators undergo aversive conditioning to wasp stimuli; fly stimuli are neutral.
- Testing includes novel stimuli along transects that vary in similarity, plus reinforcement trials to assess generalization.

## Aims and scope

- Evaluate predator responses to mimetic stimuli with varying similarity to a negatively conditioned wasp.
- Quantify how much mimetic similarity is required before a stimulus is treated as the wasp by different predator species.

## Study organisms and housing

- Praying mantises (three species: Rhombodera kirbyi, Polyspilota aeruginosa, Pseudoxyops perpulchra) housed individually in laboratory boxes; room conditions and feeding schedules specified.
- Jumping spiders (Phidippus audax) housed individually in lab boxes; subjected to controlled trials after a 30-hour post-feeding window.
- Crab spiders (Synema globosum) collected from field sites, housed individually in tubes, not fed for 48 hours prior to use.

## Experimental arena and setup

- Mantises and jumping spiders tested in small opaque boxes (19 × 13 × 8 cm); stimuli suspended on a moving line driven by Arduino-powered motor to create realistic 3D motion.
- Crab spiders tested in a larger arena (69 × 38 × 41 cm) with a perching flower and similar stimulus movement, adjusted to provide vertical approaches.

## Stimulus design

- Stimuli built from scanned 3D images of real insects; transects span combinations of features from two endpoints (e.g., M. meridiana and Vespula vulgaris).
- Stimulus naming format: [species endpoints and contributions] with variants a, b, c to capture intraspecific variation. Examples: M100, M75V25, M50V50, V100.
- Some stimuli extend beyond endpoints in trait space (extrapolated features). In some trials, alternate transects (e.g., Chrysotoxum) were used.
- Full methodological description and digital 3D files available via a referenced dataset DOI.

## Training phase

- Mantises and jumping spiders: six aversive conditioning trials on separate days.
  - First trial randomly allocated M100 or V100; subsequent trials alternate stimuli.
  - After acclimation, if a wasp stimulus (V100) was attacked, subjects were punished by prodding the thorax with a rod-mounted wasp stimulus.
  - Fly stimuli (M100) were not punished.
- Crab spiders: condensed training with three possible treatments due to practical constraints; direct punishment with a wasp stimulus, punishment with a fly stimulus, or no punishment. No prior presentations with wasp or fly stimuli.

## Testing phase

- Mantises and jumping spiders: nine trials per subject, including five probe stimuli along the transect (random order) and four reinforcement trials (two M100 and two V100).
- Spiders: each subject assigned to probe stimuli from either the Chrysotoxum or M. meridiana transects.
- Measurements:
  - Mantises: latency to attack (time from motor activation to first strike).
  - Spiders: low incidence of attacks; behaviours recorded instead (see Table 1 for categories and valence).
- Observed behaviours for spiders include orientation, alert, display, approach, attack, bungee, and hide, with positive/negative valences noted.

## Data collection and quality control

- Real-time behavioural observations; video recordings used for reference when available.
- Timing via stopwatch; data cleaned to remove invalid or unused points.
- Quality checks ensured data codes were valid and values fell within plausible ranges; analysis of missing data patterns to confirm genuine absence rather than processing loss.

## Data structure and files

- mantis_data.csv
  - Columns: species, id, instar, trial, model, phase, time_to_attack
  - 88 rows, 7 columns
- jumping_spider_data.csv
  - Columns: id, phase, trial, model, behaviour, count
  - 1355 rows, 6 columns
- crab_spider_data.csv
  - Columns: id, sex, colour, day, treatment, model, behaviour, count
  - 1260 rows, 8 columns

- Column details reference the experimental design: stimulus model codes, trial/phases, and behavioural observations.
- Behaviour categories for spiders (Table 1) include: Bungee, Hide, Orientation, Alert, Display, Approach, Attack, with positive/negative valence assignments.

## Data provenance and access notes

- Stimulus design relies on cross-species feature contributions and transects between endpoints; specifics and digital files are linked to a dataset DOI.
- Data are suitable for cross-species comparative analyses of threat-mimic recognition and learning generalization, enabling dashboards or self-service exploration of attack latency, behaviour frequencies, and transect-based responses.

## Potential data uses and considerations for analysts

- Join the three datasets on trial, phase, model, and id to compare responses across predator taxa.
- Analyze time_to_attack (mantises) alongside frequency of attack and various behaviours (spiders) to assess learning generalization and avoidance patterns.
- Explore how different stimulus transects (e.g., M100 vs V100 vs intermediate mixtures) influence behavioural responses across species.
- Build dashboards summarizing attack latency distributions, behaviour counts, and transect similarity effects; assess consistency of aversive conditioning across taxa.
- Be mindful of crab spider limitations (fewer trials) and the distinct measurement approach for spiders versus mantises.