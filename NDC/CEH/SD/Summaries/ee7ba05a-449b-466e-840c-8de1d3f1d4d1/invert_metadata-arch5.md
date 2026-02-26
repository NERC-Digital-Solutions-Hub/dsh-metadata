# OVERVIEW

- The dataset comprises three closely related experiments examining how different invertebrate predators (praying mantises, jumping spiders, and crab spiders) respond to 3D-printed mimetic stimuli that vary along a wasp-like to fly-like continuum.
- Objective: determine how accurately a stimulus must mimic the negatively conditioned wasp stimulus before predators treat it as the wasp.

## Data collection and processing

- Observations were recorded in real time during trials; some sessions used video playback for reference.
- Time measurements were taken with a stopwatch.
- Data were cleaned (e.g., removal of invalid or unused points) and formatted using custom R scripts (R v4.3.2).
- Quality control included checks that data codes were valid, values fell within plausible ranges, and patterns of missing data indicated genuine non-availability rather than processing loss.

## Data structure and files

- Three CSV files store the collected data, each corresponding to a predator group:
  - mantis_data.csv
    - 88 rows, 7 columns
    - Columns include: species, id, instar, trial, model, phase, time_to_attack
  - jumping_spider_data.csv
    - 1355 rows, 6 columns
    - Columns include: id, phase, trial, model, behaviour, count
  - crab_spider_data.csv
    - 1260 rows, 8 columns
    - Columns include: id, sex, colour, day, treatment, model, behaviour, count
- Column-level details are described in the dataset's “Nature and units of recorded values” section (not provided here).

## Study organisms and housing

- Praying mantises: three species, housed individually in controlled lab conditions (temperature 26°C, 12:12 h light:dark; trials 30 h after feeding).
- Jumping spiders: Phidippus audax, housed similarly in a lab environment.
- Crab spiders: Synema globosum, wild-caught and housed separately; kept at 22°C with no light cycle.
- Diet and housing specifics are provided to ensure replicability and traceability of behavioral responses.

## Experimental design

- Stimulus design:
  - Based on scanned 3D images of real insects; stimuli are arranged along transects of mimetic similarity between endpoints (e.g., M. meridiana and V. vulgaris) and include variants representing intraspecific variation.
  - Naming format example: M25V75 (25% M. meridiana, 75% V. vulgaris); variants a, b, c reflect different insect specimens.
  - Five transect points used per experiment (M100, M75V25, M50V50, M25V75, V100); some experiments included alternative transects (e.g., Chrysotoxum-based for some spiders) or exaggerated WASP characteristics beyond V. vulgaris.
- Training (aversive conditioning):
  - Mantises and jumping spiders: six conditioning trials on separate days; wasp stimuli (V100) punished upon attack with a thorax poke; fly stimuli (M100) paired with no reward or punishment.
  - Crab spiders: condensed protocol (no trials with wasp or fly stimuli); three training treatments (wasp punishment with no prior exposure, fly-punishment, or no punishment).
- Testing:
  - Mantises and jumping spiders: nine trials post-training, including five probe stimuli (the transect points) and four reinforcement trials (two M100, two V100).
  - Crab spiders: each tested once with a randomly selected stimulus from the available pool.
  - Primary measures: mantises – latency to attack; jumping spiders – various observed behaviours (orientation, alert, display, approach, attack) with counts; crabs – similar behaviours with counts.
- Behaviours observed:
  - Mantises: latency to attack used as primary metric.
  - Jumping and crab spiders: multiple behaviours recorded (e.g., orientation, alert, display, approach, attack) with descriptive codes and counts.

## Data governance and accessibility considerations

- Data are organized by species with clear identifiers for individuals and trials, enabling traceability and re-use.
- The dataset references an external resource for full stimulus descriptions and digital 3D files (DOI provided).
- For Data Stewards:
  - Ensure metadata include explicit column definitions, data types, units, and coding schemes (e.g., model codes, behavioural categories).
  - Maintain provenance by linking raw observations, cleaning steps, and the R v4.3.2 processing scripts used to format the data.
  - Document training/testing protocols, arena conditions, and stimulus design rationale to support reuse and replication.
  - Manage data sharing carefully, noting any restrictions implied by the training phases or animal subjects, and reference embargo or licensing terms if applicable.
  - Plan for updates and versioning, as additional trials or new transects could be added.

## Challenges and considerations for data stewardship

- Potential gaps due to incomplete user needs or evolving research questions.
- Ensuring timely access to data (especially raw video and trial-level details).
- Aligning metadata across three predator groups with different data schemas and codes.
- Handling large, multi-table datasets from diverse experimental setups and ensuring interoperability.
- Documenting non-interoperable aspects (e.g., bespoke stimuli design files) and linking to external resources for full reproducibility.