# Three Experiments Investigating Predator Responses to 3D Printed Wasp-like and Fly-like Stimuli

## Overview
- Investigates how three invertebrate predators (mantis, jumping spiders, crab spiders) respond to 3D printed stimuli that mimic wasp-like and fly-like features.
- Subjects trained to associate wasp stimuli with a negative outcome; fly stimuli were not paired with reward or punishment.
- Testing used a range of novel mimetic stimuli with varying similarity to the wasp cue to determine the level of similarity required for misidentification as the wasp.

## Aims and Approach
- Determine which visual features and degrees of mimicry trigger recognition of the wasp by predators.
- Use aversive conditioning for training and compare responses to a transect of mimetic stimuli.
- Employ real-time behavioural observations, video backups, and precise timing to quantify responses.

## Experimental Design and Stimuli
- Stimuli design:
  - 3D scanned images of real insects; stimuli formed along transects between endpoints (e.g., M. meridiana and Vespula vulgaris) with five intermediate points: M100, M75V25, M50V50, M25V75, V100.
  - Some transects included alternative bases (e.g., Chrysotoxum) or extrapolated points beyond endpoints.
  - Stimulus names encode species contributions and variants (e.g., M25V75, A-25V125, etc.).
- Training phase:
  - Mantises and jumping spiders underwent six aversive conditioning trials across separate days.
  - In trial 1, stimulus (M100 or V100) was randomly assigned; subsequent trials alternated.
  - Punishment applied after attacking a wasp stimulus (V100); fly stimuli (M100) carried no reward or punishment.
  - Crab spiders followed a condensed protocol with one of three treatments: direct wasp punishment, fly-based punishment, or no punishment.
- Testing phase:
  - Mantises and jumping spiders: nine trials, including probe stimuli (five transect points) and reinforcement trials (two M100 and two V100).
  - Spiders (P. audax and S. globosum): varied responses beyond latency; most trials limited to non-attack behaviours due to low attack rates.
  - Crab spiders: each tested once per trial with a random stimulus from the available pool.
- Measurements:
  - Mantises: latency to attack (time from trial start to first strike).
  - Jumping spiders: range of behaviours recorded; primary latency to attack unsuitable due to low attack frequency.
  - Crab spiders: counts of observed behaviours (e.g., orientation, alert, display, approach, attack, with negative/positive interpretations).

## Subjects, Housing, and Arenas
- Mantises: Rhombodera kirbyi, Polyspilota aeruginosa, Pseudoxyops perpulchra; housed individually at ~26°C, 12:12 h light:dark.
- Jumping spiders: Phidippus audax; housed individually at ~26°C, with feeding prior to trials.
- Crab spiders: Synema globosum; wild-caught, housed individually at ~22°C, no artificial light cycle; pre-trial feeding withheld for 48 hours.
- Experimental arenas:
  - Mantises and jumping spiders: small opaque boxes with a moving stimulus actuated by Arduino-controlled motor and fishing-line rig to create three-dimensional, jerky movements.
  - Crab spiders: larger arena with a flower perch and similar stimulus delivery via a fishing-line mechanism.
- Stimuli: 3D-printed mimics suspended and moved to resemble real insects; designs include multi-characteristic combinations across shape, pattern, colour, and size.

## Data Collection and Quality Control
- Data collection:
  - Real-time behavioural observations during trials; video recorded as needed.
  - Timing recorded with a stopwatch; data cleaned and formatted using R v4.3.2.
- Quality control:
  - Data checked for valid codes and plausible value ranges.
  - Missing data patterns examined to differentiate genuine absence from transcription loss.
- Data provenance:
  - Full methods for stimulus generation and digital 3D assets referenced in an external dataset (Scanned 3D images and 3D printable images; DOI provided in the original text).

## Data Structure and Files
- mantis_data.csv
  - 88 rows; 7 columns.
  - Fields include: species, id, instar, trial, model, phase, time_to_attack.
- jumping_spider_data.csv
  - 1,355 rows; 6 columns.
  - Fields include: id, phase, trial, model, behaviour, count.
- crab_spider_data.csv
  - 1,260 rows; 8 columns.
  - Fields include: id, sex, colour, day, treatment, model, behaviour, count.
- Column-level details:
  - Mantises: subject identity (species, id), developmental stage (instar), trial number, stimulus model, experimental phase, and attack latency.
  - Jumping spiders: subject identity (id), phase, trial, stimulus model, observed behaviour category, and frequency (count).
  - Crabs: subject identity (id), sex, female colour morph, day of experiment, training treatment, stimulus model, observed behaviour category, and frequency (count).

## Behavioral Categories and Table 1
- For spiders (P. audax and S. globosum): a set of observed behaviours with qualitative interpretations, including:
  - Orientation: facing the model; can be positive or negative depending on movement toward/away.
  - Alert: tracking or watching the model; direction of valence indicated.
  - Display: leg movements toward/away from the model.
  - Approach: moving toward or away from the model.
  - Attack: direct engagement with the model (jumping/biting) or avoidance.
  - Bungee, Hide: specific behaviours observed in S. globosum (e.g., jumping off the flower, moving out of sight).

## External Data and Methods Reference
- Stimulus creation and modelling details linked to an external dataset describing scanned 3D images and 3D printable images based on Diptera and Hymenoptera features collected in 2021–2022 (DOI provided in the source material).

## Relevance for Monitoring Frameworks
- Demonstrates practical data lifecycle practices:
  - Clear documentation of study design, stimuli, training/testing phases, and behavioural measures.
  - Commensurate data collection methods (real-time observation, video backup, precise timing).
  - Rigorous quality control and data cleaning steps.
  - Transparent data structure with explicit metadata (subject IDs, trial numbers, phase, stimulus model, behavioural categories).
  - Use of standardized data formats (CSV) and reproducible data processing (R 4.3.2).
  - Linkages to external resources for full methodological transparency and data provenance.
- Illustrates common monitoring-data challenges and potential mitigations:
  - Metadata completeness and standardization (e.g., consistent coding for models, behaviours).
  - Data sharing considerations (public availability of underlying datasets and refusal of some data points due to openness requirements).
  - Ensuring up-to-date metadata and governance when disseminating datasets.