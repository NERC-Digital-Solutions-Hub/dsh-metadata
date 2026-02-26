# OVERVIEW:

- This document describes two closely related experiments conducted in Madingley Wood, Cambridge:
  - Discrimination Ability experiment (Dec 2021–May 2022)
  - Multiple Models experiment (Oct 2022–Apr 2023)
- Objective: understand how wild birds (primarily Great tits) learn to discriminate mimetic stimuli from a reward structure, and how the presence of multiple model types affects protection for mimics.
- Experimental setup involved feeding stations with lids and 3D-printed insect-like stimuli, where birds could uncover mealworms or encounter empty dishes depending on the stimulus.

## Aim and Analytic Focus

- Use standardized data to assess environmental/behavioral responses over time.
- Capture learning, discrimination accuracy, and potential biases in predator-like decision making.
- Produce outputs suitable for integration into broader environmental monitoring formats (e.g., datasets, maps, charts).

## Study Site, Organisms, and Monitoring Approach

- Field site: Madingley Wood, Cambridgeshire, UK; habitat: deciduous broadleaf woodland.
- Target species: Great tits (Parus major) with PIT tagging; Blue tits and mice observed but key data are from Great tits.
- Monitoring tools:
  - Feeding stations with a 7×7 array of dishes under lids
  - Motion cameras (above the cage) and PIT-tag antennae at feeder entrances
  - Periodic researcher visits to download video/logger data
- Data management: Stimulus configurations randomized per feeder/session; data processed in R (v4.3.2); cross-referenced with Madingley Ringing Group records for bird metadata.

## Feeding Stations and Stimulus Design

- Feeding station construction:
  - Wooden board with 30 mm dishes, housed in a cage, with a single entrance/antenna for PIT tagging, and multiple perches.
  - Cameras cover the cage entrance and dishes.
- Stimuli design:
  - Based on scanned 3D images of real insects; created transects of mimetic similarity with endpoints and intermediates.
  - Stimuli labeled to reflect contributions from insect species (e.g., M25V75), with possible extrapolations beyond endpoints.
  - Variants (a, b, c) reflect intraspecific variation.

## Experimental Design Details

- Discrimination Ability experiment:
  - Training: flies (M100) rewarded; wasp (V100) unrewarded.
  - Testing: introduced unrewarded mimics and rewarded novel phenotypes to assess discrimination thresholds.
- Multiple Models experiment:
  - Training with one model (1M: V100) or two models (2M: V100 and A100) across feeders.
  - Testing included a broader set of mimics spanning intermediates and extrapolations between two model endpoints (A. mystaceus and V. vulgaris), plus a non-mimetic M100 control.
- Habituation phase preps birds by enabling lid-opening learning and acclimation to the feeding setup.

## Data Collection and Quality Control

- Data streams:
  - discrim_sessions.csv and multimod_sessions.csv: session timings, feeder IDs, treatment, phase, lid status, mealworm/peanut provisioning.
  - discrim_dishes.csv and multimod_dishes.csv: dish-level stimuli, model codes, mealworm presence, time of dish opening, and who opened it (PIT-tag, GT/BT/MOUSE, etc.).
  - discrim_logger_data.csv and multimod_logger_data.csv: logger events with feeder, datetime, PIT_tag, species.
  - discrim_bird_info.csv and multimod_bird_info.csv: per-bird summaries by experimental phase (N_records, N_days, N_feeders).
- Quality checks:
  - Verified data code validity and plausible value ranges.
  - Assessed patterns of missing data to distinguish genuine gaps from processing losses.
- Data handling:
  - Data cleaned and formatted with custom R scripts; cross-referenced PIT-tag data with ringing records; video data used to link individuals where possible.

## Datasets and Structure (Key Files)

- discrim_sessions.csv: 303 rows, 14 columns (session details per feeder)
- discrim_dishes.csv: 7137 rows, 9 columns (dish-level stimulus and response data)
- discrim_logger_data.csv: 7967 rows, 4 columns (PIT-tag events)
- discrim_bird_info.csv: 53 rows, 8 columns (bird summaries by phase)
- multimod_sessions.csv: 633 rows, 15 columns
- multimod_dishes.csv: 17885 rows, 10 columns
- multimod_logger_data.csv: 2627 rows, 4 columns
- multimod_bird_info.csv: 50 rows, 8 columns

## Field Site and Stimulus Details

- Stimuli naming and composition:
  - Codes reflect percentages from specified insect species, with endpoints and intermediates along mimetic transects.
  - Two endpoints per transect represent distinct model traits; intermediates and extrapolations explore broader mimicry space.
- Experimental phases:
  - Habituation: unexposed lids become opened with mealworms; birds learn lids flip mechanism.
  - Training: lid-opening leads to mealworms for fly-like stimuli; unrewarding wasps have no reward.
  - Testing: expanded stimulus sets with rewards to assess discrimination across mimics.

## Reproducibility and Data Availability

- All data and stimulus designs are linked to the dataset “Scanned 3D images and 3D printable images...” with a DOI, supporting reproducibility of stimuli and methods.
- Data are organized to support standardized reporting and time-series scrutiny for environmental health and policy performance assessments.

## Relevance to Environmental Monitoring

- Demonstrates standardized, repeatable collection of behavioral response data relevant to predator-prey-like decision making in a natural population.
- Provides rich, multi-layer datasets (behavioural events, individual bird metadata, and stimuli) suitable for integration into environmental health dashboards and policy monitoring.
- Addresses challenges of data utility and access by maintaining clear data dictionaries, quality checks, and cross-referenced individual identifiers.