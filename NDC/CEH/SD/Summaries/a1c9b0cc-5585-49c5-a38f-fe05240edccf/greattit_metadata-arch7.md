# OVERVIEW

- The document describes a dataset from two closely related experiments conducted at Madingley Wood, Cambridge: the Discrimination Ability experiment (Dec 2021–May 2022) and the Multiple Models experiment (Oct 2022–Apr 2023).
- Setup involved feeding stations comprised of a 7×7 array of 30 mm dishes on a wooden board within a cage, with lids containing 3D-printed insect-like stimuli. Birds (primarily Great tits) could open lids to reveal mealworms in some dishes.
- Aims:
  - Discrimination Ability: train birds to associate a fly stimulus with reward and a wasp stimulus with no reward, then test with novel mimics to assess how closely a stimulus must resemble the unrewarded wasp before being mistaken for it.
  - Multiple Models: extend with a second unrewarding wasp type and assess whether a second model improves protection for mimics, particularly intermediates between two wasp stimuli.

## Study design

- Species and stimuli:
  - Stimuli are based on 3D images of real insects, created as transects of mimetic similarity with endpoints and intermediate/extrapolated phenotypes.
  - Training used rewarded fly stimuli (M100) and unrewarded wasp stimuli (V100); testing introduced additional mimics with varying similarity.
  - The Multiple Models experiment added a second unrewarding model (A100) and a two-model treatment (2M) versus a single-model treatment (1M).
- Experimental phases:
  - Habituation: birds learn to visit open Petri dishes; lids gradually used; 3–4 weeks.
  - Training: birds learn to avoid specific lid-stimuli; 3 weeks (4–6 weeks for 2M).
  - Testing: broader range of stimuli presented; rewards maintained for new phenotypes; 5 weeks (10 weeks for 2M).
- Field deployment:
  - Seven feeders across the wood; in the Discrimination experiment, three feeders remained afterDropout; in the Multiple Models experiment, six feeders were used.
  - Stimulus assignment to dishes was randomized per feeder/session.

## Data collection and processing

- Data capture:
  - Motion-sensitive cameras above feeding stations.
  - PIT-tag readers at entrances to log tagged birds; video and logger data downloaded during site visits (approx. every 1–2 days).
  - Randomized stimulus configurations per feeder/session; data generation and storage performed in R (version 4.3.2).
- Data linkage and quality:
  - Attempted cross-referencing of video, PIT-tag logs, and observer records to identify which individual opened each dish.
  - Some gaps exist where logger triggers were missed or video could not confirm identity.
  - Bird metadata linked to a ringing group database to obtain species, sex, and ringing date.
  - Data cleaned (invalid/unused points removed) and formatted in R v4.3.2.
- Quality checks:
  - Summary data reviewed for valid codes and plausible ranges.
  - Missing data patterns examined to distinguish genuine missing values from transcription errors.

## Datasets and schema

- discrim_sessions.csv (303 rows, 14 columns): timings/setup per session per feeder (Discrimination experiment).
- discrim_dishes.csv (7137 rows, 9 columns): stimuli per dish per session per feeder; dish-opening timing/rank.
- discrim_logger_data.csv (7967 rows, 4 columns): logger-trigger events (arrivals/departures) with PIT-tag.
- discrim_bird_info.csv (53 rows, 8 columns): per-bird summary by experimental phase.
- multimod_sessions.csv (633 rows, 15 columns): timings/setup per session per feeder (Two-model vs one-model treatments).
- multimod_dishes.csv (17885 rows, 10 columns): stimuli per dish; detailed opening times or status; includes model/extrapolation codes and bird IDs when observed.
- multimod_logger_data.csv (2627 rows, 4 columns): logger events with PIT-tag.
- multimod_bird_info.csv (50 rows, 8 columns): per-bird summary by experimental phase.

- Nature and units (highlights):
  - date_start/date_end; feeder identifiers (1–7); phase (habituation/training/testing); time_start/time_end; logger states; lids_start/lids_end; mealworms_start/end; peanuts_start/end.
  - dish-level fields include start/end dates, phase, feeder, treatment (1M or 2M for multimodal), position, model code, mealworm presence, timepoint/opening timing, and identifiers for the observed bird or status (e.g., GT, BT, MOUSE, LID, NA).

## Field site and study organisms

- Location: Madingley Wood, Cambridgeshire, UK.
- Site setup: seven feeders located with cages and a 30 mm entrance for PIT-tagged birds; a motion camera captures behavior; perches arranged around the dish array.
- Study organisms: great tits (Parus major) were the primary model; blue tits also observed in some phases; some non-bird visitors (mice) noted in the Multiple Models experiment.

## Stimulus design and naming

- Stimuli derived from 3D scans of real insects; design allows varying contributions from two endpoints (e.g., M. meridiana, common wasp) with intermediate and extrapolated mixtures.
- Naming convention indicates component species and their contributions (e.g., M25V75 = 25% M. meridiana, 75% V. vulgaris).
- Stimulus sets used for discrimination and multiple-model experiments described in detail, including endpoints and intermediate/extrapolated phenotypes.

## Data usage notes for GIS specialists

- Spatial structure:
  - Feeder locations and the 7×7 dish arrangement provide a rich matrix for spatial analysis of visitation patterns and cue responses over time.
  - Dish-level data linked to feeder and session enables mapping of spatial preferences and learning effects across the study area.
- Temporal structure:
  - Session-level and dish-open timing data allow temporal GIS analyses (habituation, training, testing phases, and within-session dish openings).
- Data integration considerations:
  - Multiple linked datasets require careful joins on feeder, session, phase, and (where possible) dish position and PIT-tag identity.
  - Gaps due to logger misses or video gaps should be accounted for in spatial-temporal models.
- Data quality and limitations:
  - Not all birds could be linked to logger events; some dishes opened without sensor confirmation (noted by B status or uncertain IDs).
  - Field layout was fixed to seven feeders; some feeders were dropped in the discrimination phase, which affects spatial coverage.
- Potential GIS products:
  - Map of feeder locations, dish positions, and recorded openings by species and phase.
  - Spatial-temporal models of mimic recognition and avoidance behavior across transects of stimuli.
  - Visualization of learning progression and model protection effects across the spatial array.

## Potential analyses and GIS-oriented questions

- How do opening events cluster around certain feeders or dish positions across phases?
- Do intermediate/extrapolated mimics show spatially varying probabilities of being opened or avoided?
- Can we model visitation patterns and stimulus responses as a function of space, time, and stimulus type to identify spatial learning effects?
- How does the presence of a second model (2M) alter spatial avoidance patterns compared with 1M across the study area?