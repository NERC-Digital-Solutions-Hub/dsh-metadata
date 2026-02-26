Discrimination Ability experiment and Multiple Models experiment

## Overview
- Describes two related field experiments conducted in Madingley Wood, Cambridge, UK, using feeding stations with lids and 3D-printed insect-like stimuli.
- Aimed to study how wild birds (primarily Great tits) learn and discriminate mimetic stimuli associated with rewards, including how a second model type influences protection for certain mimics.

## Study Design and Objectives
- Discrimination Ability experiment: birds trained to associate a fly stimulus with a reward and a common wasp stimulus with no reward; later tested with novel mimetic stimuli of varying similarity to the unrewarding wasp to assess discrimination accuracy.
- Multiple Models experiment: extended the design by introducing a second unrewarding wasp type (two model types) to test whether dual-model contexts improve protection for intermediate mimics.
- Habituation, training, and testing phases structured to progressively reveal how birds respond to mimetic variation and multiple model contexts.

## Data Collection, Instruments, and Procedures
- Feeding stations: 7 locations in the wood (3 used in discrimination, 6 in multimodal), each with a 7x7 dish array, lids, and a PIT-tag reader linked to a data logger; motion-triggered cameras recorded behavior.
- Bird identification: PIT tags attached to birds; individual visits linked to logger events where possible; periodic site visits to download data and reset sessions.
- Data handling: stimuli configurations randomized per feeder/session; sessions and dish events logged in R (v4.3.2) and cross-referenced against video data; bird species and ring details obtained from a ringing group database.
- Data quality: performed basic validation (valid codes, plausible ranges) and examined missing data patterns to distinguish genuine gaps from processing artifacts.

## Stimulus Design and Experimental Phases
- Stimuli: 3D-printed, insect-based mimics generated along transects of mimetic similarity; endpoints included real insect taxa (e.g., fly, wasp) with intermediate and extrapolated phenotypes.
- Stimulus coding: detailed naming convention (e.g., M25V75, A150V-50) representing contributions from different species and extrapolated variants; includes variants a, b, c for intraspecific variation.
- Experimental design specifics:
  - Discrimination Ability: training phase with rewarded fly stimuli (M100) and unrewarding wasp stimuli (V100); testing phase introduced mimics with varied similarity and rewards.
  - Multiple Models: training with one model (1M) or two models (2M); testing with mixtures of V100, A100, and reward stimuli (M100) including intermediates and extrapolations along the A. mystaceus – V. vulgaris transect.
- Habituation: initial exposure with accessible mealworms to encourage visitation; lids then concealed mealworms to compel lid-opening behavior; cleaning and re-stocking between sessions.

## Field Site and Study Organisms
- Location: Madingley Wood, Cambridgeshire, UK; deciduous woodland with resident Great tits (Parus major) and occasional other species.
- Equipment and setup: feeding stations mounted on wooden posts with entrance antennas; motion cameras overhead; seven feeder sites distributed to minimize cross-treatment contamination.

## Data Files, Schema, and Recording Units
- discrim_sessions.csv: 303 session records (14 fields) detailing timings and setup per feeder.
- discrim_dishes.csv: 7137 dish records (9 fields) detailing stimuli, dish status, and opening times per session.
- discrim_logger_data.csv: 7967 logger event records (4 fields) for each PIT-tag trigger (arrivals/departures).
- discrim_bird_info.csv: 53 records (8 fields) summarizing per-bird metrics across experimental phases.
- multimod_sessions.csv: 633 session records (15 fields) for the two-model treatment setups.
- multimod_dishes.csv: 17885 dish records (10 fields) with detailed dish-level opening data and identity of the opening bird (PIT-tag, GT/BT/MOUSE status, etc.).
- multimod_logger_data.csv: 2627 logger events (4 fields) similar to discrim data but for the two-model experiment.
- multimod_bird_info.csv: 50 records (8 fields) summarizing per-bird metrics for the multimod dataset.
- Field-level value definitions cover: date_start/date_end, feeder, treatment (1M or 2M), phase, time_start/time_end, logger_start, lids counts and notes, mealworm/peanuts status, dish position, model codes, mealworm indicators, timepoints, and cross-reference IDs (PIT_tag, species, etc.).

## Data Quality, Provenance, and Reproducibility
- Data cleaning performed to remove invalid/unneeded points and to ensure consistency across datasets.
- Cross-referencing steps included linking video footage with PIT-tag logs where possible; some events could not be matched due to missing triggers or video gaps.
- Documentation includes explicit field definitions and units, enabling audit, replication, and reuse in downstream analyses.

## Limitations and Considerations for Data Leaders
- Some gaps exist in cross-referencing PIT-tag events to individual birds due to logger misses or video gaps.
- Complex stimulus coding and extrapolations require careful interpretation and rigorous metadata handling to ensure reproducibility.
- Study emphasizes the importance of robust data governance around multi-file datasets: consistent identifiers, clear phase mapping, and transparent handling of missing data.

## Relevance to Data Strategy and Practice
- Demonstrates end-to-end data lifecycle: from experimental design and data collection to cleaning, integration, and rich metadata provisioning.
- Highlights the value of standardized schemas, detailed stimulus metadata, and explicit provenance for complex behavioral experiments.
- Provides a blueprint for managing cross-domain data assets (sensor data, video, RFID logs) with clear attribution to individual subjects and experimental phases.
- Underlines challenges common to data ecosystems in research: data discoverability, integration across heterogeneous sources, and maintaining data quality in multi-site studies.