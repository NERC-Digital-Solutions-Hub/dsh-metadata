# Overview of Discrimination Ability and Multiple Models Experiments Dataset

## Study context
- Two related experiments conducted at Madingley Wood, Cambridge, UK:
  - Discrimination Ability (Dec 2021–May 2022)
  - Multiple Models (Oct 2022–Apr 2023)
- Aim: study how wild birds (mainly Great tits, Parus major) respond to mimetic stimuli and learn associations between stimuli and rewards.
- Birds were PIT-tagged; data collected from feeding stations with motion cameras and PIT antennae.

## Field site and organisms
- Field site: Madingley Wood, Cambridgeshire, UK; deciduous woodland with a resident great tit population.
- Feeding stations: 7 × 7 array of 30 mm dishes on a wooden board, enclosed in wire cages with a single entrance linked to a data logger; motion camera above.
- Subjects: wild birds, primarily great tits; some blue tits and mice observed incidentally; PIT-tagging of birds occurred between 2018–2022.

## Experimental design and stimuli
- Stimulus design:
  - Based on scanned 3D images of real insects; stimuli created along transects representing mimetic similarity between endpoints (e.g., wasp vs fly) with intermediate and extrapolated phenotypes.
  - Stimuli named using codes indicating insect contributions (e.g., M25V75) and variants a/b/c.
- Discrimination Ability experiment:
  - Training: bird rewarded for fly-like stimuli (M100); unrewarded wasp stimuli (V100) with no food in corresponding dishes.
  - Testing: introduced novel unrewarding stimuli across a range of mimetic similarities.
- Multiple Models experiment:
  - Training: two model conditions (1M vs 2M) with one or two unrewarding model stimuli (V100 and A100) plus M100 as rewarding.
  - Testing: broader set of unrewarding and rewarding stimuli including intermediates and extrapolations between model endpoints (A mystaceus and V vulgaris) plus a non-mimetic M100 control.

## Data collection and recording methods
- Data streams collected:
  - PIT-tag encounters via antennae at feeder entrances; video reviewed post-session.
  - Dishes opened, lids removed, and timing data recorded per session.
  - Stimulus configurations and dish-level interactions tracked per feeder and session.
- Data linkage:
  - Sessions, dishes, logger events, and bird info stored in separate CSVs for each experiment (Discrimination and Multimodal/Multi-Model).
  - PIT-tag data cross-referenced with Madingley Ringing Group records for species, sex, and ringing date.
  - Video data cross-referenced against logger events where possible; gaps exist when logs or cameras fail to capture events.

## Data files and structure
- Discrimination Ability experiment
  - discrim_sessions.csv: 303 rows, 14 columns
  - discrim_dishes.csv: 7137 rows, 9 columns
  - discrim_logger_data.csv: 7967 rows, 4 columns
  - discrim_bird_info.csv: 53 rows, 8 columns
- Multiple Models experiment (referred to as multimod)
  - multimod_sessions.csv: 633 rows, 15 columns
  - multimod_dishes.csv: 17885 rows, 10 columns
  - multimod_logger_data.csv: 2627 rows, 4 columns
  - multimod_bird_info.csv: 50 rows, 8 columns
- Column details and field definitions are provided in the accompanying “Nature and units of recorded values” section.

## Nature and units of recorded values
- Sessions (discrim_sessions.csv, multimod_sessions.csv):
  - date_start, date_end (yyyy-mm-dd)
  - feeder (location ID)
  - treatment (1M or 2M; only in multimod_sessions.csv)
  - phase (experimental stage)
  - time_start, time_end (hh:mm)
  - logger_start, lids_start/lids_end, lids_note
  - mealworms_start/mealworms_end, peanuts_start/peanuts_end
- Dishes (discrim_dishes.csv, multimod_dishes.csv):
  - start_date, end_date (yyyy-mm-dd)
  - phase, feeder, timepoint
  - model (stimulus code)
  - mealworm (TRUE/FALSE)
  - id (opening status: B, GT, BT, MOUSE, LID, NA, etc.)
  - additional fields indicating opening times and bird identity where available
- Logger data (discrim_logger_data.csv, multimod_logger_data.csv):
  - feeder, datetime (yyyy-mm-dd hh:mm:ss)
  - PIT_tag (bird tag)
  - species (BT, GT)
- Bird info (discrim_bird_info.csv, multimod_bird_info.csv):
  - PIT_tag, species, sex
  - date_ringed
  - phase (phase-specific summary)
  - N_records, N_days, N_feeders (counts across a given phase)

## Data processing and quality control
- Data cleaned and formatted with custom R scripts (R v4.3.2).
- Quality control includes:
  - Checking summary data against valid codes and plausible ranges.
  - Assessing patterns of missing data to distinguish genuine non-availability from transcription loss.
- Notes on data quality:
  - Cross-referencing gaps exist where birds failed to trigger loggers, were not video-recorded entering feeders, or events were too closely timed to distinguish.
  - Some dish openings and bird identifications may be uncertain (indicated in status codes).

## Fieldwork logistics and maintenance
- Habituation phase: birds learned to interact with lids; backgrounds include other species visiting but primarily great tits engaged with lids and mealworms.
- Training/testing phases: structured with randomization of dish configurations; regular refilling and sterilization of equipment; phase durations differ between experiments (training ~3–6 weeks; testing ~5–10 weeks).

## Considerations for data stewardship and reuse
- Clear documentation of stimulus design and naming conventions supports reproducibility and analysis of mimetic strategies.
- Data linkage across sessions, dishes, loggers, and bird identities enables individual- and group-level analyses but may require careful handling due to gaps in cross-referencing.
- Explicit notes on uncertainties and non-interpretable entries (e.g., B, NA, uncertain lids) should be preserved in any downstream use.
- Access and reuse should consider potential data gaps (e.g., missing logger events or video gaps) and the need to align analyses with the recorded phases and structures of each experiment.